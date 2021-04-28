---
description: D3DXGetImageInfoFromResource 函式-取得資源中指定影像的相關資訊。
ms.assetid: 1f811b1e-f0bd-4f64-a4c9-caf899470940
title: 'D3DXGetImageInfoFromResource 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromResource
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: ea324ef94ab765bad25f7d07eef07972ab94cff6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108114446"
---
# <a name="d3dxgetimageinfofromresource-function"></a><span data-ttu-id="c4ad2-103">D3DXGetImageInfoFromResource 函式</span><span class="sxs-lookup"><span data-stu-id="c4ad2-103">D3DXGetImageInfoFromResource function</span></span>

<span data-ttu-id="c4ad2-104">抓取資源中指定影像的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="c4ad2-104">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="c4ad2-105">語法</span><span class="sxs-lookup"><span data-stu-id="c4ad2-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromResource(
  _In_ HMODULE        hSrcModule,
  _In_ LPCTSTR        pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="c4ad2-106">參數</span><span class="sxs-lookup"><span data-stu-id="c4ad2-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c4ad2-107">*hSrcModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c4ad2-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ad2-108">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4ad2-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4ad2-109">載入資源的模組。</span><span class="sxs-lookup"><span data-stu-id="c4ad2-109">Module where the resource is loaded.</span></span> <span data-ttu-id="c4ad2-110">將此參數設定為 **Null** ，以指定與作業系統用來建立目前進程的映射相關聯的模組。</span><span class="sxs-lookup"><span data-stu-id="c4ad2-110">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="c4ad2-111">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c4ad2-111">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ad2-112">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c4ad2-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c4ad2-113">指定檔案名之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="c4ad2-113">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="c4ad2-114">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="c4ad2-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="c4ad2-115">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="c4ad2-115">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="c4ad2-116">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="c4ad2-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="c4ad2-117">*pSrcInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c4ad2-117">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c4ad2-118">類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="c4ad2-118">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="c4ad2-119">[**D3DXIMAGE \_ 資訊**](d3dximage-info.md)結構的指標，此結構會填入原始程式檔中的資料描述。</span><span class="sxs-lookup"><span data-stu-id="c4ad2-119">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c4ad2-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="c4ad2-120">Return value</span></span>

<span data-ttu-id="c4ad2-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c4ad2-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c4ad2-122">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="c4ad2-122">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c4ad2-123">如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="c4ad2-123">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="c4ad2-124">備註</span><span class="sxs-lookup"><span data-stu-id="c4ad2-124">Remarks</span></span>

<span data-ttu-id="c4ad2-125">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="c4ad2-125">The compiler setting also determines the function version.</span></span> <span data-ttu-id="c4ad2-126">如果已定義 Unicode，函式呼叫會解析為 D3DXGetImageInfoFromResourceW。</span><span class="sxs-lookup"><span data-stu-id="c4ad2-126">If Unicode is defined, the function call resolves to D3DXGetImageInfoFromResourceW.</span></span> <span data-ttu-id="c4ad2-127">否則，函式呼叫會解析為 D3DXGetImageInfoFromResourceA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="c4ad2-127">Otherwise, the function call resolves to D3DXGetImageInfoFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="c4ad2-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="c4ad2-128">Requirements</span></span>



| <span data-ttu-id="c4ad2-129">需求</span><span class="sxs-lookup"><span data-stu-id="c4ad2-129">Requirement</span></span> | <span data-ttu-id="c4ad2-130">值</span><span class="sxs-lookup"><span data-stu-id="c4ad2-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c4ad2-131">標頭</span><span class="sxs-lookup"><span data-stu-id="c4ad2-131">Header</span></span><br/>  | <dl> <span data-ttu-id="c4ad2-132"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="c4ad2-132"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="c4ad2-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="c4ad2-133">Library</span></span><br/> | <dl> <span data-ttu-id="c4ad2-134"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c4ad2-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="c4ad2-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c4ad2-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c4ad2-136">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="c4ad2-136">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="c4ad2-137">**D3DXGetImageInfoFromFile**</span><span class="sxs-lookup"><span data-stu-id="c4ad2-137">**D3DXGetImageInfoFromFile**</span></span>](d3dxgetimageinfofromfile.md)
</dt> <dt>

[<span data-ttu-id="c4ad2-138">**D3DXGetImageInfoFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="c4ad2-138">**D3DXGetImageInfoFromFileInMemory**</span></span>](d3dxgetimageinfofromfileinmemory.md)
</dt> </dl>

 

 
