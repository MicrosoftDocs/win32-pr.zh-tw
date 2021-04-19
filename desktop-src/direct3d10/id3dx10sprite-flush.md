---
description: 強制將所有批次的子層提交至裝置。 裝置狀態會維持在最後一次呼叫 ID3DX10Sprite：： Begin 之後。 然後會清除批次中的子後 sprite 清單。
ms.assetid: ae03e17c-1a14-4a41-a9a9-8757d2f7a81d
title: 'ID3DX10Sprite：： Flush 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.Flush
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 748be56a7b89223db1957b9c0144143edd90ee4c
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106990026"
---
# <a name="id3dx10spriteflush-method"></a><span data-ttu-id="58994-105">ID3DX10Sprite：： Flush 方法</span><span class="sxs-lookup"><span data-stu-id="58994-105">ID3DX10Sprite::Flush method</span></span>

<span data-ttu-id="58994-106">強制將所有批次的子層提交至裝置。</span><span class="sxs-lookup"><span data-stu-id="58994-106">Force all batched sprites to be submitted to the device.</span></span> <span data-ttu-id="58994-107">裝置狀態會維持在最後一次呼叫 ID3DX10Sprite：： Begin 之後。</span><span class="sxs-lookup"><span data-stu-id="58994-107">Device states remain as they were after the last call to ID3DX10Sprite::Begin.</span></span> <span data-ttu-id="58994-108">然後會清除批次中的子後 sprite 清單。</span><span class="sxs-lookup"><span data-stu-id="58994-108">The list of batched sprites is then cleared.</span></span>

## <a name="syntax"></a><span data-ttu-id="58994-109">語法</span><span class="sxs-lookup"><span data-stu-id="58994-109">Syntax</span></span>


```C++
HRESULT Flush();
```



## <a name="parameters"></a><span data-ttu-id="58994-110">參數</span><span class="sxs-lookup"><span data-stu-id="58994-110">Parameters</span></span>

<span data-ttu-id="58994-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="58994-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="58994-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="58994-112">Return value</span></span>

<span data-ttu-id="58994-113">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="58994-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="58994-114">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="58994-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="58994-115">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="58994-115">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="58994-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="58994-116">Requirements</span></span>



| <span data-ttu-id="58994-117">需求</span><span class="sxs-lookup"><span data-stu-id="58994-117">Requirement</span></span> | <span data-ttu-id="58994-118">值</span><span class="sxs-lookup"><span data-stu-id="58994-118">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="58994-119">標頭</span><span class="sxs-lookup"><span data-stu-id="58994-119">Header</span></span><br/>  | <dl> <span data-ttu-id="58994-120"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="58994-120"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="58994-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="58994-121">Library</span></span><br/> | <dl> <span data-ttu-id="58994-122"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="58994-122"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="58994-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="58994-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="58994-124">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="58994-124">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="58994-125">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="58994-125">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




