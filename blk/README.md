# blk

This directory contains tracing scripts for blk layer.

## opcode

For convenience we provide the request codes for blk I/Os, which are shown in several of the outputs of these scripts.

```c
enum req_opf {
    /* read sectors from the device */
    REQ_OP_READ     = 0,
    /* write sectors to the device */
    REQ_OP_WRITE        = 1,
    /* flush the volatile write cache */
    REQ_OP_FLUSH        = 2,
    /* discard sectors */
    REQ_OP_DISCARD      = 3,
    /* securely erase sectors */
    REQ_OP_SECURE_ERASE = 5,
    /* write the zero filled sector many times */
    REQ_OP_WRITE_ZEROES = 9,
    /* Open a zone */
    REQ_OP_ZONE_OPEN    = 10,
    /* Close a zone */
    REQ_OP_ZONE_CLOSE   = 11,
    /* Transition a zone to full */
    REQ_OP_ZONE_FINISH  = 12,
    /* write data at the current zone write pointer */
    REQ_OP_ZONE_APPEND  = 13,
    /* reset a zone write pointer */
    REQ_OP_ZONE_RESET   = 15,
    /* reset all the zone present on the device */
    REQ_OP_ZONE_RESET_ALL   = 17,

    /* Driver private requests */
    REQ_OP_DRV_IN       = 34,
    REQ_OP_DRV_OUT      = 35,

    REQ_OP_LAST,
};
```
