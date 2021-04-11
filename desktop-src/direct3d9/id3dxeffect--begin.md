---
description: 啟動使用中的技術。
ms.assetid: 6598d77b-8b53-4f2d-aa43-adf358ad486d
title: 'ID3DXEffect：： Begin 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.Begin
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1912698fbb6d6ac13f119161c4d05926f05d245b
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196291"
---
# <a name="id3dxeffectbegin-method"></a><span data-ttu-id="1926d-103">ID3DXEffect：： Begin 方法</span><span class="sxs-lookup"><span data-stu-id="1926d-103">ID3DXEffect::Begin method</span></span>

<span data-ttu-id="1926d-104">啟動使用中的技術。</span><span class="sxs-lookup"><span data-stu-id="1926d-104">Starts an active technique.</span></span>

## <a name="syntax"></a><span data-ttu-id="1926d-105">語法</span><span class="sxs-lookup"><span data-stu-id="1926d-105">Syntax</span></span>


```C++
HRESULT Begin(
  [out] UINT  *pPasses,
  [in]  DWORD Flags
);
```



## <a name="parameters"></a><span data-ttu-id="1926d-106">參數</span><span class="sxs-lookup"><span data-stu-id="1926d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1926d-107">*pPasses* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="1926d-107">*pPasses* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="1926d-108">類型： **[ **UINT**](../winprog/windows-data-types.md)\***</span><span class="sxs-lookup"><span data-stu-id="1926d-108">Type: **[**UINT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="1926d-109">傳回值的指標，指出轉譯目前技術所需的傳遞數目。</span><span class="sxs-lookup"><span data-stu-id="1926d-109">Pointer to a value returned that indicates the number of passes needed to render the current technique.</span></span>

</dd> <dt>

<span data-ttu-id="1926d-110">*Flags* \[in\]</span><span class="sxs-lookup"><span data-stu-id="1926d-110">*Flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1926d-111">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="1926d-111">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="1926d-112">DWORD，可決定是否儲存並還原由效果修改的狀態。</span><span class="sxs-lookup"><span data-stu-id="1926d-112">DWORD that determines if state modified by an effect is saved and restored.</span></span> <span data-ttu-id="1926d-113">預設值0指定 **ID3DXEffect：： Begin** 和 [**ID3DXEffect：： End**](id3dxeffect--end.md) 會儲存並還原效果所修改的所有狀態 (包括圖元和頂點著色器常數) 。</span><span class="sxs-lookup"><span data-stu-id="1926d-113">The default value 0 specifies that **ID3DXEffect::Begin** and [**ID3DXEffect::End**](id3dxeffect--end.md) will save and restore all state modified by the effect (including pixel and vertex shader constants).</span></span> <span data-ttu-id="1926d-114">有效的旗標可在有效的 [狀態儲存和還原旗標](d3dxfx.md)中看到。</span><span class="sxs-lookup"><span data-stu-id="1926d-114">Valid flags can be seen at [Effect State Save and Restore Flags](d3dxfx.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1926d-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="1926d-115">Return value</span></span>

<span data-ttu-id="1926d-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1926d-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1926d-117">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="1926d-117">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="1926d-118">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="1926d-118">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="1926d-119">備註</span><span class="sxs-lookup"><span data-stu-id="1926d-119">Remarks</span></span>

<span data-ttu-id="1926d-120">應用程式會藉由呼叫 **ID3DXEffect：： Begin**，在效果系統中設定一個有效的技術。</span><span class="sxs-lookup"><span data-stu-id="1926d-120">An application sets one active technique in the effect system by calling **ID3DXEffect::Begin**.</span></span> <span data-ttu-id="1926d-121">效果系統會藉由捕捉狀態欄塊中的技術可變更的所有管線狀態來進行回應。</span><span class="sxs-lookup"><span data-stu-id="1926d-121">The effect system responds by capturing all the pipeline state that can be changed by the technique in a state block.</span></span> <span data-ttu-id="1926d-122">應用程式會藉由呼叫 [**ID3DXEffect：： end**](id3dxeffect--end.md)（使用狀態欄塊來還原原始狀態）來發出技術的結尾。</span><span class="sxs-lookup"><span data-stu-id="1926d-122">An application signals the end of a technique by calling [**ID3DXEffect::End**](id3dxeffect--end.md), which uses the state block to restore the original state.</span></span> <span data-ttu-id="1926d-123">因此，效果系統會在技術變成作用中時，負責儲存狀態，並在技術結束時還原狀態。</span><span class="sxs-lookup"><span data-stu-id="1926d-123">The effect system, therefore, takes care of saving state when a technique becomes active and restoring state when a technique ends.</span></span> <span data-ttu-id="1926d-124">如果您選擇停用此儲存和還原功能，請參閱 [D3DXFX \_ DONOTSAVESAMPLERSTATE](d3dxfx.md)。</span><span class="sxs-lookup"><span data-stu-id="1926d-124">If you choose to disable this save and restore functionality, see [D3DXFX\_DONOTSAVESAMPLERSTATE](d3dxfx.md).</span></span>

<span data-ttu-id="1926d-125">在 **ID3DXEffect：： Begin** 和 [**ID3DXEffect：： End**](id3dxeffect--end.md) 配對中，應用程式會使用 [**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md) 來設定使用中的 pass、 [**ID3DXEffect：： CommitChanges**](id3dxeffect--commitchanges.md) （如果啟動成功後發生任何狀態變更），並使用 [**ID3DXEffect：： EndPass**](id3dxeffect--endpass.md) 結束主動傳遞。</span><span class="sxs-lookup"><span data-stu-id="1926d-125">Within the **ID3DXEffect::Begin** and [**ID3DXEffect::End**](id3dxeffect--end.md) pair, an application uses [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md) to set the active pass, [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md) if any state changes occurred after the pass was activated, and [**ID3DXEffect::EndPass**](id3dxeffect--endpass.md) to end the active pass.</span></span>

## <a name="requirements"></a><span data-ttu-id="1926d-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="1926d-126">Requirements</span></span>



| <span data-ttu-id="1926d-127">需求</span><span class="sxs-lookup"><span data-stu-id="1926d-127">Requirement</span></span> | <span data-ttu-id="1926d-128">值</span><span class="sxs-lookup"><span data-stu-id="1926d-128">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1926d-129">標頭</span><span class="sxs-lookup"><span data-stu-id="1926d-129">Header</span></span><br/>  | <dl> <span data-ttu-id="1926d-130"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="1926d-130"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="1926d-131">程式庫</span><span class="sxs-lookup"><span data-stu-id="1926d-131">Library</span></span><br/> | <dl> <span data-ttu-id="1926d-132"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1926d-132"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1926d-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1926d-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1926d-134">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="1926d-134">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
