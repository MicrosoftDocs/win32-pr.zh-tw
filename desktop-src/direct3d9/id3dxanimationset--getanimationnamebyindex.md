---
description: 取得動畫的名稱，指定其索引。
ms.assetid: vs|directx_sdk|~\id3dxanimationset__getanimationnamebyindex.htm
title: 'ID3DXAnimationSet：： GetAnimationNameByIndex 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetAnimationNameByIndex
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 820b21fa69fd7007bdd1971e83ea44368dce5cc2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991480"
---
# <a name="id3dxanimationsetgetanimationnamebyindex-method"></a><span data-ttu-id="75adb-103">ID3DXAnimationSet：： GetAnimationNameByIndex 方法</span><span class="sxs-lookup"><span data-stu-id="75adb-103">ID3DXAnimationSet::GetAnimationNameByIndex method</span></span>

<span data-ttu-id="75adb-104">取得動畫的名稱，指定其索引。</span><span class="sxs-lookup"><span data-stu-id="75adb-104">Gets the name of an animation, given its index.</span></span>

## <a name="syntax"></a><span data-ttu-id="75adb-105">語法</span><span class="sxs-lookup"><span data-stu-id="75adb-105">Syntax</span></span>


```C++
HRESULT GetAnimationNameByIndex(
  [in]  UINT   Index,
  [out] LPCSTR *ppName
);
```



## <a name="parameters"></a><span data-ttu-id="75adb-106">參數</span><span class="sxs-lookup"><span data-stu-id="75adb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="75adb-107">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="75adb-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="75adb-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="75adb-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="75adb-109">動畫的索引。</span><span class="sxs-lookup"><span data-stu-id="75adb-109">Index of the animation.</span></span>

</dd> <dt>

<span data-ttu-id="75adb-110">*ppName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="75adb-110">*ppName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="75adb-111">類型： **[ **LPCSTR**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="75adb-111">Type: **[**LPCSTR**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="75adb-112">接收動畫名稱之字串的指標位址。</span><span class="sxs-lookup"><span data-stu-id="75adb-112">Address of a pointer to a string that receives the animation name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="75adb-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="75adb-113">Return value</span></span>

<span data-ttu-id="75adb-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="75adb-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="75adb-115">這個方法的傳回值是由應用程式設計人員所執行。</span><span class="sxs-lookup"><span data-stu-id="75adb-115">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="75adb-116">一般情況下，如果沒有發生錯誤，請將方法程式設計為傳回「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="75adb-116">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="75adb-117">否則，請將方法程式設計成從 [D3DERR](d3derr.md) 或 [**D3DXERR**](./d3dxerr.md)傳回適當的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="75adb-117">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="75adb-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="75adb-118">Requirements</span></span>



| <span data-ttu-id="75adb-119">需求</span><span class="sxs-lookup"><span data-stu-id="75adb-119">Requirement</span></span> | <span data-ttu-id="75adb-120">值</span><span class="sxs-lookup"><span data-stu-id="75adb-120">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="75adb-121">標頭</span><span class="sxs-lookup"><span data-stu-id="75adb-121">Header</span></span><br/>  | <dl> <span data-ttu-id="75adb-122"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="75adb-122"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="75adb-123">程式庫</span><span class="sxs-lookup"><span data-stu-id="75adb-123">Library</span></span><br/> | <dl> <span data-ttu-id="75adb-124"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="75adb-124"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="75adb-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75adb-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75adb-126">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="75adb-126">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
