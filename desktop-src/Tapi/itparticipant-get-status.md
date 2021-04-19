---
description: Get \_ Status 方法會傳回 VARIANT \_ BOOL，指出參與者的狀態。
ms.assetid: 03ad763b-5223-41b5-b0cf-1f13c761f5c2
title: 'ITParticipant：： get_Status 方法 (Ipmsp .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2de39ac0833f856e35cc120b4f4e5b00bcd617de
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976072"
---
# <a name="itparticipantget_status-method"></a>ITParticipant：： get \_ Status 方法

\[**取得 \_** 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用狀態。 RTC 用戶端 API 提供類似的功能。\]

**Get \_ Status** 方法會傳回 VARIANT \_ BOOL，指出參與者的狀態。

## <a name="syntax"></a>語法


```C++
HRESULT get_Status(
  [in]  ITStream     *pITStream,
  [out] VARIANT_BOOL *pStatus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pITStream* \[在\]
</dt> <dd>

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)介面的指標。

</dd> <dt>

*pStatus* \[擴展\]
</dt> <dd>

如果已在 \_ 資料流程上啟用參與者，則為 variant TRUE，如果已停用則為 variant \_ 。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | Description                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                              |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 未執行方法。<br/>                                        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/>           |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PITStream* 參數不是有效的指標。<br/>              |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *PITStream* 參數未指向有效的介面。<br/> |



 

## <a name="remarks"></a>備註

啟用或停用某個參與者在資料流程上的狀態，可讓應用程式基本上將指定的參與者靜音。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|--------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                |
| 標頭<br/>       | <dl> <dt>Ipmsp。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>  |
| DLL<br/>          | <dl> <dt>Tapi3.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITParticipant**](itparticipant.md)
</dt> <dt>

[**ITStream**](/windows/win32/api/tapi3if/nn-tapi3if-itstream)
</dt> <dt>

[**put \_ 狀態**](itparticipant-put-status.md)
</dt> </dl>

 

