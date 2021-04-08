---
description: 必須由使用者執行以設定頂點著色器的回呼函數。
ms.assetid: 8f3d3be3-c073-441d-a318-6d2cd5e7aca5
title: 'ID3DXEffectStateManager：： SetVertexShader 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9fd25158f2aa6ab0a22d6226e8e709c3b498b0e7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103854043"
---
# <a name="id3dxeffectstatemanagersetvertexshader-method"></a><span data-ttu-id="43cd7-103">ID3DXEffectStateManager：： SetVertexShader 方法</span><span class="sxs-lookup"><span data-stu-id="43cd7-103">ID3DXEffectStateManager::SetVertexShader method</span></span>

<span data-ttu-id="43cd7-104">必須由使用者執行以設定頂點著色器的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="43cd7-104">A callback function that must be implemented by a user to set a vertex shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="43cd7-105">語法</span><span class="sxs-lookup"><span data-stu-id="43cd7-105">Syntax</span></span>


```C++
HRESULT SetVertexShader(
  [in] LPDIRECT3DVERTEXSHADER9 pShader
);
```



## <a name="parameters"></a><span data-ttu-id="43cd7-106">參數</span><span class="sxs-lookup"><span data-stu-id="43cd7-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="43cd7-107">*pShader* \[在\]</span><span class="sxs-lookup"><span data-stu-id="43cd7-107">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="43cd7-108">類型： **[ **LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)**</span><span class="sxs-lookup"><span data-stu-id="43cd7-108">Type: **[**LPDIRECT3DVERTEXSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)**</span></span>

<span data-ttu-id="43cd7-109">頂點著色器物件的指標。</span><span class="sxs-lookup"><span data-stu-id="43cd7-109">A pointer to a vertex shader object.</span></span> <span data-ttu-id="43cd7-110">請參閱 [**IDirect3DVertexShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9)。</span><span class="sxs-lookup"><span data-stu-id="43cd7-110">See [**IDirect3DVertexShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dvertexshader9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="43cd7-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="43cd7-111">Return value</span></span>

<span data-ttu-id="43cd7-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="43cd7-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="43cd7-113">使用者執行的方法應該會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="43cd7-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="43cd7-114">如果回呼在設定裝置狀態時失敗，將會發生下列其中一種情況：</span><span class="sxs-lookup"><span data-stu-id="43cd7-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="43cd7-115">[**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)期間的效果將會失敗。</span><span class="sxs-lookup"><span data-stu-id="43cd7-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="43cd7-116">動態效果狀態呼叫 (例如 [**IDirect3DDevice9：： SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)) 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="43cd7-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshader)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="43cd7-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="43cd7-117">Requirements</span></span>



| <span data-ttu-id="43cd7-118">需求</span><span class="sxs-lookup"><span data-stu-id="43cd7-118">Requirement</span></span> | <span data-ttu-id="43cd7-119">值</span><span class="sxs-lookup"><span data-stu-id="43cd7-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="43cd7-120">標頭</span><span class="sxs-lookup"><span data-stu-id="43cd7-120">Header</span></span><br/>  | <dl> <span data-ttu-id="43cd7-121"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="43cd7-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="43cd7-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="43cd7-122">Library</span></span><br/> | <dl> <span data-ttu-id="43cd7-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="43cd7-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="43cd7-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="43cd7-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="43cd7-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="43cd7-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
