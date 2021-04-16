---
description: 傳回與這個警告相關聯之任何相關內容節點的識別碼。
ms.assetid: 8c418f48-3903-47c1-82e2-085de39574d4
title: 'IAnalysisWarning：： GetNodeIds 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisWarning.GetNodeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a38abd054e457ef9dbaf5dd93c38954b1ce6dcb3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511688"
---
# <a name="ianalysiswarninggetnodeids-method"></a>IAnalysisWarning：： GetNodeIds 方法

傳回與這個警告相關聯之任何相關內容節點的識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT GetNodeIds(
  [in, out] ULONG *pulCount,
  [out]     GUID  **ppNodeIds
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pulCount* \[in、out\]
</dt> <dd>

 (Guid) 在 *ppNodeIds* 中的全域唯一識別碼數目。

</dd> <dt>

*ppNodeIds* \[擴展\]
</dt> <dd>

Guid 陣列的指標，可識別與此分析警告相關聯的內容節點，如果沒有任何內容節點與警告相關聯，則為 **Null** 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

如果 *ppNodeIds* 傳遞為 **Null**，則 **GetNodeIds** 方法會傳回 **S \_ OK** ，而且在 *pulCount* 中會傳回矩形的數目。

> [!Caution]  
> 若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請使用 CoTaskMemFree 釋放 *ppNodeIds* 的記憶體。

 

## <a name="examples"></a>範例

下列範例顯示如何取得 [**IAnalysisWarning**](ianalysiswarning.md)中的 [**ICoNtextNode**](icontextnode.md)物件，以及 `warning` 如何只取得 **ICoNtextNode** 物件的數目


```C++
// Get the count of the context nodes and their identifiers.
ULONG count = 0;
GUID* nodeIds = 0;
warning->GetNodeIds(&count, &nodeIds);

// Use nodeIds

::CoTaskMemFree(nodeIds);

// GetNodeIds just gets the count and returns S_OK
ULONG number = 0;
warning->GetNodeIds(&number, NULL); 
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAnalysisWarning**](ianalysiswarning.md)
</dt> <dt>

[**ICoNtextNode**](icontextnode.md)
</dt> <dt>

[**IInkAnalyzer：： FindNode 方法**](iinkanalyzer-findnode.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

