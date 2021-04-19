---
description: 建立會載入資源的資料處理器，然後為其建立著色器資源檢視。 資料處理器是 D3DX10 中使用執行緒抽取的非同步資料載入功能的元件。
ms.assetid: 6e5a6138-c218-4200-a24e-d906d34933b8
title: 'D3DX10CreateAsyncShaderResourceViewProcessor 函式 (D3DX10Async) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10CreateAsyncShaderResourceViewProcessor
api_type:
- HeaderDef
api_location:
- D3DX10Async.h
ms.openlocfilehash: bd55e4191382c5abde52ce05d0a16b5533d79eac
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986535"
---
# <a name="d3dx10createasyncshaderresourceviewprocessor-function"></a><span data-ttu-id="1398b-104">D3DX10CreateAsyncShaderResourceViewProcessor 函式</span><span class="sxs-lookup"><span data-stu-id="1398b-104">D3DX10CreateAsyncShaderResourceViewProcessor function</span></span>

<span data-ttu-id="1398b-105">建立會載入資源的資料處理器，然後為其建立著色器資源檢視。</span><span class="sxs-lookup"><span data-stu-id="1398b-105">Create a data processor that will load a resource and then create a shader-resource view for it.</span></span> <span data-ttu-id="1398b-106">資料處理器是 D3DX10 中使用 [**執行緒抽取**](id3dx10threadpump.md)的非同步資料載入功能的元件。</span><span class="sxs-lookup"><span data-stu-id="1398b-106">Data processors are a component of the asynchronous data loading feature in D3DX10 that uses [**thread pumps**](id3dx10threadpump.md).</span></span>

## <a name="syntax"></a><span data-ttu-id="1398b-107">語法</span><span class="sxs-lookup"><span data-stu-id="1398b-107">Syntax</span></span>


```C++
HRESULT D3DX10CreateAsyncShaderResourceViewProcessor(
  _In_  ID3D10Device           *pDevice,
  _In_  D3DX10_IMAGE_LOAD_INFO *pLoadInfo,
  _Out_ ID3DX10DataProcessor   **ppDataProcessor
);
```



## <a name="parameters"></a><span data-ttu-id="1398b-108">參數</span><span class="sxs-lookup"><span data-stu-id="1398b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1398b-109">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1398b-109">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1398b-110">類型： **[ **ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span><span class="sxs-lookup"><span data-stu-id="1398b-110">Type: **[**ID3D10Device**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)\***</span></span>

<span data-ttu-id="1398b-111">Direct3D 裝置的指標 (請參閱將用來建立資源的 [**ID3D10Device 介面**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) ，以及該資源的著色器資源檢視。</span><span class="sxs-lookup"><span data-stu-id="1398b-111">Pointer to the Direct3D device (see [**ID3D10Device Interface**](/windows/desktop/api/D3D10/nn-d3d10-id3d10device)) that will be used to create a resource and a shader-resource view for that resource.</span></span>

</dd> <dt>

<span data-ttu-id="1398b-112">*pLoadInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1398b-112">*pLoadInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1398b-113">類型： **[ **D3DX10 \_ 映射 \_ 載入 \_ 資訊**](d3dx10-image-load-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="1398b-113">Type: **[**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)\***</span></span>

<span data-ttu-id="1398b-114">選擇性。</span><span class="sxs-lookup"><span data-stu-id="1398b-114">Optional.</span></span> <span data-ttu-id="1398b-115">識別材質的特性 (請參閱資料處理器建立時) [**D3DX10 \_ 影像 \_ 載入 \_ 資訊**](d3dx10-image-load-info.md) ; 將此值設定為 **Null** ，以在載入紋理時讀取紋理的特性。</span><span class="sxs-lookup"><span data-stu-id="1398b-115">Identifies the characteristics of a texture (see [**D3DX10\_IMAGE\_LOAD\_INFO**](d3dx10-image-load-info.md)) when the data processor is created; set this to **NULL** to read the characteristics of a texture when the texture is loaded.</span></span>

</dd> <dt>

<span data-ttu-id="1398b-116">*ppDataProcessor* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1398b-116">*ppDataProcessor* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1398b-117">類型： **[ **ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span><span class="sxs-lookup"><span data-stu-id="1398b-117">Type: **[**ID3DX10DataProcessor**](id3dx10dataprocessor.md)\*\***</span></span>

<span data-ttu-id="1398b-118">緩衝區指標的位址，其中包含建立的資料處理器 (請參閱 [**ID3DX10DataProcessor 介面**](id3dx10dataprocessor.md)) 。</span><span class="sxs-lookup"><span data-stu-id="1398b-118">Address of a pointer to a buffer that contains the data processor created (see [**ID3DX10DataProcessor Interface**](id3dx10dataprocessor.md)).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1398b-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="1398b-119">Return value</span></span>

<span data-ttu-id="1398b-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1398b-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1398b-121">傳回值是 [Direct3D 10 傳回碼](d3d10-graphics-reference-returnvalues.md)中列出的其中一個值。</span><span class="sxs-lookup"><span data-stu-id="1398b-121">The return value is one of the values listed in [Direct3D 10 Return Codes](d3d10-graphics-reference-returnvalues.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="1398b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="1398b-122">Requirements</span></span>



| <span data-ttu-id="1398b-123">需求</span><span class="sxs-lookup"><span data-stu-id="1398b-123">Requirement</span></span> | <span data-ttu-id="1398b-124">值</span><span class="sxs-lookup"><span data-stu-id="1398b-124">Value</span></span> |
|-------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1398b-125">標頭</span><span class="sxs-lookup"><span data-stu-id="1398b-125">Header</span></span><br/> | <dl> <span data-ttu-id="1398b-126"><dt>D3DX10Async。h</dt></span><span class="sxs-lookup"><span data-stu-id="1398b-126"><dt>D3DX10Async.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="1398b-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1398b-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1398b-128">一般用途函數</span><span class="sxs-lookup"><span data-stu-id="1398b-128">General Purpose Functions</span></span>](d3d10-graphics-reference-d3dx10-functions-general-purpose.md)
</dt> </dl>

 

 




