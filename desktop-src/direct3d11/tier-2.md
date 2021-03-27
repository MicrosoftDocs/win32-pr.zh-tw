---
title: 第 2 層
description: 本節說明第2層支援。
ms.assetid: 4A4AEF13-2F0F-482E-9262-256C257ED85A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 58fa6e8ff3dba5780e3507bb2da5273e327a30e1
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842495"
---
# <a name="tier-2"></a>第 2 層

本節說明第2層支援。

-   硬體至少為功能層級 11.1。
-   前一層的所有功能 (但沒有[第 1 層](tier-1.md)特定的限制) 以及新增的下列項目︰
-   有著色器指示可供鉗制 LOD 與對應狀態回應使用。 如需詳細資訊，請參閱 HLSL 並排顯示 [資源暴露](hlsl-tiled-resources-exposure.md)。
-   讀取非對應的磚時，會在格式的所有非遺漏元件以及遺失元件的預設值內傳回 0。
-   非對應磚的寫入將停止移至記憶體，但最後可能會傳至快取，該快取後續會讀取同一個可能會被選取的位址。
-   記憶體使用量供 **NULL** 與非 **NULL** 磚共用的紋理篩選，會為 **NULL** 磚上的材質，而將 0 (含遺失格式元件預設值) 提供至整體篩選作業。 如果任何材質 (含非零權數) 落在 **NULL** 磚上，某些舊版的硬體會不符合此需求，並讓完整篩選結果傳回 0 (含遺失格式元件預設值)。 不允許任何其他硬體遺漏將所有 (非零權數) 材質包含在篩選作業中的需求。
-   存取 **NULL** 材質會造成狀態回應上 [**CheckAccessFullyMapped**](/windows/desktop/direct3dhlsl/checkaccessfullymapped) (英文) 作業的紋理讀取傳回 False。 無論紋理存取結果如何在著色器內寫入遮罩，以及多少元件為紋理格式 (紋理格式的組合可能會造成不須存取其紋理的假象)，都會發生這項問題。
-   標準磚圖形對齊限制︰在所有維度填滿至少一個標準磚的 Mipmap 一定會使用標準並排，餘數會視為 **單位** 而封裝至 N 磚 (將 N 回報至應用程式)。 應用程式可將 N 磚對應至磚集區中的任意斷續位置，但必須將所有的壓縮磚都對應，否則全都不對應。 Mip 套件是每個陣列切割中的一組獨特壓縮磚。
-   支援最小/最大削減篩選。 如需 Min/Max 縮減篩選的詳細資訊，請參閱並排顯示的 [資源紋理取樣功能](tiled-resources-texture-sampling-features.md)。
-   在任何維度中，將任何 mipmap 小於標準磚大小的資源，都不能有大於1的陣列大小。
-   當有重複的對應時，可以存取磚的限制，如 [圖格存取限制](tile-access-limitations-with-duplicate-mappings-.md)中有重複對應的說明，請繼續套用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[磚資源功能層級](tiled-resources-features-tiers.md)
</dt> </dl>

 

 