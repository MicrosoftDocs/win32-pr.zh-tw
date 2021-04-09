---
description: 必須由使用者執行的回呼函式，以設定 N 個修補程式的細分區段數目。
ms.assetid: f94910ee-3385-44d3-b4f1-a0e88c7afa39
title: 'ID3DXEffectStateManager：： SetNPatchMode 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetNPatchMode
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 9b8725a0482b6945b04013df43d34a502f25b7b9
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946248"
---
# <a name="id3dxeffectstatemanagersetnpatchmode-method"></a><span data-ttu-id="b1142-103">ID3DXEffectStateManager：： SetNPatchMode 方法</span><span class="sxs-lookup"><span data-stu-id="b1142-103">ID3DXEffectStateManager::SetNPatchMode method</span></span>

<span data-ttu-id="b1142-104">必須由使用者執行的回呼函式，以設定 N 個修補程式的細分區段數目。</span><span class="sxs-lookup"><span data-stu-id="b1142-104">A callback function that must be implemented by a user to set the number of subdivision segments for N-patches.</span></span>

## <a name="syntax"></a><span data-ttu-id="b1142-105">語法</span><span class="sxs-lookup"><span data-stu-id="b1142-105">Syntax</span></span>


```C++
HRESULT SetNPatchMode(
  [in] FLOAT nSegments
);
```



## <a name="parameters"></a><span data-ttu-id="b1142-106">參數</span><span class="sxs-lookup"><span data-stu-id="b1142-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="b1142-107">*nSegments* \[在\]</span><span class="sxs-lookup"><span data-stu-id="b1142-107">*nSegments* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="b1142-108">類型： **[ **FLOAT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="b1142-108">Type: **[**FLOAT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="b1142-109">將表面分成這個數目的細分。</span><span class="sxs-lookup"><span data-stu-id="b1142-109">Break the surface into this number of subdivisions.</span></span> <span data-ttu-id="b1142-110">這與 [**IDirect3DDevice9：： SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)所使用的數位相同。</span><span class="sxs-lookup"><span data-stu-id="b1142-110">This is the same as the number used by [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="b1142-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="b1142-111">Return value</span></span>

<span data-ttu-id="b1142-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="b1142-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="b1142-113">使用者執行的方法應該會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="b1142-113">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="b1142-114">如果回呼在設定裝置狀態時失敗，將會發生下列其中一種情況：</span><span class="sxs-lookup"><span data-stu-id="b1142-114">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="b1142-115">[**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)期間的效果將會失敗。</span><span class="sxs-lookup"><span data-stu-id="b1142-115">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="b1142-116">動態效果狀態呼叫 (例如 [**IDirect3DDevice9：： SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)) 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="b1142-116">The dynamic effect state call (such as [**IDirect3DDevice9::SetNPatchMode**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setnpatchmode)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="b1142-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="b1142-117">Requirements</span></span>



| <span data-ttu-id="b1142-118">需求</span><span class="sxs-lookup"><span data-stu-id="b1142-118">Requirement</span></span> | <span data-ttu-id="b1142-119">值</span><span class="sxs-lookup"><span data-stu-id="b1142-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="b1142-120">標頭</span><span class="sxs-lookup"><span data-stu-id="b1142-120">Header</span></span><br/>  | <dl> <span data-ttu-id="b1142-121"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="b1142-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="b1142-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="b1142-122">Library</span></span><br/> | <dl> <span data-ttu-id="b1142-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="b1142-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="b1142-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b1142-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b1142-125">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="b1142-125">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
