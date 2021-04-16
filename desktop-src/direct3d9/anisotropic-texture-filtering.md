---
description: 在3D 物件的材質中可見的扭曲，其介面面向于螢幕平面的角度，稱為 anisotropy。
ms.assetid: f6c8a9e2-aab0-4f06-956e-bb86557c72e7
title: " (Direct3D 9) 的非等向材質篩選"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c3443696e54410c6edc6a9998d4fcfd86b537a0e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468461"
---
# <a name="anisotropic-texture-filtering-direct3d-9"></a><span data-ttu-id="db114-103"> (Direct3D 9) 的非等向材質篩選</span><span class="sxs-lookup"><span data-stu-id="db114-103">Anisotropic Texture Filtering (Direct3D 9)</span></span>

<span data-ttu-id="db114-104">在3D 物件的材質中可見的扭曲，其介面面向于螢幕平面的角度，稱為 anisotropy。</span><span class="sxs-lookup"><span data-stu-id="db114-104">The distortion visible in the texels of a 3D object whose surface is oriented at an angle with respect to the plane of the screen is called anisotropy.</span></span> <span data-ttu-id="db114-105">當非等向性原始物件的像素對應至材質時，其形狀會失真。</span><span class="sxs-lookup"><span data-stu-id="db114-105">When a pixel from an anisotropic primitive is mapped to texels, its shape is distorted.</span></span> <span data-ttu-id="db114-106">Direct3D 將像素的非等向性測量為延長部分，意即反向對應至紋理空間之螢幕像素的長度除以寬度。</span><span class="sxs-lookup"><span data-stu-id="db114-106">Direct3D measures the anisotropy of a pixel as the elongation - that is, length divided by width - of a screen pixel that is inverse-mapped into texture space.</span></span>

<span data-ttu-id="db114-107">您可搭配使用非等向性紋理篩選與線性紋理篩選或 Mipmap 紋理篩選，以改善轉譯結果。</span><span class="sxs-lookup"><span data-stu-id="db114-107">You can use anisotropic texture filtering in conjunction with linear texture filtering or mipmap texture filtering to improve rendering results.</span></span> <span data-ttu-id="db114-108">您的應用程式會藉由呼叫 [**IDirect3DDevice9：： SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) 方法，啟用非等向材質篩選。</span><span class="sxs-lookup"><span data-stu-id="db114-108">Your application enables anisotropic texture filtering by calling the [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) method.</span></span> <span data-ttu-id="db114-109">將第一個參數的值設定為您要選取材質篩選方法之材質 (0-7) 的整數索引編號。</span><span class="sxs-lookup"><span data-stu-id="db114-109">Set the value of the first parameter to the integer index number (0-7) of the texture for which you are selecting a texture filtering method.</span></span> <span data-ttu-id="db114-110">\_ \_ 針對第二個參數傳遞 D3DSAMP MAGFILTER、D3DSAMP MINFILTER 或 D3DSAMP \_ MIPFILTER，以設定放大、縮制或 mipmap 篩選。</span><span class="sxs-lookup"><span data-stu-id="db114-110">Pass D3DSAMP\_MAGFILTER, D3DSAMP\_MINFILTER, or D3DSAMP\_MIPFILTER for the second parameter to set the magnification, minification, or mipmapping filter.</span></span> <span data-ttu-id="db114-111">將第三個參數設定為 [D3DTEXF] \_ 。</span><span class="sxs-lookup"><span data-stu-id="db114-111">Set the third parameter to D3DTEXF\_ANISOTROPIC.</span></span>

<span data-ttu-id="db114-112">您的應用程式也必須將 anisotropy 的程度設定為大於1的值。</span><span class="sxs-lookup"><span data-stu-id="db114-112">Your application must also set the degree of anisotropy to a value greater than one.</span></span> <span data-ttu-id="db114-113">若要這麼做，請呼叫 [**IDirect3DDevice9：： SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) 方法。</span><span class="sxs-lookup"><span data-stu-id="db114-113">Do this by calling the [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate) method.</span></span> <span data-ttu-id="db114-114">將第一個參數的值設定為您要設定 isotropy 程度之材質 (0-7) 的整數索引編號。</span><span class="sxs-lookup"><span data-stu-id="db114-114">Set the value of the first parameter to the integer index number (0-7) of the texture for which you are setting the degree of isotropy.</span></span> <span data-ttu-id="db114-115">傳遞 D3DSAMP \_ MAXANISOTROPY 做為第二個參數的值。</span><span class="sxs-lookup"><span data-stu-id="db114-115">Pass D3DSAMP\_MAXANISOTROPY as the value of the second parameter.</span></span> <span data-ttu-id="db114-116">最後一個參數應該是 isotropy 的程度。</span><span class="sxs-lookup"><span data-stu-id="db114-116">The final parameter should be the degree of isotropy.</span></span>

<span data-ttu-id="db114-117">您可以將 isotropy 的程度設定為1，以停用 isotropic 篩選。大於1的值會啟用它。</span><span class="sxs-lookup"><span data-stu-id="db114-117">You can disable isotropic filtering by setting the degree of isotropy to one; any value larger than one enables it.</span></span> <span data-ttu-id="db114-118">檢查 [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) 結構中的 MaxAnisotropy 旗標，以判斷 anisotropy 程度的可能值範圍。</span><span class="sxs-lookup"><span data-stu-id="db114-118">Check the MaxAnisotropy flag in the [**D3DCAPS9**](/windows/desktop/api/D3D9Caps/ns-d3d9caps-d3dcaps9) structure to determine the possible range of values for the degree of anisotropy.</span></span>

## <a name="related-topics"></a><span data-ttu-id="db114-119">相關主題</span><span class="sxs-lookup"><span data-stu-id="db114-119">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="db114-120">材質篩選</span><span class="sxs-lookup"><span data-stu-id="db114-120">Texture Filtering</span></span>](texture-filtering.md)
</dt> </dl>

 

 
