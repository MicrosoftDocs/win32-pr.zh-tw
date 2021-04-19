---
description: 取得動畫的索引，並指定其名稱。
ms.assetid: 6e91a4fe-3202-447b-b486-d29e8da64af2
title: 'ID3DXAnimationSet：： GetAnimationIndexByName 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetAnimationIndexByName
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f4d3e5fb39ebcfa5ce906d1f90c2c5c10bdd4b3d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992300"
---
# <a name="id3dxanimationsetgetanimationindexbyname-method"></a><span data-ttu-id="47cc1-103">ID3DXAnimationSet：： GetAnimationIndexByName 方法</span><span class="sxs-lookup"><span data-stu-id="47cc1-103">ID3DXAnimationSet::GetAnimationIndexByName method</span></span>

<span data-ttu-id="47cc1-104">取得動畫的索引，並指定其名稱。</span><span class="sxs-lookup"><span data-stu-id="47cc1-104">Gets the index of an animation, given its name.</span></span>

## <a name="syntax"></a><span data-ttu-id="47cc1-105">語法</span><span class="sxs-lookup"><span data-stu-id="47cc1-105">Syntax</span></span>


```C++
HRESULT GetAnimationIndexByName(
  [in]  LPCSTR pName,
  [out] UINT   *pIndex
);
```



## <a name="parameters"></a><span data-ttu-id="47cc1-106">參數</span><span class="sxs-lookup"><span data-stu-id="47cc1-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="47cc1-107">*pName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="47cc1-107">*pName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="47cc1-108">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="47cc1-108">Type: **[**LPCSTR**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="47cc1-109">動畫的名稱。</span><span class="sxs-lookup"><span data-stu-id="47cc1-109">Name of the animation.</span></span>

</dd> <dt>

<span data-ttu-id="47cc1-110">*pIndex* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="47cc1-110">*pIndex* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="47cc1-111">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="47cc1-111">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="47cc1-112">動畫索引的指標。</span><span class="sxs-lookup"><span data-stu-id="47cc1-112">Pointer to the animation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="47cc1-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="47cc1-113">Return value</span></span>

<span data-ttu-id="47cc1-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="47cc1-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="47cc1-115">這個方法的傳回值是由應用程式設計人員所執行。</span><span class="sxs-lookup"><span data-stu-id="47cc1-115">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="47cc1-116">一般情況下，如果沒有發生錯誤，請將方法程式設計為傳回「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="47cc1-116">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="47cc1-117">否則，請將方法程式設計成從 [D3DERR](d3derr.md) 或 [**D3DXERR**](./d3dxerr.md)傳回適當的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="47cc1-117">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="47cc1-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="47cc1-118">Requirements</span></span>



| <span data-ttu-id="47cc1-119">需求</span><span class="sxs-lookup"><span data-stu-id="47cc1-119">Requirement</span></span> | <span data-ttu-id="47cc1-120">值</span><span class="sxs-lookup"><span data-stu-id="47cc1-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="47cc1-121">標頭</span><span class="sxs-lookup"><span data-stu-id="47cc1-121">Header</span></span><br/>  | <dl> <span data-ttu-id="47cc1-122"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="47cc1-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="47cc1-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="47cc1-123">Library</span></span><br/> | <dl> <span data-ttu-id="47cc1-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="47cc1-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="47cc1-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="47cc1-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="47cc1-126">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="47cc1-126">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
