# Solutions Architect.
*** > find [important] points
## Domain 1

### Database
- relational
    - lift and shift
- key-value
    - high throughput low latency
    - social, bidding, shopping cart
- document
    - stores docs
    -content management
- in-memory | query-by-key | leaderboards
- graph | social networking, recommendations | 
- time-series | IoT apps, event tracking
- ledger | ledge, financial transactions | eg. qldb

### Services
- Compute Services
    - ec2, lighsail, lambda, batch, elastic, beanstalk, serverless application repository, aws outposts, ec2 image builder, aws app runner
- Storage Services
    - s3, fsx, 

[FOCUS] storage, compute, database : classes / when to use

## Domain 2

### Reliability
### Resiliency
rto rpo recovery objective - time & point

backup and restore
- rpo in hrs, rto in 24hrs or less
- back up - data and applications
- region restore

warm standby
- rto in secs, rto in mins
- keep a reduced version fully functional env.

active-active
- rpo none, rto in secs
- workload deployed and actively serves traffic from multiple aws regions
- recovery by route53/global accelerator to route traffic to..

table reliability resilience
- availability objs : max unavailability | rto | regions | approach
- 90% : 36D
- 95% : 18D
- 99% : 3D
- 99.9% : 8 hrs
- 99.99% : 4 hrs
- 99.999% : 52 mins
- 99.9999% : 5 mins

# Pillars for resilient workloads
```
infra as code_______________
|                           |
app. architecture ______ data movement
```

always stateless, if not stateful
avoid asynchronous
app in repo, container

high-availability building blocks
- elastic ip address
- elastic load balancing
- simple storage service
- kinesis streams
- rds and dynamodb
- efs and fsx for windows file server


# Storage
- object storage : S3
- block storage : EBS
- 


# High Availability Design***
## Pattern -1
- ELB to route traffic acros AZ's
- design:
## Pattern -2
- breif: HA - Database design pattern
- design: AZ1 (master db & read replica) + AZ2 (standby db & read replica)
## Pattern -3
- brief: floating IP address
## Pattern -4
- brief: floating Interface Pattern
- route53-| 1. 
## Pattern -5
- breif: state sharing
- design: `elb---(key-value store, state information)[auto-scaling]`
## Pattern -6
- brief: scheduled scale out
- design: `elb > app > db(s) <<< [auto-scaled _scheduled_] <<< ami`
## Pattern -7
- brief: job observer pattern
- design: ``