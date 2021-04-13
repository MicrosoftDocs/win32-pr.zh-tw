---
description: 必須由使用者所執行的回呼函式，以設定取樣器。
ms.assetid: 1e19e8cd-341d-4372-9182-8b3c82155407
title: 'ID3DXEffectStateManager：： SetSamplerState 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetSamplerState
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: bba12db8dbc1902adc5c64b4cc1726e081dfea70
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104323048"
---
# <a name="id3dxeffectstatemanagersetsamplerstate-method"></a><span data-ttu-id="13273-103">ID3DXEffectStateManager：： SetSamplerState 方法</span><span class="sxs-lookup"><span data-stu-id="13273-103">ID3DXEffectStateManager::SetSamplerState method</span></span>

<span data-ttu-id="13273-104">必須由使用者所執行的回呼函式，以設定取樣器。</span><span class="sxs-lookup"><span data-stu-id="13273-104">A callback function that must be implemented by a user to set a sampler.</span></span>

## <a name="syntax"></a><span data-ttu-id="13273-105">語法</span><span class="sxs-lookup"><span data-stu-id="13273-105">Syntax</span></span>


```C++
HRESULT SetSamplerState(
  [in] DWORD               Sampler,
  [in] D3DSAMPLERSTATETYPE Type,
  [in] DWORD               Value
);
```



## <a name="parameters"></a><span data-ttu-id="13273-106">參數</span><span class="sxs-lookup"><span data-stu-id="13273-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="13273-107">*取樣* \[ 器在\]</span><span class="sxs-lookup"><span data-stu-id="13273-107">*Sampler* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13273-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13273-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="13273-109">以零為基底的取樣器編號。</span><span class="sxs-lookup"><span data-stu-id="13273-109">The zero-based sampler number.</span></span>

</dd> <dt>

<span data-ttu-id="13273-110">*類型* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13273-110">*Type* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13273-111">類型： **[ **D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="13273-111">Type: **[**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)**</span></span>

<span data-ttu-id="13273-112">識別取樣器狀態，可指定篩選、定址或框線色彩。</span><span class="sxs-lookup"><span data-stu-id="13273-112">Identifies sampler state, which can specify the filtering, addressing, or the border color.</span></span> <span data-ttu-id="13273-113">請參閱 [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md)。</span><span class="sxs-lookup"><span data-stu-id="13273-113">See [**D3DSAMPLERSTATETYPE**](./d3dsamplerstatetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="13273-114">*值* \[在\]</span><span class="sxs-lookup"><span data-stu-id="13273-114">*Value* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="13273-115">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="13273-115">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="13273-116">類型中其中一個取樣器狀態類型的值。</span><span class="sxs-lookup"><span data-stu-id="13273-116">A value from one of the sampler state types in Type.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="13273-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="13273-117">Return value</span></span>

<span data-ttu-id="13273-118">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="13273-118">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="13273-119">使用者執行的方法應該會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="13273-119">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="13273-120">如果回呼在設定裝置狀態時失敗，將會發生下列其中一種情況：</span><span class="sxs-lookup"><span data-stu-id="13273-120">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="13273-121">[**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)期間的效果將會失敗。</span><span class="sxs-lookup"><span data-stu-id="13273-121">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="13273-122">動態效果狀態呼叫 (例如 [**IDirect3DDevice9：： SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)) 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="13273-122">The dynamic effect state call (such as [**IDirect3DDevice9::SetSamplerState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setsamplerstate)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="13273-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="13273-123">Requirements</span></span>



| <span data-ttu-id="13273-124">需求</span><span class="sxs-lookup"><span data-stu-id="13273-124">Requirement</span></span> | <span data-ttu-id="13273-125">值</span><span class="sxs-lookup"><span data-stu-id="13273-125">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="13273-126">標頭</span><span class="sxs-lookup"><span data-stu-id="13273-126">Header</span></span><br/>  | <dl> <span data-ttu-id="13273-127"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="13273-127"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="13273-128">程式庫</span><span class="sxs-lookup"><span data-stu-id="13273-128">Library</span></span><br/> | <dl> <span data-ttu-id="13273-129"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="13273-129"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="13273-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13273-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13273-131">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="13273-131">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
