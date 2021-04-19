---
description: 表示能夠分析筆劃集合的版面配置，並將其分成文字和圖形。
ms.assetid: 2c8e67fb-1032-4fcc-b419-82bae978daf8
title: 'InkDivider 類別 (Msinkaut15) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- InkDivider
- InkDivider.IInkDivider
api_type:
- COM
api_location:
- Inkdiv.dll
- Inkdiv.dll.dll
ms.openlocfilehash: c0658504303968803bd2abff063694701d121390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996914"
---
# <a name="inkdivider-class"></a>InkDivider 類別

表示能夠分析筆劃集合的版面配置，並將其分成文字和圖形。

**InkDivider** 具有下列類型的成員：

-   [介面](#interfaces)
-   [方法](#methods)
-   [屬性](#properties)

### <a name="interfaces"></a>介面

**InkDivider** 類別會定義這些介面。



| 介面       | 描述                                                          |
|:----------------|:---------------------------------------------------------------------|
| **IInkDivider** | 這個物件會實 **IInkDivider** COM 介面。<br/> |



 

### <a name="methods"></a>方法

**InkDivider** 類別有這些方法。



| 方法                              | 描述                                                                                                                                                        |
|:------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**劃分**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-divide) | 傳回 [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) 物件，其中包含 **InkDivider** 物件中筆劃的結構化資訊。<br/> |



 

### <a name="properties"></a>屬性

**InkDivider** 類別具有這些屬性。



| 屬性                                                             | 存取類型           | Description                                                                                                                     |
|:---------------------------------------------------------------------|:----------------------|:--------------------------------------------------------------------------------------------------------------------------------|
| [**LineHeight**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_lineheight)<br/>               | 讀取/寫入<br/> | 取得或設定 HIMETRIC 單位中預期的手寫高度。<br/>                                                      |
| [**RecognizerCoNtext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext)<br/> | 讀取/寫入<br/> | 取得或設定用於手寫辨識的 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md) 物件。<br/> |
| [**中風**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes)<br/>                     | 讀取/寫入<br/> | 取得或設定 **InkDivider** 物件所包含的 [**InkStrokes**](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合。 <br/>     |



 

## <a name="remarks"></a>備註

此物件可以透過在 c + + 中呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 方法來具現化。

**InkDivider** 物件使用筆觸的版面配置、筆劃的新增順序、筆劃的繪製方向，以及執行筆墨分析的其他因素。」。 **InkDivider** 物件所分析的 [InkStrokes](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))集合會包含在 **InkDivider** 物件的 [[**筆觸**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes)] 屬性中。 當您在集合中加入或刪除時， **InkDivider** 物件會動態分析 InkStrokes 集合，但不會執行任何筆觸修改。

分析結果會在 [**IInkDivisionResult**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult) 物件中傳回。

**InkDivider** 物件會使用 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md)物件，以更精確地分割筆劃並將辨識字串指派給結果。

> [!Note]  
> **InkDivider** 物件使用 [**InkRecognizerCoNtext**](inkrecognizercontext-class.md)物件的預設屬性設定。

 

如果您沒有將辨識器內容指派給 **InkDivider** 物件， **InkDivider** 物件仍會分析筆墨，但是會比較不精確地分割筆劃，且不會將文字與部門結果產生關聯。

> [!Note]  
> 在將筆劃新增至 [**筆觸**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_strokes)屬性之前，應該先設定 [**RecognizerCoNtext**](/windows/win32/api/msinkaut15/nf-msinkaut15-iinkdivider-get_recognizercontext)屬性。 將筆劃加入至 **InkDivider** 物件之後，就無法變更 **RecognizerCoNtext** 屬性。

 

**InkDivider** 目前不支援垂直語言。 為了讓 **InkDivider** 物件正確辨識這些語言，該語言的 [**IInkRecognizer**](/windows/desktop/api/msinkaut/nn-msinkaut-iinkrecognizer) 物件必須支援可用的輸入功能，而且必須由左至右寫入字元。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                           |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                               |
| 標頭<br/>                   | <dl> <dt>Msinkaut15 (也需要 Msinkaut15 \_ c) </dt> </dl> |
| 程式庫<br/>                  | <dl> <dt>Inkdiv.dll</dt> </dl>                                   |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInkDivisionResult 介面**](/windows/desktop/api/msinkaut15/nn-msinkaut15-iinkdivisionresult)
</dt> <dt>

[**InkRecognizerCoNtext 類別**](inkrecognizercontext-class.md)
</dt> <dt>

[InkStrokes 集合](/previous-versions/windows/desktop/legacy/ms703293(v=vs.85))
</dt> </dl>

 

