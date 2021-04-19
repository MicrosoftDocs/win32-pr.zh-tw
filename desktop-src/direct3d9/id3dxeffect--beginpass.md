---
description: 在主動技術內開始進行。
ms.assetid: fbb2bf1c-e37a-4117-8c3c-5f5b6a267301
title: 'ID3DXEffect：： BeginPass 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.BeginPass
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 56a2648f65c3747f8a98fc0cdbd3ed06cea560b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106992720"
---
# <a name="id3dxeffectbeginpass-method"></a><span data-ttu-id="c5335-103">ID3DXEffect：： BeginPass 方法</span><span class="sxs-lookup"><span data-stu-id="c5335-103">ID3DXEffect::BeginPass method</span></span>

<span data-ttu-id="c5335-104">在主動技術內開始進行。</span><span class="sxs-lookup"><span data-stu-id="c5335-104">Begins a pass, within the active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="c5335-105">語法</span><span class="sxs-lookup"><span data-stu-id="c5335-105">Syntax</span></span>


```C++
HRESULT BeginPass(
  [in] UINT Pass
);
```



## <a name="parameters"></a><span data-ttu-id="c5335-106">參數</span><span class="sxs-lookup"><span data-stu-id="c5335-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5335-107">*Pass* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5335-107">*Pass* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5335-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="c5335-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="c5335-109">技術中以零為基底的整數索引。</span><span class="sxs-lookup"><span data-stu-id="c5335-109">A zero-based integer index into the technique.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5335-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5335-110">Return value</span></span>

<span data-ttu-id="c5335-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="c5335-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="c5335-112">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="c5335-112">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="c5335-113">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="c5335-113">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5335-114">備註</span><span class="sxs-lookup"><span data-stu-id="c5335-114">Remarks</span></span>

<span data-ttu-id="c5335-115">應用程式會藉由呼叫 **ID3DXEffect：： BeginPass**，在效果系統內的一個作用中的) 技巧內設定一個主動傳遞 (。</span><span class="sxs-lookup"><span data-stu-id="c5335-115">An application sets one active pass (within one active technique) in the effect system by calling **ID3DXEffect::BeginPass**.</span></span> <span data-ttu-id="c5335-116">應用程式會藉由呼叫 [**ID3DXEffect：： EndPass**](id3dxeffect--endpass.md)來表示主動傳遞的結尾。</span><span class="sxs-lookup"><span data-stu-id="c5335-116">An application signals the end of the active pass by calling [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md).</span></span> <span data-ttu-id="c5335-117">**ID3DXEffect：： BeginPass** 和 **ID3DXEffect：： EndPass** 必須在成對的 [**ID3DXEffect：： Begin**](id3dxeffect--begin.md) 和 [**ID3DXEffect：： End**](id3dxeffect--end.md) 呼叫內的配對配對中進行。</span><span class="sxs-lookup"><span data-stu-id="c5335-117">**ID3DXEffect::BeginPass** and **ID3DXEffect::EndPass** must occur in a matching pair, within a matching pair of [**ID3DXEffect::Begin**](id3dxeffect--begin.md) and [**ID3DXEffect::End**](id3dxeffect--end.md) calls.</span></span>

<span data-ttu-id="c5335-118">如果應用程式使用 **ID3DXEffect：： BeginPass** ID3DXEffect：： EndPass 比對配對內的任何 [**effect：： Setx**](id3dxeffect.md)方法來變更任何效果狀態 / [](id3dxeffect--endpass.md) ，則應用程式必須呼叫 [**ID3DXEffect：： CommitChanges**](id3dxeffect--commitchanges.md) ，以設定狀態變更的裝置更新。</span><span class="sxs-lookup"><span data-stu-id="c5335-118">If the application changes any effect state using any of the [**Effect::Setx**](id3dxeffect.md) methods inside of a **ID3DXEffect::BeginPass**/[**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) matching pair, the application must call [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) to set the update the device with the state changes.</span></span> <span data-ttu-id="c5335-119">如果 **ID3DXEffect：： BeginPass** 和 **ID3DXEffect：： EndPass** 比對配對中沒有發生狀態變更，則不需要呼叫 **ID3DXEffect：： CommitChanges**。</span><span class="sxs-lookup"><span data-stu-id="c5335-119">If no state changes occur within a **ID3DXEffect::BeginPass** and **ID3DXEffect::EndPass** matching pair, it is not necessary to call **ID3DXEffect::CommitChanges**.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5335-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5335-120">Requirements</span></span>



| <span data-ttu-id="c5335-121">需求</span><span class="sxs-lookup"><span data-stu-id="c5335-121">Requirement</span></span> | <span data-ttu-id="c5335-122">值</span><span class="sxs-lookup"><span data-stu-id="c5335-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="c5335-123">標頭</span><span class="sxs-lookup"><span data-stu-id="c5335-123">Header</span></span><br/>  | <dl> <span data-ttu-id="c5335-124"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="c5335-124"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="c5335-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="c5335-125">Library</span></span><br/> | <dl> <span data-ttu-id="c5335-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="c5335-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="c5335-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="c5335-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="c5335-128">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="c5335-128">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
