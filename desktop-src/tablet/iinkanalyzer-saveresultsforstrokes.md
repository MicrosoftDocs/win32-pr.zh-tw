---
description: 儲存與 IInkAnalyzer 相關聯之指定筆劃的分析結果。
ms.assetid: 6ff29b95-6c76-4e3d-b4c0-5e7cb6a9ddf9
title: 'IInkAnalyzer：： SaveResultsForStrokes 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IInkAnalyzer.SaveResultsForStrokes
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: fd9a95ada1385fdbb6dbc5a1e22cde0ef319156ad7c3cd7782e911d06696af37
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119091558"
---
# <a name="iinkanalyzersaveresultsforstrokes-method"></a>IInkAnalyzer：： SaveResultsForStrokes 方法

儲存與 [**IInkAnalyzer**](iinkanalyzer.md)相關聯之指定筆劃的分析結果。

## <a name="syntax"></a>語法


```C++
HRESULT SaveResultsForStrokes(
  [in]          ULONG ulStrokeIdsCount,
  [in]          LONG  *plStrokeIds,
  [in, out]     ULONG *pulSerializedDataSize,
  [out, retval] BYTE  **ppbSerializedData
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ulStrokeIdsCount* \[在\]
</dt> <dd>

**PlStrokeIds** 中的筆觸識別碼數目。

</dd> <dt>

*plStrokeIds* \[在\]
</dt> <dd>

筆觸識別碼的陣列。

</dd> <dt>

*pulSerializedDataSize* \[in、out\]
</dt> <dd>

*PpbSerializedData* 中的位元組數目。

</dd> <dt>

*ppbSerializedData* \[退出，retval\]
</dt> <dd>

序列化分析資料的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請在 *ppbSerializedData* 上呼叫 CoTaskMemFree。

 

這個方法會儲存指定之筆劃的目前分析結果。 這個方法會儲存包含筆劃的筆墨分葉 [**ICoNtextNode**](icontextnode.md) 物件，以及這些內容節點的所有上階。 這個方法不會儲存任何筆觸資料或分析提示節點。 您的應用程式必須負責同步處理任何分析結果和對應的筆劃資料（如果保存的話）。

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

[**IInkAnalyzer：： SaveResults 方法**](iinkanalyzer-saveresults.md)
</dt> <dt>

[**IInkAnalyzer：： SaveResultsForNodes 方法**](iinkanalyzer-saveresultsfornodes.md)
</dt> <dt>

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

