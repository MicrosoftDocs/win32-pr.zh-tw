---
description: 必須由使用者執行以設定轉換的回呼函數。
ms.assetid: 5d886554-ddb6-4b8a-a7fd-453e94b9516f
title: 'ID3DXEffectStateManager：： SetTransform 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetTransform
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: b19a060cfeb09d5d1a92e5e7a1a1f25b58e64f4d
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "103946160"
---
# <a name="id3dxeffectstatemanagersettransform-method"></a><span data-ttu-id="3b401-103">ID3DXEffectStateManager：： SetTransform 方法</span><span class="sxs-lookup"><span data-stu-id="3b401-103">ID3DXEffectStateManager::SetTransform method</span></span>

<span data-ttu-id="3b401-104">必須由使用者執行以設定轉換的回呼函數。</span><span class="sxs-lookup"><span data-stu-id="3b401-104">A callback function that must be implemented by a user to set a transform.</span></span>

## <a name="syntax"></a><span data-ttu-id="3b401-105">語法</span><span class="sxs-lookup"><span data-stu-id="3b401-105">Syntax</span></span>


```C++
HRESULT SetTransform(
  [in]       D3DTRANSFORMSTATETYPE State,
  [in] const D3DMATRIX             *pMatrix
);
```



## <a name="parameters"></a><span data-ttu-id="3b401-106">參數</span><span class="sxs-lookup"><span data-stu-id="3b401-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3b401-107">*狀態* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b401-107">*State* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b401-108">類型： **[ **D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md)**</span><span class="sxs-lookup"><span data-stu-id="3b401-108">Type: **[**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md)**</span></span>

<span data-ttu-id="3b401-109">要套用矩陣的轉換類型。</span><span class="sxs-lookup"><span data-stu-id="3b401-109">The type of transform to apply the matrix to.</span></span> <span data-ttu-id="3b401-110">請參閱 [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md)。</span><span class="sxs-lookup"><span data-stu-id="3b401-110">See [**D3DTRANSFORMSTATETYPE**](./d3dtransformstatetype.md).</span></span>

</dd> <dt>

<span data-ttu-id="3b401-111">*pMatrix* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3b401-111">*pMatrix* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3b401-112">Type： **Const [**D3DMATRIX**](d3dmatrix.md) \***</span><span class="sxs-lookup"><span data-stu-id="3b401-112">Type: **const [**D3DMATRIX**](d3dmatrix.md)\***</span></span>

<span data-ttu-id="3b401-113">轉換矩陣。</span><span class="sxs-lookup"><span data-stu-id="3b401-113">A transformation matrix.</span></span> <span data-ttu-id="3b401-114">請參閱 [**D3DMATRIX**](d3dmatrix.md)。</span><span class="sxs-lookup"><span data-stu-id="3b401-114">See [**D3DMATRIX**](d3dmatrix.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3b401-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="3b401-115">Return value</span></span>

<span data-ttu-id="3b401-116">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="3b401-116">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="3b401-117">使用者執行的方法應該會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="3b401-117">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="3b401-118">如果回呼在設定裝置狀態時失敗，將會發生下列其中一種情況：</span><span class="sxs-lookup"><span data-stu-id="3b401-118">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="3b401-119">[**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)期間的效果將會失敗。</span><span class="sxs-lookup"><span data-stu-id="3b401-119">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="3b401-120">動態效果狀態呼叫 (例如 [**IDirect3DDevice9：： SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)) 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="3b401-120">The dynamic effect state call (such as [**IDirect3DDevice9::SetTransform**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-settransform)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="3b401-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="3b401-121">Requirements</span></span>



| <span data-ttu-id="3b401-122">需求</span><span class="sxs-lookup"><span data-stu-id="3b401-122">Requirement</span></span> | <span data-ttu-id="3b401-123">值</span><span class="sxs-lookup"><span data-stu-id="3b401-123">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="3b401-124">標頭</span><span class="sxs-lookup"><span data-stu-id="3b401-124">Header</span></span><br/>  | <dl> <span data-ttu-id="3b401-125"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="3b401-125"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="3b401-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="3b401-126">Library</span></span><br/> | <dl> <span data-ttu-id="3b401-127"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="3b401-127"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="3b401-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3b401-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3b401-129">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="3b401-129">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
