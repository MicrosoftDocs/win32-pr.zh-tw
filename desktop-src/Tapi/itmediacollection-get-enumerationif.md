---
description: Get \_ EnumerationIf 方法會取得媒體列舉介面的指標。
ms.assetid: d5f1e10f-e5ad-45e6-a5ec-024905603012
title: 'ITMediaCollection：： get_EnumerationIf 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: dfe14475e216b5143b599aab50d12d1d0c548b5f64dd8e44edd2e6aab249905c
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119060856"
---
# <a name="itmediacollectionget_enumerationif-method"></a>ITMediaCollection：： get \_ EnumerationIf 方法

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**Get \_ EnumerationIf** 方法會取得媒體列舉介面的指標。

## <a name="syntax"></a>語法


```C++
HRESULT get_EnumerationIf(
  [out] IEnumMedia **pVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVal* \[擴展\]
</dt> <dd>

所需專案的 [**IEnumMedia**](ienummedia.md) 介面指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                         | 意義                                                         |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 方法成功。<br/>                                    |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | *PVal* 參數不是有效的指標。<br/>         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足，無法執行操作。<br/> |
| <dl> <dt>**E \_ 失敗**</dt> </dl>        | 未指定的錯誤。<br/>                                   |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>     | 尚未實作這個方法。<br/>                  |



 

## <a name="remarks"></a>備註

這個方法可以與 [**get \_ \_ NewEnum**](itmediacollection-get--newenum.md)互換，不同之處在于它會傳回 [**IEnumMedia**](ienummedia.md)而不是 **IUnknown**。

TAPI 會在 **ITMediaCollection：： get \_ Enumerationlf** 所傳回的 [**IEnumMedia**](ienummedia.md)介面上呼叫 **AddRef** 方法。 應用程式必須在 **IEnumMedia** 介面上呼叫 **Release** ，才能釋放與其相關聯的資源。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEnumMedia**](ienummedia.md)
</dt> <dt>

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




