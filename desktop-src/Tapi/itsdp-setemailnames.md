---
description: SetEmailNames 方法會設定與會議 blob 相關聯的電子郵件地址陣列。
ms.assetid: 1d6d5b01-bc0f-455f-8b23-bc0f409afde4
title: 'ITSdp：： SetEmailNames 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f23fa550c5750a3fad5d0b20ccdf2e032ed98c20a10b2f8e758ea7c9874e05a6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119140231"
---
# <a name="itsdpsetemailnames-method"></a>ITSdp：： SetEmailNames 方法

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**SetEmailNames** 方法會設定與會議 blob 相關聯的電子郵件地址陣列。

## <a name="syntax"></a>語法


```C++
HRESULT SetEmailNames(
  [in] VARIANT Addresses,
  [in] VARIANT Names
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*位址* \[在\]
</dt> <dd>

列出電子郵件地址之 **BSTR** 的 SAFEARRAY。

</dd> <dt>

*名稱* \[在\]
</dt> <dd>

**BSTR** 清單名稱的 SAFEARRAY。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | Description                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *位址* 或 *名稱* 參數無效。<br/>   |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                   |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                  |



 

## <a name="remarks"></a>備註

*位址* 和 *名稱* 的清單會指向相同的長度。

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

 

 




