---
description: ID3DXEffectStateManager：： SetPixelShaderConstantI 方法-必須由使用者實作為的回呼函式，以設定頂點著色器整數常數的陣列。
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
ms.openlocfilehash: 53eab5993ee737efe866c73a550e6b216edaac3b
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108090476"
---
# <a name="id3dxeffectstatemanagersetpixelshaderconstanti-method"></a><span data-ttu-id="5bf3e-103">ID3DXEffectStateManager：： SetPixelShaderConstantI 方法</span><span class="sxs-lookup"><span data-stu-id="5bf3e-103">ID3DXEffectStateManager::SetPixelShaderConstantI method</span></span>

<span data-ttu-id="5bf3e-104">必須由使用者所執行的回呼函式，以設定頂點著色器整數常數的陣列。</span><span class="sxs-lookup"><span data-stu-id="5bf3e-104">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="5bf3e-105">語法</span><span class="sxs-lookup"><span data-stu-id="5bf3e-105">Syntax</span></span>


```C++
HRESULT SetPixelShaderConstantI(
  [out]       UINT StartRegister,
  [out] const INT  *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="5bf3e-106">參數</span><span class="sxs-lookup"><span data-stu-id="5bf3e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5bf3e-107">*StartRegister* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5bf3e-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bf3e-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5bf3e-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5bf3e-109">第一個常數暫存器的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="5bf3e-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="5bf3e-110">*pConstantData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5bf3e-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bf3e-111">類型： **Const [**INT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="5bf3e-111">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="5bf3e-112">整數常數的陣列。</span><span class="sxs-lookup"><span data-stu-id="5bf3e-112">An array of integer constants.</span></span>

</dd> <dt>

<span data-ttu-id="5bf3e-113">*RegisterCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5bf3e-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5bf3e-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="5bf3e-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="5bf3e-115">PConstantData 中的暫存器數目。</span><span class="sxs-lookup"><span data-stu-id="5bf3e-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5bf3e-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="5bf3e-116">Return value</span></span>

<span data-ttu-id="5bf3e-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="5bf3e-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="5bf3e-118">使用者執行的方法應該會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="5bf3e-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="5bf3e-119">如果回呼在設定裝置狀態時失敗，將會發生下列其中一種情況：</span><span class="sxs-lookup"><span data-stu-id="5bf3e-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="5bf3e-120">[**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)期間的效果將會失敗。</span><span class="sxs-lookup"><span data-stu-id="5bf3e-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="5bf3e-121">動態效果狀態呼叫 (例如 [**IDirect3DDevice9：： SetPixelShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)) 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="5bf3e-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetPixelShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setpixelshaderconstanti)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="5bf3e-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="5bf3e-122">Requirements</span></span>



| <span data-ttu-id="5bf3e-123">需求</span><span class="sxs-lookup"><span data-stu-id="5bf3e-123">Requirement</span></span> | <span data-ttu-id="5bf3e-124">值</span><span class="sxs-lookup"><span data-stu-id="5bf3e-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="5bf3e-125">標頭</span><span class="sxs-lookup"><span data-stu-id="5bf3e-125">Header</span></span><br/>  | <dl> <span data-ttu-id="5bf3e-126"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="5bf3e-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="5bf3e-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="5bf3e-127">Library</span></span><br/> | <dl> <span data-ttu-id="5bf3e-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="5bf3e-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="5bf3e-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5bf3e-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5bf3e-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="5bf3e-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
