---
description: 必須由使用者執行以設定圖元著色器的回呼函數。
ms.assetid: 4124eff2-1d88-429c-b7ed-8d87155b5ddc
title: 'ID3DXEffectStateManager：： SetPixelShader 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShader
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 71a16bc267df95ed7efc1e0f74871b131e34ebe1
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104514645"
---
# <a name="id3dxeffectstatemanagersetpixelshader-method"></a><span data-ttu-id="9cc08-103">ID3DXEffectStateManager：： SetPixelShader 方法</span><span class="sxs-lookup"><span data-stu-id="9cc08-103">ID3DXEffectStateManager::SetPixelShader method</span></span>

<span data-ttu-id="9cc08-104">必須由使用者執行以設定圖元著色器的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="9cc08-104">A callback function that must be implemented by a user to set a pixel shader.</span></span>

## <a name="syntax"></a><span data-ttu-id="9cc08-105">語法</span><span class="sxs-lookup"><span data-stu-id="9cc08-105">Syntax</span></span>


```C++
HRESULT SetPixelShader(
  [in] LPDIRECT3DPIXELSHADER9 pShader
);
```



## <a name="parameters"></a><span data-ttu-id="9cc08-106">參數</span><span class="sxs-lookup"><span data-stu-id="9cc08-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9cc08-107">*pShader* \[在\]</span><span class="sxs-lookup"><span data-stu-id="9cc08-107">*pShader* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="9cc08-108">類型： **[ **LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)**</span><span class="sxs-lookup"><span data-stu-id="9cc08-108">Type: **[**LPDIRECT3DPIXELSHADER9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)**</span></span>

<span data-ttu-id="9cc08-109">圖元著色器物件的指標。</span><span class="sxs-lookup"><span data-stu-id="9cc08-109">A pointer to a pixel shader object.</span></span> <span data-ttu-id="9cc08-110">請參閱 [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9)。</span><span class="sxs-lookup"><span data-stu-id="9cc08-110">See [**IDirect3DPixelShader9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3dpixelshader9).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9cc08-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="9cc08-111">Return value</span></span>

<span data-ttu-id="9cc08-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="9cc08-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="9cc08-113">使用者執行的方法應該會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="9cc08-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="9cc08-114">如果回呼在設定裝置狀態時失敗，將會發生下列其中一種情況：</span><span class="sxs-lookup"><span data-stu-id="9cc08-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="9cc08-115">[**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)期間的效果將會失敗。</span><span class="sxs-lookup"><span data-stu-id="9cc08-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="9cc08-116">動態效果狀態呼叫 (例如 [**IDirect3DDevice9：： SetPixelShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader)) 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="9cc08-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetPixelShader**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshader)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="9cc08-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="9cc08-117">Requirements</span></span>



| <span data-ttu-id="9cc08-118">需求</span><span class="sxs-lookup"><span data-stu-id="9cc08-118">Requirement</span></span> | <span data-ttu-id="9cc08-119">值</span><span class="sxs-lookup"><span data-stu-id="9cc08-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="9cc08-120">標頭</span><span class="sxs-lookup"><span data-stu-id="9cc08-120">Header</span></span><br/>  | <dl> <span data-ttu-id="9cc08-121"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="9cc08-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="9cc08-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="9cc08-122">Library</span></span><br/> | <dl> <span data-ttu-id="9cc08-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="9cc08-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="9cc08-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9cc08-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9cc08-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="9cc08-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
