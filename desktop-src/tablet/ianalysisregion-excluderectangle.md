---
description: 將 IAnalysisRegion 的區域限制為其區域中未與指定的矩形相交的部分。
ms.assetid: a35b8bfc-a87a-4e9a-908f-2b13a128d222
title: 'IAnalysisRegion：： ExcludeRectangle 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 684ce2ceb57c7954c732fb2816aca50fcbae5297
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972430"
---
# <a name="ianalysisregionexcluderectangle-method"></a>IAnalysisRegion：： ExcludeRectangle 方法

將 [**IAnalysisRegion**](ianalysisregion.md) 的區域限制為其區域中未與指定的矩形相交的部分。

## <a name="syntax"></a>語法


```C++
HRESULT ExcludeRectangle(
  [in] RECT *pExcludingRectangle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pExcludingRectangle* \[在\]
</dt> <dd>

要從此 [**IAnalysisRegion**](ianalysisregion.md)中排除的矩形。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

矩形座標以 HIMETRIC 單位表示。

如果這兩個區域不相交， [**IAnalysisRegion**](ianalysisregion.md) 就不會變更。

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
</dt> <dt>

[**IAnalysisRegion：： ExcludeRegion 方法**](ianalysisregion-excluderegion.md)
</dt> <dt>

[**IAnalysisRegion：： IntersectRectangle 方法**](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[**IAnalysisRegion：： IntersectRegion 方法**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**IAnalysisRegion：： UnionRectangle 方法**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**IAnalysisRegion：： UnionRegion 方法**](ianalysisregion-unionregion.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




