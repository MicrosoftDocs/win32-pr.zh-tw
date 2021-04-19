---
description: 必須由使用者執行來設定轉譯狀態的回呼函式。
ms.assetid: a5a27e30-c141-44a4-b8d4-38c1d6076b2a
title: 'ID3DXEffectStateManager：： Graphicsdevice 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetRenderState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 111ab8ff379d5b095500101674fc45b6a2b31bc1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106997405"
---
# <a name="id3dxeffectstatemanagersetrenderstate-method"></a><span data-ttu-id="28e62-103">ID3DXEffectStateManager：： Graphicsdevice 方法</span><span class="sxs-lookup"><span data-stu-id="28e62-103">ID3DXEffectStateManager::SetRenderState method</span></span>

<span data-ttu-id="28e62-104">必須由使用者執行來設定轉譯狀態的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="28e62-104">A callback function that must be implemented by a user to set render state.</span></span>

## <a name="syntax"></a><span data-ttu-id="28e62-105">語法</span><span class="sxs-lookup"><span data-stu-id="28e62-105">Syntax</span></span>


```C++
HRESULT SetRenderState(
  [in] D3DRENDERSTATETYPE State,
  [in] DWORD              Value
);
```



## <a name="parameters"></a><span data-ttu-id="28e62-106">參數</span><span class="sxs-lookup"><span data-stu-id="28e62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="28e62-107">*狀態* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28e62-107">*State* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e62-108">類型： **[ **D3DRENDERSTATETYPE**](./d3drenderstatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="28e62-108">Type: **[**D3DRENDERSTATETYPE**](./d3drenderstatetype.md)**</span></span>

<span data-ttu-id="28e62-109">要設定的呈現狀態。</span><span class="sxs-lookup"><span data-stu-id="28e62-109">The render state to set.</span></span> [<span data-ttu-id="28e62-110">**D3DRENDERSTATETYPE**</span><span class="sxs-lookup"><span data-stu-id="28e62-110">**D3DRENDERSTATETYPE**</span></span>](./d3drenderstatetype.md)

</dd> <dt>

<span data-ttu-id="28e62-111">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="28e62-111">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="28e62-112">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="28e62-112">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="28e62-113">呈現狀態值。</span><span class="sxs-lookup"><span data-stu-id="28e62-113">The render state value.</span></span> <span data-ttu-id="28e62-114">請參閱 [效果狀態 (Direct3D 9) ](effect-states.md)。</span><span class="sxs-lookup"><span data-stu-id="28e62-114">See [Effect States (Direct3D 9)](effect-states.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="28e62-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="28e62-115">Return value</span></span>

<span data-ttu-id="28e62-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="28e62-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="28e62-117">使用者執行的方法應該會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="28e62-117">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="28e62-118">如果回呼在設定裝置狀態時失敗，將會發生下列其中一種情況：</span><span class="sxs-lookup"><span data-stu-id="28e62-118">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="28e62-119">[**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)期間的效果將會失敗。</span><span class="sxs-lookup"><span data-stu-id="28e62-119">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="28e62-120">動態效果狀態呼叫 (例如 [**IDirect3DDevice9：： graphicsdevice**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="28e62-120">The dynamic effect state call (such as [**IDirect3DDevice9::SetRenderState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setrenderstate)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="28e62-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="28e62-121">Requirements</span></span>



| <span data-ttu-id="28e62-122">需求</span><span class="sxs-lookup"><span data-stu-id="28e62-122">Requirement</span></span> | <span data-ttu-id="28e62-123">值</span><span class="sxs-lookup"><span data-stu-id="28e62-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="28e62-124">標頭</span><span class="sxs-lookup"><span data-stu-id="28e62-124">Header</span></span><br/>  | <dl> <span data-ttu-id="28e62-125"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="28e62-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="28e62-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="28e62-126">Library</span></span><br/> | <dl> <span data-ttu-id="28e62-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="28e62-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="28e62-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="28e62-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="28e62-129">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="28e62-129">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
