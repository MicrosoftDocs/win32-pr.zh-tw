---
description: 捕獲定義 IAnalysisRegion 區域的矩形陣列。
ms.assetid: 40de4c27-4b3b-4db3-af08-cb53e638db6b
title: 'IAnalysisRegion：： GetRegionScans 方法 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion.GetRegionScans
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: e197126a99023fb96c2798343b391d53de4f6cd97aaaa141918f0fe705e5ad1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118045315"
---
# <a name="ianalysisregiongetregionscans-method"></a>IAnalysisRegion：： GetRegionScans 方法

捕獲定義 [**IAnalysisRegion**](ianalysisregion.md)區域的矩形陣列。

## <a name="syntax"></a>語法


```C++
HRESULT GetRegionScans(
  [out] ULONG *pulCount,
  [out] RECT  **pRegionScans
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pulCount* \[擴展\]
</dt> <dd>

*PRegionScans* 中傳回的矩形數目。

</dd> <dt>

*pRegionScans* \[擴展\]
</dt> <dd>

矩形陣列的指標，該陣列定義 [**IAnalysisRegion**](ianalysisregion.md)的區域。

</dd> </dl>

## <a name="return-value"></a>傳回值

如需傳回值的描述，請參閱 [類別和介面-筆跡分析](classes-and-interfaces---ink-analysis.md)。

## <a name="remarks"></a>備註

如果 *pRegionScans* 傳遞為 **Null**，則 **GetRegionScans** 方法會傳回 **S \_ OK** ，而且在 *pulCount* 中會傳回矩形的數目。

> [!Caution]  
> 若要避免記憶體流失， [](/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemfree) \* 當您不再需要此資訊時，請使用 CoTaskMemFree 釋放 *pRegionScans* 的記憶體。

 

矩形的界限為筆墨空間座標。

傳回之矩形的聯集代表 [**IAnalysisRegion**](ianalysisregion.md)的區域。

## <a name="examples"></a>範例

下列範例顯示如何取得定義 [**IAnalysisRegion**](ianalysisregion.md)區域的矩形， `region` 以及如何只取得矩形的數目。


```C++
// Get the count and the rectangles.
ULONG count = 0;
RECT* rects = 0;
region->GetRegionScans(&count, &rects);

// Use rects

::CoTaskMemFree(rects);

// GetRegionScans just gets the count and returns S_OK
ULONG number = 0;
region->GetRegionScans(&number, NULL); 
```



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

[**IAnalysisRegion：： GetBounds 方法**](ianalysisregion-getbounds.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

