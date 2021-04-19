---
description: 變更指定之筆劃的型別。
ms.assetid: 8d954a7d-c987-41cf-9933-b2e6bacc9489
title: 'IInkAnalyzer：： SetStrokesType 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SetStrokesType
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: de3f4e56b24226c2f74c6572561082c1d00afc8a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106970620"
---
# <a name="iinkanalyzersetstrokestype-method"></a>IInkAnalyzer：： SetStrokesType 方法

變更指定之筆劃的型別。

## <a name="syntax"></a>語法


```C++
HRESULT SetStrokesType(
  [in] ULONG      strokeIdCount,
  [in] LONG       *plStrokes,
  [in] StrokeType StrokeType
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*strokeIdCount* \[在\]
</dt> <dd>

*PlStrokes* 中的筆觸識別碼數目。

</dd> <dt>

*plStrokes* \[在\]
</dt> <dd>

陣列，其中包含要指派給 *StrokeType* 之筆劃的筆觸識別碼。

</dd> <dt>

*StrokeType* \[在\]
</dt> <dd>

要指派給筆劃的 [**StrokeType**](stroketype.md) 值。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

如果筆劃的類型是 [**StrokeType**](stroketype.md) 值 StrokeType 非 **\_ 分類**，則 [**IInkAnalyzer**](iinkanalyzer.md) 會在筆跡分析期間將筆劃分類。 否則， **IInkAnalyzer** 會使用筆劃上設定的類型。

[**IInkAnalyzer**](iinkanalyzer.md)不會將筆劃類型值設定為筆跡分析的一部分。 若要指定或變更筆觸類型，請使用 [**IInkAnalyzer：： SetStrokeType 方法**](iinkanalyzer-setstroketype.md) 或 **IInkAnalyzer：： SetStrokesType 方法**。

如果筆劃與非未分類筆墨節點的 [**ICoNtextNode**](icontextnode.md) 相關聯 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) ，這個方法會將筆劃移至包含相同語言之筆觸的非分類筆墨節點。 如果沒有這類內容節點，這個方法會建立新的非分類筆墨節點，並將筆劃加入其中。 未分類的筆墨節點是 UnclassifiedInk 類型的 **ICoNtextNode** 。

如果這個方法從非未分類筆墨節點的 [**ICoNtextNode**](icontextnode.md) 移動筆劃，此方法也會將筆劃的周框方塊新增至 ink 分析器的中途區域 (請參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)) 。

如果 *StrokeType* 參數符合筆觸的目前型別，則這個方法不會移動筆劃。

如果在 *strokeIds* 中識別的筆劃沒有與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯，這個方法會忽略識別碼。

如果任何指定的筆觸都沒有識別與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯的筆劃，這個方法會傳回而不更新 **IInkAnalyzer**。

在與已 NodeTypeAndProperties 確認的 CoNtextNode 相關聯的筆劃上設定筆劃類型，將會引發 InvalidOperationException。

當 *plStrokes* 為 **Null** 時，這個方法會傳回錯誤碼。

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

[**IInkAnalyzer：： SetStrokeType 方法**](iinkanalyzer-setstroketype.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




