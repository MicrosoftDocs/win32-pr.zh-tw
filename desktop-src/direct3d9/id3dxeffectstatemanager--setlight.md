---
description: 必須由使用者執行以設定燈光的回呼函式。
ms.assetid: 3b9b2cbd-79f5-4ea4-a47b-da23b091adfd
title: 'ID3DXEffectStateManager：： SetLight 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetLight
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 1306283b098922706f39abc7ffe2514d2fba0e5c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106991478"
---
# <a name="id3dxeffectstatemanagersetlight-method"></a><span data-ttu-id="e2e92-103">ID3DXEffectStateManager：： SetLight 方法</span><span class="sxs-lookup"><span data-stu-id="e2e92-103">ID3DXEffectStateManager::SetLight method</span></span>

<span data-ttu-id="e2e92-104">必須由使用者執行以設定燈光的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="e2e92-104">A callback function that must be implemented by a user to set a light.</span></span>

## <a name="syntax"></a><span data-ttu-id="e2e92-105">語法</span><span class="sxs-lookup"><span data-stu-id="e2e92-105">Syntax</span></span>


```C++
HRESULT SetLight(
  [in]       DWORD     Index,
  [in] const D3DLight9 *pLight
);
```



## <a name="parameters"></a><span data-ttu-id="e2e92-106">參數</span><span class="sxs-lookup"><span data-stu-id="e2e92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e2e92-107">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2e92-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e92-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e2e92-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e2e92-109">光線以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="e2e92-109">The zero-based index of the light.</span></span> <span data-ttu-id="e2e92-110">這是 [**IDirect3DDevice9：： SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)中的相同索引。</span><span class="sxs-lookup"><span data-stu-id="e2e92-110">This is the same index in [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span></span>

</dd> <dt>

<span data-ttu-id="e2e92-111">*pLight* \[在\]</span><span class="sxs-lookup"><span data-stu-id="e2e92-111">*pLight* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e2e92-112">Type： **Const [**D3DLight9**](d3dlight9.md) \***</span><span class="sxs-lookup"><span data-stu-id="e2e92-112">Type: **const [**D3DLight9**](d3dlight9.md)\***</span></span>

<span data-ttu-id="e2e92-113">光源物件。</span><span class="sxs-lookup"><span data-stu-id="e2e92-113">The light object.</span></span> <span data-ttu-id="e2e92-114">請參閱 [**D3DLIGHT9**](d3dlight9.md)。</span><span class="sxs-lookup"><span data-stu-id="e2e92-114">See [**D3DLIGHT9**](d3dlight9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e2e92-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="e2e92-115">Return value</span></span>

<span data-ttu-id="e2e92-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e2e92-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e2e92-117">使用者執行的方法應該會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="e2e92-117">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="e2e92-118">如果回呼在設定裝置狀態時失敗，將會發生下列其中一種情況：</span><span class="sxs-lookup"><span data-stu-id="e2e92-118">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="e2e92-119">[**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)期間的效果將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e2e92-119">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="e2e92-120">動態效果狀態呼叫 (例如 [**IDirect3DDevice9：： SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)) 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e2e92-120">The dynamic effect state call (such as [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="e2e92-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="e2e92-121">Requirements</span></span>



| <span data-ttu-id="e2e92-122">需求</span><span class="sxs-lookup"><span data-stu-id="e2e92-122">Requirement</span></span> | <span data-ttu-id="e2e92-123">值</span><span class="sxs-lookup"><span data-stu-id="e2e92-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e2e92-124">標頭</span><span class="sxs-lookup"><span data-stu-id="e2e92-124">Header</span></span><br/>  | <dl> <span data-ttu-id="e2e92-125"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="e2e92-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="e2e92-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="e2e92-126">Library</span></span><br/> | <dl> <span data-ttu-id="e2e92-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e2e92-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e2e92-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e2e92-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e2e92-129">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="e2e92-129">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
