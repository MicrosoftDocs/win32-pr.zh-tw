---
description: 為 IInkAnalyzer 建立新的自訂辨識器節點。
ms.assetid: bc1dbe88-8f81-48b6-9dd3-8f00e2b6c01c
title: 'IInkAnalyzer：： CreateCustomRecognizer 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.CreateCustomRecognizer
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 70cc5741faa8d54d09af000d4dbbb3c0fc423df2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191409"
---
# <a name="iinkanalyzercreatecustomrecognizer-method"></a>IInkAnalyzer：： CreateCustomRecognizer 方法

為 [**IInkAnalyzer**](iinkanalyzer.md)建立新的自訂辨識器節點。

## <a name="syntax"></a>語法


```C++
HRESULT CreateCustomRecognizer(
  [in]  const GUID         *pInkAnalysisRecognizerId,
  [out]       IContextNode **ppContextNode
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pInkAnalysisRecognizerId* \[在\]
</dt> <dd>

要建立節點之 [**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md) 的全域唯一識別碼 (GUID) 。

</dd> <dt>

*ppCoNtextNode* \[擴展\]
</dt> <dd>

[**ICoNtextNode**](icontextnode.md)物件的指標，代表新的自訂辨識器節點。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失，請在 ppCoNtextNode 上呼叫 [**IUnknown：： Release**](/windows/desktop/api/unknwn/nf-unknwn-iunknown-release) （當您不再需要使用物件時）。

 

這個方法會建立具有 CustomRecognizer 類型的新 [**ICoNtextNode**](icontextnode.md) (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) 。 然後，它會將新的自訂辨識器節點新增至 [**IInkAnalyzer**](iinkanalyzer.md) 物件根節點的子節點集合 (請參閱 [**ICoNtextNode：： GetSubNodes**](icontextnode-getsubnodes.md) 和 [**IInkAnalyzer：： GetRootNode 方法**](iinkanalyzer-getrootnode.md)) 。

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

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalysisRecognizer**](iinkanalysisrecognizer.md)
</dt> <dt>

[**IInkAnalyzer：： GetInkAnalysisRecognizersByPriority 方法**](iinkanalyzer-getinkanalysisrecognizersbypriority.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

