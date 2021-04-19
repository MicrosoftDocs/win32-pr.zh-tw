---
description: Get \_ TimeCollection 方法會取得會議的 ITTimeCollection 介面指標。
ms.assetid: 1cfe3f5a-dcf7-480b-9b23-e17259d8ee9c
title: 'ITSdp：： get_TimeCollection 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c1bac0f38f8c96762d4e36d8d3dfdff2136bdb86
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106981378"
---
# <a name="itsdpget_timecollection-method"></a>ITSdp：： get \_ TimeCollection 方法

\[ 在 Windows Vista、Windows Server 2008 和後續版本的作業系統中，無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**Get \_ TimeCollection** 方法會取得會議的 [**ITTimeCollection**](ittimecollection.md)介面指標。

## <a name="syntax"></a>語法


```C++
HRESULT get_TimeCollection(
  [out] ITTimeCollection **ppTimeCollection
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppTimeCollection* \[擴展\]
</dt> <dd>

[**ITTimeCollection**](ittimecollection.md)的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                                                           | 意義                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                                            | 方法成功。<br/>                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                    | *PpTimeCollection* 參數不是有效的指標。<br/>                         |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                                   | 記憶體不足，無法執行操作。<br/>                             |
| <dl> <dt>**E \_ 失敗**</dt> </dl>                                          | 未指定的錯誤。<br/>                                                               |
| <dl> <dt>**\_錯誤碼中的 HRESULT \_ \_ (錯誤 \_ 不正確 \_ 資料)**</dt> </dl> | 發生內部錯誤，通常是因為先前的方法失敗。<br/> |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>                                       | 尚未實作這個方法。<br/>                                              |



 

## <a name="remarks"></a>備註

您也可以使用 **QueryInterface** 來取得 [**ITTimeCollection**](ittimecollection.md)指標。

TAPI 會在 **ITSdp：： get \_ TimeCollection** 所傳回的 [**ITTimeCollection**](ittimecollection.md)介面上呼叫 **AddRef** 方法。 應用程式必須在 **ITTimeCollection** 介面上呼叫 **Release** ，才能釋放與其相關聯的資源。

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

[**ITTimeCollection**](ittimecollection.md)
</dt> </dl>

 

 




