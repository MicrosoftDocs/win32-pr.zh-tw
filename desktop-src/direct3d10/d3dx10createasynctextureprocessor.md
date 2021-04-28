---
description: D3DX10CreateAsyncTextureProcessor 函式-建立要搭配執行緒抽取使用的資料處理器。
ms.assetid: c96b0ebb-7b9c-47d0-ad4f-fa62ddb74fa1
title: 'D3DX10CreateAsyncTextureProcessor 函式 (D3DX10Tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncTextureProcessor
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: e75ab6b796f23399b453a6c7eebfe0d40e3b7b49
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108102786"
---
# <a name="d3dx10createasynctextureprocessor-function"></a><span data-ttu-id="eee7b-103">D3DX10CreateAsyncTextureProcessor 函式</span><span class="sxs-lookup"><span data-stu-id="eee7b-103">D3DX10CreateAsyncTextureProcessor function</span></span>

<span data-ttu-id="eee7b-104">建立要搭配 [**執行緒抽取**](id3dx10threadpump.md)使用的資料處理器。</span><span class="sxs-lookup"><span data-stu-id="eee7b-104">Create a data processor to be used with a [**thread pump**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="eee7b-105">語法</span><span class="sxs-lookup"><span data-stu-id="eee7b-105">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncTextureProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="eee7b-106">參數</span><span class="sxs-lookup"><span data-stu-id="eee7b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="eee7b-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eee7b-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eee7b-108">類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="eee7b-108">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="eee7b-109">Devive 的指標 (參閱 [**ID3D10Device 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) 。</span><span class="sxs-lookup"><span data-stu-id="eee7b-109">A pointer to the devive (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)).</span></span>

</dd> <dt>

<span data-ttu-id="eee7b-110">*pLoadInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="eee7b-110">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="eee7b-111">類型： **[ **D3DX10 \_ 映射 \_ 載入 \_ 資訊**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="eee7b-111">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="eee7b-112">選擇性。</span><span class="sxs-lookup"><span data-stu-id="eee7b-112">Optional.</span></span> <span data-ttu-id="eee7b-113">識別材質的特性 (請參閱資料處理器建立時) [**D3DX10 \_ 影像 \_ 載入 \_ 資訊**](d3dx10-image-load-info.md) ; 將此值設定為 **Null** ，以在載入紋理時讀取紋理的特性。</span><span class="sxs-lookup"><span data-stu-id="eee7b-113">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="eee7b-114">*ppDataProcessor* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="eee7b-114">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="eee7b-115">類型： **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="eee7b-115">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="eee7b-116">緩衝區指標的位址，其中包含建立的資料處理器 (請參閱 [**ID3DX10DataProcessor 介面**](id3dx10dataprocessor.md)) 。</span><span class="sxs-lookup"><span data-stu-id="eee7b-116">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="eee7b-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="eee7b-117">Return value</span></span>

<span data-ttu-id="eee7b-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="eee7b-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="eee7b-119">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="eee7b-119">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="eee7b-120">備註</span><span class="sxs-lookup"><span data-stu-id="eee7b-120">Remarks</span></span>

<span data-ttu-id="eee7b-121">此 API 會建立資料處理器介面並載入紋理; [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) 會建立資料處理器介面。</span><span class="sxs-lookup"><span data-stu-id="eee7b-121">This API does creates a data-processor interface and loads the texture; [**D3DX10CreateAsyncTextureInfoProcessor**](d3dx10createasynctextureinfoprocessor.md) creates the data-processor interface.</span></span>

## <a name="requirements"></a><span data-ttu-id="eee7b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="eee7b-122">Requirements</span></span>



| <span data-ttu-id="eee7b-123">需求</span><span class="sxs-lookup"><span data-stu-id="eee7b-123">Requirement</span></span> | <span data-ttu-id="eee7b-124">值</span><span class="sxs-lookup"><span data-stu-id="eee7b-124">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="eee7b-125">標頭</span><span class="sxs-lookup"><span data-stu-id="eee7b-125">Header</span></span><br/>  | <dl> <span data-ttu-id="eee7b-126"><dt>D3DX10Tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="eee7b-126"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="eee7b-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="eee7b-127">Library</span></span><br/> | <dl> <span data-ttu-id="eee7b-128"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="eee7b-128"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="eee7b-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="eee7b-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="eee7b-130">D3DX 10 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="eee7b-130">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 




