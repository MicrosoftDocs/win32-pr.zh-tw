---
title: 針對 In-Place 影像編輯解壓縮和封裝 DXGI_FORMAT
description: D3DX \_ DXGIFormatConvert. .inl 檔案包含內嵌格式轉換函式，您可以在 Direct3D 11 硬體上的計算著色器或圖元著色器中使用這些函數。
ms.assetid: 328c4488-9758-4359-a37b-ac50f20e2940
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 04f3729bbeda5b0677da9d52e595e621523ff2d1
ms.sourcegitcommit: 0e611cdff84ff9f897c59e4e1d2b2d134bc4e133
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/02/2021
ms.locfileid: "106979642"
---
# <a name="unpacking-and-packing-dxgi_format-for-in-place-image-editing"></a><span data-ttu-id="a5657-103">\_針對 In-Place 影像編輯解壓縮和封裝 DXGI 格式</span><span class="sxs-lookup"><span data-stu-id="a5657-103">Unpacking and Packing DXGI\_FORMAT for In-Place Image Editing</span></span>

<span data-ttu-id="a5657-104">D3DX \_ DXGIFormatConvert. .inl 檔案包含內嵌格式轉換函式，您可以在 Direct3D 11 硬體上的計算著色器或圖元著色器中使用這些函數。</span><span class="sxs-lookup"><span data-stu-id="a5657-104">The D3DX\_DXGIFormatConvert.inl file contains inline format conversion functions that you can use in the compute shader or pixel shader on Direct3D 11 hardware.</span></span> <span data-ttu-id="a5657-105">您可以在應用程式中使用這些函式，同時讀取和寫入材質。</span><span class="sxs-lookup"><span data-stu-id="a5657-105">You can use these functions in your application to simultaneously both read from and write to a texture.</span></span> <span data-ttu-id="a5657-106">也就是說，您可以執行就地影像編輯。</span><span class="sxs-lookup"><span data-stu-id="a5657-106">That is, you can perform in-place image editing.</span></span> <span data-ttu-id="a5657-107">若要使用這些內嵌格式轉換函式，請將 D3DX \_ DXGIFormatConvert. .inl 檔案包含在您的應用程式中。</span><span class="sxs-lookup"><span data-stu-id="a5657-107">To use these inline format conversion functions, include the D3DX\_DXGIFormatConvert.inl file in your application.</span></span>

> <span data-ttu-id="a5657-108">D3DX \_ DXGIFormatConvert. .inl 標頭隨附于舊版 DIRECTX SDK 中。</span><span class="sxs-lookup"><span data-stu-id="a5657-108">The D3DX\_DXGIFormatConvert.inl header ships in the legacy DirectX SDK.</span></span> <span data-ttu-id="a5657-109">它也包含在 [DXSDK. D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet 套件中。</span><span class="sxs-lookup"><span data-stu-id="a5657-109">It is also included in the [Microsoft.DXSDK.D3DX](https://www.nuget.org/packages/Microsoft.DXSDK.D3DX) NuGet package.</span></span>

<span data-ttu-id="a5657-110">Direct3D 11 的未排序存取視圖 (UAV) 的 Texture1D、Texture2D 或 Texture3D 資源支援從計算著色器或圖元著色器隨機存取讀取和寫入記憶體。</span><span class="sxs-lookup"><span data-stu-id="a5657-110">Direct3D 11's Unordered Access View (UAV) of a Texture1D, Texture2D, or Texture3D resource supports random access reads and writes to memory from a compute shader or pixel shader.</span></span> <span data-ttu-id="a5657-111">不過，Direct3D 11 同時支援讀取和寫入僅限 DXGI \_ 格式的 \_ R32 \_ UINT 材質格式。</span><span class="sxs-lookup"><span data-stu-id="a5657-111">However, Direct3D 11 supports simultaneously both reading from and writing to only the DXGI\_FORMAT\_R32\_UINT texture format.</span></span> <span data-ttu-id="a5657-112">例如，Direct3D 11 不支援同時讀取和寫入其他更實用的格式，例如 DXGI \_ FORMAT \_ R8G8B8A8 \_ UNORM。</span><span class="sxs-lookup"><span data-stu-id="a5657-112">For example, Direct3D 11 does not support simultaneously both reading from and writing to other, more useful formats, such as DXGI\_FORMAT\_R8G8B8A8\_UNORM.</span></span> <span data-ttu-id="a5657-113">您只能使用 UAV 來隨機寫入這類其他格式，也可以只使用著色器資源檢視 (SRV) 從這類其他格式讀取隨機存取。</span><span class="sxs-lookup"><span data-stu-id="a5657-113">You can use only a UAV to random access write to such other formats, or you can use only a Shader Resource View (SRV) to random access read from such other formats.</span></span> <span data-ttu-id="a5657-114">格式轉換硬體無法同時從這類其他格式讀取和寫入。</span><span class="sxs-lookup"><span data-stu-id="a5657-114">Format conversion hardware is not available to simultaneously both read from and write to such other formats.</span></span>

<span data-ttu-id="a5657-115">不過，您仍然可以同時讀取和寫入這類其他格式，方法是在建立 UAV 時將材質轉換成 DXGI \_ 格式 \_ R32 \_ UINT 材質格式，只要資源的原始格式支援轉換成 dxgi \_ 格式 \_ R32 \_ UINT 即可。</span><span class="sxs-lookup"><span data-stu-id="a5657-115">However, you can still simultaneously both read from and write to such other formats by casting the texture to the DXGI\_FORMAT\_R32\_UINT texture format when you create a UAV, as long as the original format of the resource supports casting to DXGI\_FORMAT\_R32\_UINT.</span></span> <span data-ttu-id="a5657-116">最多32位的每個元素格式都支援轉換成 DXGI \_ 格式 \_ \_ 的 R32 UINT。</span><span class="sxs-lookup"><span data-stu-id="a5657-116">Most 32 bit per element formats support casting to DXGI\_FORMAT\_R32\_UINT.</span></span> <span data-ttu-id="a5657-117">\_ \_ 當您建立 UAV 時，將材質轉換成 DXGI 格式 R32 \_ UINT 材質格式時，只要著色器在讀取和封裝上執行手動格式化解壓縮，就可以同時執行讀取和寫入至材質。</span><span class="sxs-lookup"><span data-stu-id="a5657-117">By casting the texture to the DXGI\_FORMAT\_R32\_UINT texture format when you create a UAV, you can then simultaneous perform reads and writes to the texture as long as the shader performs manual format unpacking on read and packing on write.</span></span>

<span data-ttu-id="a5657-118">將材質轉換成 DXGI \_ 格式 \_ R32 \_ UINT 材質格式的優點是，您稍後可以使用適當的格式 (例如， \_ [DXGI 格式] \_ R16G16 \_ FLOAT) 與相同材質上的其他視圖，例如轉譯目標視圖 (RTVs) 或 SRVs。</span><span class="sxs-lookup"><span data-stu-id="a5657-118">The benefit of casting the texture to the DXGI\_FORMAT\_R32\_UINT texture format is that later on you can use the appropriate format (for example, DXGI\_FORMAT\_R16G16\_FLOAT) with other views on the same texture, such as Render Target Views (RTVs) or SRVs.</span></span> <span data-ttu-id="a5657-119">因此，硬體可以執行一般的自動格式化解壓縮和套件、可以執行材質篩選，而不會有硬體限制。</span><span class="sxs-lookup"><span data-stu-id="a5657-119">Therefore, the hardware can perform the typical automatic format unpack and pack, can perform texture filtering, and so on where there are no hardware limitations.</span></span>

<span data-ttu-id="a5657-120">下列案例要求應用程式採取下列動作順序來就地進行影像編輯。</span><span class="sxs-lookup"><span data-stu-id="a5657-120">The following scenario requires that an application take the following sequence of actions to perform in-place image editing.</span></span>

<span data-ttu-id="a5657-121">假設您想要設定材質，讓您可以使用圖元著色器或計算著色器來執行就地編輯，而您想要將材質資料儲存為下列其中一種無類型格式的子系格式：</span><span class="sxs-lookup"><span data-stu-id="a5657-121">Suppose you want to make a texture on which you can use a pixel shader or compute shader to perform in-place editing, and you want the texture data to be stored in a format that is a descendant of one of the following TYPELESS formats:</span></span>

-   <span data-ttu-id="a5657-122">DXGI \_ 格式 \_ R10G10B10A2 無別 \_</span><span class="sxs-lookup"><span data-stu-id="a5657-122">DXGI\_FORMAT\_R10G10B10A2\_TYPELESS</span></span>
-   <span data-ttu-id="a5657-123">DXGI \_ 格式 \_ R8G8B8A8 無別 \_</span><span class="sxs-lookup"><span data-stu-id="a5657-123">DXGI\_FORMAT\_R8G8B8A8\_TYPELESS</span></span>
-   <span data-ttu-id="a5657-124">DXGI \_ 格式 \_ B8G8R8A8 無別 \_</span><span class="sxs-lookup"><span data-stu-id="a5657-124">DXGI\_FORMAT\_B8G8R8A8\_TYPELESS</span></span>
-   <span data-ttu-id="a5657-125">DXGI \_ 格式 \_ B8G8R8X8 無別 \_</span><span class="sxs-lookup"><span data-stu-id="a5657-125">DXGI\_FORMAT\_B8G8R8X8\_TYPELESS</span></span>
-   <span data-ttu-id="a5657-126">DXGI \_ 格式 \_ R16G16 無別 \_</span><span class="sxs-lookup"><span data-stu-id="a5657-126">DXGI\_FORMAT\_R16G16\_TYPELESS</span></span>

<span data-ttu-id="a5657-127">例如，DXGI \_ format \_ R10G10B10A2 \_ UNORM 格式是 dxgi \_ 格式 R10G10B10A2 無別格式的子 \_ 系 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a5657-127">For example, the DXGI\_FORMAT\_R10G10B10A2\_UNORM format is a descendant of the DXGI\_FORMAT\_R10G10B10A2\_TYPELESS format.</span></span> <span data-ttu-id="a5657-128">因此，DXGI \_ FORMAT \_ R10G10B10A2 \_ UNORM 支援下列順序所述的使用模式。</span><span class="sxs-lookup"><span data-stu-id="a5657-128">Therefore, DXGI\_FORMAT\_R10G10B10A2\_UNORM supports the usage pattern that is described in the following sequence.</span></span> <span data-ttu-id="a5657-129">從 DXGI 格式 R32 不具類型的格式（ \_ \_ \_ 例如 dxgi \_ 格式 \_ R32 \_ FLOAT）支援完整，不需要任何格式轉換說明，如下列順序所述。</span><span class="sxs-lookup"><span data-stu-id="a5657-129">Formats that descend from DXGI\_FORMAT\_R32\_TYPELESS, such as DXGI\_FORMAT\_R32\_FLOAT, are trivially supported without requiring any of the format conversion help that is described in the following sequence.</span></span>

<span data-ttu-id="a5657-130">**執行就地影像編輯**</span><span class="sxs-lookup"><span data-stu-id="a5657-130">**To perform in-place image editing**</span></span>

1.  <span data-ttu-id="a5657-131">使用上一個案例中指定的適當無類型相依格式來建立材質，以及所需的系結旗標，例如 D3D11 系結的未 \_ \_ 排序 \_ 存取 D3D11 系結 \| \_ \_ 著色器 \_ 資源。</span><span class="sxs-lookup"><span data-stu-id="a5657-131">Create a texture with the appropriate TYPELESS-dependent format that is specified in the previous scenario together with the required bind flags, such as D3D11\_BIND\_UNORDERED\_ACCESS \| D3D11\_BIND\_SHADER\_RESOURCE.</span></span>
2.  <span data-ttu-id="a5657-132">針對就地影像編輯，請使用 DXGI \_ 格式 \_ R32 UINT 格式來建立 UAV \_ 。</span><span class="sxs-lookup"><span data-stu-id="a5657-132">For in-place image editing, create a UAV with the DXGI\_FORMAT\_R32\_UINT format.</span></span> <span data-ttu-id="a5657-133">Direct3D 11 API 通常不允許在不同的格式「系列」之間進行轉換。</span><span class="sxs-lookup"><span data-stu-id="a5657-133">The Direct3D 11 API typically does not allow casting between different format "families."</span></span> <span data-ttu-id="a5657-134">不過，Direct3D 11 API 會產生具有 DXGI \_ 格式 \_ R32 UINT 格式的例外狀況 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a5657-134">However, the Direct3D 11 API makes an exception with the DXGI\_FORMAT\_R32\_UINT format.</span></span>
3.  <span data-ttu-id="a5657-135">在 [計算著色器] 或 [圖元著色器] 中，使用 D3DX DXGIFormatConvert. .inl 檔案中提供的適當內嵌格式套件和解壓縮函數 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a5657-135">In the compute shader or pixel shader, use the appropriate inline format pack and unpack functions that are provided in the D3DX\_DXGIFormatConvert.inl file.</span></span> <span data-ttu-id="a5657-136">例如，假設紋理的 DXGI \_ 格式 \_ R32 \_ UINT UAV 真正持有 DXGI \_ 格式 \_ R10G10B10A2 \_ UNORM 格式的資料。</span><span class="sxs-lookup"><span data-stu-id="a5657-136">For example, suppose the DXGI\_FORMAT\_R32\_UINT UAV of the texture really holds DXGI\_FORMAT\_R10G10B10A2\_UNORM-formatted data.</span></span> <span data-ttu-id="a5657-137">應用程式從 UAV 將 uint 讀入著色器之後，必須呼叫下列函式來將材質格式解壓縮：</span><span class="sxs-lookup"><span data-stu-id="a5657-137">After the application reads a uint from the UAV into the shader, it must call the following function to unpack the texture format:</span></span>

    ```
    XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
    ```

    

    <span data-ttu-id="a5657-138">然後，若要在相同的著色器中寫入 UAV，應用程式會呼叫下列函式，將著色器資料封裝成應用程式可寫入至 UAV 的 uint：</span><span class="sxs-lookup"><span data-stu-id="a5657-138">Then, to write to the UAV in the same shader, the application calls the following function to pack shader data into a uint that the application can write to the UAV:</span></span>

    ```
    UINT D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
    ```

    

4.  <span data-ttu-id="a5657-139">然後，應用程式可以使用所需的格式來建立其他視圖（例如 SRVs）。</span><span class="sxs-lookup"><span data-stu-id="a5657-139">The application can then create other views, such as SRVs, with the required format.</span></span> <span data-ttu-id="a5657-140">例如， \_ \_ \_ 如果資源是建立為 dxgi \_ 格式的 \_ R10G10B10A2 \_ 無別，則應用程式可以建立具有 dxgi 格式的 SRV R10G10B10A2 UNORM 格式。</span><span class="sxs-lookup"><span data-stu-id="a5657-140">For example, the application can create a SRV with the DXGI\_FORMAT\_R10G10B10A2\_UNORM format if the resource was created as DXGI\_FORMAT\_R10G10B10A2\_TYPELESS.</span></span> <span data-ttu-id="a5657-141">當著色器存取該 SRV 時，硬體可以正常執行自動類型轉換。</span><span class="sxs-lookup"><span data-stu-id="a5657-141">When a shader accesses that SRV, the hardware can perform automatic type conversion as usual.</span></span>

> [!Note]  
> <span data-ttu-id="a5657-142">如果著色器必須僅寫入至 UAV，或讀取為 SRV，則不需要這項轉換工作，因為您可以使用完整類型的 UAVs 或 SRVs。</span><span class="sxs-lookup"><span data-stu-id="a5657-142">If the shader must write only to a UAV, or read as an SRV, none of this conversion work is needed because you can use fully typed UAVs or SRVs.</span></span> <span data-ttu-id="a5657-143">D3DX DXGIFormatConvert 中提供的格式轉換函式， \_ 只有在您想要執行同時讀取和寫入材質的 UAV 時，才有可能有用。</span><span class="sxs-lookup"><span data-stu-id="a5657-143">The format conversion functions provided in D3DX\_DXGIFormatConvert.inl are potentially useful only if you want to perform simultaneous reading from and writing to a UAV of a texture.</span></span>

 

<span data-ttu-id="a5657-144">以下是包含在 D3DX DXGIFormatConvert. .inl 檔案中的格式轉換函式清單 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a5657-144">The following is the list of format conversion functions that are included in the D3DX\_DXGIFormatConvert.inl file.</span></span> <span data-ttu-id="a5657-145">這些函式會根據它們解壓縮和封裝的 DXGI 格式進行分類 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a5657-145">These functions are categorized by the DXGI\_FORMAT that they unpack and pack.</span></span> <span data-ttu-id="a5657-146">每個支援的格式都會從上述案例中所列的其中一種非型別格式進行遞減，並支援轉換成 DXGI \_ 格式的 \_ R32 \_ UINT 作為 UAV。</span><span class="sxs-lookup"><span data-stu-id="a5657-146">Each of the supported formats descends from one of the TYPELESS formats listed in the preceding scenario and supports casting to DXGI\_FORMAT\_R32\_UINT as a UAV.</span></span>

<dl> <dt>

<span data-ttu-id="a5657-147"><span id="DXGI_FORMAT_R10G10B10A2_UNORM"></span><span id="dxgi_format_r10g10b10a2_unorm"></span>DXGI \_ 格式 \_ R10G10B10A2 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="a5657-147"><span id="DXGI_FORMAT_R10G10B10A2_UNORM"></span><span id="dxgi_format_r10g10b10a2_unorm"></span>DXGI\_FORMAT\_R10G10B10A2\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R10G10B10A2_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R10G10B10A2_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="a5657-148"><span id="DXGI_FORMAT_R10G10B10A2_UINT"></span><span id="dxgi_format_r10g10b10a2_uint"></span>DXGI \_ 格式 \_ R10G10B10A2 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="a5657-148"><span id="DXGI_FORMAT_R10G10B10A2_UINT"></span><span id="dxgi_format_r10g10b10a2_uint"></span>DXGI\_FORMAT\_R10G10B10A2\_UINT</span></span>
</dt> <dd>


```
XMUINT4 D3DX_R10G10B10A2_UINT_to_UINT4(UINT packedInput)
UINT    D3DX_UINT4_to_R10G10B10A2_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="a5657-149"><span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="a5657-149"><span id="DXGI_FORMAT_R8G8B8A8_UNORM"></span><span id="dxgi_format_r8g8b8a8_unorm"></span>DXGI\_FORMAT\_R8G8B8A8\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="a5657-150"><span id="DXGI_FORMAT_R8G8B8A8_UNORM_SRGB"></span><span id="dxgi_format_r8g8b8a8_unorm_srgb"></span>DXGI \_ 格式 \_ R8G8B8A8 \_ UNORM \_ SRGB</span><span class="sxs-lookup"><span data-stu-id="a5657-150"><span id="DXGI_FORMAT_R8G8B8A8_UNORM_SRGB"></span><span id="dxgi_format_r8g8b8a8_unorm_srgb"></span>DXGI\_FORMAT\_R8G8B8A8\_UNORM\_SRGB</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_R8G8B8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> <span data-ttu-id="a5657-151">不精確的型別函 \_ 式會使用沒有足夠精確度的著色器指令來提供確切的答案。</span><span class="sxs-lookup"><span data-stu-id="a5657-151">The \_inexact-type function uses shader instructions that do not have high enough precision to give the exact answer.</span></span> <span data-ttu-id="a5657-152">替代函數會使用儲存在著色器中的查閱資料表，提供確切的 SRGB >浮點數轉換。</span><span class="sxs-lookup"><span data-stu-id="a5657-152">The alternative function uses a lookup table stored in the shader to give an exact SRGB->float conversion.</span></span>

 

</dd> <dt>

<span data-ttu-id="a5657-153"><span id="DXGI_FORMAT_R8G8B8A8_UINT"></span><span id="dxgi_format_r8g8b8a8_uint"></span>DXGI \_ 格式 \_ R8G8B8A8 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="a5657-153"><span id="DXGI_FORMAT_R8G8B8A8_UINT"></span><span id="dxgi_format_r8g8b8a8_uint"></span>DXGI\_FORMAT\_R8G8B8A8\_UINT</span></span>
</dt> <dd>


```
XMUINT4 D3DX_R8G8B8A8_UINT_to_UINT4(UINT packedInput)
XMUINT  D3DX_UINT4_to_R8G8B8A8_UINT(XMUINT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="a5657-154"><span id="DXGI_FORMAT_R8G8B8A8_SNORM"></span><span id="dxgi_format_r8g8b8a8_snorm"></span>DXGI \_ 格式 \_ R8G8B8A8 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="a5657-154"><span id="DXGI_FORMAT_R8G8B8A8_SNORM"></span><span id="dxgi_format_r8g8b8a8_snorm"></span>DXGI\_FORMAT\_R8G8B8A8\_SNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_R8G8B8A8_SNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_SNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="a5657-155"><span id="DXGI_FORMAT_R8G8B8A8_SINT"></span><span id="dxgi_format_r8g8b8a8_sint"></span>DXGI \_ 格式 \_ R8G8B8A8 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="a5657-155"><span id="DXGI_FORMAT_R8G8B8A8_SINT"></span><span id="dxgi_format_r8g8b8a8_sint"></span>DXGI\_FORMAT\_R8G8B8A8\_SINT</span></span>
</dt> <dd>


```
XMINT4 D3DX_R8G8B8A8_SINT_to_INT4(UINT packedInput)
UINT   D3DX_INT4_to_R8G8B8A8_SINT(XMINT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="a5657-156"><span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="a5657-156"><span id="DXGI_FORMAT_B8G8R8A8_UNORM"></span><span id="dxgi_format_b8g8r8a8_unorm"></span>DXGI\_FORMAT\_B8G8R8A8\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_B8G8R8A8_UNORM(hlsl_precise XMFLOAT4 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="a5657-157"><span id="DXGI_FORMAT_B8G8R8A8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8a8_unorm_srgb"></span>DXGI \_ 格式 \_ B8G8R8A8 \_ UNORM \_ SRGB</span><span class="sxs-lookup"><span data-stu-id="a5657-157"><span id="DXGI_FORMAT_B8G8R8A8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8a8_unorm_srgb"></span>DXGI\_FORMAT\_B8G8R8A8\_UNORM\_SRGB</span></span>
</dt> <dd>


```
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4_inexact(UINT packedInput) *
XMFLOAT4 D3DX_B8G8R8A8_UNORM_SRGB_to_FLOAT4(UINT packedInput)
UINT     D3DX_FLOAT4_to_R8G8B8A8_UNORM_SRGB(hlsl_precise XMFLOAT4 unpackedInput)
```



> [!Note]  
> <span data-ttu-id="a5657-158">不精確的型別函 \_ 式會使用沒有足夠精確度的著色器指令來提供確切的答案。</span><span class="sxs-lookup"><span data-stu-id="a5657-158">The \_inexact-type function uses shader instructions that do not have high enough precision to give the exact answer.</span></span> <span data-ttu-id="a5657-159">替代函數會使用儲存在著色器中的查閱資料表，提供確切的 SRGB >浮點數轉換。</span><span class="sxs-lookup"><span data-stu-id="a5657-159">The alternative function uses a lookup table stored in the shader to give an exact SRGB->float conversion.</span></span>

 

</dd> <dt>

<span data-ttu-id="a5657-160"><span id="DXGI_FORMAT_B8G8R8X8_UNORM"></span><span id="dxgi_format_b8g8r8x8_unorm"></span>DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="a5657-160"><span id="DXGI_FORMAT_B8G8R8X8_UNORM"></span><span id="dxgi_format_b8g8r8x8_unorm"></span>DXGI\_FORMAT\_B8G8R8X8\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM(hlsl_precise XMFLOAT3 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="a5657-161"><span id="DXGI_FORMAT_B8G8R8X8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8x8_unorm_srgb"></span>DXGI \_ 格式 \_ B8G8R8X8 \_ UNORM \_ SRGB</span><span class="sxs-lookup"><span data-stu-id="a5657-161"><span id="DXGI_FORMAT_B8G8R8X8_UNORM_SRGB"></span><span id="dxgi_format_b8g8r8x8_unorm_srgb"></span>DXGI\_FORMAT\_B8G8R8X8\_UNORM\_SRGB</span></span>
</dt> <dd>


```
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3_inexact(UINT packedInput) *
XMFLOAT3 D3DX_B8G8R8X8_UNORM_SRGB_to_FLOAT3(UINT packedInput)
UINT     D3DX_FLOAT3_to_B8G8R8X8_UNORM_SRGB(hlsl_precise XMFLOAT3 unpackedInput)
```



> [!Note]  
> <span data-ttu-id="a5657-162">不精確的型別函 \_ 式會使用沒有足夠精確度的著色器指令來提供確切的答案。</span><span class="sxs-lookup"><span data-stu-id="a5657-162">The \_inexact-type function uses shader instructions that do not have high enough precision to give the exact answer.</span></span> <span data-ttu-id="a5657-163">替代函數會使用儲存在著色器中的查閱資料表，提供確切的 SRGB >浮點數轉換。</span><span class="sxs-lookup"><span data-stu-id="a5657-163">The alternative function uses a lookup table stored in the shader to give an exact SRGB->float conversion.</span></span>

 

</dd> <dt>

<span data-ttu-id="a5657-164"><span id="DXGI_FORMAT_R16G16_FLOAT"></span><span id="dxgi_format_r16g16_float"></span>DXGI \_ 格式 \_ R16G16 \_ FLOAT</span><span class="sxs-lookup"><span data-stu-id="a5657-164"><span id="DXGI_FORMAT_R16G16_FLOAT"></span><span id="dxgi_format_r16g16_float"></span>DXGI\_FORMAT\_R16G16\_FLOAT</span></span>
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_FLOAT_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_FLOAT(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="a5657-165"><span id="DXGI_FORMAT_R16G16_UNORM"></span><span id="dxgi_format_r16g16_unorm"></span>DXGI \_ 格式 \_ R16G16 \_ UNORM</span><span class="sxs-lookup"><span data-stu-id="a5657-165"><span id="DXGI_FORMAT_R16G16_UNORM"></span><span id="dxgi_format_r16g16_unorm"></span>DXGI\_FORMAT\_R16G16\_UNORM</span></span>
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_UNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_UNORM(hlsl_precise FLOAT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="a5657-166"><span id="DXGI_FORMAT_R16G16_UINT"></span><span id="dxgi_format_r16g16_uint"></span>DXGI \_ 格式 \_ R16G16 \_ UINT</span><span class="sxs-lookup"><span data-stu-id="a5657-166"><span id="DXGI_FORMAT_R16G16_UINT"></span><span id="dxgi_format_r16g16_uint"></span>DXGI\_FORMAT\_R16G16\_UINT</span></span>
</dt> <dd>


```
XMUINT2 D3DX_R16G16_UINT_to_UINT2(UINT packedInput)
UINT    D3DX_UINT2_to_R16G16_UINT(XMUINT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="a5657-167"><span id="DXGI_FORMAT_R16G16_SNORM"></span><span id="dxgi_format_r16g16_snorm"></span>DXGI \_ 格式 \_ R16G16 \_ SNORM</span><span class="sxs-lookup"><span data-stu-id="a5657-167"><span id="DXGI_FORMAT_R16G16_SNORM"></span><span id="dxgi_format_r16g16_snorm"></span>DXGI\_FORMAT\_R16G16\_SNORM</span></span>
</dt> <dd>


```
XMFLOAT2 D3DX_R16G16_SNORM_to_FLOAT2(UINT packedInput)
UINT     D3DX_FLOAT2_to_R16G16_SNORM(hlsl_precise XMFLOAT2 unpackedInput)
```



</dd> <dt>

<span data-ttu-id="a5657-168"><span id="DXGI_FORMAT_R16G16_SINT"></span><span id="dxgi_format_r16g16_sint"></span>DXGI \_ 格式 \_ R16G16 \_ 聖</span><span class="sxs-lookup"><span data-stu-id="a5657-168"><span id="DXGI_FORMAT_R16G16_SINT"></span><span id="dxgi_format_r16g16_sint"></span>DXGI\_FORMAT\_R16G16\_SINT</span></span>
</dt> <dd>


```
XMINT2 D3DX_R16G16_SINT_to_INT2(UINT packedInput)
UINT   D3DX_INT2_to_R16G16_SINT(XMINT2 unpackedInput)
```



</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="a5657-169">[相關主題]</span><span class="sxs-lookup"><span data-stu-id="a5657-169">Related Topics</span></span>

[<span data-ttu-id="a5657-170">HLSL 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="a5657-170">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)


## <a name="related-topics"></a><span data-ttu-id="a5657-171">相關主題</span><span class="sxs-lookup"><span data-stu-id="a5657-171">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a5657-172">HLSL 的程式設計指南</span><span class="sxs-lookup"><span data-stu-id="a5657-172">Programming Guide for HLSL</span></span>](dx-graphics-hlsl-pguide.md)
</dt> </dl>

 

 




