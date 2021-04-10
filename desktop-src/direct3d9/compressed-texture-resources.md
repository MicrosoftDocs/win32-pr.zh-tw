---
description: 紋理貼圖為繪製在三維圖形上的數位化影像，用來增加更多視覺上的細節。
ms.assetid: 0ea5cb07-a21a-4e2c-93e2-54966153bb8a
title: " (Direct3D 9) 的壓縮材質資源"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b9b7ef048c0e1780f92246a407863a4fa48a94a0
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191000"
---
# <a name="compressed-texture-resources-direct3d-9"></a> (Direct3D 9) 的壓縮材質資源

紋理貼圖為繪製在三維圖形上的數位化影像，用來增加更多視覺上的細節。 他們在點陣化的過程中對應至這些圖形之上，並且整個過程可能會取用大量的系統匯流排及記憶體。 若要減少紋理所使用的記憶體，Direct3D 支援壓縮紋理表面。 某些 Direct3D 裝置原生支援壓縮紋理表面。 在這類裝置上，當您建立了一個壓縮表面並且將資料載入其中，該表面即可像任何其他的紋理表面一樣用於 Direct3D 之中。 Direct3D 將會在該紋理對應至 3D 物件之上時，對其進行解壓縮。

## <a name="storage-efficiency-and-texture-compression"></a>儲存效率和材質壓縮

所有紋理壓縮格式都是二的乘冪。 雖然這並不表示紋理一定是矩形，但實際上紋理的 x 值和 y 值的確都是二的乘冪。 例如：一個原本是 512 x 128 位元組的紋理，在下一個 Mipmapping 將會縮小至 256 x 64，並且在每個層級以 2 的乘冪遞減。 當紋理在較低的層級被篩選至 16 x 2 或 8 x 1 時，將會有未充分利用的位元存在，因為壓縮區塊一律都是 4 x 4 的材質區塊。 未使用的區塊部分將會獲得填補。 雖然在最低的層級時會有未充分利用的位元，整體增益仍然相當可觀。 理論上，最差的情況便是 2K x 1 的紋理 (2⁰ 乘冪)。 在這種情況下，每一區塊只有一列像素獲得編碼，區塊的其餘部分都將不會被使用到。

## <a name="mixing-formats-within-a-single-texture"></a>在單一材質內混用格式

請務必注意任何單一紋理都必須指定由 16 個材質組成的每個群組，資料將會以 64 位元或是 128 位元的方式儲存。 如果有64位區塊（也就是 DXT1 格式）用於紋理，就可以在相同材質內的每個區塊上混用不透明和1位的 Alpha 格式。 換句話說，色彩0和色彩1的不帶正負號整數量詞的比較， \_ \_ 是針對每個16材質的區塊來唯一執行。

使用128位區塊之後，必須以明確的 (格式 DXT2 和 DXT3) 或插入模式來指定 Alpha 色板， (格式 DXT4 和 DXT5) 適用于整個材質。 同樣地，如果選取了插補模式 (format DXT4 和 DXT5) ，則可以使用八個插入 Alpha 或六個插補 Alpha 模式來逐一封鎖。 同樣地，Alpha \_ 0 和 Alpha 1 的量 \_ 值比較是依區塊逐一完成。

Direct3D 針對用於 3D 模型貼圖的表面，提供了壓縮的服務。 本章節提供了建立和管理壓縮紋理表面中資料的相關資訊。

下列主題包含資訊。

-   [ (Direct3D 9) 的不透明和1位 Alpha 紋理 ](opaque-and-1-bit-alpha-textures.md)
-   [具有 Alpha 通道的材質 (Direct3D 9) ](textures-with-alpha-channels.md)
-   [ (Direct3D 9) 的壓縮材質格式 ](compressed-texture-formats.md)
-   [使用 (Direct3D 9) 的壓縮紋理 ](using-compressed-textures.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Direct3D 紋理](direct3d-textures.md)
</dt> </dl>

 

 



