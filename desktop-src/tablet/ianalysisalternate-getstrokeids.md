---
description: 傳回與這個 IAnalysisAlternate 相關聯的筆觸識別碼。
ms.assetid: 495d485f-0d16-4085-9213-cc55f3f259f0
title: 'IAnalysisAlternate：： GetStrokeIds 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisAlternate.GetStrokeIds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 80882a83e9a0fa9bf973990a689e2abf1a52a870
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848097"
---
# <a name="ianalysisalternategetstrokeids-method"></a>IAnalysisAlternate：： GetStrokeIds 方法

傳回與這個 [**IAnalysisAlternate**](ianalysisalternate.md)相關聯的筆觸識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT GetStrokeIds(
  [in, out] ULONG *pulStrokeIdsCount,
  [out]     LONG  **pplStrokeIds
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pulStrokeIdsCount* \[in、out\]
</dt> <dd>

**ULONG** 的指標，設定為與這個 [**IAnalysisAlternate**](ianalysisalternate.md)相關聯的筆觸識別碼數目。

</dd> <dt>

*pplStrokeIds* \[擴展\]
</dt> <dd>

\[out，size \_ 是 (\* *PULSTROKEIDSCOUNT* \* sizeof (LONG) ) \]

長度 **為** *pulStrokeIdsCount* 的陣列，這個陣列會設定為與此 [**IAnalysisAlternate**](ianalysisalternate.md)相關聯的筆觸識別碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

> [!Caution]  
> 若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請使用 CoTaskMemFree 釋放 *pplStrokeIds* 的記憶體。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAnalysisAlternate**](ianalysisalternate.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

