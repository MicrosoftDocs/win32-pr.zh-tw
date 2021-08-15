---
description: 抓取值，指出 IAnalysisRegion 是否代表空白區域。
ms.assetid: 3a536b01-e7ee-4103-88c4-d83377ea9fdb
title: 'IAnalysisRegion：： IsEmpty 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IsEmpty
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: a599d88371a1a6726ed2ec4ee217c36b3ea3cd71d6117305a59860cb9a8bf09f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092319"
---
# <a name="ianalysisregionisempty-method"></a>IAnalysisRegion：： IsEmpty 方法

抓取值，指出 [**IAnalysisRegion**](ianalysisregion.md) 是否代表空白區域。

## <a name="syntax"></a>語法


```C++
HRESULT IsEmpty(
  [out] VARIANT_BOOL *pfIsEmpty
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pfIsEmpty* \[擴展\]
</dt> <dd>

**變異 \_** 如果表示的區域是空的，則為 TRUE;否則， **VARIANT \_ FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows僅限 XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> <dt>

[**IAnalysisRegion：： IsInfinite 方法**](ianalysisregion-isinfinite.md)
</dt> <dt>

[**IAnalysisRegion：： MakeEmpty 方法**](ianalysisregion-makeempty.md)
</dt> <dt>

[**IAnalysisRegion：： MakeInfinite 方法**](ianalysisregion-makeinfinite.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




