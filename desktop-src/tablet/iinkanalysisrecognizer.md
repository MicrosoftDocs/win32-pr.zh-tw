---
description: 提供手寫辨識器的存取權，以搭配筆墨分析使用。
ms.assetid: de536cca-889e-413e-a6f7-c2229a77c801
title: 'IInkAnalysisRecognizer 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalysisRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d0736288658c57c1cfd346b8337f91353638b8326ed1d0b29687c812db72efba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119350878"
---
# <a name="iinkanalysisrecognizer-interface"></a>IInkAnalysisRecognizer 介面

提供手寫辨識器的存取權，以搭配筆墨分析使用。

## <a name="members"></a>成員

**IInkAnalysisRecognizer** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IInkAnalysisRecognizer** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IInkAnalysisRecognizer** 介面具有這些方法。



| 方法                                                                          | 描述                                                                                                                    |
|:--------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------|
| [**GetCapabilities**](iinkanalysisrecognizer-getcapabilities.md)               | 抓取辨識器的功能。<br/>                                                                       |
| [**GetGuid**](iinkanalysisrecognizer-getguid.md)                               | 抓取辨識器 (GUID) 的全域唯一識別碼。<br/>                                                  |
| [**GetLanguages**](iinkanalysisrecognizer-getlanguages.md)                     | 抓取此 **IInkAnalysisRecognizer** 支援之地區設定的識別碼。<br/>                            |
| [**GetName**](iinkanalysisrecognizer-getname.md)                               | 抓取辨識器的名稱。<br/>                                                                               |
| [**GetSupportedProperties**](iinkanalysisrecognizer-getsupportedproperties.md) | 針對此 **IInkAnalysisRecognizer** 所支援的屬性，抓取 (guid) 的全域唯一識別碼。<br/> |
| [**GetVendor**](iinkanalysisrecognizer-getvendor.md)                           | 抓取 **IInkAnalysisRecognizer** 的廠商名稱。<br/>                                                        |



 

## <a name="remarks"></a>備註

辨識器具有特定的屬性和屬性，可讓它執行辨識。 辨識器的屬性必須先經過判斷，才能進行辨識。 辨識器支援的屬性類型，會決定它可以執行的辨識類型。 比方說，如果辨識器不支援草書手寫，當使用者以草書寫入時，就會傳回不正確的結果。

辨識器也有內建的功能，可自動管理手寫的許多層面。 例如，它會判斷繪製筆劃之線條的度量。 您可以傳回筆劃的行號，但由於辨識器的內建功能，您永遠不需要指定這些線條度量的判斷方式。

[**IInkAnalyzer**](iinkanalyzer.md)會維護可用辨識器的清單。 若要存取此清單，請使用 [**IInkAnalyzer：： GetInkAnalysisRecognizersByPriority 方法**](iinkanalyzer-getinkanalysisrecognizersbypriority.md) 方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInkAnalysisRecognizers**](iinkanalysisrecognizers.md)
</dt> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer：： CreateCustomRecognizer 方法**](iinkanalyzer-createcustomrecognizer.md)
</dt> <dt>

[內容節點類型](context-node-types.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

