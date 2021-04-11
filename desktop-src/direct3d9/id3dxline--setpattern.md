---
description: 將 stipple 模式套用至線條。
ms.assetid: 53548a9f-cf09-4ab9-9327-d5053645fc1b
title: 'ID3DXLine：： SetPattern 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetPattern
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 80a0485991bc06bdb9fcd3280017d4cc60b492ca
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104116273"
---
# <a name="id3dxlinesetpattern-method"></a><span data-ttu-id="e889b-103">ID3DXLine：： SetPattern 方法</span><span class="sxs-lookup"><span data-stu-id="e889b-103">ID3DXLine::SetPattern method</span></span>

<span data-ttu-id="e889b-104">將 stipple 模式套用至線條。</span><span class="sxs-lookup"><span data-stu-id="e889b-104">Applies a stipple pattern to the line.</span></span>

## <a name="syntax"></a><span data-ttu-id="e889b-105">語法</span><span class="sxs-lookup"><span data-stu-id="e889b-105">Syntax</span></span>


```C++
HRESULT SetPattern(
  [in] DWORD dwPattern
);
```



## <a name="parameters"></a><span data-ttu-id="e889b-106">參數</span><span class="sxs-lookup"><span data-stu-id="e889b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e889b-107">*dwPattern* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e889b-107">*dwPattern* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e889b-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e889b-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e889b-109">描述 stipple 模式：1是不透明的，0是透明的。</span><span class="sxs-lookup"><span data-stu-id="e889b-109">Describes the stipple pattern: 1 is opaque, 0 is transparent.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e889b-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="e889b-110">Return value</span></span>

<span data-ttu-id="e889b-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e889b-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e889b-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="e889b-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="e889b-113">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="e889b-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="e889b-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="e889b-114">Requirements</span></span>



| <span data-ttu-id="e889b-115">需求</span><span class="sxs-lookup"><span data-stu-id="e889b-115">Requirement</span></span> | <span data-ttu-id="e889b-116">值</span><span class="sxs-lookup"><span data-stu-id="e889b-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="e889b-117">標頭</span><span class="sxs-lookup"><span data-stu-id="e889b-117">Header</span></span><br/>  | <dl> <span data-ttu-id="e889b-118"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="e889b-118"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="e889b-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="e889b-119">Library</span></span><br/> | <dl> <span data-ttu-id="e889b-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e889b-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="e889b-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e889b-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e889b-122">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="e889b-122">ID3DXLine</span></span>](id3dxline.md)
</dt> </dl>

 

 
