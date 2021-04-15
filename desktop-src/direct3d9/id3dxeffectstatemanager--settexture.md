---
description: 必須由使用者執行以設定材質的回呼函式。
ms.assetid: 971802f4-ea7a-4906-83b8-0cd83111716e
title: 'ID3DXEffectStateManager：： SetTexture 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTexture
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b395c19b65bb39b8328da24f727292f7dbe2a0f2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514641"
---
# <a name="id3dxeffectstatemanagersettexture-method"></a><span data-ttu-id="f13c7-103">ID3DXEffectStateManager：： SetTexture 方法</span><span class="sxs-lookup"><span data-stu-id="f13c7-103">ID3DXEffectStateManager::SetTexture method</span></span>

<span data-ttu-id="f13c7-104">必須由使用者執行以設定材質的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="f13c7-104">A callback function that must be implemented by a user to set a texture.</span></span>

## <a name="syntax"></a><span data-ttu-id="f13c7-105">語法</span><span class="sxs-lookup"><span data-stu-id="f13c7-105">Syntax</span></span>


```C++
HRESULT SetTexture(
  [in] DWORD                  Stage,
  [in] LPDIRECT3DBASETEXTURE9 pTexture
);
```



## <a name="parameters"></a><span data-ttu-id="f13c7-106">參數</span><span class="sxs-lookup"><span data-stu-id="f13c7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f13c7-107">*Stage* \[in\]</span><span class="sxs-lookup"><span data-stu-id="f13c7-107">*Stage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f13c7-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f13c7-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f13c7-109">要指派紋理的階段。</span><span class="sxs-lookup"><span data-stu-id="f13c7-109">The stage to which the texture is assigned.</span></span> <span data-ttu-id="f13c7-110">這是 [**IDirect3DDevice9：： SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) 或 [**IDirect3DDevice9：： SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate)中的索引值。</span><span class="sxs-lookup"><span data-stu-id="f13c7-110">This is the index value in [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture) or [**IDirect3DDevice9::SetTextureStageState**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexturestagestate).</span></span>

</dd> <dt>

<span data-ttu-id="f13c7-111">*pTexture* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f13c7-111">*pTexture* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f13c7-112">類型： **[ **LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span><span class="sxs-lookup"><span data-stu-id="f13c7-112">Type: **[**LPDIRECT3DBASETEXTURE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)**</span></span>

<span data-ttu-id="f13c7-113">紋理物件的指標。</span><span class="sxs-lookup"><span data-stu-id="f13c7-113">A pointer to the texture object.</span></span> <span data-ttu-id="f13c7-114">這可以是任何 Direct3D 材質類型 (cube、磁片區等 ) 。</span><span class="sxs-lookup"><span data-stu-id="f13c7-114">This can be any of the Direct3D texture types (cube, volume, etc.).</span></span> <span data-ttu-id="f13c7-115">請參閱 [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9)。</span><span class="sxs-lookup"><span data-stu-id="f13c7-115">See [**IDirect3DBaseTexture9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dbasetexture9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f13c7-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="f13c7-116">Return value</span></span>

<span data-ttu-id="f13c7-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f13c7-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f13c7-118">使用者執行的方法應該會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="f13c7-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="f13c7-119">如果回呼在設定裝置狀態時失敗，將會發生下列其中一種情況：</span><span class="sxs-lookup"><span data-stu-id="f13c7-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="f13c7-120">[**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)期間的效果將會失敗。</span><span class="sxs-lookup"><span data-stu-id="f13c7-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="f13c7-121">動態效果狀態呼叫 (例如 [**IDirect3DDevice9：： SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)) 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="f13c7-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetTexture**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settexture)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="f13c7-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="f13c7-122">Requirements</span></span>



| <span data-ttu-id="f13c7-123">需求</span><span class="sxs-lookup"><span data-stu-id="f13c7-123">Requirement</span></span> | <span data-ttu-id="f13c7-124">值</span><span class="sxs-lookup"><span data-stu-id="f13c7-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f13c7-125">標頭</span><span class="sxs-lookup"><span data-stu-id="f13c7-125">Header</span></span><br/>  | <dl> <span data-ttu-id="f13c7-126"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="f13c7-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="f13c7-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="f13c7-127">Library</span></span><br/> | <dl> <span data-ttu-id="f13c7-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f13c7-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="f13c7-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f13c7-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f13c7-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="f13c7-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
