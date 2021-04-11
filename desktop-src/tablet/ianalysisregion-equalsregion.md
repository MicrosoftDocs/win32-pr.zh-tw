---
description: 判斷指定的 IAnalysisRegion 是否包含與目前 IAnalysisRegion 物件相同的值。
ms.assetid: 44c09cfe-65fc-4175-ad05-01c605218c58
title: 'IAnalysisRegion：： EqualsRegion 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.EqualsRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 6a647c13f1279cd39e4947b9fdbcc9ed4e1ef4ac
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113408"
---
# <a name="ianalysisregionequalsregion-method"></a>IAnalysisRegion：： EqualsRegion 方法

判斷指定的 [**IAnalysisRegion**](ianalysisregion.md) 是否包含與目前 **IAnalysisRegion** 物件相同的值。

## <a name="syntax"></a>語法


```C++
HRESULT EqualsRegion(
  [in]  IAnalysisRegion *pOtherRegion,
  [out] VARIANT_BOOL    *pfRegionsEqual
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pOtherRegion* \[在\]
</dt> <dd>

要與目前 **IAnalysisRegion** 比較的 [**IAnalysisRegion**](ianalysisregion.md)物件。

</dd> <dt>

*pfRegionsEqual* \[擴展\]
</dt> <dd>

**變異 \_** 如果指定的 [**IAnalysisRegion**](ianalysisregion.md)包含與目前 IAnalysisRegion 相同的值，則為 TRUE;否則， **VARIANT \_ FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IAnalysisRegion**](ianalysisregion.md)
</dt> </dl>

 

 




