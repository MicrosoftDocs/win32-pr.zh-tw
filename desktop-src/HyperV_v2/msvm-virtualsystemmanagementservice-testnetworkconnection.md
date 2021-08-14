---
description: 測試 Windows 網路虛擬化環境中 VM 的網路連線能力。
ms.assetid: 37d4c34d-406e-4c52-afce-b0eef754eeb3
title: Msvm_VirtualSystemManagementService 類別的 TestNetworkConnection 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemManagementService.TestNetworkConnection
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 66988944b6c4f4a97a450f63964d57084fc5886716d109e655921d8744bba721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119388376"
---
# <a name="testnetworkconnection-method-of-the-msvm_virtualsystemmanagementservice-class"></a>Msvm VirtualSystemManagementService 類別的 TestNetworkConnection 方法 \_

測試 Windows 網路虛擬化環境中 VM 的網路連線能力。

## <a name="syntax"></a>語法


```mof
uint32 TestNetworkConnection(
  [in]  Msvm_EthernetPortAllocationSettingData REF TargetNetworkAdapter,
  [in]  boolean                                    IsSender,
  [in]  string                                     SenderIP,
  [in]  string                                     ReceiverIP,
  [in]  string                                     ReceiverMac,
  [in]  uint32                                     IsolationId,
  [in]  uint32                                     SequenceNumber,
  [out] uint32                                     RoundTripTime,
  [out] CIM_ConcreteJob                        REF Job
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*TargetNetworkAdapter* \[在\]
</dt> <dd>

描述目標網路介面卡的 [**Msvm \_ EthernetPortAllocationSettingData**](msvm-ethernetportallocationsettingdata.md) 參考。

</dd> <dt>

*IsSender* \[在\]
</dt> <dd>

指出是否要在傳送者端或接收者叫用此方法。

</dd> <dt>

*SenderIP* \[在\]
</dt> <dd>

寄件者 IP 位址。

</dd> <dt>

*ReceiverIP* \[在\]
</dt> <dd>

寄件者 Mac 位址。

</dd> <dt>

*ReceiverMac* \[在\]
</dt> <dd>

寄件者 Mac 位址。

</dd> <dt>

*IsolationId* \[在\]
</dt> <dd>

隔離識別碼。

</dd> <dt>

*SequenceNumber* \[在\]
</dt> <dd>

隔離識別碼。

</dd> <dt>

*RoundTripTime* \[擴展\]
</dt> <dd>

來回行程時間。

</dd> <dt>

*作業* \[擴展\]
</dt> <dd>

如果作業是以非同步方式執行，這個方法會傳回4096，而此參數會包含衍生自 [**CIM \_ ConcreteJob**](/previous-versions//cc136808(v=vs.85))之物件的參考。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法會傳回下列其中一個值。

<dl> <dt>

**已完成，沒有錯誤** (0) 
</dt> <dt>

**不支援** (1) 
</dt> <dt>

**失敗** (2) 
</dt> <dt>

**Timeout** (3) 
</dt> <dt>

**不正確參數** (4) 
</dt> <dt>

**DMTF 保留** ( .。。) 
</dt> <dt>

**已檢查方法參數-工作已啟動** (4096) 
</dt> <dt>

**方法保留** (4097. 32767) 
</dt> <dt>

**廠商特定** (32768. 65535) 
</dt> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                                       |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ VirtualSystemManagementService**](msvm-virtualsystemmanagementservice.md)
</dt> </dl>

 

