---
description: 將目前的上方替代變更為指定的 IAnalysisAlternate。
ms.assetid: 0867a662-d172-4ca2-a41f-49c0ea454768
title: 'IInkAnalyzer：： ModifyTopAlternateWithConfirmation 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.ModifyTopAlternateWithConfirmation
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 60b0221e7d27cfd5d601dcf77e80a297045d39a7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318452"
---
# <a name="iinkanalyzermodifytopalternatewithconfirmation-method"></a>IInkAnalyzer：： ModifyTopAlternateWithConfirmation 方法

將目前的上方替代變更為指定的 [**IAnalysisAlternate**](ianalysisalternate.md)。

## <a name="syntax"></a>語法


```C++
HRESULT ModifyTopAlternateWithConfirmation(
  [in] IAnalysisAlternate *alternate,
  [in] VARIANT_BOOL       fconfirmAutomatically
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*替代* \[在\]
</dt> <dd>

要設定為新的 top 替代的分析替代。

</dd> <dt>

*fconfirmAutomatically* \[在\]
</dt> <dd>

**變異 \_TRUE** 表示將對應至分析替代的所有筆墨分葉內容節點設定為 **ConfirmationType \_ NodeTypeAndProperties** 的確認類型 (請參閱 [**ICoNtextNode：： IsConfirmed**](icontextnode-isconfirmed.md) 和 [**ConfirmationType**](confirmationtype.md)) ; **變異 \_FALSE** 表示將對應至分析替代的所有筆墨分葉內容節點設定為 **ConfirmationType \_ None** 的確認類型。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

若要取得分析替代項，請使用 [**IInkAnalyzer：： GetAlternates 方法**](iinkanalyzer-getalternates.md)、 [**IInkAnalyzer：： GetAlternatesForCoNtextNodes 方法**](iinkanalyzer-getalternatesforcontextnodes.md)或 [**IInkAnalyzer：： GetAlternatesForStrokes 方法**](iinkanalyzer-getalternatesforstrokes.md)。 若要取得與分析替代相關聯的內容節點物件，請使用 [**IAnalysisAlternate：： GetAlternateNodes 方法**](ianalysisalternate-getalternatenodes.md)。

若要變更內容節點的確認類型，請使用 [**ICoNtextNode：： Confirm**](icontextnode-confirm.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
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

[**筆墨分析 ConfirmationType**](confirmationtype.md)
</dt> <dt>

[參考](ink-analysis-reference.md)
</dt> </dl>

 

 




