---
description: 建立效果的複本。
ms.assetid: 6272bce0-b712-4a61-afe2-8f572993b03e
title: 'ID3DXEffect：： CloneEffect 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.CloneEffect
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: eba2f6248bd1373ebf0aae55cf94103e2c269be7
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "107000601"
---
# <a name="id3dxeffectcloneeffect-method"></a><span data-ttu-id="2a671-103">ID3DXEffect：： CloneEffect 方法</span><span class="sxs-lookup"><span data-stu-id="2a671-103">ID3DXEffect::CloneEffect method</span></span>

<span data-ttu-id="2a671-104">建立效果的複本。</span><span class="sxs-lookup"><span data-stu-id="2a671-104">Creates a copy of an effect.</span></span>

## <a name="syntax"></a><span data-ttu-id="2a671-105">語法</span><span class="sxs-lookup"><span data-stu-id="2a671-105">Syntax</span></span>


```C++
HRESULT CloneEffect(
  [in]  LPDIRECT3DDEVICE9 pDevice,
  [out] LPD3DXEFFECT      *ppEffect
);
```



## <a name="parameters"></a><span data-ttu-id="2a671-106">參數</span><span class="sxs-lookup"><span data-stu-id="2a671-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="2a671-107">*pDevice* \[在\]</span><span class="sxs-lookup"><span data-stu-id="2a671-107">*pDevice* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="2a671-108">類型： **[ **LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span><span class="sxs-lookup"><span data-stu-id="2a671-108">Type: **[**LPDIRECT3DDEVICE9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)**</span></span>

<span data-ttu-id="2a671-109">[**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9)介面的指標，代表與效果相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="2a671-109">Pointer to an [**IDirect3DDevice9**](/windows/win32/api/d3d9helper/nn-d3d9helper-idirect3ddevice9) interface, representing the device associated with the effect.</span></span>

</dd> <dt>

<span data-ttu-id="2a671-110">*ppEffect* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="2a671-110">*ppEffect* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="2a671-111">類型： **[ **LPD3DXEFFECT**](id3dxeffect.md)\***</span><span class="sxs-lookup"><span data-stu-id="2a671-111">Type: **[**LPD3DXEFFECT**](id3dxeffect.md)\***</span></span>

<span data-ttu-id="2a671-112">[**ID3DXEffect**](id3dxeffect.md)介面的指標，其中包含複製的效果。</span><span class="sxs-lookup"><span data-stu-id="2a671-112">Pointer to an [**ID3DXEffect**](id3dxeffect.md) interface, containing the cloned effect.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="2a671-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="2a671-113">Return value</span></span>

<span data-ttu-id="2a671-114">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="2a671-114">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="2a671-115">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="2a671-115">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="2a671-116">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="2a671-116">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="2a671-117">備註</span><span class="sxs-lookup"><span data-stu-id="2a671-117">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="2a671-118">如果使用者在效果建立期間指定了 [D3DXFX \_ not \_ CLONEABLE](d3dxfx.md) ，此函式將不會複製效果。</span><span class="sxs-lookup"><span data-stu-id="2a671-118">This function will not clone an effect if the user specifies [D3DXFX\_NOT\_CLONEABLE](d3dxfx.md) during effect creation.</span></span>

 

<span data-ttu-id="2a671-119">若要以已複製效果的有效技術來更新共用和非共用參數，請參閱 [**ID3DXEffect：： CommitChanges**](id3dxeffect--commitchanges.md)。</span><span class="sxs-lookup"><span data-stu-id="2a671-119">To update shared and non-shared parameters in an active technique of a cloned effect, see [**ID3DXEffect::CommitChanges**](id3dxeffect--commitchanges.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="2a671-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="2a671-120">Requirements</span></span>



| <span data-ttu-id="2a671-121">需求</span><span class="sxs-lookup"><span data-stu-id="2a671-121">Requirement</span></span> | <span data-ttu-id="2a671-122">值</span><span class="sxs-lookup"><span data-stu-id="2a671-122">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="2a671-123">標頭</span><span class="sxs-lookup"><span data-stu-id="2a671-123">Header</span></span><br/>  | <dl> <span data-ttu-id="2a671-124"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="2a671-124"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="2a671-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="2a671-125">Library</span></span><br/> | <dl> <span data-ttu-id="2a671-126"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="2a671-126"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="2a671-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2a671-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="2a671-128">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="2a671-128">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> </dl>

 

 
