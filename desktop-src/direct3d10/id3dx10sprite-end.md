---
description: 在 ID3DX10Sprite：： Flush 之後呼叫此動作。 如果 \_ \_ \_ 在呼叫 ID3DX10Sprite：： begin 時指定了 D3DX10 SPRITE SAVE 狀態，此 API 會將裝置狀態還原為在呼叫 ID3DX10Sprite：： begin 之前的狀態。
ms.assetid: 71645edb-be4a-4d87-9fb0-557cf5cf10e5
title: 'ID3DX10Sprite：： End 方法 (D3DX10 .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DX10Sprite.End
api_type:
- COM
api_location:
- D3DX10.lib
- D3DX10.dll
ms.openlocfilehash: 02d25e41916bd5d7605f3c0e1bc6e7998ea06e86
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975716"
---
# <a name="id3dx10spriteend-method"></a><span data-ttu-id="d0c92-104">ID3DX10Sprite：： End 方法</span><span class="sxs-lookup"><span data-stu-id="d0c92-104">ID3DX10Sprite::End method</span></span>

<span data-ttu-id="d0c92-105">在 ID3DX10Sprite：： Flush 之後呼叫此動作。</span><span class="sxs-lookup"><span data-stu-id="d0c92-105">Call this after ID3DX10Sprite::Flush.</span></span> <span data-ttu-id="d0c92-106">如果 \_ \_ \_ 在呼叫 ID3DX10Sprite：： begin 時指定了 D3DX10 SPRITE SAVE 狀態，此 API 會將裝置狀態還原為在呼叫 ID3DX10Sprite：： begin 之前的狀態。</span><span class="sxs-lookup"><span data-stu-id="d0c92-106">If D3DX10\_SPRITE\_SAVE\_STATE was specified when ID3DX10Sprite::Begin was called, this API will restore the device state to how it was before ID3DX10Sprite::Begin was called.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0c92-107">語法</span><span class="sxs-lookup"><span data-stu-id="d0c92-107">Syntax</span></span>


```C++
HRESULT End();
```



## <a name="parameters"></a><span data-ttu-id="d0c92-108">參數</span><span class="sxs-lookup"><span data-stu-id="d0c92-108">Parameters</span></span>

<span data-ttu-id="d0c92-109">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="d0c92-109">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="d0c92-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="d0c92-110">Return value</span></span>

<span data-ttu-id="d0c92-111">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="d0c92-111">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="d0c92-112">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="d0c92-112">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="d0c92-113">如果方法失敗，則會傳回下列值： D3DERR \_ INVALIDCALL。</span><span class="sxs-lookup"><span data-stu-id="d0c92-113">If the method fails, the following value will be returned: D3DERR\_INVALIDCALL.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0c92-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0c92-114">Requirements</span></span>



| <span data-ttu-id="d0c92-115">需求</span><span class="sxs-lookup"><span data-stu-id="d0c92-115">Requirement</span></span> | <span data-ttu-id="d0c92-116">值</span><span class="sxs-lookup"><span data-stu-id="d0c92-116">Value</span></span> |
|--------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="d0c92-117">標頭</span><span class="sxs-lookup"><span data-stu-id="d0c92-117">Header</span></span><br/>  | <dl> <span data-ttu-id="d0c92-118"><dt>D3DX10。h</dt></span><span class="sxs-lookup"><span data-stu-id="d0c92-118"><dt>D3DX10.h</dt></span></span> </dl>   |
| <span data-ttu-id="d0c92-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="d0c92-119">Library</span></span><br/> | <dl> <span data-ttu-id="d0c92-120"><dt>D3DX10 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d0c92-120"><dt>D3DX10.lib</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d0c92-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0c92-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d0c92-122">ID3DX10Sprite</span><span class="sxs-lookup"><span data-stu-id="d0c92-122">ID3DX10Sprite</span></span>](id3dx10sprite.md)
</dt> <dt>

[<span data-ttu-id="d0c92-123">D3DX 介面</span><span class="sxs-lookup"><span data-stu-id="d0c92-123">D3DX Interfaces</span></span>](d3d10-graphics-reference-d3dx10-interfaces.md)
</dt> </dl>

 

 




