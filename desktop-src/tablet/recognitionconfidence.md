---
description: 指出 IInkAnalyzer 具有辨識結果精確度的信賴等級。
ms.assetid: fd4fc350-b4db-4f9a-a5ae-00065e33606c
title: 'RecognitionConfidence 列舉 (IACom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RecognitionConfidence
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: e0358aacf789c391d99c10fc0fea64670dc4710e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987395"
---
# <a name="recognitionconfidence-enumeration"></a>RecognitionConfidence 列舉

指出 [**IInkAnalyzer**](iinkanalyzer.md) 具有辨識結果精確度的信賴等級。

## <a name="syntax"></a>Syntax


```C++
typedef enum RecognitionConfidence { 
  RecognitionConfidence_Strong        = 0,
  RecognitionConfidence_Intermediate  = 1,
  RecognitionConfidence_Poor          = 2,
  RecognitionConfidence_Unknown       = 3
} RecognitionConfidence;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="RecognitionConfidence_Strong"></span><span id="recognitionconfidence_strong"></span><span id="RECOGNITIONCONFIDENCE_STRONG"></span>**RecognitionConfidence \_ 強式**
</dt> <dd>

在結果或替代方面具有強烈的信賴度。

</dd> <dt>

<span id="RecognitionConfidence_Intermediate"></span><span id="recognitionconfidence_intermediate"></span><span id="RECOGNITIONCONFIDENCE_INTERMEDIATE"></span>**RecognitionConfidence \_ 中繼**
</dt> <dd>

結果或替代中的中繼信賴度。

</dd> <dt>

<span id="RecognitionConfidence_Poor"></span><span id="recognitionconfidence_poor"></span><span id="RECOGNITIONCONFIDENCE_POOR"></span>**RecognitionConfidence \_ 不良**
</dt> <dd>

結果或替代的信賴度不佳。

</dd> <dt>

<span id="RecognitionConfidence_Unknown"></span><span id="recognitionconfidence_unknown"></span><span id="RECOGNITIONCONFIDENCE_UNKNOWN"></span>**RecognitionConfidence \_ 不明**
</dt> <dd>

產生已辨識文字的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 不支援信賴等級。

</dd> </dl>

## <a name="remarks"></a>備註

[**IInkAnalyzer**](iinkanalyzer.md)會使用一或多個 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)物件，將手寫轉換成文字。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAnalysisAlternate：： GetRecognitionConfidence 方法**](ianalysisalternate-getrecognitionconfidence.md)
</dt> <dt>

[**ICoNtextNode::GetPropertyData**](icontextnode-getpropertydata.md)
</dt> <dt>

[內容節點屬性](context-node-properties.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




