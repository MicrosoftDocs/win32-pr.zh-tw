---
description: 從檔案建立著色器資源檢視。
ms.assetid: 97aa848b-e24c-4ebd-8819-b9741ea12b60
title: 'D3DX10CreateShaderResourceViewFromFile 函式 (D3DX10Tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateShaderResourceViewFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: eb787bed64d16f7593fba1f97c96ceeaa217b4e0
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104386475"
---
# <a name="d3dx10createshaderresourceviewfromfile-function"></a><span data-ttu-id="8f3bd-103">D3DX10CreateShaderResourceViewFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="8f3bd-103">D3DX10CreateShaderResourceViewFromFile function</span></span>

<span data-ttu-id="8f3bd-104">從檔案建立著色器資源檢視。</span><span class="sxs-lookup"><span data-stu-id="8f3bd-104">Create a shader-resource view from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="8f3bd-105">語法</span><span class="sxs-lookup"><span data-stu-id="8f3bd-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateShaderResourceViewFromFile(
  _In_  ID3D10Device             *pDevice,
  _In_  LPCTSTR                  pSrcFile,
  _In_  D3DX10_IMAGE_LOAD_INFO   *pLoadInfo,
  _In_  ID3DX10ThreadPump        *pPump,
  _Out_ ID3D10ShaderResourceView **ppShaderResourceView,
  _Out_ HRESULT                  *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="8f3bd-106">參數</span><span class="sxs-lookup"><span data-stu-id="8f3bd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8f3bd-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f3bd-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f3bd-108">類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="8f3bd-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="8f3bd-109">裝置的指標 (查看將使用該資源的 [**ID3D10Device 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) 。</span><span class="sxs-lookup"><span data-stu-id="8f3bd-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="8f3bd-110">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f3bd-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f3bd-111">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="8f3bd-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="8f3bd-112">包含著色器資源檢視的檔案名。</span><span class="sxs-lookup"><span data-stu-id="8f3bd-112">Name of the file that contains the shader-resource view.</span></span> <span data-ttu-id="8f3bd-113">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="8f3bd-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="8f3bd-114">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="8f3bd-114">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="8f3bd-115">*pLoadInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f3bd-115">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f3bd-116">類型： **[ **D3DX10 \_ 映射 \_ 載入 \_ 資訊**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="8f3bd-116">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="8f3bd-117">選擇性。</span><span class="sxs-lookup"><span data-stu-id="8f3bd-117">Optional.</span></span> <span data-ttu-id="8f3bd-118">識別材質的特性 (請參閱資料處理器建立時) [**D3DX10 \_ 影像 \_ 載入 \_ 資訊**](d3dx10-image-load-info.md) ; 將此值設定為 **Null** ，以在載入紋理時讀取紋理的特性。</span><span class="sxs-lookup"><span data-stu-id="8f3bd-118">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="8f3bd-119">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8f3bd-119">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8f3bd-120">類型： **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="8f3bd-120">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="8f3bd-121">執行緒抽取介面的指標 (查看 [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)) 。</span><span class="sxs-lookup"><span data-stu-id="8f3bd-121">Pointer to a thread-pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="8f3bd-122">如果指定 **Null** ，此函式會以同步方式運作，直到完成為止才會傳回。</span><span class="sxs-lookup"><span data-stu-id="8f3bd-122">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="8f3bd-123">*ppShaderResourceView* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8f3bd-123">*ppShaderResourceView* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f3bd-124">類型： **[ **ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span><span class="sxs-lookup"><span data-stu-id="8f3bd-124">Type: **[**ID3D10ShaderResourceView**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)\*\***</span></span>

<span data-ttu-id="8f3bd-125">著色器資源檢視之指標的位址 (參閱 [**ID3D10ShaderResourceView 介面**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)) 。</span><span class="sxs-lookup"><span data-stu-id="8f3bd-125">Address of a pointer to the shader-resource view (see [**ID3D10ShaderResourceView Interface**](/windows/desktop/api/d3d10/nn-d3d10-id3d10shaderresourceview)).</span></span>

</dd> <dt>

<span data-ttu-id="8f3bd-126">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="8f3bd-126">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="8f3bd-127">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="8f3bd-127">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="8f3bd-128">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="8f3bd-128">A pointer to the return value.</span></span> <span data-ttu-id="8f3bd-129">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8f3bd-129">May be **NULL**.</span></span> <span data-ttu-id="8f3bd-130">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="8f3bd-130">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8f3bd-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="8f3bd-131">Return value</span></span>

<span data-ttu-id="8f3bd-132">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="8f3bd-132">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="8f3bd-133">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="8f3bd-133">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="8f3bd-134">備註</span><span class="sxs-lookup"><span data-stu-id="8f3bd-134">Remarks</span></span>

<span data-ttu-id="8f3bd-135">如需支援的影像格式清單，請參閱 [**D3DX10 \_ 影像檔案 \_ \_ 格式**](d3dx10-image-file-format.md)。</span><span class="sxs-lookup"><span data-stu-id="8f3bd-135">For a list of supported image formats, see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="8f3bd-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="8f3bd-136">Requirements</span></span>



| <span data-ttu-id="8f3bd-137">需求</span><span class="sxs-lookup"><span data-stu-id="8f3bd-137">Requirement</span></span> | <span data-ttu-id="8f3bd-138">值</span><span class="sxs-lookup"><span data-stu-id="8f3bd-138">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="8f3bd-139">標頭</span><span class="sxs-lookup"><span data-stu-id="8f3bd-139">Header</span></span><br/>  | <dl> <span data-ttu-id="8f3bd-140"><dt>D3DX10Tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="8f3bd-140"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="8f3bd-141">程式庫</span><span class="sxs-lookup"><span data-stu-id="8f3bd-141">Library</span></span><br/> | <dl> <span data-ttu-id="8f3bd-142"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="8f3bd-142"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="8f3bd-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8f3bd-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8f3bd-144">D3DX 10 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="8f3bd-144">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="8f3bd-145">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="8f3bd-145">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
