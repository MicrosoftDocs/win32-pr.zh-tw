---
description: 表示 ICoNtextNode 物件的可能手寫辨識字組相符專案。
ms.assetid: a497c140-6166-4309-af0f-851af09015c6
title: 'IAnalysisAlternate 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8f65b97ca3811212b73c6bdb12e9b889636dd6ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191427"
---
# <a name="ianalysisalternate-interface"></a>IAnalysisAlternate 介面

表示 [**ICoNtextNode**](icontextnode.md) 物件的可能手寫辨識字組相符專案。

## <a name="members"></a>成員

**IAnalysisAlternate** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IAnalysisAlternate** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IAnalysisAlternate** 介面具有這些方法。



| 方法                                                                          | 描述                                                                                                                                                          |
|:--------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAlternateNodes**](ianalysisalternate-getalternatenodes.md)               | 抓取與這個替代相關聯的 [**ICoNtextNode**](icontextnode.md) 物件。<br/>                                                       |
| [**GetRecognitionConfidence**](ianalysisalternate-getrecognitionconfidence.md) | 抓取值，指出 [**IInkAnalyzer**](iinkanalyzer.md) 對 **IAnalysisAlternate** 精確度的信賴等級。<br/> |
| [**GetRecognizedString**](ianalysisalternate-getrecognizedstring.md)           | 抓取 **IAnalysisAlternate** 物件的已識別字串值。<br/>                                                                               |
| [**GetStrokeIds**](ianalysisalternate-getstrokeids.md)                         | 抓取與這個 **IAnalysisAlternate** 相關聯的筆觸識別碼。<br/>                                                                    |



 

## <a name="remarks"></a>備註

使用者的手寫形式有許多變化。 基於這個理由，手寫辨識器有時可以將手寫轉換成文字，與使用者所預期的不同。 當 [**IInkAnalyzer**](iinkanalyzer.md) 對筆劃集合執行分析時， **IInkAnalyzer** 會尋找手寫表示的最可能字組。 此外， **IInkAnalyzer** 也會尋找替代辨識相符專案的集合，這些專案會儲存在 [**IAnalysisAlternates**](ianalysisalternates.md) 集合中。 為了讓使用者能夠利用辨識替代，您必須建立使用者介面，讓使用者可以選取正確的 **IAnalysisAlternate**。

**IAnalysisAlternate** 物件通常是透過 [**IInkAnalyzer：： GetAlternates 方法**](iinkanalyzer-getalternates.md)來取得。 集合中的第一個 **IAnalysisAlternate** 物件是 [**IInkAnalyzer**](iinkanalyzer.md) 視為最可能替代的物件。

這個介面相當於 .NET Framework 中的 [AnalysisCore. AnalysisAlternateBase](/previous-versions/ms610092(v=vs.100)) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAnalysisAlternates**](ianalysisalternates.md)
</dt> <dt>

[**IInkAnalyzer：： GetAlternatesForCoNtextNodes 方法**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**IInkAnalyzer：： GetAlternatesForStrokes 方法**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[**IInkAnalyzer：： GetAlternates 方法**](iinkanalyzer-getalternates.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

