---
description: 建立另一個資源的材質。
ms.assetid: 9758968a-652f-42bb-8c81-ad7816c57b17
title: 'D3DX10CreateTextureFromResource 函式 (D3DX10) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateTextureFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 22be3b54c7aa9090fd95624a51bc248b01003dcc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982902"
---
# <a name="d3dx10createtexturefromresource-function"></a><span data-ttu-id="77611-103">D3DX10CreateTextureFromResource 函式</span><span class="sxs-lookup"><span data-stu-id="77611-103">D3DX10CreateTextureFromResource function</span></span>

<span data-ttu-id="77611-104">建立另一個資源的材質。</span><span class="sxs-lookup"><span data-stu-id="77611-104">Create a texture from another resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="77611-105">語法</span><span class="sxs-lookup"><span data-stu-id="77611-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateTextureFromResource(
  _In_  ID3D10Device           *pDevice,
  _In_  HMODULE                hSrcModule,
  _In_  LPCTSTR                pSrcResource,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _In_  ID3DX10ThreadPump      *pPump,
  _Out_ ID3D10Resource         **ppTexture,
  _Out_ HRESULT                *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="77611-106">參數</span><span class="sxs-lookup"><span data-stu-id="77611-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="77611-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77611-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77611-108">類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="77611-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="77611-109">裝置的指標 (查看將使用該資源的 [**ID3D10Device 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) 。</span><span class="sxs-lookup"><span data-stu-id="77611-109">A pointer to the device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will use the resource.</span></span>

</dd> <dt>

<span data-ttu-id="77611-110">*hSrcModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77611-110">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77611-111">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77611-111">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="77611-112">來源資源的控制碼。</span><span class="sxs-lookup"><span data-stu-id="77611-112">A handle to the source resource.</span></span> <span data-ttu-id="77611-113">您可以使用 [GetModuleHandle 函數](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea)來取得 HMODULE。</span><span class="sxs-lookup"><span data-stu-id="77611-113">HMODULE can be obtained with [GetModuleHandle Function](/windows/desktop/api/libloaderapi/nf-libloaderapi-getmodulehandlea).</span></span>

</dd> <dt>

<span data-ttu-id="77611-114">*pSrcResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77611-114">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77611-115">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="77611-115">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="77611-116">包含來源資源名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="77611-116">A string that contains the name of the source resource.</span></span> <span data-ttu-id="77611-117">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="77611-117">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="77611-118">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="77611-118">Otherwise, the data type resolves to LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="77611-119">*pLoadInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77611-119">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77611-120">類型： **[ **D3DX10 \_ 映射 \_ 載入 \_ 資訊**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="77611-120">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="77611-121">選擇性。</span><span class="sxs-lookup"><span data-stu-id="77611-121">Optional.</span></span> <span data-ttu-id="77611-122">識別材質的特性 (請參閱資料處理器建立時) [**D3DX10 \_ 影像 \_ 載入 \_ 資訊**](d3dx10-image-load-info.md) ; 將此值設定為 **Null** ，以在載入紋理時讀取紋理的特性。</span><span class="sxs-lookup"><span data-stu-id="77611-122">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="77611-123">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="77611-123">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="77611-124">類型： **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="77611-124">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="77611-125">執行緒抽取介面的指標 (查看 [**ID3DX10ThreadPump 介面**](id3dx10threadpump.md)) 。</span><span class="sxs-lookup"><span data-stu-id="77611-125">A pointer to a thread pump interface (see [**ID3DX10ThreadPump Interface**](id3dx10threadpump.md)).</span></span> <span data-ttu-id="77611-126">如果指定 **Null** ，此函式會以同步方式運作，直到完成為止才會傳回。</span><span class="sxs-lookup"><span data-stu-id="77611-126">If **NULL** is specified, this function will behave synchronously and will not return until it is finished.</span></span>

</dd> <dt>

<span data-ttu-id="77611-127">*ppTexture* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="77611-127">*ppTexture* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77611-128">類型： **[ **ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span><span class="sxs-lookup"><span data-stu-id="77611-128">Type: **[**ID3D10Resource**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)\*\***</span></span>

<span data-ttu-id="77611-129">材質資源指標的位址 (參閱 [**ID3D10Resource 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)) 。</span><span class="sxs-lookup"><span data-stu-id="77611-129">The address of a pointer to the texture resource (see [**ID3D10Resource Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10resource)).</span></span>

</dd> <dt>

<span data-ttu-id="77611-130">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="77611-130">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="77611-131">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="77611-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="77611-132">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="77611-132">A pointer to the return value.</span></span> <span data-ttu-id="77611-133">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="77611-133">May be **NULL**.</span></span> <span data-ttu-id="77611-134">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="77611-134">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="77611-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="77611-135">Return value</span></span>

<span data-ttu-id="77611-136">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="77611-136">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="77611-137">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="77611-137">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="77611-138">備註</span><span class="sxs-lookup"><span data-stu-id="77611-138">Remarks</span></span>

<span data-ttu-id="77611-139">如需支援的影像格式清單，請參閱 [**D3DX10 \_ 圖像 \_ 檔案 \_ 格式**](d3dx10-image-file-format.md)。</span><span class="sxs-lookup"><span data-stu-id="77611-139">For a list of supported image formats see [**D3DX10\_IMAGE\_FILE\_FORMAT**](d3dx10-image-file-format.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="77611-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="77611-140">Requirements</span></span>



| <span data-ttu-id="77611-141">需求</span><span class="sxs-lookup"><span data-stu-id="77611-141">Requirement</span></span> | <span data-ttu-id="77611-142">值</span><span class="sxs-lookup"><span data-stu-id="77611-142">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="77611-143">標頭</span><span class="sxs-lookup"><span data-stu-id="77611-143">Header</span></span><br/>  | <dl> <span data-ttu-id="77611-144"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="77611-144"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="77611-145">程式庫</span><span class="sxs-lookup"><span data-stu-id="77611-145">Library</span></span><br/> | <dl> <span data-ttu-id="77611-146"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="77611-146"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="77611-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="77611-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="77611-148">D3DX 10 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="77611-148">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> <dt>

[<span data-ttu-id="77611-149">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="77611-149">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 
