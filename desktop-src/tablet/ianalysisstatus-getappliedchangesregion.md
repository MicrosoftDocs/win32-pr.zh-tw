---
description: 抓取檔的區域，該區域對應于 IInkAnalyzer 物件的內容節點樹狀結構中，做為筆跡分析結果的變更。
ms.assetid: 25d511fb-ba2d-4c46-8a8c-8bb4187c9a5c
title: 'IAnalysisStatus：： GetAppliedChangesRegion 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisStatus.GetAppliedChangesRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: d3b2fec2528cbf961956e8b41f9eb6c985bd745d5dad097eb05544e64c42d122
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118044991"
---
# <a name="ianalysisstatusgetappliedchangesregion-method"></a>IAnalysisStatus：： GetAppliedChangesRegion 方法

抓取檔的區域，該區域對應于 [**IInkAnalyzer**](iinkanalyzer.md) 物件的內容節點樹狀結構中，做為筆跡分析結果的變更。

## <a name="syntax"></a>語法


```C++
HRESULT GetAppliedChangesRegion(
  [out] IAnalysisRegion **pAppliedChangesRegion
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAppliedChangesRegion* \[擴展\]
</dt> <dd>

已進行變更之檔的 [**IAnalysisRegion**](ianalysisregion.md) 指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失，請在 pAppliedChangesRegion 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （ \* 當您不再需要流量分析區域時）。

 

當應用程式收到用於偵測的資訊，而且需要使變更可能發生，以便繪製偵錯工具資訊時，最常使用這個方法。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAnalysisStatus**](ianalysisstatus.md)
</dt> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

