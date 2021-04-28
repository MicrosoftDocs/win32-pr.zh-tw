---
description: D3DX10GetImageInfoFromFile 函式-取得指定影像檔案的相關資訊。
ms.assetid: 59bdce45-82d9-42da-b847-a29ca71919b5
title: 'D3DX10GetImageInfoFromFile 函式 (D3DX10Tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DX10GetImageInfoFromFile
api_type:
- LibDef
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 3e11c4cb52176b0a144e164501f8c70d1e3678c1
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108098328"
---
# <a name="d3dx10getimageinfofromfile-function"></a><span data-ttu-id="b53d5-103">D3DX10GetImageInfoFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="b53d5-103">D3DX10GetImageInfoFromFile function</span></span>

<span data-ttu-id="b53d5-104">抓取指定影像檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b53d5-104">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="b53d5-105">語法</span><span class="sxs-lookup"><span data-stu-id="b53d5-105">Syntax</span></span>


```C++
HRESULT D3DX10GetImageInfoFromFile(
  _In_  LPCTSTR           pSrcFile,
  _In_  ID3DX10ThreadPump *pPump,
  _In_  D3DX10_IMAGE_INFO *pSrcInfo,
  _Out_ HRESULT           *pHResult
);
```



## <a name="parameters"></a><span data-ttu-id="b53d5-106">參數</span><span class="sxs-lookup"><span data-stu-id="b53d5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b53d5-107">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b53d5-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b53d5-108">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b53d5-108">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b53d5-109">要取得相關資訊之影像的檔案名。</span><span class="sxs-lookup"><span data-stu-id="b53d5-109">File name of image to retrieve information about.</span></span> <span data-ttu-id="b53d5-110">如果 \_ 已定義 unicode 或 unicode，則此參數類型為 LPCWSTR，否則為 LPCSTR 類型。</span><span class="sxs-lookup"><span data-stu-id="b53d5-110">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="b53d5-111">*pPump* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b53d5-111">*pPump* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b53d5-112">類型： **[ **ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span><span class="sxs-lookup"><span data-stu-id="b53d5-112">Type: **[**ID3DX10ThreadPump**](id3dx10threadpump.md)\***</span></span>

<span data-ttu-id="b53d5-113">選擇性的執行緒抽取，可用來以非同步方式載入資訊。</span><span class="sxs-lookup"><span data-stu-id="b53d5-113">Optional thread pump that can be used to load the info asynchronously.</span></span> <span data-ttu-id="b53d5-114">可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b53d5-114">Can be **NULL**.</span></span> <span data-ttu-id="b53d5-115">請參閱 [**ID3DX10ThreadPump**](id3dx10threadpump.md)。</span><span class="sxs-lookup"><span data-stu-id="b53d5-115">See [**ID3DX10ThreadPump**](id3dx10threadpump.md).</span></span>

</dd> <dt>

<span data-ttu-id="b53d5-116">*pSrcInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b53d5-116">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b53d5-117">類型： **[ **D3DX10 \_ 影像 \_ 資訊**](d3dx10-image-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="b53d5-117">Type: **[**D3DX10\_IMAGE\_INFO**](d3dx10-image-info.md)\***</span></span>

<span data-ttu-id="b53d5-118">D3DX10 影像資訊結構的指標，此 \_ \_ 結構會填入原始程式檔中的資料描述。</span><span class="sxs-lookup"><span data-stu-id="b53d5-118">Pointer to a D3DX10\_IMAGE\_INFO structure to be filled with the description of the data in the source file.</span></span>

</dd> <dt>

<span data-ttu-id="b53d5-119">*pHResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="b53d5-119">*pHResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="b53d5-120">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span><span class="sxs-lookup"><span data-stu-id="b53d5-120">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)\***</span></span>

<span data-ttu-id="b53d5-121">傳回值的指標。</span><span class="sxs-lookup"><span data-stu-id="b53d5-121">A pointer to the return value.</span></span> <span data-ttu-id="b53d5-122">可能是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="b53d5-122">May be **NULL**.</span></span> <span data-ttu-id="b53d5-123">如果 *pPump* 不是 **Null**，則 *pHResult* 必須是有效的記憶體位置，直到非同步執行完成為止。</span><span class="sxs-lookup"><span data-stu-id="b53d5-123">If *pPump* is not **NULL**, then *pHResult* must be a valid memory location until the asynchronous execution completes.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b53d5-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="b53d5-124">Return value</span></span>

<span data-ttu-id="b53d5-125">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b53d5-125">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b53d5-126">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="b53d5-126">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="b53d5-127">如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="b53d5-127">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="b53d5-128">備註</span><span class="sxs-lookup"><span data-stu-id="b53d5-128">Remarks</span></span>

<span data-ttu-id="b53d5-129">此函數支援 Unicode 和 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="b53d5-129">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="b53d5-130">規格需求</span><span class="sxs-lookup"><span data-stu-id="b53d5-130">Requirements</span></span>



| <span data-ttu-id="b53d5-131">需求</span><span class="sxs-lookup"><span data-stu-id="b53d5-131">Requirement</span></span> | <span data-ttu-id="b53d5-132">值</span><span class="sxs-lookup"><span data-stu-id="b53d5-132">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="b53d5-133">標頭</span><span class="sxs-lookup"><span data-stu-id="b53d5-133">Header</span></span><br/>  | <dl> <span data-ttu-id="b53d5-134"><dt>D3DX10Tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="b53d5-134"><dt>D3DX10Tex.h</dt></span></span> </dl> |
| <span data-ttu-id="b53d5-135">程式庫</span><span class="sxs-lookup"><span data-stu-id="b53d5-135">Library</span></span><br/> | <dl> <span data-ttu-id="b53d5-136"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b53d5-136"><dt>D3DX10.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="b53d5-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b53d5-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b53d5-138">D3DX 10 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="b53d5-138">Texture Functions in D3DX 10</span></span>](d3d10-graphics-reference-d3dx10-functions-texturing.md)
</dt> </dl>

 

 
