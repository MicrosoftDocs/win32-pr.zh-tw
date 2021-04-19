---
description: 取得效果狀態管理員。
ms.assetid: 4a09eb2a-2393-40b0-81b9-3c27998c2b77
title: 'ID3DXEffect：： GetStateManager 方法 (D3DX9Effect .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXEffect.GetStateManager
api_type:
- COM
api_location:
- D3dx9.lib
- D3dx9.dll
ms.openlocfilehash: 293b642dfecfa4cc14426addf2567d43dffa7233
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106993866"
---
# <a name="id3dxeffectgetstatemanager-method"></a><span data-ttu-id="61a18-103">ID3DXEffect：： GetStateManager 方法</span><span class="sxs-lookup"><span data-stu-id="61a18-103">ID3DXEffect::GetStateManager method</span></span>

<span data-ttu-id="61a18-104">取得效果狀態管理員。</span><span class="sxs-lookup"><span data-stu-id="61a18-104">Get the effect state manager.</span></span>

## <a name="syntax"></a><span data-ttu-id="61a18-105">語法</span><span class="sxs-lookup"><span data-stu-id="61a18-105">Syntax</span></span>


```C++
HRESULT GetStateManager(
  [out] LPD3DXEFFECTSTATEMANAGER *ppManager
);
```



## <a name="parameters"></a><span data-ttu-id="61a18-106">參數</span><span class="sxs-lookup"><span data-stu-id="61a18-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="61a18-107">*ppManager* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="61a18-107">*ppManager* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="61a18-108">類型： **[ **LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)\***</span><span class="sxs-lookup"><span data-stu-id="61a18-108">Type: **[**LPD3DXEFFECTSTATEMANAGER**](id3dxeffectstatemanager.md)\***</span></span>

<span data-ttu-id="61a18-109">傳回狀態管理員的指標。</span><span class="sxs-lookup"><span data-stu-id="61a18-109">Returns a pointer to the state manager.</span></span> <span data-ttu-id="61a18-110">請參閱 [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md)。</span><span class="sxs-lookup"><span data-stu-id="61a18-110">See [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="61a18-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="61a18-111">Return value</span></span>

<span data-ttu-id="61a18-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="61a18-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="61a18-113">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="61a18-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="61a18-114">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="61a18-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="remarks"></a><span data-ttu-id="61a18-115">備註</span><span class="sxs-lookup"><span data-stu-id="61a18-115">Remarks</span></span>

<span data-ttu-id="61a18-116">[**ID3DXEffectStateManager**](id3dxeffectstatemanager.md)是使用者執行的介面，可將回呼提供至應用程式，以從效果設定裝置狀態。</span><span class="sxs-lookup"><span data-stu-id="61a18-116">The [**ID3DXEffectStateManager**](id3dxeffectstatemanager.md) is a user-implemented interface that furnishes callbacks into an application for setting device state from an effect.</span></span>

## <a name="requirements"></a><span data-ttu-id="61a18-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="61a18-117">Requirements</span></span>



| <span data-ttu-id="61a18-118">需求</span><span class="sxs-lookup"><span data-stu-id="61a18-118">Requirement</span></span> | <span data-ttu-id="61a18-119">值</span><span class="sxs-lookup"><span data-stu-id="61a18-119">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="61a18-120">標頭</span><span class="sxs-lookup"><span data-stu-id="61a18-120">Header</span></span><br/>  | <dl> <span data-ttu-id="61a18-121"><dt>D3DX9Effect。h</dt></span><span class="sxs-lookup"><span data-stu-id="61a18-121"><dt>D3DX9Effect.h</dt></span></span> </dl> |
| <span data-ttu-id="61a18-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="61a18-122">Library</span></span><br/> | <dl> <span data-ttu-id="61a18-123"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="61a18-123"><dt>D3dx9.lib</dt></span></span> </dl>     |



## <a name="see-also"></a><span data-ttu-id="61a18-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61a18-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61a18-125">ID3DXEffect</span><span class="sxs-lookup"><span data-stu-id="61a18-125">ID3DXEffect</span></span>](id3dxeffect.md)
</dt> <dt>

[<span data-ttu-id="61a18-126">**ID3DXEffect::SetStateManager**</span><span class="sxs-lookup"><span data-stu-id="61a18-126">**ID3DXEffect::SetStateManager**</span></span>](id3dxeffect--setstatemanager.md)
</dt> </dl>

 

 




