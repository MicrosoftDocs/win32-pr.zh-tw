---
description: CMediaPosition 類別會處理 IMediaPosition 雙重介面的 IDispatch 方法。
ms.assetid: 5e84a2b6-39d4-47a4-93b4-690df12e2d19
title: 'CMediaPosition 類別 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMediaPosition
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 7305d5eded589e167352ce7ff13194b52965b939daf907e8381b64684a03d1bb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119634848"
---
# <a name="cmediaposition-class"></a>CMediaPosition 類別

![cmediaposition 類別階層](images/cutil14.png)

**CMediaPosition** 類別會處理 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)雙重介面的 **IDispatch** 方法。

此類別會繼承 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition) 介面，但不會加以執行。 它會透過 [**CBaseDispatch**](cbasedispatch.md)類別和 DirectShow 類型程式庫來實行 **IDispatch** 。 請勿直接使用這個類別。 相反地，請使用下列其中一個類別：

-   來源篩選器：使用 [**CSourceSeeking**](csourceseeking.md) 基類來執行搜尋。
-   轉換篩選：使用 [**CPosPassThru**](cpospassthru.md) 類別傳遞上游的搜尋命令。
-   轉譯器：使用 [**CRendererPosPassThru**](crendererpospassthru.md) 類別傳遞上游的搜尋命令。



| 公用方法                                              | 描述                                                                                                         |
|-------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**CMediaPosition**](cmediaposition-cmediaposition.md)     | 函式方法。                                                                                                 |
| IDispatch 方法                                           | 描述                                                                                                         |
| [**GetIDsOfNames**](cmediaposition-getidsofnames.md)       | 地圖一組名稱一組對應的 Dispid。                                                              |
| [**GetTypeInfo**](cmediaposition-gettypeinfo.md)           | 抓取物件的型別資訊，然後用來取得介面的型別資訊。 |
| [**GetTypeInfoCount**](cmediaposition-gettypeinfocount.md) | 抓取物件提供的類型資訊介面數目。                                            |
| [**調用**](cmediaposition-invoke.md)                     | 提供物件所公開之屬性和方法的存取權。                                                    |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow基類](directshow-base-classes.md)
</dt> </dl>

 

 




