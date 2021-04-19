---
description: CSeekingPassThru 類別是建立 CPosPassThru 和 CRendererPosPassThru 物件的 helper 物件。
ms.assetid: a748ea5c-d93f-4f80-9d2f-bef5a5c1c2fb
title: 'CSeekingPassThru 類別 (Seekpt) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CSeekingPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 273f9b6686c4455452924dc43628801fae5d518a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990030"
---
# <a name="cseekingpassthru-class"></a>CSeekingPassThru 類別

`CSeekingPassThru`類別是可建立 [**CPosPassThru**](cpospassthru.md)和 [**CRendererPosPassThru**](crendererpospassthru.md)物件的 helper 物件。

**CPosPassThru** 和 **CRendererPosPassThru** 類別是通過上游搜尋命令的協助程式物件，因此 `CSeekingPassThru` 類別是用來建立 helper 物件的 helper 物件。

不需要直接使用這個類別。 相反地，請使用 [**CreatePosPassThru**](createpospassthru.md) 函式，此函式會處理所有使用這個類別的詳細資料。 它有更多從 Quartz.dll 載入物件的優點，這會稍微減少篩選的程式碼大小。 如需詳細資訊，請參閱 [**CPosPassThru**](cpospassthru.md)。

`CSeekingPassThru`類別會公開 [**ISeekingPassThru**](/windows/desktop/api/Strmif/nn-strmif-iseekingpassthru)介面。 [**ISeekingPassThru：： Init**](/windows/desktop/api/Strmif/nf-strmif-iseekingpassthru-init)方法會初始化物件。 物件初始化之後，篩選可以針對 [**IMediaSeeking**](/windows/desktop/api/Strmif/nn-strmif-imediaseeking) 和 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) 介面進行查詢。



| 公用方法                                                  | Description                        |
|-----------------------------------------------------------------|------------------------------------|
| [**CSeekingPassThru**](cseekingpassthru-cseekingpassthru.md)   | 函式方法。                |
| [**~ CSeekingPassThru**](cseekingpassthru--cseekingpassthru.md) | 函式方法。                 |
| [**CreateInstance**](cseekingpassthru-createinstance.md)       | 建立物件的實例。 |
| ISeekingPassThru 方法                                        | Description                        |
| [**Init**](cseekingpassthru-init.md)                           | 初始化物件。            |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Seekpt (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




