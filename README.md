# Configuration Update 

## Standard Defination

3GPP Standard: [TS 38.473 Section 8.2.4](./TS-38.473.pdf)

### DU Configuration Update

![duConfigUpdate1](./images/duCfgUpd1.png)

![duConfigUpdate2](./images/duCfgUpd2.png)

## Elements for F1AP DU Configuration Update  

### DU Configuration Update

![du-cfg1](./images/du-cfg1.png)

![du-cfg2](./images/du-cfg2.png)

### DU Configuration Update Acknowledgement

![du-cfg-ack1](./images/du-cfg-ack1.png)

![du-cfg-ack2](./images/du-cfg-ack2.png)

### DU Configuration Update Failure

![du-cfg-fail](./images/du-cfg-fail.png)

## Current Status

### OSC DU-High

Currently, OAI DU-High only provides `Served Cells to Modify Lists IE` & `Served Cells to Delete Lists IE`.

path: `o-du-l2/src/du_app/du_f1ap_msg_hdl.c`

![osc-du1](./images/osc-du1.png)

Even, it only handles `Served Cells to Delete Lists` in **DU Configuration Update Acknowledgement** message.

![osc-du2](./images/osc-du2.png)

### OSC CU STUB

Call Flow:

![Call Flow](./images/F1APMsgHdlr.png)

Handling of **DU Configuration Update** by OSC-CU:

path: `o-du-l2/src/cu_stub/cu_f1ap_msg_hdl.c`

![osc-cu1](./images/osc-cu1.png)

Only handles the `Served Cells to Delete List` in processing **DU Configuration Update** in OSC-CU.

![osc-cu2](./images/osc-cu2.png)

![osc-cu3](./images/osc-cu3.png)

### OAI CU 

In OAI CU side, there are only macros for the **DU Configuration Update** message.

path: `openairinterface/openair2/F1AP/f1ap_cu_interface_management.c`

![oai-cu](./images/oai-cu.png)

