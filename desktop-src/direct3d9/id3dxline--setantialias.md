---
description: 切換線條消除鋸齒。
ms.assetid: 9c212823-2dc6-40dd-b1aa-9fc4a2c540f4
title: 'ID3DXLine：： SetAntialias 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXLine.SetAntialias
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 893e2061beedb6d45dc86e87903613984e3d1785
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106976752"
---
# <a name="id3dxlinesetantialias-method"></a><span data-ttu-id="f8a0b-103">ID3DXLine：： SetAntialias 方法</span><span class="sxs-lookup"><span data-stu-id="f8a0b-103">ID3DXLine::SetAntialias method</span></span>

<span data-ttu-id="f8a0b-104">切換線條消除鋸齒。</span><span class="sxs-lookup"><span data-stu-id="f8a0b-104">Toggles line antialiasing.</span></span>

## <a name="syntax"></a><span data-ttu-id="f8a0b-105">語法</span><span class="sxs-lookup"><span data-stu-id="f8a0b-105">Syntax</span></span>


```C++
HRESULT SetAntialias(
  [in] BOOL bAntiAlias
);
```



## <a name="parameters"></a><span data-ttu-id="f8a0b-106">參數</span><span class="sxs-lookup"><span data-stu-id="f8a0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f8a0b-107">*bAntiAlias* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f8a0b-107">*bAntiAlias* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f8a0b-108">類型： **[ **BOOL**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f8a0b-108">Type: **[**BOOL**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f8a0b-109">切換消除鋸齒功能。</span><span class="sxs-lookup"><span data-stu-id="f8a0b-109">Toggles antialiasing on and off.</span></span> <span data-ttu-id="f8a0b-110">**TRUE** 會開啟消除鋸齒，而 **FALSE** 則會關閉消除鋸齒功能。</span><span class="sxs-lookup"><span data-stu-id="f8a0b-110">**TRUE** turns antialiasing on, and **FALSE** turns antialiasing off.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f8a0b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f8a0b-111">Return value</span></span>

<span data-ttu-id="f8a0b-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f8a0b-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f8a0b-113">如果方法成功，則傳回值為「D3D \_ 正常」。</span><span class="sxs-lookup"><span data-stu-id="f8a0b-113">If the method succeeds, the return value is D3D\_OK.</span></span> <span data-ttu-id="f8a0b-114">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL，D3DXERR \_ INVALIDDATA。</span><span class="sxs-lookup"><span data-stu-id="f8a0b-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DXERR\_INVALIDDATA.</span></span>

## <a name="requirements"></a><span data-ttu-id="f8a0b-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="f8a0b-115">Requirements</span></span>



| <span data-ttu-id="f8a0b-116">需求</span><span class="sxs-lookup"><span data-stu-id="f8a0b-116">Requirement</span></span> | <span data-ttu-id="f8a0b-117">值</span><span class="sxs-lookup"><span data-stu-id="f8a0b-117">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="f8a0b-118">標頭</span><span class="sxs-lookup"><span data-stu-id="f8a0b-118">Header</span></span><br/>  | <dl> <span data-ttu-id="f8a0b-119"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="f8a0b-119"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="f8a0b-120">程式庫</span><span class="sxs-lookup"><span data-stu-id="f8a0b-120">Library</span></span><br/> | <dl> <span data-ttu-id="f8a0b-121"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f8a0b-121"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="f8a0b-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f8a0b-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f8a0b-123">ID3DXLine</span><span class="sxs-lookup"><span data-stu-id="f8a0b-123">ID3DXLine</span></span>](id3dxline.md)
</dt> <dt>

[<span data-ttu-id="f8a0b-124">**ID3DXLine::GetAntialias**</span><span class="sxs-lookup"><span data-stu-id="f8a0b-124">**ID3DXLine::GetAntialias**</span></span>](id3dxline--getantialias.md)
</dt> </dl>

 

 
