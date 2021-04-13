---
description: 包含物件的集合，這些物件會執行 IInkAnalysisRecognizer 介面，以及表示辨識手寫、物件或手勢的能力。
ms.assetid: d9264c9f-bf75-493e-8e41-57ea69955e6b
title: 'IInkAnalysisRecognizers 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizers
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: ba9bbcd029803e613fb27d351de554c013c02616
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318463"
---
# <a name="iinkanalysisrecognizers-interface"></a>IInkAnalysisRecognizers 介面

包含物件的集合，這些物件會執行 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 介面，以及表示辨識手寫、物件或手勢的能力。

## <a name="members"></a>成員

**IInkAnalysisRecognizers** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IInkAnalysisRecognizers** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IInkAnalysisRecognizers** 介面具有這些方法。



| 方法                                                                               | 描述                                                                                                             |
|:-------------------------------------------------------------------------------------|:------------------------------------------------------------------------------------------------------------------------|
| [**GetCount**](iinkanalysisrecognizers-getcount.md)                                 | 抓取這個集合中的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 物件數目。<br/> |
| [**GetInkAnalysisRecognizer**](iinkanalysisrecognizers-getinkanalysisrecognizer.md) | 抓取位於指定之索引處的 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 。<br/>               |



 

## <a name="remarks"></a>備註

[**IInkAnalyzer**](iinkanalyzer.md)的 [**IInkAnalyzer：： GetInkAnalysisRecognizersByPriority 方法**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)方法會傳回 **IInkAnalysisRecognizers** 集合，其中包含目前平板電腦上可用的筆墨辨識器。

針對語言辨識器， [**IInkAnalysisRecognizer：： GetLanguages**](iinkanalysisrecognizer-getlanguages.md) 方法會傳回非空白的陣列。 針對筆勢辨識器和物件辨識器， **IInkAnalysisRecognizer：： GetLanguages** 方法會傳回空陣列。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**IInkAnalyzer：： GetInkAnalysisRecognizersByPriority 方法**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

