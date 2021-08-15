---
description: 儲存 IInkAnalyzer 的所有分析結果。
ms.assetid: 538eb781-d831-475b-ba09-271d71f6a6bf
title: 'IInkAnalyzer：： SaveResults 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResults
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 216f238776cf88a24d10f57671aa4f03c71d07962ff480d5b219653a5c9d338e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091988"
---
# <a name="iinkanalyzersaveresults-method"></a>IInkAnalyzer：： SaveResults 方法

儲存 [**IInkAnalyzer**](iinkanalyzer.md)的所有分析結果。

## <a name="syntax"></a>語法


```C++
HRESULT SaveResults(
  [out] ULONG *pulSerializedDataSize,
  [out] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pulSerializedDataSize* \[擴展\]
</dt> <dd>

*PpbSerializedData* 中的位元組數目。

</dd> <dt>

*ppbSerializedData* \[擴展\]
</dt> <dd>

包含已儲存分析結果的陣列。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請使用 CoTaskMemFree 釋放 *ppbSerializedData* 的記憶體。

 

這個方法會儲存所有目前的分析結果，其中包括目前的分析提示和自訂辨識器節點 (請參閱 [**ICoNtextNode：： GetType**](icontextnode-gettype.md)) 。 這個方法不會儲存任何筆觸資料。 您的應用程式必須負責同步處理任何分析結果和對應的筆劃（如果它保存資料）。

當要儲存的 [**ICoNtextNode**](icontextnode.md) 物件已部分填入時，這個方法會傳回錯誤碼 (請參閱 [**ICoNtextNode：： GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)) 。

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

[**IInkAnalyzer：： LoadResults 方法**](iinkanalyzer-loadresults.md)
</dt> <dt>

[**IInkAnalyzer：： SaveResultsForNodes 方法**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**IInkAnalyzer：： SaveResultsForStrokes 方法**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

