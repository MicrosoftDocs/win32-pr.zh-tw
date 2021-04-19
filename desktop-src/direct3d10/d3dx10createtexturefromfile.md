---
description: 從檔案建立材質資源。
ms.assetid: 23edad1f-89bb-4b62-8c48-3be1cd0690d2
title: 'D3DX10CreateTextureFromFile 函式 (D3DX10) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 27db799bfd521133a2c137556fdd7408be974854
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106988598"
---
# <a name="d3dx10createtexturefromfile-function"></a><span data-ttu-id="0f9a7-103">D3DX10CreateTextureFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="0f9a7-103">D3DX10CreateTextureFromFile function</span></span>

<span data-ttu-id="0f9a7-104">從檔案建立材質資源。</span><span class="sxs-lookup"><span data-stu-id="0f9a7-104">Create a texture resource from a file.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f9a7-105">語法</span><span class="sxs-lookup"><span data-stu-id="0f9a7-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateTextureFromFile(
  _In_  ID3D10Device           *pDevice,
  _In_  LPCTSTR                pSrcFile,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="0f9a7-106">參數</span><span class="sxs-lookup"><span data-stu-id="0f9a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f9a7-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0f9a7-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f9a7-108">類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="0f9a7-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="0f9a7-109">裝置的指標 (查看將使用該資源的 [**ID3D10Device 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) 。</span><span class="sxs-lookup"><span data-stu-id="0f9a7-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="0f9a7-110">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0f9a7-110">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f9a7-111">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="0f9a7-111">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="0f9a7-112">包含資源的檔案名。</span><span class="sxs-lookup"><span data-stu-id="0f9a7-112">The name of the file containing the resource.</span></span> <span data-ttu-id="0f9a7-113">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="0f9a7-113">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="0f9a7-114">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="0f9a7-114">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="0f9a7-115">如需支援之影像檔案格式的清單，請參閱 [**D3DX10 \_ 圖像 \_ 檔案 \_ 格式**](d3dx10-image-file-format.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="0f9a7-115">See [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md) enumeration for a list of the supported image file formats.</span></span>

</dd> <dt>

<span data-ttu-id="0f9a7-116">*pLoadInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0f9a7-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f9a7-117">類型： **[ **D3DX10 \_ 映射 \_ 載入 \_ 資訊**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="0f9a7-117">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="0f9a7-118">選擇性。</span><span class="sxs-lookup"><span data-stu-id="0f9a7-118">Optional.</span></span> <span data-ttu-id="0f9a7-119">識別材質的特性 (請參閱資料處理器建立時) [**D3DX10 \_ 影像 \_ 載入 \_ 資訊**](d3dx10-image-load-info.md) ; 將此值設定為 **Null** ，以在載入紋理時讀取紋理的特性。</span><span class="sxs-lookup"><span data-stu-id="0f9a7-119">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="0f9a7-120">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0f9a7-120">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f9a7-121">類型： **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="0f9a7-121">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="0f9a7-122">執行緒抽取介面的指標 (查看 [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)) 。</span><span class="sxs-lookup"><span data-stu-id="0f9a7-122">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="0f9a7-123">如果指定 **Null** ，此函式會以同步方式運作，直到完成為止才會傳回。</span><span class="sxs-lookup"><span data-stu-id="0f9a7-123">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="0f9a7-124">*ppTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0f9a7-124">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f9a7-125">類型： **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="0f9a7-125">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span></span>

<span data-ttu-id="0f9a7-126">材質資源指標的位址 (參閱 [**ID3D10Resource 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)) 。</span><span class="sxs-lookup"><span data-stu-id="0f9a7-126">The address of a pointer to the texture resource (see [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)).</span></span>

</dd> <dt>

<span data-ttu-id="0f9a7-127">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0f9a7-127">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0f9a7-128">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="0f9a7-128">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="0f9a7-129">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="0f9a7-129">A pointer to the return value.</span></span> <span data-ttu-id="0f9a7-130">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="0f9a7-130">May be **NULL**.</span></span> <span data-ttu-id="0f9a7-131">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="0f9a7-131">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f9a7-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="0f9a7-132">Return value</span></span>

<span data-ttu-id="0f9a7-133">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="0f9a7-133">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="0f9a7-134">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="0f9a7-134">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="0f9a7-135">備註</span><span class="sxs-lookup"><span data-stu-id="0f9a7-135">Remarks</span></span>

<span data-ttu-id="0f9a7-136">如需支援的影像格式清單，請參閱 [**D3DX10 \_ 圖像 \_ 檔案 \_ 格式**](d3dx10-image-file-format.md)。</span><span class="sxs-lookup"><span data-stu-id="0f9a7-136">For a list of supported image formats see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="0f9a7-137">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f9a7-137">Requirements</span></span>



| <span data-ttu-id="0f9a7-138">需求</span><span class="sxs-lookup"><span data-stu-id="0f9a7-138">Requirement</span></span> | <span data-ttu-id="0f9a7-139">值</span><span class="sxs-lookup"><span data-stu-id="0f9a7-139">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0f9a7-140">標頭</span><span class="sxs-lookup"><span data-stu-id="0f9a7-140">Header</span></span><br/>  | <dl> <span data-ttu-id="0f9a7-141"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="0f9a7-141"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="0f9a7-142">程式庫</span><span class="sxs-lookup"><span data-stu-id="0f9a7-142">Library</span></span><br/> | <dl> <span data-ttu-id="0f9a7-143"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="0f9a7-143"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0f9a7-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0f9a7-144">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0f9a7-145">D3DX 10 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="0f9a7-145">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="0f9a7-146">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="0f9a7-146">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
