---
description: 抓取記憶體中指定影像檔案的相關資訊。
ms.assetid: 6363aaf1-abfc-49df-9b99-be8a1c3540e1
title: 'D3DXGetImageInfoFromFileInMemory 函式 (D3dx9tex) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DXGetImageInfoFromFileInMemory
api_type:
- LibDef
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: e2bad56cb2aa769be80a6b031b1783d8717bc485
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000591"
---
# <a name="d3dxgetimageinfofromfileinmemory-function"></a><span data-ttu-id="ac967-103">D3DXGetImageInfoFromFileInMemory 函式</span><span class="sxs-lookup"><span data-stu-id="ac967-103">D3DXGetImageInfoFromFileInMemory function</span></span>

<span data-ttu-id="ac967-104">抓取記憶體中指定影像檔案的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="ac967-104">Retrieves information about a given image file in memory.</span></span>

## <a name="syntax"></a><span data-ttu-id="ac967-105">語法</span><span class="sxs-lookup"><span data-stu-id="ac967-105">Syntax</span></span>


```C++
HRESULT D3DXGetImageInfoFromFileInMemory(
  _In_ LPCVOID        pSrcData,
  _In_ UINT           SrcDataSize,
  _In_ D3DXIMAGE_INFO *pSrcInfo
);
```



## <a name="parameters"></a><span data-ttu-id="ac967-106">參數</span><span class="sxs-lookup"><span data-stu-id="ac967-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ac967-107">*pSrcData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ac967-107">*pSrcData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac967-108">類型： **[ **LPCVOID**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac967-108">Type: **[**LPCVOID**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac967-109">記憶體中來源檔案的 VOID 指標。</span><span class="sxs-lookup"><span data-stu-id="ac967-109">VOID pointer to the source file in memory.</span></span>

</dd> <dt>

<span data-ttu-id="ac967-110">*SrcDataSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ac967-110">*SrcDataSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac967-111">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ac967-111">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ac967-112">記憶體中的檔案大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="ac967-112">Size of file in memory, in bytes.</span></span> <span data-ttu-id="ac967-113">.</span><span class="sxs-lookup"><span data-stu-id="ac967-113">.</span></span>

</dd> <dt>

<span data-ttu-id="ac967-114">*pSrcInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ac967-114">*pSrcInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ac967-115">類型： **[ **D3DXIMAGE \_ 資訊**](d3dximage-info.md)\***</span><span class="sxs-lookup"><span data-stu-id="ac967-115">Type: **[**D3DXIMAGE\_INFO**](d3dximage-info.md)\***</span></span>

<span data-ttu-id="ac967-116">[**D3DXIMAGE \_ 資訊**](d3dximage-info.md)結構的指標，此結構會填入原始程式檔中的資料描述。</span><span class="sxs-lookup"><span data-stu-id="ac967-116">Pointer to a [**D3DXIMAGE\_INFO**](d3dximage-info.md) structure to be filled with the description of the data in the source file.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ac967-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="ac967-117">Return value</span></span>

<span data-ttu-id="ac967-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ac967-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ac967-119">如果函式成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="ac967-119">If the function succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="ac967-120">如果函式失敗，則傳回值可以是下列值： D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="ac967-120">If the function fails, the return value can be the following: D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="ac967-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="ac967-121">Requirements</span></span>



| <span data-ttu-id="ac967-122">需求</span><span class="sxs-lookup"><span data-stu-id="ac967-122">Requirement</span></span> | <span data-ttu-id="ac967-123">值</span><span class="sxs-lookup"><span data-stu-id="ac967-123">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="ac967-124">標頭</span><span class="sxs-lookup"><span data-stu-id="ac967-124">Header</span></span><br/>  | <dl> <span data-ttu-id="ac967-125"><dt>D3dx9tex。h</dt></span><span class="sxs-lookup"><span data-stu-id="ac967-125"><dt>D3dx9tex.h</dt></span></span> </dl> |
| <span data-ttu-id="ac967-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="ac967-126">Library</span></span><br/> | <dl> <span data-ttu-id="ac967-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ac967-127"><dt>D3dx9.lib</dt></span></span> </dl>  |



## <a name="see-also"></a><span data-ttu-id="ac967-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ac967-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ac967-129">D3DX 9 中的材質函數</span><span class="sxs-lookup"><span data-stu-id="ac967-129">Texture Functions in D3DX 9</span></span>](dx9-graphics-reference-d3dx-functions-texture.md)
</dt> <dt>

[<span data-ttu-id="ac967-130">**D3DXGetImageInfoFromFile**</span><span class="sxs-lookup"><span data-stu-id="ac967-130">**D3DXGetImageInfoFromFile**</span></span>](d3dxgetimageinfofromfile.md)
</dt> <dt>

[<span data-ttu-id="ac967-131">**D3DXGetImageInfoFromResource**</span><span class="sxs-lookup"><span data-stu-id="ac967-131">**D3DXGetImageInfoFromResource**</span></span>](d3dxgetimageinfofromresource.md)
</dt> </dl>

 

 
