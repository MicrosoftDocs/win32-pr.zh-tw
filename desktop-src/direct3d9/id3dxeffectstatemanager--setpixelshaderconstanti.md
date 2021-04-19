---
description: 必須由使用者所執行的回呼函式，以設定頂點著色器整數常數的陣列。
ms.assetid: 55f5747d-b7f8-4d13-ac2c-df2dcb160091
title: 'ID3DXEffectStateManager：： SetPixelShaderConstantI 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetPixelShaderConstantI
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 2e84d883370038435dc59bb948ef94fcd82223db
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106986526"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstanti-method"></a><span data-ttu-id="e9e37-103">ID3DXEffectStateManager：： SetPixelShaderConstantI 方法</span><span class="sxs-lookup"><span data-stu-id="e9e37-103">ID3DXEffectStateManager::SetPixelShaderConstantI method</span></span>

<span data-ttu-id="e9e37-104">必須由使用者所執行的回呼函式，以設定頂點著色器整數常數的陣列。</span><span class="sxs-lookup"><span data-stu-id="e9e37-104">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="e9e37-105">語法</span><span class="sxs-lookup"><span data-stu-id="e9e37-105">Syntax</span></span>


```C++
HRESULT SetPixelShaderConstantI(
  [out]       UINT StartRegister,
  [out] const INT  *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="e9e37-106">參數</span><span class="sxs-lookup"><span data-stu-id="e9e37-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e9e37-107">*StartRegister* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e9e37-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9e37-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e9e37-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e9e37-109">第一個常數暫存器的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="e9e37-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="e9e37-110">*pConstantData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e9e37-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9e37-111">類型： **Const [**INT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="e9e37-111">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="e9e37-112">整數常數的陣列。</span><span class="sxs-lookup"><span data-stu-id="e9e37-112">An array of integer constants.</span></span>

</dd> <dt>

<span data-ttu-id="e9e37-113">*RegisterCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e9e37-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e9e37-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="e9e37-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="e9e37-115">PConstantData 中的暫存器數目。</span><span class="sxs-lookup"><span data-stu-id="e9e37-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="e9e37-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="e9e37-116">Return value</span></span>

<span data-ttu-id="e9e37-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="e9e37-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="e9e37-118">使用者執行的方法應該會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="e9e37-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="e9e37-119">如果回呼在設定裝置狀態時失敗，將會發生下列其中一種情況：</span><span class="sxs-lookup"><span data-stu-id="e9e37-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="e9e37-120">[**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)期間的效果將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e9e37-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="e9e37-121">動態效果狀態呼叫 (例如 [**IDirect3DDevice9：： SetPixelShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)) 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="e9e37-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetPixelShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="e9e37-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="e9e37-122">Requirements</span></span>



| <span data-ttu-id="e9e37-123">需求</span><span class="sxs-lookup"><span data-stu-id="e9e37-123">Requirement</span></span> | <span data-ttu-id="e9e37-124">值</span><span class="sxs-lookup"><span data-stu-id="e9e37-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="e9e37-125">標頭</span><span class="sxs-lookup"><span data-stu-id="e9e37-125">Header</span></span><br/>  | <dl> <span data-ttu-id="e9e37-126"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="e9e37-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="e9e37-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="e9e37-127">Library</span></span><br/> | <dl> <span data-ttu-id="e9e37-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="e9e37-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="e9e37-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e9e37-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e9e37-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="e9e37-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
