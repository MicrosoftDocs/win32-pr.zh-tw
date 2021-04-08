---
description: 抓取資源中指定影像的相關資訊。
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
ms.openlocfilehash: 6875719123fe0b4dca4405570703b2587492975b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103696639"
---
# <a name="d3dxgetimageinfofromresource-function"></a><span data-ttu-id="aba0e-103">D3DXGetImageInfoFromResource 函式</span><span class="sxs-lookup"><span data-stu-id="aba0e-103">D3DXGetImageInfoFromResource function</span></span>

<span data-ttu-id="aba0e-104">抓取資源中指定影像的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="aba0e-104">Retrieves information about a given image in a resource.</span></span>

## <a name="syntax"></a><span data-ttu-id="aba0e-105">語法</span><span class="sxs-lookup"><span data-stu-id="aba0e-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromResource(
  _In_ HMODULE        hSrcModule,
  _In_ LPCTSTR        pSrcFile,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="aba0e-106">參數</span><span class="sxs-lookup"><span data-stu-id="aba0e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aba0e-107">*hSrcModule* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aba0e-107">*hSrcModule* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aba0e-108">類型： **[ **HMODULE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aba0e-108">Type: **[**HMODULE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aba0e-109">載入資源的模組。</span><span class="sxs-lookup"><span data-stu-id="aba0e-109">Module where the resource is loaded.</span></span> <span data-ttu-id="aba0e-110">將此參數設定為 **Null** ，以指定與作業系統用來建立目前進程的映射相關聯的模組。</span><span class="sxs-lookup"><span data-stu-id="aba0e-110">Set this parameter to **NULL** to specify the module associated with the image that the operating system used to create the current process.</span></span>

</dd> <dt>

<span data-ttu-id="aba0e-111">*pSrcFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aba0e-111">*pSrcFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aba0e-112">類型： **[ **LPCTSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="aba0e-112">Type: **[**LPCTSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="aba0e-113">指定檔案名之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="aba0e-113">Pointer to a string that specifies the filename.</span></span> <span data-ttu-id="aba0e-114">如果編譯器設定需要 Unicode，則資料類型 LPCTSTR 會解析為 LPCWSTR。</span><span class="sxs-lookup"><span data-stu-id="aba0e-114">If the compiler settings require Unicode, the data type LPCTSTR resolves to LPCWSTR.</span></span> <span data-ttu-id="aba0e-115">否則，字串資料類型會解析為 LPCSTR。</span><span class="sxs-lookup"><span data-stu-id="aba0e-115">Otherwise, the string data type resolves to LPCSTR.</span></span> <span data-ttu-id="aba0e-116">請參閱＜備註＞。</span><span class="sxs-lookup"><span data-stu-id="aba0e-116">See Remarks.</span></span>

</dd> <dt>

<span data-ttu-id="aba0e-117">*pSrcInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aba0e-117">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aba0e-118">類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="aba0e-118">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="aba0e-119">[**D3DXIMAGE \_ 資訊**](d3dximage-info.md)結構的指標，此結構會填入原始程式檔中的資料描述。</span><span class="sxs-lookup"><span data-stu-id="aba0e-119">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aba0e-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="aba0e-120">Return value</span></span>

<span data-ttu-id="aba0e-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="aba0e-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="aba0e-122">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="aba0e-122">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="aba0e-123">如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="aba0e-123">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="remarks"></a><span data-ttu-id="aba0e-124">備註</span><span class="sxs-lookup"><span data-stu-id="aba0e-124">Remarks</span></span>

<span data-ttu-id="aba0e-125">編譯器設定也會決定函式版本。</span><span class="sxs-lookup"><span data-stu-id="aba0e-125">The compiler setting also determines the function version.</span></span> <span data-ttu-id="aba0e-126">如果已定義 Unicode，函式呼叫會解析為 D3DXGetImageInfoFromResourceW。</span><span class="sxs-lookup"><span data-stu-id="aba0e-126">If Unicode is defined, the function call resolves to D3DXGetImageInfoFromResourceW.</span></span> <span data-ttu-id="aba0e-127">否則，函式呼叫會解析為 D3DXGetImageInfoFromResourceA，因為正在使用 ANSI 字串。</span><span class="sxs-lookup"><span data-stu-id="aba0e-127">Otherwise, the function call resolves to D3DXGetImageInfoFromResourceA because ANSI strings are being used.</span></span>

## <a name="requirements"></a><span data-ttu-id="aba0e-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="aba0e-128">Requirements</span></span>



| <span data-ttu-id="aba0e-129">需求</span><span class="sxs-lookup"><span data-stu-id="aba0e-129">Requirement</span></span> | <span data-ttu-id="aba0e-130">值</span><span class="sxs-lookup"><span data-stu-id="aba0e-130">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="aba0e-131">標頭</span><span class="sxs-lookup"><span data-stu-id="aba0e-131">Header</span></span><br/>  | <dl> <span data-ttu-id="aba0e-132"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="aba0e-132"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="aba0e-133">程式庫</span><span class="sxs-lookup"><span data-stu-id="aba0e-133">Library</span></span><br/> | <dl> <span data-ttu-id="aba0e-134"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="aba0e-134"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="aba0e-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="aba0e-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="aba0e-136">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="aba0e-136">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="aba0e-137">**D3DXGetImageInfoFromFile**</span><span class="sxs-lookup"><span data-stu-id="aba0e-137">**D3DXGetImageInfoFromFile**</span></span>](d3dxgetimageinfofromfile.md)
</dt> <dt>

[<span data-ttu-id="aba0e-138">**D3DXGetImageInfoFromFileInMemory**</span><span class="sxs-lookup"><span data-stu-id="aba0e-138">**D3DXGetImageInfoFromFileInMemory**</span></span>](d3dxgetimageinfofromfileinmemory.md)
</dt> </dl>

 

 
