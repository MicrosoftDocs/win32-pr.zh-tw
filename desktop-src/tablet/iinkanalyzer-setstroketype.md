---
description: 變更指定之筆劃的型別。
ms.assetid: 1608fed1-cd6c-46c3-a35f-3d262279ec2e
title: 'IInkAnalyzer：： SetStrokeType 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokeType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 8a5f77cbefb200bad973c0f2cf28fea5d3efe1da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113320"
---
# <a name="iinkanalyzersetstroketype-method"></a>IInkAnalyzer：： SetStrokeType 方法

變更指定之筆劃的型別。

## <a name="syntax"></a>語法


```C++
HRESULT SetStrokeType(
  [in] LONG       lStrokeId,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*lStrokeId* \[在\]
</dt> <dd>

要指派 *StrokeType* 之筆劃的筆觸識別碼。

</dd> <dt>

*StrokeType* \[在\]
</dt> <dd>

要指派給筆劃的 [**StrokeType**](stroketype.md) 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

如果筆劃的類型是 [**StrokeType**](stroketype.md) 值 StrokeType 非 **\_ 分類**，則 [**IInkAnalyzer**](iinkanalyzer.md) 會在筆跡分析期間將筆劃分類。 否則， **IInkAnalyzer** 會使用筆劃上設定的類型。

[**IInkAnalyzer**](iinkanalyzer.md)不會將筆劃類型值設定為筆跡分析的一部分。 若要指定或變更筆觸類型，請使用 **IInkAnalyzer：： SetStrokeType 方法** 或 [**IInkAnalyzer：： SetStrokesType 方法**](iinkanalyzer-setstrokestype.md)。

如果筆劃與非未分類筆墨節點的 [**ICoNtextNode**](icontextnode.md) 相關聯 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) ，這個方法會將筆劃移至包含相同語言之筆觸的非分類筆墨節點。 如果沒有這類內容節點，這個方法會建立新的非分類筆墨節點，並將筆劃加入其中。 未分類的筆墨節點是 UnclassifiedInk 類型的 **ICoNtextNode** 。

如果這個方法從非未分類筆墨節點的 [**ICoNtextNode**](icontextnode.md) 移動筆劃，此方法也會將筆劃的周框方塊新增至 ink 分析器的中途區域 (請參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)) 。

如果 *StrokeType* 參數符合筆觸的目前型別，則這個方法不會移動筆劃。

在與已 NodeTypeAndProperties 確認的 CoNtextNode 相關聯的筆劃上設定筆劃類型，將會引發 InvalidOperationException。

如果指定的筆劃沒有與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯，這個方法會傳回而不更新 **IInkAnalyzer**。

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

[**IInkAnalyzer：： GetStrokeType 方法**](iinkanalyzer-getstroketype.md)
</dt> <dt>

[**IInkAnalyzer：： SetStrokesType 方法**](iinkanalyzer-setstrokestype.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




