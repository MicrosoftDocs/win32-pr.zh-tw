---
description: 將 IAnalysisRegion 的區域限制為其區域中未與指定 IAnalysisRegion 相交的部分。
ms.assetid: 7a11d2a8-c2ca-4088-b932-8a6c3e789b7f
title: 'IAnalysisRegion：： ExcludeRegion 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.ExcludeRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 4a26bc234a5a99d2ba692b02097d348b83878c47ea3c9a1cbd21e1558fc41950
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119092349"
---
# <a name="ianalysisregionexcluderegion-method"></a>IAnalysisRegion：： ExcludeRegion 方法

將 [**IAnalysisRegion**](ianalysisregion.md) 的區域限制為其區域中未與指定 **IAnalysisRegion** 相交的部分。

## <a name="syntax"></a>語法


```C++
HRESULT ExcludeRegion(
  [in] IAnalysisRegion *pRegionToExclude
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pRegionToExclude* \[在\]
</dt> <dd>

要從此 **IAnalysisRegion** 排除的 [**IAnalysisRegion**](ianalysisregion.md) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

如果這兩個區域不相交，此 [**IAnalysisRegion**](ianalysisregion.md) 就不會變更。

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

 

 




