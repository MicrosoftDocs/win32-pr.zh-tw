---
description: 將指定的筆觸與這個 ICoNtextNode 相關聯。
ms.assetid: 5ce8893a-da59-4cec-a349-d5ffc4f43905
title: 'ICoNtextNode：： SetStrokes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IContextNode.SetStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 67834a10e5e08070c991af76fe19b720853789a9f5e2c771f5c1ed0dc4fc9754
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119552598"
---
# <a name="icontextnodesetstrokes-method"></a>ICoNtextNode：： SetStrokes 方法

將指定的筆觸與這個 [**ICoNtextNode**](icontextnode.md)相關聯。

## <a name="syntax"></a>語法


```C++
HRESULT SetStrokes(
  [in] ULONG ulStrokeIdsCount,
  [in] LONG  *plStrokeIds
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ulStrokeIdsCount* \[在\]
</dt> <dd>

*PlStrokeIds* 中的筆觸識別碼數目。

</dd> <dt>

*plStrokeIds* \[在\]
</dt> <dd>

要與此 [**ICoNtextNode**](icontextnode.md)建立關聯之筆劃的識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

這個方法不會更新筆墨分析器的中途區域 (請參閱 [**IInkAnalyzer：： GetDirtyRegion 方法**](iinkanalyzer-getdirtyregion.md)) 。

當您的應用程式維護自己的資料結構（與 [**IInkAnalyzer**](iinkanalyzer.md)同步處理）時，請使用這個方法。 使用這個方法可將筆劃資料指派給特定的內容節點。 如需有關同步處理應用程式資料與 **IInkAnalyzer** 的詳細資訊，請參閱 [使用筆墨分析的資料 Proxy](data-proxy-with-ink-analysis.md)。

如果任何指定的筆劃已經與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯，這個方法會傳回 **E \_ INVALIDARG**。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer：： AddStroke 方法**](iinkanalyzer-addstroke.md)
</dt> <dt>

[**IInkAnalyzer：： AddStrokeForLanguage 方法**](iinkanalyzer-addstrokeforlanguage.md)
</dt> <dt>

[**IInkAnalyzer：： AddStrokes 方法**](iinkanalyzer-addstrokes.md)
</dt> <dt>

[**IInkAnalyzer：： AddStrokesForLanguage 方法**](iinkanalyzer-addstrokesforlanguage.md)
</dt> <dt>

[**IInkAnalyzer：： AddStrokesToCustomRecognizer 方法**](iinkanalyzer-addstrokestocustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer：： AddStrokeToCustomRecognizer 方法**](iinkanalyzer-addstroketocustomrecognizer.md)
</dt> <dt>

[**IInkAnalyzer：： RemoveStroke 方法**](iinkanalyzer-removestroke.md)
</dt> <dt>

[**IInkAnalyzer：： RemoveStrokes 方法**](iinkanalyzer-removestrokes.md)
</dt> <dt>

[**ICoNtextNode::GetStrokeId**](icontextnode-getstrokeid.md)
</dt> <dt>

[**ICoNtextNode::GetStrokeIds**](icontextnode-getstrokeids.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




