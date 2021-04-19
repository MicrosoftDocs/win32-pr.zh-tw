---
description: CBaseDispatch 類別是在 DirectShow 篩選器中實作為 IDispatch 介面的基類。
ms.assetid: 33a989be-d059-4ad7-99f8-715c55a128a2
title: 'CBaseDispatch 類別 (Ctlutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CBaseDispatch
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: d115412b2b668f640834d5a3fa3b134f7a8d9c01
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995936"
---
# <a name="cbasedispatch-class"></a>CBaseDispatch 類別

![cbasedispatch 類別階層](images/cutil01.png)

**CBaseDispatch** 類別是在 DirectShow 篩選器中實作為 **IDispatch** 介面的基類。

此類別僅限於支援 DirectShow 類型程式庫（QuartzTypeLib）所匯出的自動化相容介面。 例如， [**CMediaControl**](cmediacontrol.md) 和 [**CMediaPosition**](cmediaposition.md) 類別會使用 **CBaseDispatch** 分別執行 [**IMediaControl**](/windows/desktop/api/Control/nn-control-imediacontrol) 和 [**IMediaPosition**](/windows/desktop/api/Control/nn-control-imediaposition)。 由於這項限制，因此可能沒有理由直接在您自己的篩選器中使用 **CBaseDispatch** 。

若要使用此類別，請執行下列動作：

-   宣告支援 **IDispatch** 的新類別。
-   為您的新類別提供 **CBaseDispatch** 型別的私用成員變數。
-   執行 **IDispatch** 方法。
-   在您的 **IDispatch** 方法中，呼叫 **CBaseDispatch** 方法。

如需詳細資訊，請參閱 Ctlutil 中所宣告的任何範例類別的原始程式碼。



| 公用方法                                             | Description                                                                                                         |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------|
| [**CBaseDispatch**](cbasedispatch-cbasedispatch.md)       | 函式方法。                                                                                                 |
| [**~ CBaseDispatch**](cbasedispatch--cbasedispatch.md)     | 函式方法。                                                                                                  |
| [**GetIDsOfNames**](cbasedispatch-getidsofnames.md)       | 將一組名稱對應至一組對應的 Dispid。                                                              |
| [**GetTypeInfo**](cbasedispatch-gettypeinfo.md)           | 抓取物件的型別資訊，然後用來取得介面的型別資訊。 |
| [**GetTypeInfoCount**](cbasedispatch-gettypeinfocount.md) | 抓取物件提供的類型資訊介面數目。                                            |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Ctlutil (包含： .h) </dt> </dl>                                                                                   |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[DirectShow 基類](directshow-base-classes.md)
</dt> </dl>

 

 




