---
description: D3DX10GetImageInfoFromResource 函式-取得資源中指定影像的相關資訊。
ms.assetid: d413d887-77e0-43cc-a30e-67c3c40772f0
title: 'D3DX10GetImageInfoFromResource 函式 (D3DX10Tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromResource
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 650d05f379be634bfdd9dfb0908153260f795b00
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098366"
---
# <a name="d3dx10getimageinfofromresource-function"></a><span data-ttu-id="2f50f-103">D3DX10GetImageInfoFromResource 函式</span><span class="sxs-lookup"><span data-stu-id="2f50f-103">D3DX10GetImageInfoFromResource function</span></span>

<span data-ttu-id="2f50f-104">抓取資源中指定影像的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="2f50f-104">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="2f50f-105">語法</span><span class="sxs-lookup"><span data-stu-id="2f50f-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromResource(
  _In_  HMODULE           hSrcModule,
  _In_  LPCTSTR           pSrcResource,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="2f50f-106">參數</span><span class="sxs-lookup"><span data-stu-id="2f50f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2f50f-107">*hSrcModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f50f-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f50f-108">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f50f-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f50f-109">載入資源的模組。</span><span class="sxs-lookup"><span data-stu-id="2f50f-109">Module where the resource is loaded.</span></span> <span data-ttu-id="2f50f-110">將此參數設定為 **Null** ，以指定與作業系統用來建立目前進程的映射相關聯的模組。</span><span class="sxs-lookup"><span data-stu-id="2f50f-110">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="2f50f-111">*pSrcResource* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f50f-111">*pSrcResource* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f50f-112">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="2f50f-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="2f50f-113">指定檔案名之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="2f50f-113">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="2f50f-114">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="2f50f-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="2f50f-115">否則，資料型別會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="2f50f-115">Otherwise, the data type resolves to LPCSTR.</span></span> <span data-ttu-id="2f50f-116">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="2f50f-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="2f50f-117">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f50f-117">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f50f-118">類型： **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f50f-118">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="2f50f-119">選擇性的執行緒抽取，可用來以非同步方式載入資訊。</span><span class="sxs-lookup"><span data-stu-id="2f50f-119">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="2f50f-120">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2f50f-120">Can be **NULL**.</span></span> <span data-ttu-id="2f50f-121">請參閱 [**ID3DX10ThreadPump**](id3dx10threadpump.md)。</span><span class="sxs-lookup"><span data-stu-id="2f50f-121">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="2f50f-122">*pSrcInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2f50f-122">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2f50f-123">類型： **[ **D3DX10 \_ 影像 \_ 資訊**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="2f50f-123">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="2f50f-124">D3DX10 影像資訊結構的指標，此 \_ \_ 結構會填入原始程式檔中的資料描述。</span><span class="sxs-lookup"><span data-stu-id="2f50f-124">Pointer to a D3DX10\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="2f50f-125">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2f50f-125">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2f50f-126">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="2f50f-126">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="2f50f-127">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="2f50f-127">A pointer to the return value.</span></span> <span data-ttu-id="2f50f-128">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="2f50f-128">May be **NULL**.</span></span> <span data-ttu-id="2f50f-129">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="2f50f-129">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2f50f-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="2f50f-130">Return value</span></span>

<span data-ttu-id="2f50f-131">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2f50f-131">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2f50f-132">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="2f50f-132">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="2f50f-133">如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="2f50f-133">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="2f50f-134">備註</span><span class="sxs-lookup"><span data-stu-id="2f50f-134">Remarks</span></span>

<span data-ttu-id="2f50f-135">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="2f50f-135">The compiler setting also determines the function version.</span></span> <span data-ttu-id="2f50f-136">如果已定義 Unicode，函式呼叫會解析為 D3DX10GetImageInfoFromResourceW。</span><span class="sxs-lookup"><span data-stu-id="2f50f-136">If Unicode is defined, the function call resolves to D3DX10GetImageInfoFromResourceW.</span></span> <span data-ttu-id="2f50f-137">否則，函式呼叫會解析為 D3DX10GetImageInfoFromResourceA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="2f50f-137">Otherwise, the function call resolves to D3DX10GetImageInfoFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="2f50f-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="2f50f-138">Requirements</span></span>



| <span data-ttu-id="2f50f-139">需求</span><span class="sxs-lookup"><span data-stu-id="2f50f-139">Requirement</span></span> | <span data-ttu-id="2f50f-140">值</span><span class="sxs-lookup"><span data-stu-id="2f50f-140">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="2f50f-141">標頭</span><span class="sxs-lookup"><span data-stu-id="2f50f-141">Header</span></span><br/>  | <dl> <span data-ttu-id="2f50f-142"><dt>D3DX10Tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="2f50f-142"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="2f50f-143">程式庫</span><span class="sxs-lookup"><span data-stu-id="2f50f-143">Library</span></span><br/> | <dl> <span data-ttu-id="2f50f-144"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2f50f-144"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="2f50f-145">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2f50f-145">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2f50f-146">D3DX 10 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="2f50f-146">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
