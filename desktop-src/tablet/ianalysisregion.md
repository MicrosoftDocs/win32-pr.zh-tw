---
description: 公開代表檔區域之區域的方法和屬性。
ms.assetid: ee823a9e-a144-4394-847e-abf390fb839a
title: 'IAnalysisRegion 介面 (IACom .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IAnalysisRegion
api_type:
- COM
api_location:
- IACom.dll
ms.openlocfilehash: c9c5e7653790e193c03b1cf4e0c489ea39c3eec3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690607"
---
# <a name="ianalysisregion-interface"></a>IAnalysisRegion 介面

公開代表檔區域之區域的方法和屬性。

## <a name="members"></a>成員

**IAnalysisRegion** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **IAnalysisRegion** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**IAnalysisRegion** 介面具有這些方法。



| 方法                                                           | 描述                                                                                                                                    |
|:-----------------------------------------------------------------|:-----------------------------------------------------------------------------------------------------------------------------------------------|
| [**克隆**](ianalysisregion-clone.md)                           | 建立 **IAnalysisRegion** 的複本。<br/>                                                                                          |
| [**ExcludeRectangle**](ianalysisregion-excluderectangle.md)     | 將 **IAnalysisRegion** 的區域限制為其區域中未與指定的矩形相交的部分。<br/>           |
| [**ExcludeRegion**](ianalysisregion-excluderegion.md)           | 將 **IAnalysisRegion** 的區域限制為其區域中未與指定 **IAnalysisRegion** 相交的部分。<br/> |
| [**GetBounds**](ianalysisregion-getbounds.md)                   | 抓取 **IAnalysisRegion** 的周框。<br/>                                                                        |
| [**GetRegionScans**](ianalysisregion-getregionscans.md)         | 捕獲定義 **IAnalysisRegion** 區域的矩形陣列。<br/>                                                  |
| [**IntersectRectangle**](ianalysisregion-intersectrectangle.md) | 將這個 **IAnalysisRegion** 的區域限制為其與指定矩形的交集所建立的區域。<br/>                |
| [**IntersectRegion**](ianalysisregion-intersectregion.md)       | 將 **IAnalysisRegion** 的區域限制為其與指定 **IAnalysisRegion** 的交集所建立的區域。<br/>       |
| [**IntersectsWith**](ianalysisregion-intersectswith.md)         | 判斷 **IAnalysisRegion** 的區域是否與指定的矩形相交。<br/>                                     |
| [**IsEmpty**](ianalysisregion-isempty.md)                       | 抓取值，指出 **IAnalysisRegion** 是否代表空白區域。<br/>                                            |
| [**IsInfinite**](ianalysisregion-isinfinite.md)                 | 抓取值，指出 **IAnalysisRegion** 是否代表無限區域。<br/>                                         |
| [**MakeEmpty**](ianalysisregion-makeempty.md)                   | 減少 **IAnalysisRegion** 以代表空白區域。<br/>                                                                         |
| [**MakeInfinite**](ianalysisregion-makeinfinite.md)             | 展開 **IAnalysisRegion** 以代表無限區域。<br/>                                                                      |
| [**UnionRectangle**](ianalysisregion-unionrectangle.md)         | 將這個 **IAnalysisRegion** 的區域展開至其聯集所建立的區域（具有指定的矩形）。<br/>                         |
| [**UnionRegion**](ianalysisregion-unionregion.md)               | 將這個 **IAnalysisRegion** 的區域展開至具有指定 **IAnalysisRegion** 的聯集所建立的區域。<br/>               |



 

## <a name="remarks"></a>備註

此介面代表從矩形區域所建立的區域。 [**IInkAnalyzer**](iinkanalyzer.md)會在其接收筆觸資料的座標空間內，傳回或解讀區域的座標。

若要取得目前的 **IAnalysisRegion** 範圍，請使用 [**IAnalysisRegion：： GetBounds 方法**](ianalysisregion-getbounds.md) 或 [**IAnalysisRegion：： GetRegionScans 方法**](ianalysisregion-getregionscans.md)。

若要修改現有 **IAnalysisRegion** 的區域，請使用下列方法。

-   [**IAnalysisRegion::ExcludeRectangle**](ianalysisregion-excluderectangle.md)
-   [**IAnalysisRegion：： ExcludeRegion 方法**](ianalysisregion-excluderegion.md)
-   [**IAnalysisRegion：： IntersectRectangle 方法**](ianalysisregion-intersectrectangle.md)
-   [**IAnalysisRegion：： IntersectRegion 方法**](ianalysisregion-intersectregion.md)
-   [**IAnalysisRegion：： MakeEmpty 方法**](ianalysisregion-makeempty.md)
-   [**IAnalysisRegion：： MakeInfinite 方法**](ianalysisregion-makeinfinite.md)
-   [**IAnalysisRegion：： UnionRectangle 方法**](ianalysisregion-unionrectangle.md)
-   [**IAnalysisRegion：： UnionRegion 方法**](ianalysisregion-unionregion.md)

這個介面相當於 .NET Framework 中的 AnalysisCore. AnalysisRegionBase 類別。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                                                 |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                                     |
| 標頭<br/>                   | <dl> <dt>IACom (也需要 IACom \_ c) </dt> </dl> |
| DLL<br/>                      | <dl> <dt>IACom.dll</dt> </dl>                          |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IInkAnalyzer**](iinkanalyzer.md)
</dt> <dt>

[筆跡分析參考](ink-analysis-reference.md)
</dt> </dl>

 

