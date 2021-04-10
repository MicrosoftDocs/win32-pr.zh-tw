---
description: 材質資源是一種結構化的資料集合。
ms.assetid: 4c716be8-044e-4ed4-aeca-4379440826bd
title: 建立 (Direct3D 10) 的材質資源
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 81f2ca200b566d17b02af56c48cb1227c41106ad
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936326"
---
# <a name="creating-texture-resources-direct3d-10"></a><span data-ttu-id="aa27d-103">建立 (Direct3D 10) 的材質資源</span><span class="sxs-lookup"><span data-stu-id="aa27d-103">Creating Texture Resources (Direct3D 10)</span></span>

<span data-ttu-id="aa27d-104">[材質](d3d10-graphics-programming-guide-resources-types.md)資源是一種結構化的資料集合。</span><span class="sxs-lookup"><span data-stu-id="aa27d-104">A [texture](d3d10-graphics-programming-guide-resources-types.md) resource is a structured collection of data.</span></span> <span data-ttu-id="aa27d-105">一般而言，色彩值會儲存在材質中，並在 [管線](d3d10-graphics-programming-guide-pipeline-stages.md) 于輸入和輸出的不同階段呈現時存取。</span><span class="sxs-lookup"><span data-stu-id="aa27d-105">Typically, color values are stored in textures and accessed during rendering by the [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) at various stages for both input and output.</span></span> <span data-ttu-id="aa27d-106">建立材質和定義其使用方式，是在 Direct3D 10 中呈現有趣外觀的重要部分。</span><span class="sxs-lookup"><span data-stu-id="aa27d-106">Creating textures and defining how they will be used is an important part of rendering interesting-looking scenes in Direct3D 10.</span></span>

<span data-ttu-id="aa27d-107">雖然材質通常包含色彩資訊，但使用不同的 [**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) 建立紋理可讓它們儲存不同類型的資料。</span><span class="sxs-lookup"><span data-stu-id="aa27d-107">Even though textures typically contain color information, creating textures using different [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format) enables them to store different kinds of data.</span></span> <span data-ttu-id="aa27d-108">如此一來，Direct3D 10 管線便可利用非傳統的方式來利用這項資料。</span><span class="sxs-lookup"><span data-stu-id="aa27d-108">This data can then be leveraged by the Direct3D 10 pipeline in non-traditional ways.</span></span>

<span data-ttu-id="aa27d-109">所有紋理都有其所耗用的記憶體數量，以及它們所包含的材質數目的限制。</span><span class="sxs-lookup"><span data-stu-id="aa27d-109">All textures have limits on how much memory they consume, and how many texels they contain.</span></span> <span data-ttu-id="aa27d-110">這些限制是由 [資源常數](d3d10-graphics-reference-resource-constants.md)指定。</span><span class="sxs-lookup"><span data-stu-id="aa27d-110">These limits are specified by [resource constants](d3d10-graphics-reference-resource-constants.md).</span></span>

-   [<span data-ttu-id="aa27d-111">從檔案建立材質</span><span class="sxs-lookup"><span data-stu-id="aa27d-111">Create a Texture from a File</span></span>](#create-a-texture-from-a-file)
    -   [<span data-ttu-id="aa27d-112">另外建立材質和視野</span><span class="sxs-lookup"><span data-stu-id="aa27d-112">Create Texture and View Separately</span></span>](#create-texture-and-view-separately)
    -   [<span data-ttu-id="aa27d-113">同時建立材質和視野</span><span class="sxs-lookup"><span data-stu-id="aa27d-113">Create Texture and View Simultaneously</span></span>](#create-texture-and-view-simultaneously)
-   [<span data-ttu-id="aa27d-114">建立空白紋理</span><span class="sxs-lookup"><span data-stu-id="aa27d-114">Creating Empty Textures</span></span>](#creating-empty-textures)
    -   [<span data-ttu-id="aa27d-115">轉譯成材質</span><span class="sxs-lookup"><span data-stu-id="aa27d-115">Rendering to a texture</span></span>](#rendering-to-a-texture)
    -   [<span data-ttu-id="aa27d-116">手動填入紋理</span><span class="sxs-lookup"><span data-stu-id="aa27d-116">Filling Textures Manually</span></span>](#filling-textures-manually)
-   [<span data-ttu-id="aa27d-117">多個 Rendertargets</span><span class="sxs-lookup"><span data-stu-id="aa27d-117">Multiple Rendertargets</span></span>](#multiple-rendertargets)
-   [<span data-ttu-id="aa27d-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="aa27d-118">Related topics</span></span>](#related-topics)

## <a name="create-a-texture-from-a-file"></a><span data-ttu-id="aa27d-119">從檔案建立材質</span><span class="sxs-lookup"><span data-stu-id="aa27d-119">Create a Texture from a File</span></span>

> [!Note]  
> <span data-ttu-id="aa27d-120">[D3DX 公用程式程式庫](d3d10-graphics-reference-d3dx10.md)已針對 Windows 8 淘汰，不支援 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="aa27d-120">The [D3DX utility library](d3d10-graphics-reference-d3dx10.md) is deprecated for Windows 8 and is not supported for Windows Store apps.</span></span>

 

<span data-ttu-id="aa27d-121">當您在 Direct3D 10 中建立材質時，您也需要建立一個 [view](d3d10-graphics-programming-guide-resources-access-views.md)。</span><span class="sxs-lookup"><span data-stu-id="aa27d-121">When you create a texture in Direct3D 10, you also need to create a [view](d3d10-graphics-programming-guide-resources-access-views.md).</span></span> <span data-ttu-id="aa27d-122">View 是一個物件，會告知裝置在轉譯期間應如何存取材質。</span><span class="sxs-lookup"><span data-stu-id="aa27d-122">A view is an object that tells the device how a texture should be accessed during rendering.</span></span> <span data-ttu-id="aa27d-123">存取材質最常見的方式是使用 [著色器](../direct3dhlsl/dx-graphics-hlsl.md)來讀取它。</span><span class="sxs-lookup"><span data-stu-id="aa27d-123">The most common way to access a texture is to read from it using a [shader](../direct3dhlsl/dx-graphics-hlsl.md).</span></span> <span data-ttu-id="aa27d-124">著色器資源檢視會告知著色器如何在轉譯期間讀取紋理。</span><span class="sxs-lookup"><span data-stu-id="aa27d-124">A shader-resource view will tell a shader how to read from a texture during rendering.</span></span> <span data-ttu-id="aa27d-125">當您建立材質時，必須指定材質的檢視類型。</span><span class="sxs-lookup"><span data-stu-id="aa27d-125">The kind of view a texture will use must be specified when you create it.</span></span>

<span data-ttu-id="aa27d-126">您可以透過兩種不同的方式來建立材質和載入其初始資料：個別建立材質和視圖，或是同時建立材質和視圖。</span><span class="sxs-lookup"><span data-stu-id="aa27d-126">Creating a texture and loading its initial data can be done in two different ways: create a texture and view separately, or create both the texture and the view at the same time.</span></span> <span data-ttu-id="aa27d-127">API 提供這兩種技術，讓您可以選擇更適合您的需求。</span><span class="sxs-lookup"><span data-stu-id="aa27d-127">The API provides both techniques so you can choose which better suits your needs.</span></span>

### <a name="create-texture-and-view-separately"></a><span data-ttu-id="aa27d-128">另外建立材質和視野</span><span class="sxs-lookup"><span data-stu-id="aa27d-128">Create Texture and View Separately</span></span>

<span data-ttu-id="aa27d-129">建立材質最簡單的方式，就是從影像檔載入它。</span><span class="sxs-lookup"><span data-stu-id="aa27d-129">The easiest way to create a texture is to load it from an image file.</span></span> <span data-ttu-id="aa27d-130">若要建立紋理，請只填妥一個結構，並將材質的名稱提供給 [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md)。</span><span class="sxs-lookup"><span data-stu-id="aa27d-130">To create the texture, just fill in one structure and provide the texture's name to [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md).</span></span>


```
ID3D10Device *pDevice = NULL;
// Initialize D3D10 device...

D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;

ID3D10Resource *pTexture = NULL;
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pTexture, NULL );
```



<span data-ttu-id="aa27d-131">D3DX 函式 [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) 會執行三件事：首先，它會建立 Direct3D 10 紋理物件;其次，它會讀取輸入影像檔案;第三，它會將影像資料儲存在材質物件中。</span><span class="sxs-lookup"><span data-stu-id="aa27d-131">The D3DX function [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) does three things: first, it creates a Direct3D 10 texture object; second, it reads the input image file; third, it stores the image data in the texture object.</span></span> <span data-ttu-id="aa27d-132">在上述範例中，會載入 BMP 檔案，但函數可以載入各種檔案類型。</span><span class="sxs-lookup"><span data-stu-id="aa27d-132">In the sample above, a BMP file is loaded, but the function can load a variety of file types.</span></span>

<span data-ttu-id="aa27d-133">系結旗標表示紋理將建立為著色器資源，可讓著色器階段在轉譯期間讀取紋理。</span><span class="sxs-lookup"><span data-stu-id="aa27d-133">The bind flag indicates the texture will be created as a shader resource which allows a shader stage to read from the texture during rendering.</span></span>

<span data-ttu-id="aa27d-134">上述範例未指定所有載入參數。</span><span class="sxs-lookup"><span data-stu-id="aa27d-134">The above example does not specify all of the loading parameters.</span></span> <span data-ttu-id="aa27d-135">事實上，直接將載入參數輸出為零很有説明，因為這可讓 D3DX 根據輸入影像選擇適當的值。</span><span class="sxs-lookup"><span data-stu-id="aa27d-135">In fact, it's often beneficial to simply zero out the loading parameters as this enables D3DX to choose appropriate values based on the input image.</span></span> <span data-ttu-id="aa27d-136">如果您希望輸入影像判斷材質建立時所使用的所有參數，只要針對 **loadInfo** 參數指定 **Null** 即可，如下所示：</span><span class="sxs-lookup"><span data-stu-id="aa27d-136">If you want the input image to determine all of the parameters the texture is created with, simply specify **NULL** for the **loadInfo** parameter like this:</span></span>


```
D3DX10CreateTextureFromFile( pDevice, L"sample.bmp", NULL, NULL, &pTexture, NULL );
```



<span data-ttu-id="aa27d-137">針對載入資訊指定 **Null** 是一個簡單但功能強大的快捷方式。</span><span class="sxs-lookup"><span data-stu-id="aa27d-137">Specifying **NULL** for the loading information is a simple yet powerful shortcut.</span></span>

<span data-ttu-id="aa27d-138">現在已建立紋理，您需要建立著色器資源的視圖，讓材質可以系結為著色器的輸入。</span><span class="sxs-lookup"><span data-stu-id="aa27d-138">Now that a texture has been created, you need to create a shader-resource view so that the texture can be bound as an input to a shader.</span></span> <span data-ttu-id="aa27d-139">由於 [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) 會傳回資源的指標，而不是紋理的指標，因此您必須判斷所載入的確切資源類型，然後您可以使用 [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview)來建立著色器資源檢視。</span><span class="sxs-lookup"><span data-stu-id="aa27d-139">Since [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) returns a pointer to a resource and not a pointer to a texture, you have to determine the exact type of resource that was loaded, and then you can create a shader-resource view using [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview).</span></span>


```
D3D10_SHADER_RESOURCE_VIEW_DESC srvDesc;
D3D10_RESOURCE_DIMENSION type;
pTexture->GetType( &type );
switch( type )
{
    case D3D10_RESOURCE_DIMENSION_BUFFER:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE1D:
    //...
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE2D:
    {
        D3D10_TEXTURE2D_DESC desc;
        ID3D10Texture2D *pTexture2D = (ID3D10Texture2D*)pTexture;
        pTexture2D->GetDesc( &desc );
        
        srvDesc.Format = desc.Format;
        srvDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
        srvDesc.Texture2D.MipLevels = desc.MipLevels;
        srvDesc.Texture2D.MostDetailedMip = desc.MipLevels -1;

    }
    break;
    case D3D10_RESOURCE_DIMENSION_TEXTURE3D:
    //...
    break;
    default:
    //...
    break;
}

ID3D10ShaderResourceView *pSRView = NULL;
pDevice->CreateShaderResourceView( pTexture, &srvDesc, &pSRView );
```



<span data-ttu-id="aa27d-140">雖然上述範例會建立2D 著色器資源檢視，但建立其他著色器資源檢視類型的程式碼非常相似。</span><span class="sxs-lookup"><span data-stu-id="aa27d-140">Although the above sample creates a 2D shader-resource view, the code to create other shader-resource view types is very similar.</span></span> <span data-ttu-id="aa27d-141">任何著色器階段現在都可以使用此材質做為輸入。</span><span class="sxs-lookup"><span data-stu-id="aa27d-141">Any shader stage can now use this texture as an input.</span></span>

<span data-ttu-id="aa27d-142">使用 [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) 和 [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview) 建立材質和其相關聯的視圖是準備材質系結至著色器階段的一種方式。</span><span class="sxs-lookup"><span data-stu-id="aa27d-142">Using [**D3DX10CreateTextureFromFile**](d3dx10createtexturefromfile.md) and [**CreateShaderResourceView**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-createshaderresourceview) to create a texture and its associated view is one way to prepare a texture to be bound to a shader stage.</span></span> <span data-ttu-id="aa27d-143">另一種方式是同時建立材質和其觀點，在下一節中將會討論。</span><span class="sxs-lookup"><span data-stu-id="aa27d-143">Another way to do so is to create both the texture and its view at the same time, which is discussed in the next section.</span></span>

### <a name="create-texture-and-view-simultaneously"></a><span data-ttu-id="aa27d-144">同時建立材質和視野</span><span class="sxs-lookup"><span data-stu-id="aa27d-144">Create Texture and View Simultaneously</span></span>

<span data-ttu-id="aa27d-145">Direct3D 10 同時需要材質和著色器資源檢視，才能在執行時間期間讀取材質。</span><span class="sxs-lookup"><span data-stu-id="aa27d-145">Direct3D 10 requires both a texture and a shader-resource view to read from a texture during runtime.</span></span> <span data-ttu-id="aa27d-146">由於建立材質和著色器資源檢視是很常見的工作，D3DX 會提供 [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) 來為您完成此作業。</span><span class="sxs-lookup"><span data-stu-id="aa27d-146">Since the creation of a texture and a shader-resource view is such a common task, D3DX provides the [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) to do it for you.</span></span>


```
D3DX10_IMAGE_LOAD_INFO loadInfo;
ZeroMemory( &loadInfo, sizeof(D3DX10_IMAGE_LOAD_INFO) );
loadInfo.BindFlags = D3D10_BIND_SHADER_RESOURCE;
loadInfo.Format = DXGI_FORMAT_BC1_UNORM;

ID3D10ShaderResourceView *pSRView = NULL;
D3DX10CreateShaderResourceViewFromFile( pDevice, L"sample.bmp", &loadInfo, NULL, &pSRView, NULL );
```



<span data-ttu-id="aa27d-147">使用單一 D3DX 呼叫時，會建立材質和著色器資源檢視。</span><span class="sxs-lookup"><span data-stu-id="aa27d-147">With a single D3DX call, both the texture and shader-resource view are created.</span></span> <span data-ttu-id="aa27d-148">**LoadInfo** 參數的功能未變更;您可以使用它來自訂材質的建立方式，或針對 **loadInfo** 參數指定 **Null** ，以從輸入檔衍生必要的參數。</span><span class="sxs-lookup"><span data-stu-id="aa27d-148">The functionality of the **loadInfo** parameter is unchanged; you can use it to customize how the texture is created, or derive the necessary parameters from the input file by specifying **NULL** for the **loadInfo** parameter.</span></span>

<span data-ttu-id="aa27d-149">[**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md)函數所傳回的 [**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)物件稍後可以用來取得原始 [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)介面（如有需要）。</span><span class="sxs-lookup"><span data-stu-id="aa27d-149">The [**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview) object returned by the [**D3DX10CreateShaderResourceViewFromFile**](d3dx10createshaderresourceviewfromfile.md) function can later be used to retrieve the original [**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource) interface if it is needed.</span></span> <span data-ttu-id="aa27d-150">這可以藉由呼叫 [**GetResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10view-getresource) 方法來完成。</span><span class="sxs-lookup"><span data-stu-id="aa27d-150">This can be done by calling the [**GetResource**](/windows/desktop/api/D3D10/nf-d3d10-id3d10view-getresource) method.</span></span>

<span data-ttu-id="aa27d-151">D3DX 提供單一函式，可將材質和著色器資源檢視建立為 convienience;您決定哪一種方法來建立材質和視野最適合您的應用程式需求。</span><span class="sxs-lookup"><span data-stu-id="aa27d-151">D3DX provides a single function to create a texture and shader-resource view as a convienience; it is up to you to decide which method of creating a texture and view best suits the needs of your application.</span></span>

<span data-ttu-id="aa27d-152">現在您已瞭解如何建立材質和其著色器資源檢視，下一節將示範如何使用著色器 (從該材質讀取) 。</span><span class="sxs-lookup"><span data-stu-id="aa27d-152">Now that you know how to create a texture and its shader-resource view, the next section will show you how you can sample (read) from that texture using a shader.</span></span>

## <a name="creating-empty-textures"></a><span data-ttu-id="aa27d-153">建立空白紋理</span><span class="sxs-lookup"><span data-stu-id="aa27d-153">Creating Empty Textures</span></span>

<span data-ttu-id="aa27d-154">有時候，應用程式會想要建立材質並計算要儲存在材質中的資料，或使用圖形 [管線](d3d10-graphics-programming-guide-pipeline-stages.md) 來轉譯成此材質，稍後再使用其他處理的結果。</span><span class="sxs-lookup"><span data-stu-id="aa27d-154">Sometimes applications will want to create a texture and compute the data to be stored in the texture, or use the graphics [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) to render to this texture and later use the results in other processing.</span></span> <span data-ttu-id="aa27d-155">圖形管線或應用程式本身可以更新這些紋理，這取決於建立時所指定的材質 [**使用**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) 類型。</span><span class="sxs-lookup"><span data-stu-id="aa27d-155">These textures could be updated by the graphics pipeline or by the application itself, depending on what kind of [**usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage) was specified for the texture when it was created.</span></span>

### <a name="rendering-to-a-texture"></a><span data-ttu-id="aa27d-156">轉譯成材質</span><span class="sxs-lookup"><span data-stu-id="aa27d-156">Rendering to a texture</span></span>

<span data-ttu-id="aa27d-157">在執行時間中建立空白紋理以填滿資料的最常見案例，就是應用程式想要轉譯成材質，然後在後續階段中使用轉譯作業的結果。</span><span class="sxs-lookup"><span data-stu-id="aa27d-157">The most common case of creating an empty texture to be filled with data during runtime is the case where an application wants to render to a texture and then use the results of the rendering operation in a subsequent pass.</span></span> <span data-ttu-id="aa27d-158">以此目的建立的材質應指定預設 [**使用**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage)方式。</span><span class="sxs-lookup"><span data-stu-id="aa27d-158">Textures created with this purpose should specify default [**usage**](/windows/desktop/api/D3D10/ne-d3d10-d3d10_usage).</span></span>

<span data-ttu-id="aa27d-159">下列程式碼範例會建立空的材質，讓管線可轉譯為，然後再作為 [著色器](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md)的輸入使用。</span><span class="sxs-lookup"><span data-stu-id="aa27d-159">The following code sample creates an empty texture that the pipeline can render to and subsequently use as an input to a [shader](../direct3dhlsl/dx-graphics-hlsl-using-shaders-10.md).</span></span>


```
// Create the render target texture
D3D10_TEXTURE2D_DESC desc;
ZeroMemory( &desc, sizeof(desc) );
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = 1;
desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R32G32B32A32_FLOAT;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DEFAULT;
desc.BindFlags = D3D10_BIND_RENDER_TARGET | D3D10_BIND_SHADER_RESOURCE;

ID3D10Texture2D *pRenderTarget = NULL;
pDevice->CreateTexture2D( &desc, NULL, &pRenderTarget );
```



<span data-ttu-id="aa27d-160">建立材質需要應用程式指定材質將擁有之屬性的一些相關資訊。</span><span class="sxs-lookup"><span data-stu-id="aa27d-160">Creating the texture requires the application to specify some information about the properties the texture will have.</span></span> <span data-ttu-id="aa27d-161">材質中材質的寬度和高度設定為256。</span><span class="sxs-lookup"><span data-stu-id="aa27d-161">The width and height of the texture in texels is set to 256.</span></span> <span data-ttu-id="aa27d-162">針對此轉譯目標，我們只需要一個 mipmap 層級。</span><span class="sxs-lookup"><span data-stu-id="aa27d-162">For this render target, a single mipmap level is all we need.</span></span> <span data-ttu-id="aa27d-163">只有一個轉譯目標是必要的，因此陣列大小設定為1。</span><span class="sxs-lookup"><span data-stu-id="aa27d-163">Only one render target is required so the array size is set to 1.</span></span> <span data-ttu-id="aa27d-164">每個材質都包含 4 32 位浮點值，可用來儲存非常精確的資訊 (查看 [**DXGI \_ 格式**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)) 。</span><span class="sxs-lookup"><span data-stu-id="aa27d-164">Each texel contains four 32-bit floating point values, which can be used to store very precise information (see [**DXGI\_FORMAT**](/windows/win32/api/dxgiformat/ne-dxgiformat-dxgi_format)).</span></span> <span data-ttu-id="aa27d-165">每個圖元都需要一個樣本。</span><span class="sxs-lookup"><span data-stu-id="aa27d-165">One sample per pixel is all that will be needed.</span></span> <span data-ttu-id="aa27d-166">使用方式會設定為 [預設]，因為這樣可讓轉譯目標在記憶體中最有效率的放置位置。</span><span class="sxs-lookup"><span data-stu-id="aa27d-166">The usage is set to default because this allows for the most efficient placement of the render target in memory.</span></span> <span data-ttu-id="aa27d-167">最後，紋理會系結為轉譯目標，並指定不同時間點的著色器資源。</span><span class="sxs-lookup"><span data-stu-id="aa27d-167">Finally, the fact that the texture will be bound as a render target and a shader resource at different points in time is specified.</span></span>

<span data-ttu-id="aa27d-168">紋理無法系結以直接轉譯為管線;使用呈現目標視圖，如下列程式碼範例所示。</span><span class="sxs-lookup"><span data-stu-id="aa27d-168">Textures cannot be bound for rendering to the pipeline directly; use a render-target view as shown in the following code sample.</span></span>


```
D3D10_RENDER_TARGET_VIEW_DESC rtDesc;
rtDesc.Format = desc.Format;
rtDesc.ViewDimension = D3D10_RTV_DIMENSION_TEXTURE2D;
rtDesc.Texture2D.MipSlice = 0;

ID3D10RenderTargetView *pRenderTargetView = NULL;
pDevice->CreateRenderTargetView( pRenderTarget, &rtDesc, &pRenderTargetView );
```



<span data-ttu-id="aa27d-169">轉譯目標視圖的格式只是設定為原始紋理的格式。</span><span class="sxs-lookup"><span data-stu-id="aa27d-169">The format of the render-target view is simply set to the format of the original texture.</span></span> <span data-ttu-id="aa27d-170">資源中的資訊應該被視為2D 材質，而我們只想要使用轉譯目標的第一個 mipmap 層級。</span><span class="sxs-lookup"><span data-stu-id="aa27d-170">The information in the resource should be interpreted as a 2D texture, and we only want to use the first mipmap level of the render target.</span></span>

<span data-ttu-id="aa27d-171">同樣地，您必須建立轉譯目標視圖，才能系結轉譯目標以輸出至管線，必須建立著色器資源檢視，才能將轉譯目標系結至管線做為輸入。</span><span class="sxs-lookup"><span data-stu-id="aa27d-171">Similarly to how a render-target view must be created so that the render target can be bound for output to the pipeline, a shader-resource view must be created so that the render target can be bound to the pipeline as an input.</span></span> <span data-ttu-id="aa27d-172">下列程式碼範例將示範這一點。</span><span class="sxs-lookup"><span data-stu-id="aa27d-172">The following code sample demonstrates this.</span></span>


```
// Create the shader-resource view
D3D10_SHADER_RESOURCE_VIEW_DESC srDesc;
srDesc.Format = desc.Format;
srDesc.ViewDimension = D3D10_SRV_DIMENSION_TEXTURE2D;
srDesc.Texture2D.MostDetailedMip = 0;
srDesc.Texture2D.MipLevels = 1;

ID3D10ShaderResourceView *pShaderResView = NULL;
pDevice->CreateShaderResourceView( pRenderTarget, &srDesc, &pShaderResView );
```



<span data-ttu-id="aa27d-173">著色器-資源檢視描述的參數與轉譯目標視圖描述的參數非常類似，而且基於相同的原因而被選擇。</span><span class="sxs-lookup"><span data-stu-id="aa27d-173">The parameters of shader-resource view descriptions are very similar to those of render-target view descriptions and were chosen for the same reasons.</span></span>

### <a name="filling-textures-manually"></a><span data-ttu-id="aa27d-174">手動填入紋理</span><span class="sxs-lookup"><span data-stu-id="aa27d-174">Filling Textures Manually</span></span>

<span data-ttu-id="aa27d-175">有時候應用程式會想要在執行時間計算值、手動將它們放入材質，然後讓圖形 [管線](d3d10-graphics-programming-guide-pipeline-stages.md) 在後續轉譯作業中使用此材質。</span><span class="sxs-lookup"><span data-stu-id="aa27d-175">Sometimes applications would like to compute values at runtime, put them into a texture manually and then have the graphics [pipeline](d3d10-graphics-programming-guide-pipeline-stages.md) use this texture in later rendering operations.</span></span> <span data-ttu-id="aa27d-176">若要這樣做，應用程式必須以允許 CPU 存取基礎記憶體的方式，建立空的材質。</span><span class="sxs-lookup"><span data-stu-id="aa27d-176">To do this, the application must create an empty texture in such a way to allow the CPU to access the underlying memory.</span></span> <span data-ttu-id="aa27d-177">這是藉由建立動態材質來完成，並藉由呼叫特定方法來取得基礎記憶體的存取權。</span><span class="sxs-lookup"><span data-stu-id="aa27d-177">This is done by creating a dynamic texture and gaining access to the underlying memory by calling a particular method.</span></span> <span data-ttu-id="aa27d-178">下列程式碼範例示範如何執行這項操作。</span><span class="sxs-lookup"><span data-stu-id="aa27d-178">The following code sample demonstrates how to do this.</span></span>


```
D3D10_TEXTURE2D_DESC desc;
desc.Width = 256;
desc.Height = 256;
desc.MipLevels = desc.ArraySize = 1;
desc.Format = DXGI_FORMAT_R8G8B8A8_UNORM;
desc.SampleDesc.Count = 1;
desc.Usage = D3D10_USAGE_DYNAMIC;
desc.BindFlags = D3D10_BIND_SHADER_RESOURCE;
desc.CPUAccessFlags = D3D10_CPU_ACCESS_WRITE;
ID3D10Texture2D *pTexture = NULL;
pd3dDevice->CreateTexture2D( &desc, NULL, &pTexture );
```



<span data-ttu-id="aa27d-179">請注意，格式設定為每圖元32位，其中每個元件都是由8個位定義。</span><span class="sxs-lookup"><span data-stu-id="aa27d-179">Note that the format is set to a 32 bits per pixel where each component is defined by 8 bits.</span></span> <span data-ttu-id="aa27d-180">使用方式參數設定為動態，而系結旗標設定為指定材質將由著色器存取。</span><span class="sxs-lookup"><span data-stu-id="aa27d-180">The usage parameter is set to dynamic while the bind flags are set to specify the texture will be accessed by a shader.</span></span> <span data-ttu-id="aa27d-181">材質描述的其餘部分類似于建立轉譯目標。</span><span class="sxs-lookup"><span data-stu-id="aa27d-181">The rest of the texture description is similar to creating a render target.</span></span>

<span data-ttu-id="aa27d-182">呼叫 [**對應**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) 可讓應用程式存取材質的基礎記憶體。</span><span class="sxs-lookup"><span data-stu-id="aa27d-182">Calling [**Map**](/windows/desktop/api/D3D10/nf-d3d10-id3d10texture2d-map) enables the application to access the underlying memory of the texture.</span></span> <span data-ttu-id="aa27d-183">然後，會使用已取出的指標來填滿具有資料的材質。</span><span class="sxs-lookup"><span data-stu-id="aa27d-183">The pointer retrieved is then used to fill the texture with data.</span></span> <span data-ttu-id="aa27d-184">這可以在下列程式碼範例中看到。</span><span class="sxs-lookup"><span data-stu-id="aa27d-184">This can be seen in the following code sample.</span></span>


```
D3D10_MAPPED_TEXTURE2D mappedTex;
pTexture->Map( D3D10CalcSubresource(0, 0, 1), D3D10_MAP_WRITE_DISCARD, 0, &mappedTex );

UCHAR* pTexels = (UCHAR*)mappedTex.pData;
for( UINT row = 0; row < desc.Height; row++ )
{
    UINT rowStart = row * mappedTex.RowPitch;
    for( UINT col = 0; col < desc.Width; col++ )
    {
        UINT colStart = col * 4;
        pTexels[rowStart + colStart + 0] = 255; // Red
        pTexels[rowStart + colStart + 1] = 128; // Green
        pTexels[rowStart + colStart + 2] = 64;  // Blue
        pTexels[rowStart + colStart + 3] = 32;  // Alpha
    }
}

pTexture->Unmap( D3D10CalcSubresource(0, 0, 1) );
```



## <a name="multiple-rendertargets"></a><span data-ttu-id="aa27d-185">多個 Rendertargets</span><span class="sxs-lookup"><span data-stu-id="aa27d-185">Multiple Rendertargets</span></span>

<span data-ttu-id="aa27d-186">使用 [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets))  (時，最多可以將8個轉譯目標視圖系結至管線。</span><span class="sxs-lookup"><span data-stu-id="aa27d-186">Up to eight render-target views can be bound to the pipeline at a time (with [**OMSetRenderTargets**](/windows/desktop/api/D3D10/nf-d3d10-id3d10device-omsetrendertargets)).</span></span> <span data-ttu-id="aa27d-187">針對每個圖元 (或每個範例，如果已啟用 [取樣]) ，則會針對每個轉譯目標視圖獨立進行混合。</span><span class="sxs-lookup"><span data-stu-id="aa27d-187">For each pixel (or each sample if multisampling is enabled), blending is done independently for each render-target view.</span></span> <span data-ttu-id="aa27d-188">其中兩個 blend 狀態變數（BlendEnable 和 RenderTargetWriteMask）是八陣列，每個陣列成員都對應到轉譯目標視圖。</span><span class="sxs-lookup"><span data-stu-id="aa27d-188">Two of the blend state variables - BlendEnable and RenderTargetWriteMask - are arrays of eight, each array member corresponds to a render-target view.</span></span> <span data-ttu-id="aa27d-189">使用多個呈現目標時，每個轉譯目標都必須是相同的 [資源類型](d3d10-graphics-programming-guide-resources-types.md) (緩衝區、1d 材質、2d 材質陣列等 ) ，而且必須具有相同的維度 (寬度、高度、3d 紋理的深度，以及紋理陣列的陣列大小) 。</span><span class="sxs-lookup"><span data-stu-id="aa27d-189">When using multiple render targets, each render target must be the same [resource type](d3d10-graphics-programming-guide-resources-types.md) (buffer, 1D texture, 2D texture array, etc.) and must have the same dimension (width, height, depth for 3D textures, and array size for texture arrays).</span></span> <span data-ttu-id="aa27d-190">如果呈現目標是多重取樣，則它們的每個圖元都必須有相同的樣本數目。</span><span class="sxs-lookup"><span data-stu-id="aa27d-190">If the render targets are multisampled, then they must all have the same number of samples per pixel.</span></span>

<span data-ttu-id="aa27d-191">不論使用中的轉譯目標數目為何，都只能有一個作用中的深度樣板緩衝區為啟用狀態。</span><span class="sxs-lookup"><span data-stu-id="aa27d-191">There can only be one depth-stencil buffer active, regardless of how many render targets are active.</span></span> <span data-ttu-id="aa27d-192">使用紋理陣列做為轉譯目標時，所有視圖維度都必須相符。</span><span class="sxs-lookup"><span data-stu-id="aa27d-192">When using texture arrays as render targets, all view dimensions must match.</span></span> <span data-ttu-id="aa27d-193">轉譯目標不需要具有相同的材質格式。</span><span class="sxs-lookup"><span data-stu-id="aa27d-193">The render targets do not need to have the same texture format.</span></span>

## <a name="related-topics"></a><span data-ttu-id="aa27d-194">相關主題</span><span class="sxs-lookup"><span data-stu-id="aa27d-194">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="aa27d-195"> (Direct3D 10) 的資源 </span><span class="sxs-lookup"><span data-stu-id="aa27d-195">Resources (Direct3D 10)</span></span>](d3d10-graphics-programming-guide-resources.md)
</dt> </dl>

 

 
