---
description: 判斷 IAnalysisRegion 的區域是否與指定的矩形相交。
ms.assetid: 683c3ad8-0236-474e-a16d-6164c2244cfb
title: 'IAnalysisRegion：： IntersectsWith 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.IntersectsWith
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 04613e061929bba04c14be37914b22a51de0377f125b21fa29db9c56fc8dfeff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118720015"
---
# <a name="ianalysisregionintersectswith-method"></a>IAnalysisRegion：： IntersectsWith 方法

判斷 [**IAnalysisRegion**](ianalysisregion.md) 的區域是否與指定的矩形相交。

## <a name="syntax"></a>語法


```C++
HRESULT IntersectsWith(
  [in]  RECT         *pRectangle,
  [out] VARIANT_BOOL *pfIsIntersecting
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pRectangle* \[在\]
</dt> <dd>

要與之比較的矩形指標，以筆墨的空格座標表示。

</dd> <dt>

*pfIsIntersecting* \[擴展\]
</dt> <dd>

**變異 \_** 如果 [**IAnalysisRegion**](ianalysisregion.md)的區域與指定的矩形相交，則為 TRUE;否則， **VARIANT \_ FALSE**。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

比較是以筆墨空間座標表示。

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

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




