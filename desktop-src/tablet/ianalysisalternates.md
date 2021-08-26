---
description: 包含物件的集合，這些物件會執行 IAnalysisAlternate 介面，且為筆跡分析的結果。
ms.assetid: 53802a62-4425-40fd-bf48-0da55ea8ffbe
title: 'IAnalysisAlternates 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternates
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e2643ef8ea90d029aee6bd0673931d27e9987b0af0a898e854cb87d74a89c0af
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058088"
---
# <a name="ianalysisalternates-interface"></a>IAnalysisAlternates 介面

包含物件的集合，這些物件會執行 [**IAnalysisAlternate**](ianalysisalternate.md) 介面，且為筆跡分析的結果。

## <a name="members"></a>成員

**IAnalysisAlternates** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IAnalysisAlternates** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IAnalysisAlternates** 介面具有這些方法。



| 方法                                                                   | 描述                                                                                                                                      |
|:-------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetAnalysisAlternate**](ianalysisalternates-getanalysisalternate.md) | 抓取集合中位於指定索引位置的 [**IAnalysisAlternate**](ianalysisalternate.md) 物件。<br/>                   |
| [**GetCount**](ianalysisalternates-getcount.md)                         | 捕獲 **IAnalysisAlternates** 集合中包含的 [**IAnalysisAlternate**](ianalysisalternate.md)物件數目。<br/> |



 

## <a name="remarks"></a>備註

這個介面相當於 [**System. Windows。.NET Framework 中的 AnalysisCore. AnalysisAlternateBaseCollection**](/previous-versions/ms610094(v=vs.100))類別。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**IInkAnalyzer：： GetAlternates 方法**](iinkanalyzer-getalternates.md)
</dt> <dt>

[**IInkAnalyzer：： GetAlternatesForCoNtextNodes 方法**](iinkanalyzer-getalternatesforcontextnodes.md)
</dt> <dt>

[**IInkAnalyzer：： GetAlternatesForStrokes 方法**](iinkanalyzer-getalternatesforstrokes.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

