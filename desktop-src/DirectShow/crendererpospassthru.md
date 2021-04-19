---
description: CRendererPosPassThru 類別會處理轉譯器篩選的搜尋命令，方法是將它們傳遞給下一個篩選器。
ms.assetid: 7b532177-939c-4cb7-a6fa-c0133f65c768
title: 'CRendererPosPassThru 類別 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRendererPosPassThru
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7154dde8adefdb3292107e9c33d7b6a2b54f6af0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994043"
---
# <a name="crendererpospassthru-class"></a>CRendererPosPassThru 類別

![crendererpospassthru 類別階層](images/cutil14.png)

`CRendererPosPassThru`類別會處理轉譯器篩選的搜尋命令，方法是將它們傳遞給下一個篩選器。

這個類別衍生自 [**CPosPassThru**](cpospassthru.md) 類別。 它新增了在範例抵達時快取時間戳記的支援。 使用與 **CPosPassThru** 類別相同的方式來使用這個類別。 如需詳細資訊，請參閱 **CPosPassThru** 檔。

轉譯器篩選準則必須更新 `CRendererPosPassThru` 物件的快取時間戳記，如下所示：

-   針對篩選器收到的每個範例，呼叫 [**CRendererPosPassThru：： RegisterMediaTime**](crendererpospassthru-registermediatime.md) 方法。
-   當篩選準則停止或接收 **EndFlush** 呼叫時，請呼叫 [**CRendererPosPassThru：： ResetMediaTime**](crendererpospassthru-resetmediatime.md) 方法。
-   當篩選接收到資料流程結束通知時，請呼叫 [**CRendererPosPassThru：： EOS**](crendererpospassthru-eos.md) 方法。

如需如何使用這個類別的範例，請參閱 [**CBaseRenderer**](cbaserenderer.md) 原始程式碼。



| 公用方法                                                            | Description                                                         |
|---------------------------------------------------------------------------|---------------------------------------------------------------------|
| [**CRendererPosPassThru**](crendererpospassthru-crendererpospassthru.md) | 函式方法。                                                 |
| [**GetMediaTime**](crendererpospassthru-getmediatime.md)                 | 抓取目前樣本上的時間戳記。                    |
| [**RegisterMediaTime**](crendererpospassthru-registermediatime.md)       | 快取目前範例中的時間戳記。                     |
| [**ResetMediaTime**](crendererpospassthru-resetmediatime.md)             | 將快取的時間戳記重設為零。                              |
| [**Eos**](crendererpospassthru-eos.md)                                   | 在結束資料流程通知之後，更新快取的時間戳記。 |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



 

 




