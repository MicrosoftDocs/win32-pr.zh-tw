---
description: 指定 IInkAnalyzer 執行筆墨分析的方式。
ms.assetid: bc526445-0c9c-4c53-8b02-32cf758266e6
title: 'AnalysisModes 列舉 (IACom) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AnalysisModes
api_type:
- HeaderDef
api_location:
- IACom.h
ms.openlocfilehash: b9fdebd3ef3cd505b49ff6c82f7609bc339af0a4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386014"
---
# <a name="analysismodes-enumeration"></a>AnalysisModes 列舉

指定 [**IInkAnalyzer**](iinkanalyzer.md) 執行筆墨分析的方式。

## <a name="syntax"></a>Syntax


```C++
typedef enum AnalysisModes { 
  AnalysisModes_None                     = 0x0000,
  AnalysisModes_AutomaticReconciliation  = 0x0002,
  AnalysisModes_StrokeCacheAutoCleanup   = 0x0004,
  AnalysisModes_PersonalizationEnabled   = 0x0008,
  AnalysisModes_Default                  = 0x000d
} AnalysisModes;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="AnalysisModes_None"></span><span id="analysismodes_none"></span><span id="ANALYSISMODES_NONE"></span>**AnalysisModes \_ 無**
</dt> <dd>

未指定任何模式。

</dd> <dt>

<span id="AnalysisModes_AutomaticReconciliation"></span><span id="analysismodes_automaticreconciliation"></span><span id="ANALYSISMODES_AUTOMATICRECONCILIATION"></span>**AnalysisModes \_ AutomaticReconciliation**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md)是否會在中繼或最終結果就緒時，立即自動啟動對帳作業。

如果啟用此模式，則不會引發 [**\_ IAnalysisEvents：： ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)事件。 如果停用此模式，則會引發 **\_ IAnalysisEvents：： ReadyToReconcile** 事件。

</dd> <dt>

<span id="AnalysisModes_StrokeCacheAutoCleanup"></span><span id="analysismodes_strokecacheautocleanup"></span><span id="ANALYSISMODES_STROKECACHEAUTOCLEANUP"></span>**AnalysisModes \_ StrokeCacheAutoCleanup**
</dt> <dd>

[**IInkAnalyzer**](iinkanalyzer.md)是否會在執行分析之前，自動從筆劃快取清除不需要的筆觸。

如果啟用此模式， [**IInkAnalyzer**](iinkanalyzer.md) 會在執行分析之前清除筆觸資料。 您的程式碼也必須處理 [**\_ IAnalysisEvents：： UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)事件。 如果未處理 **\_ IAnalysisEvents：： UpdateStrokesCache** 事件，則會引發例外狀況。 這項檢查是在 [分析 (] 或 [BackgroundAnalyze]) 和 [對帳] 階段完成。

如果停用此模式，則 [**IInkAnalyzer**](iinkanalyzer.md) 不會清除筆觸資料。 若要清除筆觸資料，請呼叫 [**IInkAnalyzer：： ClearStrokeData 方法**](iinkanalyzer-clearstrokedata.md)。 如果此模式已停用，則會引發 [**\_ IAnalysisEvents：： UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)事件，讓 **IInkAnalyzer** 可以針對已清除快取的任何筆劃取得最新的筆劃資料。 如果已清除筆觸快取，但未處理 **\_ IAnalysisEvents：： UpdateStrokesCache** 事件，則會引發例外狀況。

</dd> <dt>

<span id="AnalysisModes_PersonalizationEnabled"></span><span id="analysismodes_personalizationenabled"></span><span id="ANALYSISMODES_PERSONALIZATIONENABLED"></span>**AnalysisModes \_ PersonalizationEnabled**
</dt> <dd>

已啟用手寫辨識的個人化。

</dd> <dt>

<span id="AnalysisModes_Default"></span><span id="analysismodes_default"></span><span id="ANALYSISMODES_DEFAULT"></span>**AnalysisModes \_ 預設值**
</dt> <dd>

所有模式都會啟用。

</dd> </dl>

## <a name="remarks"></a>備註

此列舉允許其成員值的位元組合。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInkAnalyzer：： GetAnalysisModes 方法**](iinkanalyzer-getanalysismodes.md)
</dt> <dt>

[**IInkAnalyzer：： SetAnalysisModes 方法**](iinkanalyzer-setanalysismodes.md)
</dt> <dt>

[**\_IAnalysisEvents::IntermediateResults**](-ianalysisevents-intermediateresults.md)
</dt> <dt>

[**\_IAnalysisEvents::ReadyToReconcile**](-ianalysisevents-readytoreconcile.md)
</dt> <dt>

[**\_IAnalysisEvents::UpdateStrokesCache**](-ianalysisevents-updatestrokescache.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




