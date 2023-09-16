# DU Configuration Update 

[TS 38.473 Section 8.2.4](./TS-38.473.pdf)

## Standards Defination

### DU Configuration Update

![duConfigUpdate1](./images/s1.png)

![duConfigUpdate2](./images/s2.png)

## Elements for F1AP DU Configuration Update  

### DU Configuration Update

![du-cfg1](./images/du-cfg1.png)

![du-cfg2](./images/du-cfg2.png)

### DU Configuration Update Acknowledgement

![du-cfg-ack1](./images/du-cfg-ack1.png)

![du-cfg-ack2](./images/du-cfg-ack2.png)

### DU Configuration Update Failure

![du-cfg-fail](./images/du-cfg-fail.png)

## Progress

### OSC DU-High

Currently, OAI DU-High only provides `Served Cells to Modify Lists IE` & `Served Cells to Delete Lists IE`.

`o-du-l2/src/du_app/du_f1ap_msg_hdl.c`

![osc-du1](./images/osc-du1.png)

Then handling of only `Served Cells to Delete Lists IE` in **DU Configuration Update Acknowledgement** message:

![osc-du2](./images/osc-du2.png)

### OSC CU STUB

Call Flow:

![Call Flow](./images/F1APMsgHdlr.png)

Handling of DU Configuration Update by OSC-CU:

![osc-cu1](./images/osc-cu1.png)

Only handles the `Served Cells to Delete List` in processing DU Configuration Update in OSC-CU.

`o-du-l2/src/cu_stub/cu_f1ap_msg_hdl.c`

![osc-cu2](./images/osc-cu2.png)

![osc-cu3](./images/osc-cu3.png)

### OAI CU 

In OAI CU side, there are only macros for the **DU Configuration Update** message.

![oai-cu](./images/oai-cu.png)

