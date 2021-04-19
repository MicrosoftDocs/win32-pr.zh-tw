---
description: GetPhoneNumbers 方法會取得與會議 blob 相關聯的電話號碼陣列。
ms.assetid: c4ad6c5a-e15c-45ae-94de-763a843554bb
title: 'ITSdp：： GetPhoneNumbers 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 465bc6b2d2167ca17d25b8f50466f111724ea3b5
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001626"
---
# <a name="itsdpgetphonenumbers-method"></a>ITSdp：： GetPhoneNumbers 方法

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**GetPhoneNumbers** 方法會取得與會議 blob 相關聯的電話號碼陣列。

## <a name="syntax"></a>語法


```C++
HRESULT GetPhoneNumbers(
  [out] VARIANT *pNumbers,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pNumbers* \[擴展\]
</dt> <dd>

列出電話號碼的 **BSTR** 之 SAFEARRAY 的 **VARIANT** 指標。

</dd> <dt>

*pNames* \[擴展\]
</dt> <dd>

**BSTR** 清單名稱之 SAFEARRAY 的 **VARIANT** 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | Description                                                             |
|-----------------------------------------------------------------------------------------------|-------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                            |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PNumbers* 或 *pNames* 參數不是有效的指標。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/>         |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                           |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                          |



 

## <a name="remarks"></a>備註

*PNumbers* 和 *pNames* 所指向的清單長度相同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITSdp**](itsdp.md)
</dt> </dl>

 

 




