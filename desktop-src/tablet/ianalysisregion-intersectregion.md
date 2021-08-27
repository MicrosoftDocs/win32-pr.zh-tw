---
description: 將 IAnalysisRegion 的區域限制為其與指定 IAnalysisRegion 的交集所建立的區域。
ms.assetid: 02b3049f-ada9-4de3-a7a2-f9ff8313fbab
title: 'IAnalysisRegion：： IntersectRegion 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 0db58dcc7fc1c1e7458cf804eb82af236de8f1997ddcc658391da19641d1cfdb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120058078"
---
# <a name="ianalysisregionintersectregion-method"></a>IAnalysisRegion：： IntersectRegion 方法

將 [**IAnalysisRegion**](ianalysisregion.md) 的區域限制為其與指定 **IAnalysisRegion** 的交集所建立的區域。

## <a name="syntax"></a>語法


```C++
HRESULT IntersectRegion(
  [in] IAnalysisRegion *pRegionToIntersect
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pRegionToIntersect* \[在\]
</dt> <dd>

要與之交集的 [**IAnalysisRegion**](ianalysisregion.md) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

如果兩個區域不相交，則新區域是空的。

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

[**IAnalysisRegion::ExcludeRectangle**](ianalysisregion-excluderectangle.md)
</dt> <dt>

[**IAnalysisRegion：： ExcludeRegion 方法**](ianalysisregion-excluderegion.md)
</dt> <dt>

[**IAnalysisRegion：： IntersectRectangle 方法**](ianalysisregion-intersectrectangle.md)
</dt> <dt>

[**IAnalysisRegion：： UnionRectangle 方法**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[**IAnalysisRegion：： UnionRegion 方法**](ianalysisregion-unionregion.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




