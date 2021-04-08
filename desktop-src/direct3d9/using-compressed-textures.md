---
description: 使用 (Direct3D 9) 的壓縮紋理
ms.assetid: 60892a8b-93f4-43ba-87ef-d5c7cc6fb8c6
title: 使用 (Direct3D 9) 的壓縮紋理
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 643b0618043f12ff3e1a84b806c86edb780ad929
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103688479"
---
# <a name="using-compressed-textures-direct3d-9"></a><span data-ttu-id="312de-103">使用 (Direct3D 9) 的壓縮紋理</span><span class="sxs-lookup"><span data-stu-id="312de-103">Using Compressed Textures (Direct3D 9)</span></span>

## <a name="determining-support-for-compressed-textures"></a><span data-ttu-id="312de-104">判斷支援壓縮的材質</span><span class="sxs-lookup"><span data-stu-id="312de-104">Determining Support for Compressed Textures</span></span>

<span data-ttu-id="312de-105">若要測試介面卡，請指定任何使用 DXT1、DXT2、DXT3、DXT4 或 DXT5 的像素格式。</span><span class="sxs-lookup"><span data-stu-id="312de-105">To test the adapter, specify any pixel format that uses the DXT1, DXT2, DXT3, DXT4, or DXT5.</span></span> <span data-ttu-id="312de-106">如果 [**IDirect3D9：： CheckDeviceFormat**](/windows/desktop/api) 傳回 D3D \_ OK，則裝置可以直接從使用該格式的壓縮紋理介面建立紋理。</span><span class="sxs-lookup"><span data-stu-id="312de-106">If [**IDirect3D9::CheckDeviceFormat**](/windows/desktop/api) returns D3D\_OK, the device can create texture directly from a compressed texture surface that uses that format.</span></span> <span data-ttu-id="312de-107">若是如此，您可以藉由呼叫 [**IDirect3DDevice9：： SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 方法，直接透過 Direct3D 使用壓縮的材質介面。</span><span class="sxs-lookup"><span data-stu-id="312de-107">If so, you can use compressed texture surfaces directly with Direct3D by calling the [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) method.</span></span> <span data-ttu-id="312de-108">下列程式碼範例顯示如何判斷介面卡是否支援壓縮的材質格式。</span><span class="sxs-lookup"><span data-stu-id="312de-108">The following code example shows how to determine if the adapter supports a compressed texture format.</span></span>


```
BOOL IsCompressedTextureFormatOk( D3DFORMAT TextureFormat, 
                                  D3DFORMAT AdapterFormat ) 
{
    HRESULT hr = pD3D->CheckDeviceFormat( D3DADAPTER_DEFAULT,
                                          D3DDEVTYPE_HAL,
                                          AdapterFormat,
                                          0,
                                          D3DRTYPE_TEXTURE,
                                          TextureFormat);

    return SUCCEEDED( hr );
}
```



<span data-ttu-id="312de-109">如果裝置不支援從壓縮的材質表面進行紋理，您仍然可以將材質資料儲存為壓縮格式介面，但您必須先將任何壓縮紋理轉換成支援的格式，才能將其用於紋理。</span><span class="sxs-lookup"><span data-stu-id="312de-109">If the device does not support texturing from compressed texture surfaces, you can still store texture data in a compressed format surface, but you must convert any compressed textures to a supported format before they can be used for texturing.</span></span>

## <a name="creating-compressed-textures"></a><span data-ttu-id="312de-110">建立壓縮的材質</span><span class="sxs-lookup"><span data-stu-id="312de-110">Creating Compressed Textures</span></span>

<span data-ttu-id="312de-111">在介面卡上建立支援壓縮材質格式的裝置之後，您就可以建立壓縮的材質資源。</span><span class="sxs-lookup"><span data-stu-id="312de-111">After creating a device that supports a compressed texture format on the adapter, you can create a compressed texture resource.</span></span> <span data-ttu-id="312de-112">呼叫 [**IDirect3DDevice9：： CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) ，並針對 format 參數指定壓縮的材質格式。</span><span class="sxs-lookup"><span data-stu-id="312de-112">Call [**IDirect3DDevice9::CreateTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-createtexture) and specify a compressed texture format for the Format parameter.</span></span>

<span data-ttu-id="312de-113">將影像載入材質物件之前，請呼叫 [**IDirect3DTexture9：： GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) 方法，以取出紋理介面的指標。</span><span class="sxs-lookup"><span data-stu-id="312de-113">Before loading an image into a texture object, retrieve a pointer to the texture surface by calling the [**IDirect3DTexture9::GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel) method.</span></span>

<span data-ttu-id="312de-114">現在您可以使用任何 D3DXLoadSurfacexxx 函式，將影像載入至使用 [**IDirect3DTexture9：： GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel)所抓取的介面。</span><span class="sxs-lookup"><span data-stu-id="312de-114">Now you can use any D3DXLoadSurfacexxx function to load an image to the surface that was retrieved by using [**IDirect3DTexture9::GetSurfaceLevel**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3dtexture9-getsurfacelevel).</span></span> <span data-ttu-id="312de-115">這些函式會處理壓縮材質格式的轉換。</span><span class="sxs-lookup"><span data-stu-id="312de-115">These functions handle conversion to and from compressed texture formats.</span></span>

<span data-ttu-id="312de-116">您可以使用 [DirectX 材質編輯器] (Dxtex.exe) 隨附于 DirectX SDK，來建立和轉換壓縮的材質 (DDS) 檔。</span><span class="sxs-lookup"><span data-stu-id="312de-116">You can create and convert compressed texture (DDS) files using the DirectX Texture Editor (Dxtex.exe) supplied with the DirectX SDK.</span></span> <span data-ttu-id="312de-117">您可以從 DirectX SDK 取得 Dxtex.exe 並瞭解它的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="312de-117">You can get Dxtex.exe and learn about it from the DirectX SDK.</span></span> <span data-ttu-id="312de-118">如需有關 DirectX SDK 的資訊，請參閱 [什麼是 DIRECTX sdk？](../directx-sdk--august-2009-.md)。</span><span class="sxs-lookup"><span data-stu-id="312de-118">For info about the DirectX SDK, see [Where is the DirectX SDK?](../directx-sdk--august-2009-.md).</span></span>

<span data-ttu-id="312de-119">這種行為的優點是，應用程式可以將壓縮表面的內容複寫到檔案中，而不需要計算特定格式的特定寬度和高度的介面需要多少儲存空間。</span><span class="sxs-lookup"><span data-stu-id="312de-119">The advantage of this behavior is that an application can copy the contents of a compressed surface to a file without calculating how much storage is required for a surface of a particular width and height in the specific format.</span></span>

<span data-ttu-id="312de-120">下表顯示五種類型的壓縮紋理。</span><span class="sxs-lookup"><span data-stu-id="312de-120">The following table shows the five types of compressed textures.</span></span> <span data-ttu-id="312de-121">如需有關如何儲存資料的詳細資訊，請參閱 [ (Direct3D 9) 壓縮的材質格式 ](compressed-texture-formats.md)。</span><span class="sxs-lookup"><span data-stu-id="312de-121">For more information about how the data is stored, see [Compressed Texture Formats (Direct3D 9)](compressed-texture-formats.md).</span></span> <span data-ttu-id="312de-122">如果您要撰寫自己的壓縮常式，則只需要此資訊。</span><span class="sxs-lookup"><span data-stu-id="312de-122">You only need this information if you are writing your own compression routines.</span></span>



| <span data-ttu-id="312de-123">FOURCC</span><span class="sxs-lookup"><span data-stu-id="312de-123">FOURCC</span></span> | <span data-ttu-id="312de-124">Description</span><span class="sxs-lookup"><span data-stu-id="312de-124">Description</span></span>        | <span data-ttu-id="312de-125">Alpha 預乘？</span><span class="sxs-lookup"><span data-stu-id="312de-125">Alpha premultiplied?</span></span> |
|--------|--------------------|----------------------|
| <span data-ttu-id="312de-126">DXT1</span><span class="sxs-lookup"><span data-stu-id="312de-126">DXT1</span></span>   | <span data-ttu-id="312de-127">不透明/1 位 Alpha</span><span class="sxs-lookup"><span data-stu-id="312de-127">Opaque/1-bit alpha</span></span> | <span data-ttu-id="312de-128">N/A</span><span class="sxs-lookup"><span data-stu-id="312de-128">N/A</span></span>                  |
| <span data-ttu-id="312de-129">DXT2</span><span class="sxs-lookup"><span data-stu-id="312de-129">DXT2</span></span>   | <span data-ttu-id="312de-130">明確 Alpha</span><span class="sxs-lookup"><span data-stu-id="312de-130">Explicit alpha</span></span>     | <span data-ttu-id="312de-131">Yes</span><span class="sxs-lookup"><span data-stu-id="312de-131">Yes</span></span>                  |
| <span data-ttu-id="312de-132">DXT3</span><span class="sxs-lookup"><span data-stu-id="312de-132">DXT3</span></span>   | <span data-ttu-id="312de-133">明確 Alpha</span><span class="sxs-lookup"><span data-stu-id="312de-133">Explicit alpha</span></span>     | <span data-ttu-id="312de-134">No</span><span class="sxs-lookup"><span data-stu-id="312de-134">No</span></span>                   |
| <span data-ttu-id="312de-135">DXT4</span><span class="sxs-lookup"><span data-stu-id="312de-135">DXT4</span></span>   | <span data-ttu-id="312de-136">插補 Alpha</span><span class="sxs-lookup"><span data-stu-id="312de-136">Interpolated alpha</span></span> | <span data-ttu-id="312de-137">Yes</span><span class="sxs-lookup"><span data-stu-id="312de-137">Yes</span></span>                  |
| <span data-ttu-id="312de-138">DXT5</span><span class="sxs-lookup"><span data-stu-id="312de-138">DXT5</span></span>   | <span data-ttu-id="312de-139">插補 Alpha</span><span class="sxs-lookup"><span data-stu-id="312de-139">Interpolated alpha</span></span> | <span data-ttu-id="312de-140">No</span><span class="sxs-lookup"><span data-stu-id="312de-140">No</span></span>                   |



 

<span data-ttu-id="312de-141">當您將資料從 nonpremultiplied 格式傳送到預先設置的格式時，Direct3D 會根據 Alpha 值調整色彩。</span><span class="sxs-lookup"><span data-stu-id="312de-141">When you transfer data from a nonpremultiplied format to a premultiplied format, Direct3D scales the colors based on the alpha values.</span></span> <span data-ttu-id="312de-142">不支援將資料從預乘格式傳送至 nonpremultiplied 格式。</span><span class="sxs-lookup"><span data-stu-id="312de-142">Transferring data from a premultiplied format to a nonpremultiplied format is not supported.</span></span> <span data-ttu-id="312de-143">如果您嘗試將資料從預乘的 Alpha 來源傳送至 nonpremultiplied Alpha 目的地，則此方法會傳回 D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="312de-143">If you try to transfer data from a premultiplied alpha source to a nonpremultiplied alpha destination, the method returns D3DERR\_INVALIDCALL.</span></span> <span data-ttu-id="312de-144">如果您將資料從預乘的 Alpha 來源傳送至沒有 Alpha 的目的地，則會依原樣複製來源色彩元件（已透過 Alpha 調整）。</span><span class="sxs-lookup"><span data-stu-id="312de-144">If you transfer data from a premultiplied alpha source to a destination that has no alpha, the source color components, which have been scaled by alpha, are copied as is.</span></span>

## <a name="decompressing-compressed-texture-surfaces"></a><span data-ttu-id="312de-145">解壓縮壓縮的材質表面</span><span class="sxs-lookup"><span data-stu-id="312de-145">Decompressing Compressed Texture Surfaces</span></span>

<span data-ttu-id="312de-146">就像壓縮材質介面一樣，解壓縮壓縮的材質是透過 Direct3D 複製服務來執行。</span><span class="sxs-lookup"><span data-stu-id="312de-146">As with compressing a texture surface, decompressing a compressed texture is performed through Direct3D copying services.</span></span>

<span data-ttu-id="312de-147">若要將壓縮的材質介面複製到未壓縮的材質介面，請使用函數 [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md)。</span><span class="sxs-lookup"><span data-stu-id="312de-147">To copy a compressed texture surface to a uncompressed texture surface, use the function [**D3DXLoadSurfaceFromSurface**](d3dxloadsurfacefromsurface.md).</span></span> <span data-ttu-id="312de-148">此函式會處理壓縮和未壓縮表面的壓縮。</span><span class="sxs-lookup"><span data-stu-id="312de-148">This functions handles compression to and from compressed and uncompressed surfaces.</span></span>

## <a name="related-topics"></a><span data-ttu-id="312de-149">相關主題</span><span class="sxs-lookup"><span data-stu-id="312de-149">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="312de-150">壓縮的材質資源</span><span class="sxs-lookup"><span data-stu-id="312de-150">Compressed Texture Resources</span></span>](compressed-texture-resources.md)
</dt> </dl>

 

 
