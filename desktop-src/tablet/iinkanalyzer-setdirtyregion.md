---
description: 修改自上次分析作業之後變更的區域。
ms.assetid: 1484fd96-2791-4583-b13b-e5a8275ecb0e
title: 'IInkAnalyzer：： SetDirtyRegion 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetDirtyRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a39fc420b368911788efcb9462c9c4be5b4828c82906ef2c94bb5be99ca17568
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091468"
---
# <a name="iinkanalyzersetdirtyregion-method"></a>IInkAnalyzer：： SetDirtyRegion 方法

修改自上次分析作業之後變更的區域。

## <a name="syntax"></a>語法


```C++
HRESULT SetDirtyRegion(
  [in] IAnalysisRegion *pDirtyRegion
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pDirtyRegion* \[在\]
</dt> <dd>

描述自上次分析作業之後變更之區域的 [**IAnalysisRegion**](ianalysisregion.md) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

這個方法會識別需要分析或重新分析的區域。 新增、更新或移除筆劃資料的所有 [**IInkAnalyzer**](iinkanalyzer.md) 方法會更新已變更的區域。 若要手動標記 reanalysis 的區域：

1.  使用 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)取得中途區域。
2.  使用 [**IAnalysisRegion：： UnionRegion 方法**](ianalysisregion-unionregion.md) 或 [**IAnalysisRegion：： UnionRectangle 方法**](ianalysisregion-unionrectangle.md) ，將區域新增至步驟1中的區域。
3.  使用 **IInkAnalyzer：： SetDirtyRegion 方法** 來更新中途區域。

[**IInkAnalyzer**](iinkanalyzer.md)會在呼叫 [**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md)或 [**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)期間，分析其中途區域內的筆墨。 不過， **IInkAnalyzer** 可能會擴充分析作業，以包含鄰近區域。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[**IInkAnalyzer：：分析方法**](iinkanalyzer-analyze.md)
</dt> <dt>

[**IInkAnalyzer：： BackgroundAnalyze 方法**](iinkanalyzer-backgroundanalyze.md)
</dt> <dt>

[**IInkAnalyzer：： AddStroke 方法**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**IInkAnalyzer：： AddStrokeForLanguage 方法**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer：： AddStrokes 方法**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer：： AddStrokesForLanguage 方法**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer：： RemoveStroke 方法**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**IInkAnalyzer：： RemoveStrokes 方法**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**IInkAnalyzer：： UpdateStrokesData 方法**](iinkanalyzer-updatestrokesdata.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




