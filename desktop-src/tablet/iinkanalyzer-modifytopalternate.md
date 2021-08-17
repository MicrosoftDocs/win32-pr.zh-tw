---
description: 將目前的上方替代變更為指定的替代，並清除所有與替代物件相關聯之 ICoNtextNode 物件的確認類型。
ms.assetid: a4ff7e82-623f-4501-9641-5235c3083757
title: 'IInkAnalyzer：： ModifyTopAlternate 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternate
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: b35cda4534bc5c791e4815c584f6da5d9972c018283b6c9385f6bad998187505
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092038"
---
# <a name="iinkanalyzermodifytopalternate-method"></a>IInkAnalyzer：： ModifyTopAlternate 方法

將目前的上方替代變更為指定的替代，並清除所有與替代物件相關聯之 [**ICoNtextNode**](icontextnode.md) 物件的確認類型。

## <a name="syntax"></a>語法


```C++
HRESULT ModifyTopAlternate(
  [in] IAnalysisAlternate *pAlternate
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pAlternate* \[在\]
</dt> <dd>

[**IAnalysisAlternate**](ianalysisalternate.md)物件，其中包含新的 top 替代。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

若要取得分析替代項，請使用 [**IInkAnalyzer：： GetAlternates 方法**](iinkanalyzer-getalternates.md)、 [**IInkAnalyzer：： GetAlternatesForCoNtextNodes 方法**](iinkanalyzer-getalternatesforcontextnodes.md)或 [**IInkAnalyzer：： GetAlternatesForStrokes 方法**](iinkanalyzer-getalternatesforstrokes.md)。 若要取得與分析替代相關聯的 [**ICoNtextNode**](icontextnode.md) 物件，請使用 [**IAnalysisAlternate：： GetAlternateNodes 方法**](ianalysisalternate-getalternatenodes.md)。

若要變更內容節點的確認類型，請使用 [**ICoNtextNode：： Confirm**](icontextnode-confirm.md)。

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

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[**ConfirmationType**](confirmationtype.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




