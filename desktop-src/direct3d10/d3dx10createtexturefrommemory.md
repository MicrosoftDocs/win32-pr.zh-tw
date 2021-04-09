---
description: 從位於系統記憶體中的檔案建立材質資源。
ms.assetid: 63eac44b-0540-457f-96c0-d151fbd44df0
title: 'D3DX10CreateTextureFromMemory 函式 (D3DX10) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromMemory
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 885f734cd9caeaccbab27b2fcdb258c032c5d7c5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946074"
---
# <a name="d3dx10createtexturefrommemory-function"></a><span data-ttu-id="7c45d-103">D3DX10CreateTextureFromMemory 函式</span><span class="sxs-lookup"><span data-stu-id="7c45d-103">D3DX10CreateTextureFromMemory function</span></span>

<span data-ttu-id="7c45d-104">從位於系統記憶體中的檔案建立材質資源。</span><span class="sxs-lookup"><span data-stu-id="7c45d-104">Create a texture resource from a file residing in system memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="7c45d-105">語法</span><span class="sxs-lookup"><span data-stu-id="7c45d-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateTextureFromMemory(
  _In_  ID3D10Device           *pDevice,
  _In_  LPCVOID                pSrcData,
  _In_  SIZE_T                 SrcDataSize,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="7c45d-106">參數</span><span class="sxs-lookup"><span data-stu-id="7c45d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7c45d-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7c45d-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c45d-108">類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="7c45d-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="7c45d-109">裝置的指標 (查看將使用該資源的 [**ID3D10Device 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) 。</span><span class="sxs-lookup"><span data-stu-id="7c45d-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="7c45d-110">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7c45d-110">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c45d-111">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c45d-111">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c45d-112">系統記憶體中資源的指標。</span><span class="sxs-lookup"><span data-stu-id="7c45d-112">Pointer to the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="7c45d-113">*SrcDataSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7c45d-113">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c45d-114">類型： **[**大小 \_ T**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="7c45d-114">Type: **[**SIZE\_T**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="7c45d-115">系統記憶體中資源的大小。</span><span class="sxs-lookup"><span data-stu-id="7c45d-115">Size of the resource in system memory.</span></span>

</dd> <dt>

<span data-ttu-id="7c45d-116">*pLoadInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7c45d-116">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c45d-117">類型： **[ **D3DX10 \_ 映射 \_ 載入 \_ 資訊**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="7c45d-117">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="7c45d-118">選擇性。</span><span class="sxs-lookup"><span data-stu-id="7c45d-118">Optional.</span></span> <span data-ttu-id="7c45d-119">識別材質的特性 (請參閱資料處理器建立時) [**D3DX10 \_ 影像 \_ 載入 \_ 資訊**](d3dx10-image-load-info.md) ; 將此值設定為 **Null** ，以在載入紋理時讀取紋理的特性。</span><span class="sxs-lookup"><span data-stu-id="7c45d-119">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="7c45d-120">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7c45d-120">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7c45d-121">類型： **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="7c45d-121">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="7c45d-122">執行緒抽取介面的指標 (查看 [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)) 。</span><span class="sxs-lookup"><span data-stu-id="7c45d-122">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="7c45d-123">如果指定 **Null** ，此函式會以同步方式運作，直到完成為止才會傳回。</span><span class="sxs-lookup"><span data-stu-id="7c45d-123">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="7c45d-124">*ppTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7c45d-124">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c45d-125">類型： **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="7c45d-125">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span></span>

<span data-ttu-id="7c45d-126">所建立資源指標的位址。</span><span class="sxs-lookup"><span data-stu-id="7c45d-126">Address of a pointer to the created resource.</span></span> <span data-ttu-id="7c45d-127">請參閱 [**ID3D10Resource 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)。</span><span class="sxs-lookup"><span data-stu-id="7c45d-127">See [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource).</span></span>

</dd> <dt>

<span data-ttu-id="7c45d-128">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="7c45d-128">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="7c45d-129">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="7c45d-129">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="7c45d-130">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="7c45d-130">A pointer to the return value.</span></span> <span data-ttu-id="7c45d-131">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7c45d-131">May be **NULL**.</span></span> <span data-ttu-id="7c45d-132">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="7c45d-132">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7c45d-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="7c45d-133">Return value</span></span>

<span data-ttu-id="7c45d-134">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="7c45d-134">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="7c45d-135">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="7c45d-135">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="7c45d-136">備註</span><span class="sxs-lookup"><span data-stu-id="7c45d-136">Remarks</span></span>

<span data-ttu-id="7c45d-137">如需支援的影像格式清單，請參閱 [**D3DX10 \_ 圖像 \_ 檔案 \_ 格式**](d3dx10-image-file-format.md)。</span><span class="sxs-lookup"><span data-stu-id="7c45d-137">For a list of supported image formats see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="7c45d-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="7c45d-138">Requirements</span></span>



| <span data-ttu-id="7c45d-139">需求</span><span class="sxs-lookup"><span data-stu-id="7c45d-139">Requirement</span></span> | <span data-ttu-id="7c45d-140">值</span><span class="sxs-lookup"><span data-stu-id="7c45d-140">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="7c45d-141">標頭</span><span class="sxs-lookup"><span data-stu-id="7c45d-141">Header</span></span><br/>  | <dl> <span data-ttu-id="7c45d-142"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="7c45d-142"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="7c45d-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="7c45d-143">Library</span></span><br/> | <dl> <span data-ttu-id="7c45d-144"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="7c45d-144"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="7c45d-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c45d-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7c45d-146">D3DX 10 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="7c45d-146">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="7c45d-147">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="7c45d-147">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
