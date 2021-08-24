---
description: Get \_ MediaCollection 方法會取得會議的 ITMediaCollection 介面指標。
ms.assetid: 8109582a-74f0-47e8-91d1-0d89c3d3c331
title: 'ITSdp：： get_MediaCollection 方法 (Sdpblb .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4cf358089a394775c753adc0642897021e91df5bfcd5f23418e638df82db03a1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119774508"
---
# <a name="itsdpget_mediacollection-method"></a>ITSdp：： get \_ MediaCollection 方法

\[Windows Vista、Windows Server 2008 及後續版本的作業系統無法使用會合 IP 電話語音會議控制項和介面。 RTC 用戶端 API 提供類似的功能。\]

**Get \_ MediaCollection** 方法會取得會議的 [**ITMediaCollection**](itmediacollection.md)介面指標。

## <a name="syntax"></a>語法


```C++
HRESULT get_MediaCollection(
  [out] ITMediaCollection **ppMediaCollection
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppMediaCollection* \[擴展\]
</dt> <dd>

[**ITMediaCollection**](itmediacollection.md)的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 值                                                                                                                           | 意義                                                                                     |
|---------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>                                            | 方法成功。<br/>                                                                |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>                                    | *PpMediaCollection* 參數不是有效的指標。<br/>                        |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl>                                   | 記憶體不足，無法執行操作。<br/>                             |
| <dl> <dt>**E \_ 失敗**</dt> </dl>                                          | 未指定的錯誤。<br/>                                                               |
| <dl> <dt>**\_錯誤碼中的 HRESULT \_ \_ (錯誤 \_ 不正確 \_ 資料)**</dt> </dl> | 發生內部錯誤，通常是因為先前的方法失敗。<br/> |
| <dl> <dt>**E \_ >NOTIMPL**</dt> </dl>                                       | 尚未實作這個方法。<br/>                                              |



 

## <a name="remarks"></a>備註

您也可以使用 **QueryInterface** 來取得 [**ITMediaCollection**](itmediacollection.md)指標。

TAPI 會在 **ITSdp：： get \_ MediaCollection** 所傳回的 [**ITMediaCollection**](itmediacollection.md)介面上呼叫 **AddRef** 方法。 應用程式必須在 **ITMediaCollection** 介面上呼叫 **Release** ，才能釋放與其相關聯的資源。

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

[**ITMediaCollection**](itmediacollection.md)
</dt> </dl>

 

 




