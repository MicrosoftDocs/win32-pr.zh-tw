---
description: GetEmailNames 方法會取得與會議 blob 相關聯之電子郵件名稱的陣列。
ms.assetid: e51f25d7-41e5-408e-930b-396c7ac24437
title: 'ITSdp：： GetEmailNames 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f74ea369210a6ca32e47bb3359000195c544374b7352da96570f6d0f58f2af4f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140261"
---
# <a name="itsdpgetemailnames-method"></a>ITSdp：： GetEmailNames 方法

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**GetEmailNames** 方法會取得與會議 blob 相關聯之電子郵件名稱的陣列。

## <a name="syntax"></a>語法


```C++
HRESULT GetEmailNames(
  [out] VARIANT *pAddresses,
  [out] VARIANT *pNames
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAddresses* \[擴展\]
</dt> <dd>

會列出電子郵件地址的 **BSTR** 之 SAFEARRAY 的 **VARIANT** 指標。

</dd> <dt>

*pNames* \[擴展\]
</dt> <dd>

**BSTR** 清單名稱之 SAFEARRAY 的 **VARIANT** 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | 描述                                                               |
|-----------------------------------------------------------------------------------------------|---------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                              |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PAddresses* 或 *pNames* 參數不是有效的指標。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/>           |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                             |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                            |



 

## <a name="remarks"></a>備註

*PAddresses* 和 *pNames* 所指向的清單長度相同。

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

 

 




