---
description: Msvm_StorageJob 類別的 RequestStateChange 方法-要求狀態變更。
ms.assetid: 2960bc44-f2af-49c6-9c33-5d9e1ad8056c
title: Msvm_StorageJob 類別的 RequestStateChange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_StorageJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: e15f28af892e713f8bd6897b2d75b6b227886ad1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108111346"
---
# <a name="requeststatechange-method-of-the-msvm_storagejob-class"></a>Msvm Get-storagejob 類別的 RequestStateChange 方法 \_

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

RequestStateChange 會變更工作的狀態。 可能的值如下：

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

這個方法會傳回下列其中一個值：

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
| 最低支援的用戶端<br/> | Windows 8.1<br/>                                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2012 R2<br/>                                                                       |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ get-storagejob**](msvm-storagejob.md)
</dt> </dl>

 

 




