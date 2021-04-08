---
description: Direct3D 9 支援點、線條、三角形和方格基本專案。
ms.assetid: 474e8bee-336d-491f-afa0-f0186a8d19c7
title: " (Direct3D 9 的 Higher-Order 基本) "
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67767dd955fa5c0c5c21315d7c1c510de422870c
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687459"
---
# <a name="higher-order-primitives-direct3d-9"></a> (Direct3D 9 的 Higher-Order 基本) 

Direct3D 9 支援點、線條、三角形和方格基本專案。 這些已擴充，可支援高序位的插補超過線性。 雖然三角形和線條具有空間範圍，但是現在它們都是使用線性插補來呈現。 在 Direct3D 9 中，Direct3D 支援使用較高的順序（最多 quintic 的插補）來轉譯這些基本類型。 此外，現在支援新的四基本類型。 這個新類型也可以使用較高順序的插補來呈現。 這項功能主要是由動畫和字元轉譯的需求所驅動。 也可用於其他表面，例如地形或水。

當您以清單、帶狀、風扇或索引網格形式傳送至 API 時，較高順序的基本專案支援高序位的插補。 您可以使用在頂點本身編碼的額外資訊來達成這個目的。 例如，一般向量可以用來定義頂點的正切平面，以啟用三次插補。 大部分的實作為以鑲嵌為平面三角形的方式支援高階插補。 鑲嵌式步驟會以邏輯方式在頂點著色器階段之前套用。 因為頂點著色器 API 不會在其輸入資料上強加語義，所以會提供特殊機制來識別代表位置的頂點資料流程元件，並選擇性地識別一般向量。 所有其他元件則會據以插補。

本節介紹高階的基本專案，並討論如何在應用程式中使用它們。 資訊分成下列主題。

-   [透過解析度增強功能改善品質](#improved-quality-through-resolution-enhancement)
-   [Spline-Based 工具的直接對應](#direct-mapping-from-spline-based-tools)

## <a name="improved-quality-through-resolution-enhancement"></a>透過解析度增強功能改善品質

目前的基本專案不適合用來表示平滑表面。 較高順序的插補方法（例如立方 polynomials）允許更精確的計算呈現曲線形狀。 藉由減少或消除在側面剪影邊緣或反射表面光源上可見的 facet 構件，可提供更高的真實性。 此外，在晶片上進行鑲嵌時，鑲嵌三角形不會影響匯流排頻寬。 在許多情況下，少量鑲嵌可提供映射品質的改進，並對效能造成最小的影響。

Direct3D 9 提供簡單的方法，讓您將解析度增強功能套用至現有的多邊形導向工具和藝術管線所建立的內容。 應用程式只需要提供所需的鑲嵌層級，並使用包含一般向量的標準三角形語法來傳輸資料。

## <a name="direct-mapping-from-spline-based-tools"></a>Spline-Based 工具的直接對應

許多目前的撰寫工具都支援較高順序的基本專案，以啟用比一般提供的平面三角形網格更強大的模型作業。 當有效率地使用時，可讓產生的修補程式數目合理，這類工具可以產生可直接由 API 轉譯的內容。 為了滿足這項需求，已加入新的進入點，可將傳入的頂點資料流程視為控制點的2D 陣列，並 tessellates 為所需的解析度。

-   [使用 Higher-Order 基本 (Direct3D 9) ](using-higher-order-primitives.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[頂點管線](vertex-pipeline.md)
</dt> </dl>

 

 



