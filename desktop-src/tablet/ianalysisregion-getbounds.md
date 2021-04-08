---
description: 取得 IAnalysisRegion 的周框。
ms.assetid: 6b9deff7-12e9-4b30-86cb-25b94737d28d
title: 'IAnalysisRegion：： GetBounds 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetBounds
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: 12bbb8163aa866648a83effc75d668bc4032c8d7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690615"
---
# <a name="ianalysisregiongetbounds-method"></a>IAnalysisRegion：： GetBounds 方法

取得 [**IAnalysisRegion**](ianalysisregion.md)的周框。

## <a name="syntax"></a>語法


```C++
HRESULT GetBounds(
  [out] RECT *pBoundingRectangle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pBoundingRectangle* \[擴展\]
</dt> <dd>

[**IAnalysisRegion**](ianalysisregion.md)的周框（以筆墨空間座標表示）。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

範圍是以筆墨空間座標表示。

如果 [**IAnalysisRegion**](ianalysisregion.md) 代表無限區域，則左側和頂端界限為 **int \_ MIN**，右邊和下界限則為 **int \_ MAX**。

如果 [**IAnalysisRegion**](ianalysisregion.md) 代表空白區域，則矩形的所有界限都是0。

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

[**IAnalysisRegion：： GetRegionScans 方法**](ianalysisregion-getregionscans.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

 




