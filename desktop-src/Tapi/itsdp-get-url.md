---
description: Get \_ url 方法會取得 url。
ms.assetid: 9ea2ddf6-b8c7-4bfa-aab3-ff2d2056837f
title: 'ITSdp：： get_Url 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 48c024a176c4acadebad7973df01a8448cdbf83ed50b1b404f01baef00e8c8b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119873678"
---
# <a name="itsdpget_url-method"></a>ITSdp：： get \_ Url 方法

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**Get \_ url** 方法會取得 url。

## <a name="syntax"></a>語法


```C++
HRESULT get_Url(
  [out] BSTR *ppUrl
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppUrl* \[擴展\]
</dt> <dd>

URL 之 **BSTR** 表示的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | 描述                                                     |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PpUrl* 參數不是有效的指標。<br/>        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                   |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                  |



 

## <a name="remarks"></a>備註

應用程式必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放配置給 *ppUrl* 參數的記憶體。

URL 通常用來參考包含其他資源的網頁或有關會議的背景資訊。

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
</dt> <dt>

[**ITSdp：:p 的內容 \_ Url**](itsdp-put-url.md)
</dt> </dl>

 

