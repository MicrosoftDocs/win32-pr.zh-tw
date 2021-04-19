---
description: Get \_ EnumerationIf 方法會傳回列舉 ITTime 的 IEnumTime 列舉介面。
ms.assetid: 31f6fa94-d047-4c53-96ae-8dd7e66a4e33
title: 'ITTimeCollection：： get_EnumerationIf 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a698fca73e923597b2dff5b82e3258dd79306f05
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990590"
---
# <a name="ittimecollectionget_enumerationif-method"></a>ITTimeCollection：： get \_ EnumerationIf 方法

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**Get \_ EnumerationIf** 方法會傳回列舉 [**ITTime**](ittime.md)的 [**IEnumTime**](ienumtime.md)列舉介面。

## <a name="syntax"></a>語法


```C++
HRESULT get_EnumerationIf(
  [out] IEnumTime **pVal
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pVal* \[擴展\]
</dt> <dd>

[**IEnumTime**](ienumtime.md)介面的指標。

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

這個方法可以與 [**get \_ \_ NewEnum**](ittimecollection-get--newenum.md)互換，不同之處在于它會傳回 [**IEnumTime**](ienumtime.md)而不是 **IUnknown**。

TAPI 會在 **ITTimeCollection：： get \_ EnumerationIf** 所傳回的 [**IEnumTime**](ienumtime.md)介面上呼叫 **AddRef** 方法。 應用程式必須在 [**IEnumTime**](ienumtime.md)介面上呼叫 **Release** ，才能釋放與其相關聯的資源。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------|---------------------------------------------------------------------------------------|
| TAPI 版本<br/> | 需要 TAPI 3.0 或更新版本<br/>                                                 |
| 標頭<br/>       | <dl> <dt>Sdpblb。h</dt> </dl>   |
| 程式庫<br/>      | <dl> <dt>Uuid</dt> </dl>   |
| DLL<br/>          | <dl> <dt>Sdpblb.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IEnumTime**](ienumtime.md)
</dt> <dt>

[**ITTimeCollection**](ittimecollection.md)
</dt> <dt>

[**ITTime**](ittime.md)
</dt> </dl>

 

 




