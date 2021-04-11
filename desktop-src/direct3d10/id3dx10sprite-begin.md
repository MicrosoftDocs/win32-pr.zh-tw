---
description: 準備用來繪製 sprite 的裝置。
ms.assetid: cffe5ac3-eeee-4ece-afcc-04a476b75863
title: 'ID3DX10Sprite：： Begin 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Begin
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: ede2995f72eb1200e68f035119643a362e15701e
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "104196350"
---
# <a name="id3dx10spritebegin-method"></a><span data-ttu-id="f1a62-103">ID3DX10Sprite：： Begin 方法</span><span class="sxs-lookup"><span data-stu-id="f1a62-103">ID3DX10Sprite::Begin method</span></span>

<span data-ttu-id="f1a62-104">準備用來繪製 sprite 的裝置。</span><span class="sxs-lookup"><span data-stu-id="f1a62-104">Prepare a device for drawing sprites.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1a62-105">語法</span><span class="sxs-lookup"><span data-stu-id="f1a62-105">Syntax</span></span>


```C++
HRESULT Begin(
  [in] UINT flags
);
```



## <a name="parameters"></a><span data-ttu-id="f1a62-106">參數</span><span class="sxs-lookup"><span data-stu-id="f1a62-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1a62-107">*旗標* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1a62-107">*flags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1a62-108">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="f1a62-108">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="f1a62-109">控制如何繪製 sprite 的旗標。</span><span class="sxs-lookup"><span data-stu-id="f1a62-109">Flags that control how the sprites will be drawn.</span></span> <span data-ttu-id="f1a62-110">請參閱 [**D3DX10 \_ SPRITE \_ 旗**](d3dx10-sprite-flag.md)標。</span><span class="sxs-lookup"><span data-stu-id="f1a62-110">See [**D3DX10\_SPRITE\_FLAG**](d3dx10-sprite-flag.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1a62-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1a62-111">Return value</span></span>

<span data-ttu-id="f1a62-112">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="f1a62-112">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="f1a62-113">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="f1a62-113">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="f1a62-114">如果方法失敗，則傳回值可以是下列其中一項： D3DERR \_ INVALIDCALL、D3DERR \_ OUTOFVIDEOMEMORY、D3DXERR \_ INVALIDDATA、E \_ OUTOFMEMORY。</span><span class="sxs-lookup"><span data-stu-id="f1a62-114">If the method fails, the return value can be one of the following: D3DERR\_INVALIDCALL, D3DERR\_OUTOFVIDEOMEMORY, D3DXERR\_INVALIDDATA, E\_OUTOFMEMORY.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1a62-115">備註</span><span class="sxs-lookup"><span data-stu-id="f1a62-115">Remarks</span></span>

<span data-ttu-id="f1a62-116">每次開始呼叫都必須與 [**ID3DX10Sprite：： End**](id3dx10sprite-end.md)的呼叫相符。</span><span class="sxs-lookup"><span data-stu-id="f1a62-116">Every call to Begin must be matched with a call to [**ID3DX10Sprite::End**](id3dx10sprite-end.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="f1a62-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1a62-117">Requirements</span></span>



| <span data-ttu-id="f1a62-118">需求</span><span class="sxs-lookup"><span data-stu-id="f1a62-118">Requirement</span></span> | <span data-ttu-id="f1a62-119">值</span><span class="sxs-lookup"><span data-stu-id="f1a62-119">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1a62-120">標頭</span><span class="sxs-lookup"><span data-stu-id="f1a62-120">Header</span></span><br/>  | <dl> <span data-ttu-id="f1a62-121"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="f1a62-121"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="f1a62-122">程式庫</span><span class="sxs-lookup"><span data-stu-id="f1a62-122">Library</span></span><br/> | <dl> <span data-ttu-id="f1a62-123"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="f1a62-123"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f1a62-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f1a62-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f1a62-125">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="f1a62-125">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="f1a62-126">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="f1a62-126">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 
