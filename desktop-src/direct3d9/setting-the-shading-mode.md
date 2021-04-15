---
description: Direct3D 可以一次選取一種網底模式。
ms.assetid: 9531947d-4cd8-43c3-8825-4c48a0d69395
title: 設定 (Direct3D 9) 的陰影模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62f93d79e4507d9e9d08569e5cbd75bb8b42aa4f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104467782"
---
# <a name="setting-the-shading-mode-direct3d-9"></a><span data-ttu-id="6f271-103">設定 (Direct3D 9) 的陰影模式</span><span class="sxs-lookup"><span data-stu-id="6f271-103">Setting the Shading Mode (Direct3D 9)</span></span>

<span data-ttu-id="6f271-104">Direct3D 可以一次選取一種網底模式。</span><span class="sxs-lookup"><span data-stu-id="6f271-104">Direct3D enables one shading mode to be selected at a time.</span></span> <span data-ttu-id="6f271-105">預設會選取 [Gouraud] 網底。</span><span class="sxs-lookup"><span data-stu-id="6f271-105">By default, Gouraud shading is selected.</span></span> <span data-ttu-id="6f271-106">在 c + + 中，您可以藉由呼叫 [**IDirect3DDevice9：： graphicsdevice**](/windows/desktop/api) 方法來變更陰影模式。</span><span class="sxs-lookup"><span data-stu-id="6f271-106">In C++, you can change the shading mode by calling the [**IDirect3DDevice9::SetRenderState**](/windows/desktop/api) method.</span></span> <span data-ttu-id="6f271-107">將 *State* 參數設定為 D3DRS \_ SHADEMODE。</span><span class="sxs-lookup"><span data-stu-id="6f271-107">Set the *State* parameter to D3DRS\_SHADEMODE.</span></span> <span data-ttu-id="6f271-108">*State* 參數必須設定為 [**D3DSHADEMODE**](./d3dshademode.md)列舉的成員。</span><span class="sxs-lookup"><span data-stu-id="6f271-108">The *State* parameter must be set to a member of the [**D3DSHADEMODE**](./d3dshademode.md) enumeration.</span></span> <span data-ttu-id="6f271-109">下列範例程式碼範例說明如何將 Direct3D 應用程式的目前網底模式設定為 [一般] 或 [Gouraud] 陰影模式。</span><span class="sxs-lookup"><span data-stu-id="6f271-109">The following sample code examples illustrate how the current shading mode of a Direct3D application can be set to flat or Gouraud shading mode.</span></span>


```
// Set to flat shading.
// This code example assumes that pDev is a valid pointer to 
// an IDirect3DDevice9 interface.
hr = pDev->SetRenderState(D3DRS_SHADEMODE, D3DSHADE_FLAT);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}

// Set to Gouraud shading. This is the default for Direct3D.
hr = pDev->SetRenderState(D3DRS_SHADEMODE,
                            D3DSHADE_GOURAUD);
if(FAILED(hr))
{
    // Code to handle the error goes here.
}
```



## <a name="related-topics"></a><span data-ttu-id="6f271-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="6f271-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6f271-111">陰影</span><span class="sxs-lookup"><span data-stu-id="6f271-111">Shading</span></span>](shading.md)
</dt> </dl>

 

 
