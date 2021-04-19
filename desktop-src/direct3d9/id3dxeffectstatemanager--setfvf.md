---
description: 必須由使用者執行來設定 FVF 程式碼的回呼函式。
ms.assetid: 701a4333-a71e-4d84-a06c-1c86312ee4ff
title: 'ID3DXEffectStateManager：： SetFVF 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetFVF
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: a68ab07e4f486a8df80ecde5844739a6a010c2dc
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106982888"
---
# <a name="id3dxeffectstatemanagersetfvf-method"></a><span data-ttu-id="ebe3d-103">ID3DXEffectStateManager：： SetFVF 方法</span><span class="sxs-lookup"><span data-stu-id="ebe3d-103">ID3DXEffectStateManager::SetFVF method</span></span>

<span data-ttu-id="ebe3d-104">必須由使用者執行來設定 FVF 程式碼的回呼函式。</span><span class="sxs-lookup"><span data-stu-id="ebe3d-104">A callback function that must be implemented by a user to set a FVF code.</span></span>

## <a name="syntax"></a><span data-ttu-id="ebe3d-105">語法</span><span class="sxs-lookup"><span data-stu-id="ebe3d-105">Syntax</span></span>


```C++
HRESULT SetFVF(
  [in] DWORD FVF
);
```



## <a name="parameters"></a><span data-ttu-id="ebe3d-106">參數</span><span class="sxs-lookup"><span data-stu-id="ebe3d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ebe3d-107">*FVF* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ebe3d-107">*FVF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ebe3d-108">類型： **[ **DWORD**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="ebe3d-108">Type: **[**DWORD**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="ebe3d-109">FVF 常數，決定如何解讀頂點資料。</span><span class="sxs-lookup"><span data-stu-id="ebe3d-109">The FVF constant, that determines how to interpret vertex data.</span></span> <span data-ttu-id="ebe3d-110">請參閱 [D3DFVF](d3dfvf.md)。</span><span class="sxs-lookup"><span data-stu-id="ebe3d-110">See [D3DFVF](d3dfvf.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ebe3d-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="ebe3d-111">Return value</span></span>

<span data-ttu-id="ebe3d-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="ebe3d-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="ebe3d-113">使用者執行的方法應該會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="ebe3d-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="ebe3d-114">如果回呼在設定裝置狀態時失敗，將會發生下列其中一種情況：</span><span class="sxs-lookup"><span data-stu-id="ebe3d-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="ebe3d-115">[**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)期間的效果將會失敗。</span><span class="sxs-lookup"><span data-stu-id="ebe3d-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="ebe3d-116">動態效果狀態呼叫 (例如 [**IDirect3DDevice9：： SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf)) 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="ebe3d-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetFVF**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setfvf)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="ebe3d-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="ebe3d-117">Requirements</span></span>



| <span data-ttu-id="ebe3d-118">需求</span><span class="sxs-lookup"><span data-stu-id="ebe3d-118">Requirement</span></span> | <span data-ttu-id="ebe3d-119">值</span><span class="sxs-lookup"><span data-stu-id="ebe3d-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="ebe3d-120">標頭</span><span class="sxs-lookup"><span data-stu-id="ebe3d-120">Header</span></span><br/>  | <dl> <span data-ttu-id="ebe3d-121"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="ebe3d-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="ebe3d-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="ebe3d-122">Library</span></span><br/> | <dl> <span data-ttu-id="ebe3d-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="ebe3d-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="ebe3d-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ebe3d-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ebe3d-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="ebe3d-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
