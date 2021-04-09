---
description: 本章節包含了壓縮紋理格式內部組織的相關資訊。
ms.assetid: a916d635-2be4-48be-ba70-a743b2969553
title: " (Direct3D 9) 的壓縮材質格式"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: dcecf6e98d125f3a391ab0e7a7c569a8dbd27d0d
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689076"
---
# <a name="compressed-texture-formats-direct3d-9"></a> (Direct3D 9) 的壓縮材質格式

本章節包含了壓縮紋理格式內部組織的相關資訊。 您不需要這些詳細資料來使用壓縮的材質，因為您可以使用 D3DX 函式來轉換成壓縮格式以及進行轉換。 但是，若您想要對壓縮表面資料進行直接的操作，這項資訊對您將會非常有幫助。

Direct3D 使用壓縮格式，將材質貼圖分為 4 x 4 的材質區塊。 如果紋理沒有設定任何透明度 (不透明)，或是其透明度由一個 1 位元的 Alpha 值所指定，一個 8 位元組的區塊將會代表材質貼圖區塊。 如果材質貼圖中包含了透明的材質，一個利用 Alpha 色板的 16 位元區塊將會代表它。

-   [ (Direct3D 9) 的不透明和1位 Alpha 紋理 ](opaque-and-1-bit-alpha-textures.md)
-   [具有 Alpha 通道的材質 (Direct3D 9) ](textures-with-alpha-channels.md)

任何單一紋理都必須指定由 16 個材質組成的每個群組，資料將會以 64 位元或是 128 位元的方式儲存。 如果有64位區塊（也就是 DXT1 格式）用於紋理，就可以在相同材質內的每個區塊上混用不透明和1位的 Alpha 格式。 換句話說，色彩0和色彩1的不帶正負號整數量詞的比較， \_ \_ 是針對每個16材質的區塊來唯一執行。

使用128位區塊時，必須以明確的 (格式 DXT2 或 DXT3) 或插入模式來指定 Alpha 色板， (格式 DXT4 或 DXT5) 適用于整個材質。 至於色彩，在選取插入模式時，您可逐區塊地選擇使用 8 個 Alpha 值插入模式或 6 個 Alpha 值插入模式。 同樣地，Alpha \_ 0 和 Alpha 1 的量 \_ 值比較是依區塊逐一完成。

DXTn 格式的音調與 DirectX 7.0 中傳回的格式不同。 現在以位元組為單位來測量音調， (不會封鎖) 。 例如，如果您的寬度是16，則會有四個區塊的 DXT1，4個區塊 (4 個 \* \* DXT2-5 個) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[壓縮的材質資源](compressed-texture-resources.md)
</dt> </dl>

 

 



