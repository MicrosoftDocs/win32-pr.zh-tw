---
description: ID3DXAnimationSet：： GetCallback 方法-取得動畫集中特定回呼的相關資訊。
ms.assetid: e8388bfc-5438-4216-a98f-dd0dbca12c87
title: 'ID3DXAnimationSet：： GetCallback 方法 (D3dx9anim .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXAnimationSet.GetCallback
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 563c1007cc471ab10a9609e776da69b7c5ed493b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108097536"
---
# <a name="id3dxanimationsetgetcallback-method"></a><span data-ttu-id="78517-103">ID3DXAnimationSet：： GetCallback 方法</span><span class="sxs-lookup"><span data-stu-id="78517-103">ID3DXAnimationSet::GetCallback method</span></span>

<span data-ttu-id="78517-104">取得動畫集中特定回呼的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="78517-104">Gets information about a specific callback in the animation set.</span></span>

## <a name="syntax"></a><span data-ttu-id="78517-105">語法</span><span class="sxs-lookup"><span data-stu-id="78517-105">Syntax</span></span>


```C++
HRESULT GetCallback(
  [in]  DOUBLE Position,
  [in]  DWORD  Flags,
  [out] DOUBLE *pCallbackPosition,
  [out] LPVOID *ppCallbackData
);
```



## <a name="parameters"></a><span data-ttu-id="78517-106">參數</span><span class="sxs-lookup"><span data-stu-id="78517-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78517-107">*位置* \[在\]</span><span class="sxs-lookup"><span data-stu-id="78517-107">*Position* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78517-108">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78517-108">Type: **[**DOUBLE**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78517-109">要尋找回呼的位置。</span><span class="sxs-lookup"><span data-stu-id="78517-109">Position from which to find callbacks.</span></span>

</dd> <dt>

<span data-ttu-id="78517-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="78517-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="78517-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="78517-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="78517-112">回呼搜尋旗標。</span><span class="sxs-lookup"><span data-stu-id="78517-112">Callback search flags.</span></span> <span data-ttu-id="78517-113">這個參數可以設定為 [**D3DXCALLBACK \_ 搜尋 \_ 旗標**](./d3dxcallback-search-flags.md)中一或多個旗標的組合。</span><span class="sxs-lookup"><span data-stu-id="78517-113">This parameter can be set to a combination of one or more flags from [**D3DXCALLBACK\_SEARCH\_FLAGS**](./d3dxcallback-search-flags.md).</span></span>

</dd> <dt>

<span data-ttu-id="78517-114">*pCallbackPosition* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="78517-114">*pCallbackPosition* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78517-115">類型： **[ **DOUBLE**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="78517-115">Type: **[**DOUBLE**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="78517-116">回呼位置的指標。</span><span class="sxs-lookup"><span data-stu-id="78517-116">Pointer to the position of the callback.</span></span>

</dd> <dt>

<span data-ttu-id="78517-117">*ppCallbackData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="78517-117">*ppCallbackData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="78517-118">類型： **[ **LPVOID**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="78517-118">Type: **[**LPVOID**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="78517-119">回呼資料指標的位址。</span><span class="sxs-lookup"><span data-stu-id="78517-119">Address of the callback data pointer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78517-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="78517-120">Return value</span></span>

<span data-ttu-id="78517-121">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="78517-121">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="78517-122">這個方法的傳回值是由應用程式設計人員所執行。</span><span class="sxs-lookup"><span data-stu-id="78517-122">The return values of this method are implemented by an application programmer.</span></span> <span data-ttu-id="78517-123">一般情況下，如果沒有發生錯誤，請將方法程式設計為傳回「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="78517-123">In general, if no error occurs, program the method to return D3D\_OK.</span></span> <span data-ttu-id="78517-124">否則，請將方法程式設計成從 [D3DERR](d3derr.md) 或 [**D3DXERR**](./d3dxerr.md)傳回適當的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="78517-124">Otherwise, program the method to return an appropriate error message from [D3DERR](d3derr.md) or [**D3DXERR**](./d3dxerr.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="78517-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="78517-125">Requirements</span></span>



| <span data-ttu-id="78517-126">需求</span><span class="sxs-lookup"><span data-stu-id="78517-126">Requirement</span></span> | <span data-ttu-id="78517-127">值</span><span class="sxs-lookup"><span data-stu-id="78517-127">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="78517-128">標頭</span><span class="sxs-lookup"><span data-stu-id="78517-128">Header</span></span><br/>  | <dl> <span data-ttu-id="78517-129"><dt>D3dx9anim。h</dt></span><span class="sxs-lookup"><span data-stu-id="78517-129"><dt>D3dx9anim.h</dt></span></span> </dl> |
| <span data-ttu-id="78517-130">程式庫</span><span class="sxs-lookup"><span data-stu-id="78517-130">Library</span></span><br/> | <dl> <span data-ttu-id="78517-131"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="78517-131"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="78517-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="78517-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="78517-133">ID3DXAnimationSet</span><span class="sxs-lookup"><span data-stu-id="78517-133">ID3DXAnimationSet</span></span>](id3dxanimationset.md)
</dt> </dl>

 

 
