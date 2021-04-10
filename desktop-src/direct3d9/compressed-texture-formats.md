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
# <a name="compressed-texture-formats-direct3d-9"></a><span data-ttu-id="a20ac-103"> (Direct3D 9) 的壓縮材質格式</span><span class="sxs-lookup"><span data-stu-id="a20ac-103">Compressed Texture Formats (Direct3D 9)</span></span>

<span data-ttu-id="a20ac-104">本章節包含了壓縮紋理格式內部組織的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="a20ac-104">This section contains information about the internal organization of compressed texture formats.</span></span> <span data-ttu-id="a20ac-105">您不需要這些詳細資料來使用壓縮的材質，因為您可以使用 D3DX 函式來轉換成壓縮格式以及進行轉換。</span><span class="sxs-lookup"><span data-stu-id="a20ac-105">You do not need these details to use compressed textures, because you can use D3DX functions for conversion to and from compressed formats.</span></span> <span data-ttu-id="a20ac-106">但是，若您想要對壓縮表面資料進行直接的操作，這項資訊對您將會非常有幫助。</span><span class="sxs-lookup"><span data-stu-id="a20ac-106">However, this information is useful if you want to operate on compressed surface data directly.</span></span>

<span data-ttu-id="a20ac-107">Direct3D 使用壓縮格式，將材質貼圖分為 4 x 4 的材質區塊。</span><span class="sxs-lookup"><span data-stu-id="a20ac-107">Direct3D uses a compression format that divides texture maps into 4x4 texel blocks.</span></span> <span data-ttu-id="a20ac-108">如果紋理沒有設定任何透明度 (不透明)，或是其透明度由一個 1 位元的 Alpha 值所指定，一個 8 位元組的區塊將會代表材質貼圖區塊。</span><span class="sxs-lookup"><span data-stu-id="a20ac-108">If the texture contains no transparency - is opaque - or if the transparency is specified by a 1-bit alpha, an 8-byte block represents the texture map block.</span></span> <span data-ttu-id="a20ac-109">如果材質貼圖中包含了透明的材質，一個利用 Alpha 色板的 16 位元區塊將會代表它。</span><span class="sxs-lookup"><span data-stu-id="a20ac-109">If the texture map does contain transparent texels, using an alpha channel, a 16-byte block represents it.</span></span>

-   [<span data-ttu-id="a20ac-110"> (Direct3D 9) 的不透明和1位 Alpha 紋理 </span><span class="sxs-lookup"><span data-stu-id="a20ac-110">Opaque and 1-Bit Alpha Textures (Direct3D 9)</span></span>](opaque-and-1-bit-alpha-textures.md)
-   [<span data-ttu-id="a20ac-111">具有 Alpha 通道的材質 (Direct3D 9) </span><span class="sxs-lookup"><span data-stu-id="a20ac-111">Textures with Alpha Channels (Direct3D 9)</span></span>](textures-with-alpha-channels.md)

<span data-ttu-id="a20ac-112">任何單一紋理都必須指定由 16 個材質組成的每個群組，資料將會以 64 位元或是 128 位元的方式儲存。</span><span class="sxs-lookup"><span data-stu-id="a20ac-112">Any single texture must specify that its data is stored as 64 or 128 bits per group of 16 texels.</span></span> <span data-ttu-id="a20ac-113">如果有64位區塊（也就是 DXT1 格式）用於紋理，就可以在相同材質內的每個區塊上混用不透明和1位的 Alpha 格式。</span><span class="sxs-lookup"><span data-stu-id="a20ac-113">If 64-bit blocks - that is, format DXT1 - are used for the texture, it is possible to mix the opaque and 1-bit alpha formats on a per-block basis within the same texture.</span></span> <span data-ttu-id="a20ac-114">換句話說，色彩0和色彩1的不帶正負號整數量詞的比較， \_ \_ 是針對每個16材質的區塊來唯一執行。</span><span class="sxs-lookup"><span data-stu-id="a20ac-114">In other words, the comparison of the unsigned integer magnitude of color\_0 and color\_1 is performed uniquely for each block of 16 texels.</span></span>

<span data-ttu-id="a20ac-115">使用128位區塊時，必須以明確的 (格式 DXT2 或 DXT3) 或插入模式來指定 Alpha 色板， (格式 DXT4 或 DXT5) 適用于整個材質。</span><span class="sxs-lookup"><span data-stu-id="a20ac-115">When 128-bit blocks are used, the alpha channel must be specified in either explicit (format DXT2 or DXT3) or interpolated mode (format DXT4 or DXT5) for the entire texture.</span></span> <span data-ttu-id="a20ac-116">至於色彩，在選取插入模式時，您可逐區塊地選擇使用 8 個 Alpha 值插入模式或 6 個 Alpha 值插入模式。</span><span class="sxs-lookup"><span data-stu-id="a20ac-116">As with color, when interpolated mode is selected, either eight interpolated alphas or six interpolated alphas mode can be used on a block-by-block basis.</span></span> <span data-ttu-id="a20ac-117">同樣地，Alpha \_ 0 和 Alpha 1 的量 \_ 值比較是依區塊逐一完成。</span><span class="sxs-lookup"><span data-stu-id="a20ac-117">Again the magnitude comparison of alpha\_0 and alpha\_1 is done uniquely on a block-by-block basis.</span></span>

<span data-ttu-id="a20ac-118">DXTn 格式的音調與 DirectX 7.0 中傳回的格式不同。</span><span class="sxs-lookup"><span data-stu-id="a20ac-118">The pitch for DXTn formats is different from what was returned in DirectX 7.0.</span></span> <span data-ttu-id="a20ac-119">現在以位元組為單位來測量音調， (不會封鎖) 。</span><span class="sxs-lookup"><span data-stu-id="a20ac-119">Pitch is now measured in bytes (not blocks).</span></span> <span data-ttu-id="a20ac-120">例如，如果您的寬度是16，則會有四個區塊的 DXT1，4個區塊 (4 個 \* \* DXT2-5 個) 。</span><span class="sxs-lookup"><span data-stu-id="a20ac-120">For example, if you have a width of 16, then you will have a pitch of four blocks (4\*8 for DXT1, 4\*16 for DXT2-5).</span></span>

## <a name="related-topics"></a><span data-ttu-id="a20ac-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="a20ac-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a20ac-122">壓縮的材質資源</span><span class="sxs-lookup"><span data-stu-id="a20ac-122">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 



