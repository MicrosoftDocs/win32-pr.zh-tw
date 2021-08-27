---
description: 將這個 IAnalysisRegion 的區域展開至具有指定 IAnalysisRegion 的聯集所建立的區域。
ms.assetid: cc3ec5c6-98ff-442e-a1e8-d1a57752ad56
title: 'IAnalysisRegion：： UnionRegion 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 760296552dc13ac394d4554903d84f596faba14318db9af3145c79f156c736fb
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720005"
---
# <a name="ianalysisregionunionregion-method"></a>IAnalysisRegion：： UnionRegion 方法

將這個 [**IAnalysisRegion**](ianalysisregion.md) 的區域展開至具有指定 **IAnalysisRegion** 的聯集所建立的區域。

## <a name="syntax"></a>語法


```C++
HRESULT UnionRegion(
  [in] IAnalysisRegion *pRegionToUnion
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pRegionToUnion* \[在\]
</dt> <dd>

要合併的 [**IAnalysisRegion**](ianalysisregion.md) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

如果任一區域都是無限的，則新區域也是無限的。

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

[**IAnalysisRegion：： IntersectRegion 方法**](ianalysisregion-intersectregion.md)
</dt> <dt>

[**IAnalysisRegion：： UnionRectangle 方法**](ianalysisregion-unionrectangle.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




