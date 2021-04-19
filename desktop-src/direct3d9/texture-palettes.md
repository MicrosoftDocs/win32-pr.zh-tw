---
description: Direct3D 9 透過一組與 IDirect3DDevice9 物件相關聯的256專案調色板來支援調色板紋理。
ms.assetid: dea4b4bc-7eba-40fa-9c2c-0851fe7e231b
title: " (Direct3D 9) 的材質調色板"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a0fbb1c5d6766b879b898145ec2385a41d94b8e
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106970689"
---
# <a name="texture-palettes-direct3d-9"></a><span data-ttu-id="5663c-103"> (Direct3D 9) 的材質調色板</span><span class="sxs-lookup"><span data-stu-id="5663c-103">Texture Palettes (Direct3D 9)</span></span>

<span data-ttu-id="5663c-104">Direct3D 9 透過一組與 [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) 物件相關聯的256專案調色板來支援調色板紋理。</span><span class="sxs-lookup"><span data-stu-id="5663c-104">Direct3D 9 supports paletted textures through a set of 256 entry palettes associated with the [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) object.</span></span> <span data-ttu-id="5663c-105">藉由呼叫 [**IDirect3DDevice9：： SetCurrentTexturePalette**](/windows/desktop/api) 方法，將元件設為最新。</span><span class="sxs-lookup"><span data-stu-id="5663c-105">A palette is made current by calling the [**IDirect3DDevice9::SetCurrentTexturePalette**](/windows/desktop/api) method.</span></span> <span data-ttu-id="5663c-106">目前的調色板用於轉譯所有使用中材質階段的所有調色板紋理。</span><span class="sxs-lookup"><span data-stu-id="5663c-106">The current palette is used for translating all paletted textures for all active texture stages.</span></span> <span data-ttu-id="5663c-107">[**IDirect3DDevice9：： SetPaletteEntries**](/windows/desktop/api) 會更新所有調色板的256專案。</span><span class="sxs-lookup"><span data-stu-id="5663c-107">[**IDirect3DDevice9::SetPaletteEntries**](/windows/desktop/api) updates all of a palette's 256 entries.</span></span> <span data-ttu-id="5663c-108">每個專案都是 D3DFMT A8R8G8B8 格式的 [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) 結構 \_ 。</span><span class="sxs-lookup"><span data-stu-id="5663c-108">Each entry is a [**PALETTEENTRY**](/windows/win32/api/wingdi/ns-wingdi-paletteentry) structure of the format D3DFMT\_A8R8G8B8.</span></span> <span data-ttu-id="5663c-109">所有專案都會預設為0xFFFFFFFF。</span><span class="sxs-lookup"><span data-stu-id="5663c-109">All entries default to 0xFFFFFFFF.</span></span>

<span data-ttu-id="5663c-110">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)調色板包含 Alpha 色板。</span><span class="sxs-lookup"><span data-stu-id="5663c-110">The [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) palettes contain an alpha channel.</span></span> <span data-ttu-id="5663c-111">設定 D3DPTEXTURECAPS ALPHAPALETTE 裝置功能旗標時，可以使用此 Alpha 通道 \_ ，表示裝置支援來自調色板的 Alpha。</span><span class="sxs-lookup"><span data-stu-id="5663c-111">This alpha channel can be used when the D3DPTEXTURECAPS\_ALPHAPALETTE device capability flag is set, indicating that the device supports alpha from the palette.</span></span> <span data-ttu-id="5663c-112">當材質格式沒有 Alpha 色板時，會使用調色板 Alpha 通道。</span><span class="sxs-lookup"><span data-stu-id="5663c-112">The palette alpha channel is used when the texture format does not have an alpha channel.</span></span> <span data-ttu-id="5663c-113">如果裝置不支援來自調色板的 Alpha，且材質格式沒有 Alpha 色板，則會將0xFF 的值用於 Alpha。</span><span class="sxs-lookup"><span data-stu-id="5663c-113">If the device does not support alpha from the palette and the texture format does not have an alpha channel, then a value of 0xFF is used for alpha.</span></span>

<span data-ttu-id="5663c-114">最多可以有 65536 (0x0000FFFF) 調色板。</span><span class="sxs-lookup"><span data-stu-id="5663c-114">There is a maximum of 65,536 (0x0000FFFF) palettes.</span></span> <span data-ttu-id="5663c-115">由於與應用程式所參考的最大調色板數目成正比，因此與一組調色板相關聯的記憶體資源會使用從零開始的連續調色板編號。</span><span class="sxs-lookup"><span data-stu-id="5663c-115">Because memory resources associated with the set of palettes are proportional to the maximum palette number that an application references, use contiguous palette numbers starting at zero.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5663c-116">相關主題</span><span class="sxs-lookup"><span data-stu-id="5663c-116">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5663c-117">基本紋理概念</span><span class="sxs-lookup"><span data-stu-id="5663c-117">Basic Texturing Concepts</span></span>](basic-texturing-concepts.md)
</dt> </dl>

 

 
