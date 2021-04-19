---
description: 抓取指定影像檔案的相關資訊。
ms.assetid: 2e9d7073-4136-4fb7-8749-810aee000433
title: 'D3DXGetImageInfoFromFile 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromFile
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ff5d540871482b2628fd48deb382121591a9594f
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985885"
---
# <a name="d3dxgetimageinfofromfile-function"></a><span data-ttu-id="3c2b8-103">D3DXGetImageInfoFromFile 函式</span><span class="sxs-lookup"><span data-stu-id="3c2b8-103">D3DXGetImageInfoFromFile function</span></span>

<span data-ttu-id="3c2b8-104">抓取指定影像檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3c2b8-104">Retrieves information about a given image file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3c2b8-105">語法</span><span class="sxs-lookup"><span data-stu-id="3c2b8-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromFile(
  _In_ LPCSTR         pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="3c2b8-106">參數</span><span class="sxs-lookup"><span data-stu-id="3c2b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c2b8-107">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c2b8-107">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c2b8-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="3c2b8-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="3c2b8-109">要取得相關資訊之影像的檔案名。</span><span class="sxs-lookup"><span data-stu-id="3c2b8-109">File name of image to retrieve information about.</span></span> <span data-ttu-id="3c2b8-110">如果 \_ 已定義 unicode 或 unicode，則此參數類型為 LPCWSTR，否則為 LPCSTR 類型。</span><span class="sxs-lookup"><span data-stu-id="3c2b8-110">If UNICODE or \_UNICODE are defined, this parameter type is LPCWSTR, otherwise, the type is LPCSTR.</span></span>

</dd> <dt>

<span data-ttu-id="3c2b8-111">*pSrcInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c2b8-111">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c2b8-112">類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="3c2b8-112">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="3c2b8-113">[**D3DXIMAGE \_ 資訊**](d3dximage-info.md)結構的指標，此結構會填入原始程式檔中的資料描述。</span><span class="sxs-lookup"><span data-stu-id="3c2b8-113">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c2b8-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c2b8-114">Return value</span></span>

<span data-ttu-id="3c2b8-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3c2b8-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3c2b8-116">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="3c2b8-116">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="3c2b8-117">如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="3c2b8-117">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="3c2b8-118">備註</span><span class="sxs-lookup"><span data-stu-id="3c2b8-118">Remarks</span></span>

<span data-ttu-id="3c2b8-119">此函數支援 Unicode 和 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="3c2b8-119">This function supports both Unicode and ANSI strings.</span></span>

## <a name="requirements"></a><span data-ttu-id="3c2b8-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c2b8-120">Requirements</span></span>



| <span data-ttu-id="3c2b8-121">需求</span><span class="sxs-lookup"><span data-stu-id="3c2b8-121">Requirement</span></span> | <span data-ttu-id="3c2b8-122">值</span><span class="sxs-lookup"><span data-stu-id="3c2b8-122">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3c2b8-123">標頭</span><span class="sxs-lookup"><span data-stu-id="3c2b8-123">Header</span></span><br/>  | <dl> <span data-ttu-id="3c2b8-124"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="3c2b8-124"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="3c2b8-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="3c2b8-125">Library</span></span><br/> | <dl> <span data-ttu-id="3c2b8-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3c2b8-126"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="3c2b8-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c2b8-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3c2b8-128">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="3c2b8-128">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="3c2b8-129">**D3DXGetImageInfoFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="3c2b8-129">**D3DXGetImageInfoFromFileInMemory**</span></span>](d3dxgetimageinfofromfileinmemory.md)
</dt> <dt>

[<span data-ttu-id="3c2b8-130">**D3DXGetImageInfoFromResource**</span><span class="sxs-lookup"><span data-stu-id="3c2b8-130">**D3DXGetImageInfoFromResource**</span></span>](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
