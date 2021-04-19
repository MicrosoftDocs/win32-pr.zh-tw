---
description: 必須由使用者所執行的回呼函式，以設定頂點著色器整數常數的陣列。
ms.assetid: 0035c97a-1b17-4665-9032-7b3b9a9d2cff
title: 'ID3DXEffectStateManager：： SetVertexShaderConstantI 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffectStateManager.SetVertexShaderConstantI
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: be95d678ee6b0c44dc49e180df4d3332a84d5fe7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106999020"
---
# <a name="id3dxeffectstatemanagersetvertexshaderconstanti-method"></a><span data-ttu-id="14299-103">ID3DXEffectStateManager：： SetVertexShaderConstantI 方法</span><span class="sxs-lookup"><span data-stu-id="14299-103">ID3DXEffectStateManager::SetVertexShaderConstantI method</span></span>

<span data-ttu-id="14299-104">必須由使用者所執行的回呼函式，以設定頂點著色器整數常數的陣列。</span><span class="sxs-lookup"><span data-stu-id="14299-104">A callback function that must be implemented by a user to set an array of vertex shader integer constants.</span></span>

## <a name="syntax"></a><span data-ttu-id="14299-105">語法</span><span class="sxs-lookup"><span data-stu-id="14299-105">Syntax</span></span>


```C++
HRESULT SetVertexShaderConstantI(
  [out]       UINT StartRegister,
  [out] const INT  *pConstantData,
  [out]       UINT RegisterCount
);
```



## <a name="parameters"></a><span data-ttu-id="14299-106">參數</span><span class="sxs-lookup"><span data-stu-id="14299-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="14299-107">*StartRegister* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="14299-107">*StartRegister* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14299-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14299-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14299-109">第一個常數暫存器的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="14299-109">The zero-based index of the first constant register.</span></span>

</dd> <dt>

<span data-ttu-id="14299-110">*pConstantData* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="14299-110">*pConstantData* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14299-111">類型： **Const [**INT**](../winprog/windows-data-types.md) \***</span><span class="sxs-lookup"><span data-stu-id="14299-111">Type: **const [**INT**](../winprog/windows-data-types.md)\***</span></span>

<span data-ttu-id="14299-112">整數常數的陣列。</span><span class="sxs-lookup"><span data-stu-id="14299-112">An array of integer constants.</span></span>

</dd> <dt>

<span data-ttu-id="14299-113">*RegisterCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="14299-113">*RegisterCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="14299-114">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="14299-114">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="14299-115">PConstantData 中的暫存器數目。</span><span class="sxs-lookup"><span data-stu-id="14299-115">The number of registers in pConstantData.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="14299-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="14299-116">Return value</span></span>

<span data-ttu-id="14299-117">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="14299-117">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="14299-118">使用者執行的方法應該會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="14299-118">The user-implemented method should return S\_OK.</span></span> <span data-ttu-id="14299-119">如果回呼在設定裝置狀態時失敗，將會發生下列其中一種情況：</span><span class="sxs-lookup"><span data-stu-id="14299-119">If the callback fails when setting the device state, either of the following will occur:</span></span>

-   <span data-ttu-id="14299-120">[**ID3DXEffect：： BeginPass**](id3dxeffect--beginpass.md)期間的效果將會失敗。</span><span class="sxs-lookup"><span data-stu-id="14299-120">The effect will fail during [**ID3DXEffect::BeginPass**](id3dxeffect--beginpass.md).</span></span>
-   <span data-ttu-id="14299-121">動態效果狀態呼叫 (例如 [**IDirect3DDevice9：： SetVertexShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)) 將會失敗。</span><span class="sxs-lookup"><span data-stu-id="14299-121">The dynamic effect state call (such as [**IDirect3DDevice9::SetVertexShaderConstantI**](/windows/win32/api/d3d9helper/nf-d3d9helper-idirect3ddevice9-setvertexshaderconstanti)) will fail.</span></span>

## <a name="requirements"></a><span data-ttu-id="14299-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="14299-122">Requirements</span></span>



| <span data-ttu-id="14299-123">需求</span><span class="sxs-lookup"><span data-stu-id="14299-123">Requirement</span></span> | <span data-ttu-id="14299-124">值</span><span class="sxs-lookup"><span data-stu-id="14299-124">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="14299-125">標頭</span><span class="sxs-lookup"><span data-stu-id="14299-125">Header</span></span><br/>  | <dl> <span data-ttu-id="14299-126"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="14299-126"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="14299-127">程式庫</span><span class="sxs-lookup"><span data-stu-id="14299-127">Library</span></span><br/> | <dl> <span data-ttu-id="14299-128"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="14299-128"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="14299-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="14299-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="14299-130">ID3DXEffectStateManager</span><span class="sxs-lookup"><span data-stu-id="14299-130">ID3DXEffectStateManager</span></span>](id3dxeffectstatemanager.md)
</dt> </dl>

 

 
