---
description: 將這個 IAnalysisRegion 的區域展開至其聯集所建立的區域（具有指定的矩形）。
ms.assetid: 9b12f509-4f6a-43b0-9639-bef060fd6d50
title: 'IAnalysisRegion：： UnionRectangle 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.UnionRectangle
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: da3eefb3a527646ba416d62783421d6dfe9be5706c0527df7eb321d3945b6f92
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119596749"
---
# <a name="ianalysisregionunionrectangle-method"></a>IAnalysisRegion：： UnionRectangle 方法

將這個 [**IAnalysisRegion**](ianalysisregion.md) 的區域展開至其聯集所建立的區域（具有指定的矩形）。

## <a name="syntax"></a>語法


```C++
HRESULT UnionRectangle(
  [in] RECT *pRectangle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pRectangle* \[在\]
</dt> <dd>

要結合的矩形指標，以筆墨的空格座標表示。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

矩形座標以 HIMETRIC 單位表示。

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

[**IAnalysisRegion：： UnionRegion 方法**](ianalysisregion-unionregion.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




