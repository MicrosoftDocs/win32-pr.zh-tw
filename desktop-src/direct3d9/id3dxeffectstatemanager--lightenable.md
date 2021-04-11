---
description: 必須由使用者執行以啟用/停用燈光的回呼函數。
ms.assetid: 11522ca3-8a2f-4767-a6e6-4186cb4f3115
title: 'ID3DXEffectStateManager：： LightEnable 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.LightEnable
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: d065540eb036b26cdd19791dc393d32c5b45e3ee
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196342"
---
# <a name="id3dxeffectstatemanagerlightenable-method"></a><span data-ttu-id="009f7-103">ID3DXEffectStateManager：： LightEnable 方法</span><span class="sxs-lookup"><span data-stu-id="009f7-103">ID3DXEffectStateManager::LightEnable method</span></span>

<span data-ttu-id="009f7-104">必須由使用者執行以啟用/停用燈光的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="009f7-104">A callback function that must be implemented by a user to enable/disable a light.</span></span>

## <a name="syntax"></a><span data-ttu-id="009f7-105">語法</span><span class="sxs-lookup"><span data-stu-id="009f7-105">Syntax</span></span>


```C++
HRESULT LightEnable(
  [in] DWORD Index,
  [in] BOOL  Enable
);
```



## <a name="parameters"></a><span data-ttu-id="009f7-106">參數</span><span class="sxs-lookup"><span data-stu-id="009f7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="009f7-107">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="009f7-107">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="009f7-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="009f7-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="009f7-109">光線以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="009f7-109">The zero-based index of the light.</span></span> <span data-ttu-id="009f7-110">這是 [**IDirect3DDevice9：： SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight)中的相同索引。</span><span class="sxs-lookup"><span data-stu-id="009f7-110">This is the same index in [**IDirect3DDevice9::SetLight**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setlight).</span></span>

</dd> <dt>

<span data-ttu-id="009f7-111">*啟用* \[在\]</span><span class="sxs-lookup"><span data-stu-id="009f7-111">*Enable* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="009f7-112">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="009f7-112">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="009f7-113">True 表示啟用淺色，否則為 false。</span><span class="sxs-lookup"><span data-stu-id="009f7-113">True to enable the light, false otherwise.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="009f7-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="009f7-114">Return value</span></span>

<span data-ttu-id="009f7-115">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="009f7-115">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="009f7-116">使用者執行的方法應該會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="009f7-116">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="009f7-117">如果回呼在設定裝置狀態時失敗，將會發生下列其中一種情況：</span><span class="sxs-lookup"><span data-stu-id="009f7-117">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="009f7-118">[**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)期間的效果將會失敗。</span><span class="sxs-lookup"><span data-stu-id="009f7-118">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="009f7-119">動態效果狀態呼叫 (例如 [**IDirect3DDevice9：： LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)) 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="009f7-119">The dynamic effect state call (such as [**IDirect3DDevice9::LightEnable**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-lightenable)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="009f7-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="009f7-120">Requirements</span></span>



| <span data-ttu-id="009f7-121">需求</span><span class="sxs-lookup"><span data-stu-id="009f7-121">Requirement</span></span> | <span data-ttu-id="009f7-122">值</span><span class="sxs-lookup"><span data-stu-id="009f7-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="009f7-123">標頭</span><span class="sxs-lookup"><span data-stu-id="009f7-123">Header</span></span><br/>  | <dl> <span data-ttu-id="009f7-124"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="009f7-124"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="009f7-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="009f7-125">Library</span></span><br/> | <dl> <span data-ttu-id="009f7-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="009f7-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="009f7-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="009f7-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="009f7-128">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="009f7-128">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
