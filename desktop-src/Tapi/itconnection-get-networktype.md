---
description: Get \_ NetworkType 方法會取得網路類型。
ms.assetid: 5597284a-9cc6-422b-a064-cda25aa5964b
title: 'ITConnection：： get_NetworkType 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 5d323d7465563d0a0d400c930585c2c0df002cedfae252d205d53aea8040f337
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119660328"
---
# <a name="itconnectionget_networktype-method"></a>ITConnection：： get \_ NetworkType 方法

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**Get \_ NetworkType** 方法會取得網路類型。

## <a name="syntax"></a>語法


```C++
HRESULT get_NetworkType(
  [out] BSTR *ppNetworkType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppNetworkType* \[擴展\]
</dt> <dd>

包含網路類型之 **BSTR** 的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回碼                                                                                   | 描述                                                      |
|-----------------------------------------------------------------------------------------------|------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                     |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PpNetworkType* 參數不是有效的指標。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/>  |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                    |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                   |



 

## <a name="remarks"></a>備註

應用程式必須使用 [**SysFreeString**](/windows/win32/api/oleauto/nf-oleauto-sysfreestring) 來釋放配置給 *ppNetworkType* 參數的記憶體。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITConnection**](itconnection.md)
</dt> <dt>

[**ITConnection：:p 的 \_ NetworkType**](itconnection-put-networktype.md)
</dt> </dl>

 

