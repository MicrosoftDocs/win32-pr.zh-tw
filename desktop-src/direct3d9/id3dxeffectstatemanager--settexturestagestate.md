---
description: 必須由使用者執行以設定材質階段狀態的回呼函式。
ms.assetid: cc86a483-ccf0-400d-b14d-ab55a3cf4b98
title: 'ID3DXEffectStateManager：： SetTextureStageState 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTextureStageState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 937fd3f2b89dc093d9dceb9441f53d6be2cb06b5
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999027"
---
# <a name="id3dxeffectstatemanagersettexturestagestate-method"></a><span data-ttu-id="49c91-103">ID3DXEffectStateManager：： SetTextureStageState 方法</span><span class="sxs-lookup"><span data-stu-id="49c91-103">ID3DXEffectStateManager::SetTextureStageState method</span></span>

<span data-ttu-id="49c91-104">必須由使用者執行以設定材質階段狀態的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="49c91-104">A callback function that must be implemented by a user to set the texture stage state.</span></span>

## <a name="syntax"></a><span data-ttu-id="49c91-105">語法</span><span class="sxs-lookup"><span data-stu-id="49c91-105">Syntax</span></span>


```C++
HRESULT SetTextureStageState(
  [in] DWORD                    Stage,
  [in] D3DTEXTURESTAGESTATETYPE Type,
  [in] DWORD                    Value
);
```



## <a name="parameters"></a><span data-ttu-id="49c91-106">參數</span><span class="sxs-lookup"><span data-stu-id="49c91-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49c91-107">*Stage* \[in\]</span><span class="sxs-lookup"><span data-stu-id="49c91-107">*Stage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49c91-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49c91-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="49c91-109">材質指派給的階段。</span><span class="sxs-lookup"><span data-stu-id="49c91-109">The stage that the texture is assigned to.</span></span> <span data-ttu-id="49c91-110">這是 [**IDirect3DDevice9：： SetTexture**](/windows/desktop/api) 或 [**IDirect3DDevice9：： SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)中的索引值。</span><span class="sxs-lookup"><span data-stu-id="49c91-110">This is the index value in [**IDirect3DDevice9::SetTexture**](/windows/desktop/api) or [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span></span>

</dd> <dt>

<span data-ttu-id="49c91-111">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49c91-111">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49c91-112">類型： **[ **D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="49c91-112">Type: **[**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)**</span></span>

<span data-ttu-id="49c91-113">定義紋理階段將執行的作業類型。</span><span class="sxs-lookup"><span data-stu-id="49c91-113">Defines the type of operation that a texture stage will perform.</span></span> <span data-ttu-id="49c91-114">請參閱 [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md)。</span><span class="sxs-lookup"><span data-stu-id="49c91-114">See [**D3DTEXTURESTAGESTATETYPE**](./d3dtexturestagestatetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="49c91-115">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="49c91-115">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49c91-116">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="49c91-116">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="49c91-117">可以是 ([**D3DTEXTUREOP**](./d3dtextureop.md)) 的作業，或是 ([D3DTA](d3dta.md)) 的引數值（視選擇的類型而定）。</span><span class="sxs-lookup"><span data-stu-id="49c91-117">Can be either an operation ([**D3DTEXTUREOP**](./d3dtextureop.md)) or an argument value ([D3DTA](d3dta.md)), depending on what is chosen for Type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="49c91-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="49c91-118">Return value</span></span>

<span data-ttu-id="49c91-119">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="49c91-119">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="49c91-120">使用者執行的方法應該會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="49c91-120">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="49c91-121">如果回呼在設定裝置狀態時失敗，將會發生下列其中一種情況：</span><span class="sxs-lookup"><span data-stu-id="49c91-121">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="49c91-122">[**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)期間的效果將會失敗。</span><span class="sxs-lookup"><span data-stu-id="49c91-122">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="49c91-123">動態效果狀態呼叫 (例如 [**IDirect3DDevice9：： SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)) 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="49c91-123">The dynamic effect state call (such as [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="49c91-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="49c91-124">Requirements</span></span>



| <span data-ttu-id="49c91-125">需求</span><span class="sxs-lookup"><span data-stu-id="49c91-125">Requirement</span></span> | <span data-ttu-id="49c91-126">值</span><span class="sxs-lookup"><span data-stu-id="49c91-126">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="49c91-127">標頭</span><span class="sxs-lookup"><span data-stu-id="49c91-127">Header</span></span><br/>  | <dl> <span data-ttu-id="49c91-128"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="49c91-128"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="49c91-129">程式庫</span><span class="sxs-lookup"><span data-stu-id="49c91-129">Library</span></span><br/> | <dl> <span data-ttu-id="49c91-130"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="49c91-130"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="49c91-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="49c91-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="49c91-132">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="49c91-132">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
