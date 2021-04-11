---
description: 指定線條的粗細。
ms.assetid: cedf9217-2b47-40c3-a64c-9872c1083d71
title: 'ID3DXLine：： SetWidth 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetWidth
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: d357d7516233caf6ef9206aa2aecc2a98a435cde
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104035418"
---
# <a name="id3dxlinesetwidth-method"></a><span data-ttu-id="a85a7-103">ID3DXLine：： SetWidth 方法</span><span class="sxs-lookup"><span data-stu-id="a85a7-103">ID3DXLine::SetWidth method</span></span>

<span data-ttu-id="a85a7-104">指定線條的粗細。</span><span class="sxs-lookup"><span data-stu-id="a85a7-104">Specifies the thickness of the line.</span></span>

## <a name="syntax"></a><span data-ttu-id="a85a7-105">語法</span><span class="sxs-lookup"><span data-stu-id="a85a7-105">Syntax</span></span>


```C++
HRESULT SetWidth(
  [in] FLOAT fWidth
);
```



## <a name="parameters"></a><span data-ttu-id="a85a7-106">參數</span><span class="sxs-lookup"><span data-stu-id="a85a7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a85a7-107">*fWidth* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a85a7-107">*fWidth* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a85a7-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="a85a7-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="a85a7-109">描述線條寬度。</span><span class="sxs-lookup"><span data-stu-id="a85a7-109">Describes the line width.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a85a7-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="a85a7-110">Return value</span></span>

<span data-ttu-id="a85a7-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="a85a7-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="a85a7-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="a85a7-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="a85a7-113">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="a85a7-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="a85a7-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="a85a7-114">Requirements</span></span>



| <span data-ttu-id="a85a7-115">需求</span><span class="sxs-lookup"><span data-stu-id="a85a7-115">Requirement</span></span> | <span data-ttu-id="a85a7-116">值</span><span class="sxs-lookup"><span data-stu-id="a85a7-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a85a7-117">標頭</span><span class="sxs-lookup"><span data-stu-id="a85a7-117">Header</span></span><br/>  | <dl> <span data-ttu-id="a85a7-118"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="a85a7-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="a85a7-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="a85a7-119">Library</span></span><br/> | <dl> <span data-ttu-id="a85a7-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="a85a7-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="a85a7-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a85a7-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a85a7-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="a85a7-122">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
