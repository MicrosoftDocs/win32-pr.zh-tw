---
description: 變更作業的狀態。
ms.assetid: 3B11CE45-63E4-43D1-AAF6-02F83C9CBB85
title: Msvm_CopyFileToGuestJob：： RequestStateChange 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_CopyFileToGuestJob.RequestStateChange
api_type:
- COM
api_location:
- vmms.exe
ms.openlocfilehash: 09fdc3a1ee7d0f8942e1e02c5d18f20c42f74db2e65ae065132f164b199ee861
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119014336"
---
# <a name="msvm_copyfiletoguestjobrequeststatechange-method"></a>Msvm \_ CopyFileToGuestJob：： RequestStateChange 方法

變更作業的狀態。

## <a name="syntax"></a>語法


```C++
uint32 RequestStateChange(
  [in] uint16   RequestedState,
  [in] datetime TimeoutPeriod
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*RequestedState* \[在\]
</dt> <dd>

新狀態。 以下是可能的值：

<dt>

<span id="Start"></span><span id="start"></span><span id="START"></span>

<span id="Start"></span><span id="start"></span><span id="START"></span>**開始** (2) 


</dt> <dd>

將狀態變更為「正在執行」。

</dd> <dt>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>

<span id="Suspend"></span><span id="suspend"></span><span id="SUSPEND"></span>**暫** 止 (3) 


</dt> <dd>

暫時停止作業。 接著，用戶端可以使用「開始」重新開機作業。 用戶端可能會在暫停時進入「服務」狀態 (這是工作特定) 。

</dd> <dt>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>

<span id="Terminate"></span><span id="terminate"></span><span id="TERMINATE"></span>**終止** (4) 


</dt> <dd>

以有條理的方式，完全停止工作、儲存資料、保留狀態，以及關閉所有基礎進程。

</dd> <dt>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>

<span id="Kill"></span><span id="kill"></span><span id="KILL"></span>**終止** (5) 


</dt> <dd>

立即終止工作，不需要儲存資料或保留狀態。

</dd> <dt>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>

<span id="Service"></span><span id="service"></span><span id="SERVICE"></span>**Service** (6) 


</dt> <dd>

將工作放入廠商特定的服務狀態。 用戶端可能會重新開機作業。

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

這個方法會傳回下列其中一個值。



| 傳回碼/值                                                                                                                                                               | 描述                                                                        |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------|
| <dl> <dt>**已完成，沒有錯誤**</dt> <dt>0</dt> </dl>                   | 成功。<br/>                                                                |
| <dl> <dt>**不支援使用 Timeout 參數**</dt> <dt>4098</dt> </dl> |                                                                                    |
| <dl> <dt>**失敗**</dt> <dt>32768</dt> </dl>                                |                                                                                    |
| <dl> <dt>**拒絕存取**</dt> <dt>32769</dt> </dl>                         | 拒絕存取。<br/>                                                          |
| <dl> <dt>**不支援**</dt> <dt>32770</dt> </dl>                         |                                                                                    |
| <dl> <dt>**狀態為未知**</dt> <dt>32771</dt> </dl>                     |                                                                                    |
| <dl> <dt>**Timeout**</dt> <dt>32772</dt> </dl>                               |                                                                                    |
| <dl> <dt>**不正確參數**</dt> <dt>32773</dt> </dl>                     |                                                                                    |
| <dl> <dt>**系統使用中**</dt> <dt>32774</dt> </dl>                      |                                                                                    |
| <dl> <dt>**此操作的狀態無效**</dt> <dt>32775</dt> </dl>      | 不支援在 *RequestedState* 參數中指定的值。<br/> |
| <dl> <dt>**不正確的資料類型**</dt> <dt>32776</dt> </dl>                   |                                                                                    |
| <dl> <dt>**系統無法使用**</dt> <dt>32777</dt> </dl>               |                                                                                    |
| <dl> <dt>**記憶體不足**</dt> <dt>32778</dt> </dl>                         |                                                                                    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 8.1 \[僅限桌面應用程式\]<br/>                                                            |
| 最低支援的伺服器<br/> | Windows Server 2012\[僅限 R2 desktop 應用程式\]<br/>                                                 |
| 命名空間<br/>                | \\\\根 \\ 虛擬化 \\ V2<br/>                                                                 |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Msvm \_ CopyFileToGuestJob**](msvm-copyfiletoguestjob.md)
</dt> </dl>

 

 




