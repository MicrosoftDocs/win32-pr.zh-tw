---
title: Direct2D 函式
description: Direct2D 提供下列功能。
ms.assetid: 1a7ae962-9b70-442c-a676-f172a2d9bfd3
keywords:
- Direct2D，函數
ms.topic: article
ms.date: 09/19/2019
ms.openlocfilehash: 9cbe07a6c1054036030395ff965610919ee48a97
ms.sourcegitcommit: 73417d55867c804274a55abe5ca71bcba7006119
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2020
ms.locfileid: "104463897"
---
# <a name="direct2d-functions"></a>Direct2D 函式

Direct2D 提供下列功能。 額外的函式會在 [D2D1 命名空間](d2d1-namespace.md)中定義。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [**D2D1ComputeMaximumScaleFactor**](/windows/desktop/api/d2d1_2/nf-d2d1_2-d2d1computemaximumscalefactor) | 計算給定轉換可以延展任何向量的最大因數。 |
| [**D2D1CreateDevice**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevice) | 建立與提供的 DXGI 裝置相關聯的新 Direct2D 裝置。  |
| [**D2D1CreateDeviceCoNtext**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1createdevicecontext) | 建立與 DXGI 介面相關聯的新 Direct2D 裝置內容。  |
| [**D2D1CreateFactory (D2D1_FACTORY_TYPE、REFIID、void \* \*)**](/windows/win32/api/d2d1/nf-d2d1-d2d1createfactory-r1) | 建立可用於建立 Direct2D 資源的 factory 物件。 |
| [**D2D1CreateFactory (D2D1_FACTORY_TYPE、REFIID、D2D1_FACTORY_OPTIONS \* 、void \* \*)**](/windows/desktop/api/d2d1/nf-d2d1-d2d1createfactory) | 建立可用於建立 Direct2D 資源的 factory 物件。 |
| [**D2D1GetGradientMeshInteriorPointsFromCoonsPatch**](/windows/desktop/api/d2d1_3/nf-d2d1_3-d2d1getgradientmeshinteriorpointsfromcoonspatch) | 根據定義 Coons patch 的點，傳回漸層網格修補程式的內部點。 |
| [**D2D1InvertMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1invertmatrix) | 嘗試將指定的矩陣反轉。 |
| [**D2D1IsMatrixInvertible**](/windows/desktop/api/d2d1/nf-d2d1-d2d1ismatrixinvertible) | 指出指定的矩陣是否可反轉。 |
| [**D2D1MakeRotateMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1makerotatematrix) | 建立旋轉轉換，以根據指定點的指定角度旋轉。 |
| [**D2D1MakeSkewMatrix**](/windows/desktop/api/d2d1/nf-d2d1-d2d1makeskewmatrix) | 建立具有指定 X 軸角度、y 軸角度和中心點的扭曲轉換。  |
| [**運算子 \* (const D2D1\MATRIX\3X2\F&，const D2D1\MATRIX\3X2\F&)**](/windows/win32/api/d2d1helper/nf-d2d1helper-matrix3x2f-setproduct) | 將兩個矩陣相乘，並傳回結果。 |
| [**BlobGetter**](blobgetter.md) | 呼叫 blob 型別屬性的成員函式屬性 getter 回呼。 |
| [**BlobSetter**](blobsetter.md) | 呼叫 blob 型別屬性的成員函式屬性 setter 回呼。 |
| [**DeducingBlobGetter**](deducingblobgetter.md) | 會推算類別和引數，然後針對 blob 類型屬性呼叫成員函式屬性 getter 回呼。 |
| [**DeducingBlobSetter**](deducingblobsetter.md) | 會推算類別和引數，然後針對 blob 類型屬性呼叫成員函式屬性 setter 回呼。 |
| [**DeducingStringGetter**](deducingstringgetter.md) | 會推算類別和引數，然後針對字串類型屬性呼叫成員函式屬性 getter 回呼。 |
| [**DeducingStringSetter**](deducingstringsetter.md) | 會推算類別和引數，然後針對字串類型屬性呼叫成員函式屬性 setter 回呼。 |
| [**DeducingValueGetter**](deducingvaluegetter.md) | 會推算類別和引數，然後針對實數值型別屬性呼叫成員函式屬性 getter 回呼。 |
| [**DeducingValueSetter**](deducingvaluesetter.md) | 會推算類別和引數，然後針對實數值型別屬性呼叫成員函式屬性 setter 回呼。 |
| [**GetType**](/previous-versions/windows/desktop/legacy/hh847962(v=vs.85)) | 抓取指定屬性的型別。 |
| [**StringGetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-stringgetter) | 針對字串類型屬性呼叫成員函式屬性 getter 回呼。 |
| [**StringSetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-stringsetter) | 針對字串類型屬性呼叫成員函式屬性 setter 回呼。 |
| [**ValueGetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-valuegetter) | 針對實數值型別屬性呼叫成員函式屬性 setter 回呼。 |
| [**ValueSetter**](/windows/desktop/api/d2d1effecthelpers/nf-d2d1effecthelpers-valuesetter) | 針對實數值型別屬性呼叫成員函式屬性 setter 回呼。 |
| [**D2D1ConvertColorSpace**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1convertcolorspace) | 將指定的色彩從一個 colorspace 轉換成另一個。 |
| [**D2D1SinCos**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1sincos) | 傳回角度的正弦和余弦。 |
| [**D2D1Tan**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1tan) | 傳回角度的正切。 |
| [**D2D1Vec3Length**](/windows/desktop/api/d2d1_1/nf-d2d1_1-d2d1vec3length) | 傳回3維度向量的長度。 |
| [**PD2D1\PROPERTY\GET\FUNCTION**](/windows/desktop/api/D2d1effectauthor/nc-d2d1effectauthor-pd2d1_property_get_function) | 從效果中取得屬性。 |
| [**PD2D1\PROPERTY\SET\FUNCTION**](/windows/desktop/api/D2d1effectauthor/nc-d2d1effectauthor-pd2d1_property_set_function) | 設定效果的屬性。 |