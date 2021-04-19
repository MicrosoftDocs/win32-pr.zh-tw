---
description: 請注意，此介面已被取代。
ms.assetid: d9800850-b0ee-44f7-bcb4-f2bac8d17693
title: 'IAMFilterData 介面 (Fil \_ data .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAMFilterData
api_type:
- COM
api_location:
- fil_data.h
ms.openlocfilehash: 1ab5ea8e9c90c043c33cca4d9f8138dd7d9937ad
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989557"
---
# <a name="iamfilterdata-interface"></a>IAMFilterData 介面

> [!Note]  
> 這個介面已被取代。 新的應用程式應該改用 [**IFilterMapper2**](/windows/desktop/api/Strmif/nn-strmif-ifiltermapper2) 介面。

 

`IAMFilterData`介面會將篩選資訊轉換成封裝的二進位資料，而這些資料可以儲存在登錄中。 篩選對應程式物件會公開這個介面。

## <a name="members"></a>成員

**IAMFilterData** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。 **IAMFilterData** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IAMFilterData** 介面具有這些方法。



| 方法                                                     | 描述                                               |
|:-----------------------------------------------------------|:----------------------------------------------------------|
| [**CreateFilterData**](iamfilterdata-createfilterdata.md) | 建立篩選的二進位登錄資料。<br/>     |
| [**ParseFilterData**](iamfilterdata-parsefilterdata.md)   | 解壓縮篩選的二進位登錄資料。<br/> |



 

## <a name="remarks"></a>備註

> [!Note]  
> 標頭 Fil \_ data .h 位於 Windows SDK 的對應工具 [範例](mapper-sample.md) 目錄中。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Fil \_ 資料。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[已淘汰的介面](deprecated-interfaces.md)
</dt> </dl>

 

 
