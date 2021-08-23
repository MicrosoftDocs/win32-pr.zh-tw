---
description: 儲存與 IInkAnalyzer 相關聯之特定內容節點集合的分析結果。
ms.assetid: 671bdb11-6e30-4254-b320-208face1f593
title: 'IInkAnalyzer：： SaveResultsForNodes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForNodes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4386f9b051bf1cfcda6ee55d7b83728b096dc6f69de4d87745ce564f19249565
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091567"
---
# <a name="iinkanalyzersaveresultsfornodes-method"></a>IInkAnalyzer：： SaveResultsForNodes 方法

儲存與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯之特定內容節點集合的分析結果。

## <a name="syntax"></a>語法


```C++
HRESULT SaveResultsForNodes(
  [in]      IContextNodes *pContextNodes,
  [in, out] ULONG         *pulSerializedDataSize,
  [out]     BYTE          **ppbSerializedData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pCoNtextNodes* \[在\]
</dt> <dd>

要儲存分析結果的 [**ICoNtextNode**](icontextnode.md) 集合。

</dd> <dt>

*pulSerializedDataSize* \[in、out\]
</dt> <dd>

*PpbSerializedData* 中的位元組數目。

</dd> <dt>

*ppbSerializedData* \[擴展\]
</dt> <dd>

序列化分析資料的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請在 *ppbSerializedData* 上呼叫 CoTaskMemFree。

 

這個方法會將 [**ICoNtextNode**](icontextnode.md) 物件的目前分析結果儲存在 *pCoNtextNodes* 中，以及其所有上階和子系內容節點。 這個方法不會儲存任何筆觸資料。 您的應用程式必須負責同步處理任何分析結果和對應的筆劃資料（如果保存的話）。

如果要儲存的 [**ICoNtextNode**](icontextnode.md) 物件只部分填入，這個方法會傳回錯誤碼 (請參閱 [**ICoNtextNode：： GetPartiallyPopulated**](icontextnode-getpartiallypopulated.md)) 。

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

[**IInkAnalyzer：： SaveResults 方法**](iinkanalyzer-saveresults.md)
</dt> <dt>

[**IInkAnalyzer：： SaveResultsForStrokes 方法**](iinkanalyzer-saveresultsforstrokes.md)
</dt> <dt>

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

