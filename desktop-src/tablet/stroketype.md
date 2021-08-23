---
description: 指出是否應該在繪圖中分析筆劃，或是做為書寫的一部分進行分析。
ms.assetid: 3f4c4522-ada7-4759-bca7-88b2a71f36ea
title: 'StrokeType 列舉 (IACom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrokeType
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: 4b02a05582d675f04ad4458b1cb21c6d4a1797bacf15baf5d0851804d1a95d49
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119589578"
---
# <a name="stroketype-enumeration"></a>StrokeType 列舉

指出是否應該在繪圖中分析筆劃，或是做為書寫的一部分進行分析。

## <a name="syntax"></a>Syntax


```C++
typedef enum StrokeType { 
  StrokeType_Unclassified  = 0,
  StrokeType_Writing       = 1,
  StrokeType_Drawing       = 2
} StrokeType;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="StrokeType_Unclassified"></span><span id="stroketype_unclassified"></span><span id="STROKETYPE_UNCLASSIFIED"></span>**StrokeType 非 \_ 分類**
</dt> <dd>

筆劃可能是繪圖或部分書寫的一部分。

</dd> <dt>

<span id="StrokeType_Writing"></span><span id="stroketype_writing"></span><span id="STROKETYPE_WRITING"></span>**StrokeType \_ 撰寫**
</dt> <dd>

筆劃是撰寫的一部分。

</dd> <dt>

<span id="StrokeType_Drawing"></span><span id="stroketype_drawing"></span><span id="STROKETYPE_DRAWING"></span>**StrokeType \_ 繪圖**
</dt> <dd>

筆觸是繪圖的一部分。

</dd> </dl>

## <a name="examples"></a>範例

下列範例顯示的部分筆觸事件處理常式，是以類似于 [c + + 事件接收器範例](c---event-sinks-sample.md)的方式來執行。 已檢查新增的筆觸，以查看其周框方塊的頂端是否已繪製在邊界下方 `drawingMargin` 。 如果是，則[](iinkanalyzer.md) `m_spInkAnalyzer` 會將 IInkAnalyzer 物件設定為將筆劃分析為繪圖筆劃，而不是手寫筆劃。 `CheckHResult` 是採用和字串的函式 `HRESULT` ，如果 `HRESULT` 不 **成功**，則會擲回以字串建立的例外狀況。


```C++
IInkRectangle* bounds;
CheckHResult(pStroke->GetBoundingBox(IBBM_Default, &bounds), "IInkStrokeDisp::GetBoundingBox failed");
long top;
CheckHResult(bounds->get_Top(&top), "IInkRectangle::get_Top failed");
if (top > drawingMargin)
{
    long strokeId;
    CheckHResult(pStroke->get_ID(&strokeId), "IInkStrokeDisp::get_ID failed");
    m_pInkAnalyzer->SetStrokeType(strokeId, StrokeType_Drawing);
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInkAnalyzer：： SetStrokeType 方法**](iinkanalyzer-setstroketype.md)
</dt> </dl>

 

 




