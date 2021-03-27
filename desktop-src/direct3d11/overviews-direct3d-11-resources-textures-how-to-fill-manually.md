---
title: 如何以程式設計方式初始化材質
description: 本主題包含數個範例，示範如何初始化使用不同類型的使用方式所建立的材質。
ms.assetid: 65e8ae82-50aa-4303-853e-3457da18f44f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5584885b885f6026ee32a3e4c52a24aad78c3c08
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840308"
---
# <a name="how-to-initialize-a-texture-programmatically"></a><span data-ttu-id="3de0d-103">如何：以程式設計方式初始化材質</span><span class="sxs-lookup"><span data-stu-id="3de0d-103">How to: Initialize a Texture Programmatically</span></span>

<span data-ttu-id="3de0d-104">您可以在物件建立期間初始化材質，也可以在建立物件之後，以程式設計的方式填入該物件。</span><span class="sxs-lookup"><span data-stu-id="3de0d-104">You can initialize a texture during object creation, or you can fill the object programmatically after it is created.</span></span> <span data-ttu-id="3de0d-105">本主題包含數個範例，示範如何初始化使用不同類型的使用方式所建立的材質。</span><span class="sxs-lookup"><span data-stu-id="3de0d-105">This topic has several examples showing how to initialize textures that are created with different types of usages.</span></span> <span data-ttu-id="3de0d-106">此範例假設您已經知道如何 [建立材質](overviews-direct3d-11-resources-textures-create.md)。</span><span class="sxs-lookup"><span data-stu-id="3de0d-106">This example assumes you already know how to [Create a Texture](overviews-direct3d-11-resources-textures-create.md).</span></span>

-   [<span data-ttu-id="3de0d-107">預設使用方式</span><span class="sxs-lookup"><span data-stu-id="3de0d-107">Default Usage</span></span>](#default-usage)
-   [<span data-ttu-id="3de0d-108">動態使用方式</span><span class="sxs-lookup"><span data-stu-id="3de0d-108">Dynamic Usage</span></span>](#dynamic-usage)
-   [<span data-ttu-id="3de0d-109">暫存使用量</span><span class="sxs-lookup"><span data-stu-id="3de0d-109">Staging Usage</span></span>](#staging-usage)
-   [<span data-ttu-id="3de0d-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="3de0d-110">Related topics</span></span>](#related-topics)

## <a name="default-usage"></a><span data-ttu-id="3de0d-111">預設使用方式</span><span class="sxs-lookup"><span data-stu-id="3de0d-111">Default Usage</span></span>

<span data-ttu-id="3de0d-112">最常見的使用類型是預設使用方式。</span><span class="sxs-lookup"><span data-stu-id="3de0d-112">The most common type of usage is default usage.</span></span> <span data-ttu-id="3de0d-113">若要填滿預設材質 (使用 **D3D11 \_ \_ 預設值** 建立的材質) 您可以：</span><span class="sxs-lookup"><span data-stu-id="3de0d-113">To fill a default texture (one created with **D3D11\_USAGE\_DEFAULT**) you can either:</span></span>

-   <span data-ttu-id="3de0d-114">呼叫 [**ID3D11Device：： CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) 並初始化 *pInitialData* ，以指向應用程式所提供的資料。</span><span class="sxs-lookup"><span data-stu-id="3de0d-114">Call [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d) and initialize *pInitialData* to point to data provided from an application.</span></span>

    <span data-ttu-id="3de0d-115">或</span><span class="sxs-lookup"><span data-stu-id="3de0d-115">or</span></span>

-   <span data-ttu-id="3de0d-116">呼叫 [**ID3D11Device：： CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d)之後，請使用 [**>id3d11devicecoNtext：： UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) ，將來自應用程式所提供之指標的資料填入預設材質。</span><span class="sxs-lookup"><span data-stu-id="3de0d-116">After calling [**ID3D11Device::CreateTexture2D**](/windows/desktop/api/D3D11/nf-d3d11-id3d11device-createtexture2d), use [**ID3D11DeviceContext::UpdateSubresource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-updatesubresource) to fill the default texture with data from a pointer provided by the application.</span></span>

## <a name="dynamic-usage"></a><span data-ttu-id="3de0d-117">動態使用方式</span><span class="sxs-lookup"><span data-stu-id="3de0d-117">Dynamic Usage</span></span>

<span data-ttu-id="3de0d-118">若要填滿動態材質 (使用 **\_ \_ 動態** 材質建立的) ：</span><span class="sxs-lookup"><span data-stu-id="3de0d-118">To fill a dynamic texture (one created with **D3D11\_USAGE\_DYNAMIC**):</span></span>

1.  <span data-ttu-id="3de0d-119">藉由在呼叫 [**>id3d11devicecoNtext：： MAP**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)時傳遞 **D3D11 \_ 對應 \_ 寫入 \_ 捨棄**，來取得材質記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="3de0d-119">Get a pointer to the texture memory by passing in **D3D11\_MAP\_WRITE\_DISCARD** when calling [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span></span>
2.  <span data-ttu-id="3de0d-120">將資料寫入記憶體。</span><span class="sxs-lookup"><span data-stu-id="3de0d-120">Write data to the memory.</span></span>
3.  <span data-ttu-id="3de0d-121">當您完成寫入資料時，請呼叫 [**>id3d11devicecoNtext：：**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) 取消對應。</span><span class="sxs-lookup"><span data-stu-id="3de0d-121">Call [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) when you are finished writing data.</span></span>

## <a name="staging-usage"></a><span data-ttu-id="3de0d-122">暫存使用量</span><span class="sxs-lookup"><span data-stu-id="3de0d-122">Staging Usage</span></span>

<span data-ttu-id="3de0d-123">若要填入預備材質 (使用 **D3D11 \_ 使用量 \_ 暫存**) 建立一個：</span><span class="sxs-lookup"><span data-stu-id="3de0d-123">To fill a staging texture (one created with **D3D11\_USAGE\_STAGING**):</span></span>

1.  <span data-ttu-id="3de0d-124">在呼叫 [**>id3d11devicecoNtext：： MAP**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map)時傳遞 **D3D11 \_ MAP \_ WRITE** ，以取得紋理記憶體的指標。</span><span class="sxs-lookup"><span data-stu-id="3de0d-124">Get a pointer to the texture memory by passing in **D3D11\_MAP\_WRITE** when calling [**ID3D11DeviceContext::Map**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-map).</span></span>
2.  <span data-ttu-id="3de0d-125">將資料寫入記憶體。</span><span class="sxs-lookup"><span data-stu-id="3de0d-125">Write data to the memory.</span></span>
3.  <span data-ttu-id="3de0d-126">當您完成寫入資料時，請呼叫 [**>id3d11devicecoNtext：：**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) 取消對應。</span><span class="sxs-lookup"><span data-stu-id="3de0d-126">Call [**ID3D11DeviceContext::Unmap**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-unmap) when you are finished writing data.</span></span>

<span data-ttu-id="3de0d-127">接下來可以使用預備紋理作為 [**>id3d11devicecoNtext：： CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) 或 [**>id3d11devicecoNtext：： CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) 的來源參數，以填滿預設或動態的資源。</span><span class="sxs-lookup"><span data-stu-id="3de0d-127">A staging texture can then be used as the source parameter to [**ID3D11DeviceContext::CopyResource**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copyresource) or [**ID3D11DeviceContext::CopySubresourceRegion**](/windows/desktop/api/D3D11/nf-d3d11-id3d11devicecontext-copysubresourceregion) to fill a default or dynamic resource.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3de0d-128">相關主題</span><span class="sxs-lookup"><span data-stu-id="3de0d-128">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3de0d-129">如何使用 Direct3D 11</span><span class="sxs-lookup"><span data-stu-id="3de0d-129">How to Use Direct3D 11</span></span>](how-to-use-direct3d-11.md)
</dt> <dt>

[<span data-ttu-id="3de0d-130">紋理</span><span class="sxs-lookup"><span data-stu-id="3de0d-130">Textures</span></span>](overviews-direct3d-11-resources-textures.md)
</dt> </dl>

 

 




