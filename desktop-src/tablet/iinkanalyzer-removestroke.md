---
description: 從 IInkAnalyzer 中移除指定的筆觸。
ms.assetid: e182ae35-854e-401d-8e26-aee645c05430
title: 'IInkAnalyzer：： RemoveStroke 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.RemoveStroke
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: dd0a972ed776c40fc42d695df2058c62f9af84f8fc09155758d197772e9abfc7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092008"
---
# <a name="iinkanalyzerremovestroke-method"></a>IInkAnalyzer：： RemoveStroke 方法

從 [**IInkAnalyzer**](iinkanalyzer.md)中移除指定的筆觸。

## <a name="syntax"></a>語法


```C++
HRESULT RemoveStroke(
  [in] LONG *plStrokeId
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*plStrokeId* \[在\]
</dt> <dd>

筆觸識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

這個方法會從 [**IInkAnalyzer**](iinkanalyzer.md)中移除指定之筆劃的封包資料和參考。

這個方法會從參考筆劃的分葉內容節點移除筆劃。 如果 [**ICoNtextNode**](icontextnode.md) 不再參考任何筆劃，這個方法會刪除 **ICoNtextNode** ，以及不再有任何子節點的任何上階 **ICoNtextNode** 物件。

在這個方法從 [**ICoNtextNode**](icontextnode.md)中移除筆觸之後，它會更新 [**IInkAnalyzer**](iinkanalyzer.md) 物件的中途區域 (請參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md) ，) 包含已移除筆劃的周框方塊。

如果 *plStrokeId* 未識別與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯的筆劃，這個方法會傳回而不更新筆墨分析器。

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

[**IInkAnalyzer：： AddStroke 方法**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**IInkAnalyzer：： AddStrokeForLanguage 方法**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer：： AddStrokes 方法**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer：： AddStrokesForLanguage 方法**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer：： RemoveStrokes 方法**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




