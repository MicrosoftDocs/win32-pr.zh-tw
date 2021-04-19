---
title: 'DeducingBlobSetter (D2d1effecthelpers) '
description: 會推算類別和引數，然後針對 blob 類型屬性呼叫成員函式屬性 setter 回呼。
ms.assetid: 4B8B871D-FE5E-4EF3-AEED-A3D92C10E8C6
keywords:
- DeducingBlobSetter Direct2D
topic_type:
- apiref
api_name:
- DeducingBlobSetter
api_location:
- d2d1effecthelpers.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a2d3bbfcc0a48d722bd98456821d7f7df5e8780a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106978417"
---
# <a name="deducingblobsetter"></a>DeducingBlobSetter

會推算類別和引數，然後針對 blob 類型屬性呼叫成員函式屬性 setter 回呼。

> [!Note]  
> DeducingBlobSetter 不應該直接呼叫。

 

``` syntax
template<class C, typename I>  
HRESULT DeducingBlobSetter(  
    _In_ HRESULT (C::*callback)(const BYTE *, UINT32),  
    _In_ I *effect,  
    _In_reads_(dataSize) const BYTE *data,  
    UINT32 dataSize,  
    ) 
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D2d1effecthelpers。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Direct2D：:D educingBlobGetter**](deducingblobgetter.md)
</dt> </dl>

 

 





