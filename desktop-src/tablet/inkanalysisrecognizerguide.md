---
description: 指定用來繪製和辨識筆墨的節目表或區域。
ms.assetid: 5bd874ff-003b-4471-b4ef-50731007dc5a
title: 'InkAnalysisRecognizerGuide 結構 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkAnalysisRecognizerGuide
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: eab5b1d09354f021f2c0a7e66a41b53e761d51e8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970801"
---
# <a name="inkanalysisrecognizerguide-structure"></a>InkAnalysisRecognizerGuide 結構

指定用來繪製和辨識筆墨的節目表或區域。

## <a name="syntax"></a>語法


```C++
typedef struct InkAnalysisRecognizerGuide {
  RECT rectWritingBox;
  RECT rectDrawnBox;
  long cRows;
  long cColumns;
  long midline;
} InkAnalysisRecognizerGuide;
```



## <a name="members"></a>成員

<dl> <dt>

**rectWritingBox**
</dt> <dd>

辨識指南中的不可見書寫區域，其實可以進行寫入。

</dd> <dt>

**rectDrawnBox**
</dt> <dd>

在平板電腦螢幕上繪製的矩形，以及進行寫入的位置。

</dd> <dt>

**烏鴉**
</dt> <dd>

[辨識指南] 方塊中的資料列數目。

</dd> <dt>

**cColumns**
</dt> <dd>

[辨識指南] 方塊中的資料行數目。

</dd> <dt>

**中線**
</dt> <dd>

辨識指南方塊的中線高度。 中線高度是繪製方塊的距離，從基準到中線的距離。

</dd> </dl>

## <a name="remarks"></a>備註

**InkAnalysisRecognizerGuide** 會針對字元定義預期的輸入區域，例如行或方塊。 **InkAnalysisRecognizerGuide** 結構只能在分析提示內容節點上設定 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) 。 [**IInkAnalyzer**](iinkanalyzer.md)會流量分析提示節點的位置和筆墨筆劃的位置，以將筆劃與分析提示節點產生關聯。 如果 **IInkAnalyzer** 支援 **InkAnalysisRecognizerGuide**，則任何與分析提示節點相關聯的筆劃都將具有指定的 **InkAnalysisRecognizerGuide** ，以供 **IInkAnalyzer** 辨識。 **InkAnalysisRecognizerGuide** 類別中表示的值一律相對於分析提示節點的位置，並且以筆墨空間座標指定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[分析提示屬性](analysis-hint-properties.md)
</dt> <dt>

[**IInkAnalyzer：： CreateAnalysisHint 方法**](iinkanalyzer-createanalysishint.md)
</dt> <dt>

[**ICoNtextNode::AddPropertyData**](icontextnode-addpropertydata.md)
</dt> <dt>

[**ICoNtextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




