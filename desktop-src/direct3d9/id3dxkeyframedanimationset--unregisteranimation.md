---
description: 從動畫集合中移除動畫資料。
ms.assetid: 9821d21e-fe8f-4742-b4f3-63b2578d29ec
title: 'ID3DXKeyframedAnimationSet：： UnregisterAnimation 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXKeyframedAnimationSet.UnregisterAnimation
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: f5ee7718fb73e441daacf9fdaff38499239915e2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993908"
---
# <a name="id3dxkeyframedanimationsetunregisteranimation-method"></a><span data-ttu-id="57a6c-103">ID3DXKeyframedAnimationSet：： UnregisterAnimation 方法</span><span class="sxs-lookup"><span data-stu-id="57a6c-103">ID3DXKeyframedAnimationSet::UnregisterAnimation method</span></span>

<span data-ttu-id="57a6c-104">從動畫集合中移除動畫資料。</span><span class="sxs-lookup"><span data-stu-id="57a6c-104">Remove the animation data from the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="57a6c-105">語法</span><span class="sxs-lookup"><span data-stu-id="57a6c-105">Syntax</span></span>


```C++
HRESULT UnregisterAnimation(
  [in] UINT Index
);
```



## <a name="parameters"></a><span data-ttu-id="57a6c-106">參數</span><span class="sxs-lookup"><span data-stu-id="57a6c-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="57a6c-107">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="57a6c-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="57a6c-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="57a6c-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="57a6c-109">動畫索引。</span><span class="sxs-lookup"><span data-stu-id="57a6c-109">The animation index.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="57a6c-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="57a6c-110">Return value</span></span>

<span data-ttu-id="57a6c-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="57a6c-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="57a6c-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="57a6c-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="57a6c-113">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="57a6c-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="57a6c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="57a6c-114">Requirements</span></span>



| <span data-ttu-id="57a6c-115">需求</span><span class="sxs-lookup"><span data-stu-id="57a6c-115">Requirement</span></span> | <span data-ttu-id="57a6c-116">值</span><span class="sxs-lookup"><span data-stu-id="57a6c-116">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="57a6c-117">標頭</span><span class="sxs-lookup"><span data-stu-id="57a6c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="57a6c-118"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="57a6c-118"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="57a6c-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="57a6c-119">Library</span></span><br/> | <dl> <span data-ttu-id="57a6c-120"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="57a6c-120"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="57a6c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="57a6c-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="57a6c-122">ID3DXKeyframedAnimationSet</span><span class="sxs-lookup"><span data-stu-id="57a6c-122">ID3DXKeyframedAnimationSet</span></span>](id3dxkeyframedanimationset.md)
</dt> </dl>

 

 
