---
description: 要求狀態變更。
ms.assetid: 53c24e17-2b59-4439-a6d1-e971c189d223
title: Msvm_VirtualSystemReferencePointExportJob 類別的 RequestStateChange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_VirtualSystemReferencePointExportJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 5612371738915b5e38657eca0773a88e31e3b0d2
ms.sourcegitcommit: c16214e53680dc71d1c07111b51f72b82a4512d8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/03/2021
ms.locfileid: "106993789"
---
# <a name="requeststatechange-method-of-the-msvm_virtualsystemreferencepointexportjob-class"></a>Msvm VirtualSystemReferencePointExportJob 類別的 RequestStateChange 方法 \_

要求狀態變更。

## <a name="syntax"></a>語法


```mof
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*RequestedState* \[在\]
</dt> <dd>

變更作業的狀態。 可能的值如下：

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**開始** (2) 


</dt> <dd>

將狀態變更為「正在執行」。

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**暫** 止 (3) 


</dt> <dd>

暫時停止作業。 其目的是要以 ' Start ' 重新開機作業。 您可能可以在暫停時輸入「服務」狀態。  (這是特定作業。 ) 

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**終止** (4) 


</dt> <dd>

完全停止工作、儲存資料、保留狀態，並以有條理的方式關閉所有基礎進程。

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**終止** (5) 


</dt> <dd>

立即終止工作，不需要儲存資料或保留狀態。

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6) 


</dt> <dd>

將工作放入廠商特定的服務狀態。 您可以重新開機作業。

</dd> <dt>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>

<span id="DMTF_Reserved"></span><span id="dmtf_reserved"></span><span id="DMTF_RESERVED"></span>**DMTF 保留** (7. 32767) 


</dt> <dd></dd> <dt>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>

<span id="Vendor_Reserved"></span><span id="vendor_reserved"></span><span id="VENDOR_RESERVED"></span>**廠商保留** (32768. 65535) 


</dt> <dd></dd> </dl> </dd> <dt>

*TimeoutPeriod* \[在\]
</dt> <dd>

指定用戶端預期轉換至新狀態所需的最大時間量的超時時間。 間隔格式必須用來指定時間長度。 值為0或 **Null** 表示用戶端沒有轉換的時間需求。 如果這個屬性不包含0或 **Null** ，且執行不支援這個參數，則傳回碼 4098 (**不支援使用 Timeout 參數**) 必須傳回。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回 0;否則，會傳回錯誤。

<dl> <dt>

  (0)
</dt> <dt>

  (32768) 
</dt> <dt>

  (32769) 
</dt> <dt>

  (32770) 
</dt> <dt>

  (32771) 
</dt> <dt>

  (32772) 
</dt> <dt>

  (32773) 
</dt> <dt>

  (32774) 
</dt> <dt>

  (32775) 
</dt> <dt>

  (32776) 
</dt> <dt>

  (32777) 
</dt> <dt>

  (32778) 
</dt> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1703版桌面應用程式\]<br/>                                               |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ VirtualSystemReferencePointExportJob**](msvm-virtualsystemreferencepointexportjob.md)
</dt> </dl>

 

 




