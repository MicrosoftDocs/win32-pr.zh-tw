---
description: 必須由使用者執行以設定材質狀態的回呼函式。
ms.assetid: 4c5e903f-551b-4346-a5eb-301a3a5b9b44
title: 'ID3DXEffectStateManager：： SetMaterial 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetMaterial
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b503bd195468fb323e7e655c0bdd201e25dfdce2
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106998211"
---
# <a name="id3dxeffectstatemanagersetmaterial-method"></a><span data-ttu-id="1778f-103">ID3DXEffectStateManager：： SetMaterial 方法</span><span class="sxs-lookup"><span data-stu-id="1778f-103">ID3DXEffectStateManager::SetMaterial method</span></span>

<span data-ttu-id="1778f-104">必須由使用者執行以設定材質狀態的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="1778f-104">A callback function that must be implemented by a user to set material state.</span></span>

## <a name="syntax"></a><span data-ttu-id="1778f-105">語法</span><span class="sxs-lookup"><span data-stu-id="1778f-105">Syntax</span></span>


```C++
HRESULT SetMaterial(
  [in] const D3DMATERIAL9 *pMaterial
);
```



## <a name="parameters"></a><span data-ttu-id="1778f-106">參數</span><span class="sxs-lookup"><span data-stu-id="1778f-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="1778f-107">*pMaterial* \[在\]</span><span class="sxs-lookup"><span data-stu-id="1778f-107">*pMaterial* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="1778f-108">Type： **Const [**D3DMATERIAL9**](d3dmaterial9.md) \***</span><span class="sxs-lookup"><span data-stu-id="1778f-108">Type: **const [**D3DMATERIAL9**](d3dmaterial9.md)\***</span></span>

<span data-ttu-id="1778f-109">材質狀態的指標。</span><span class="sxs-lookup"><span data-stu-id="1778f-109">A pointer to the material state.</span></span> <span data-ttu-id="1778f-110">請參閱 [**D3DMATERIAL9**](d3dmaterial9.md)。</span><span class="sxs-lookup"><span data-stu-id="1778f-110">See [**D3DMATERIAL9**](d3dmaterial9.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="1778f-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="1778f-111">Return value</span></span>

<span data-ttu-id="1778f-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="1778f-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="1778f-113">使用者執行的方法應該會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="1778f-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="1778f-114">如果回呼在設定裝置狀態時失敗，將會發生下列其中一種情況：</span><span class="sxs-lookup"><span data-stu-id="1778f-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="1778f-115">[**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)期間的效果將會失敗。</span><span class="sxs-lookup"><span data-stu-id="1778f-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="1778f-116">動態效果狀態呼叫 (例如 [**IDirect3DDevice9：： SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)) 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="1778f-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetMaterial**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setmaterial)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="1778f-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="1778f-117">Requirements</span></span>



| <span data-ttu-id="1778f-118">需求</span><span class="sxs-lookup"><span data-stu-id="1778f-118">Requirement</span></span> | <span data-ttu-id="1778f-119">值</span><span class="sxs-lookup"><span data-stu-id="1778f-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="1778f-120">標頭</span><span class="sxs-lookup"><span data-stu-id="1778f-120">Header</span></span><br/>  | <dl> <span data-ttu-id="1778f-121"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="1778f-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="1778f-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="1778f-122">Library</span></span><br/> | <dl> <span data-ttu-id="1778f-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="1778f-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="1778f-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1778f-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="1778f-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="1778f-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
