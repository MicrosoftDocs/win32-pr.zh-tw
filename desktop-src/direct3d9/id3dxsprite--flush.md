---
description: 強制將所有批次中的 sprite 提交至裝置。 裝置狀態會維持在最後一次呼叫 ID3DXSprite：： Begin 之後。 然後會清除批次中的子後 sprite 清單。
ms.assetid: e5717bde-e339-4344-8ce7-b0c3fe118887
title: 'ID3DXSprite：： Flush 方法 (D3dx9core .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXSprite.Flush
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 3bcd89984672f0dcfa2df120ede1abdfee23d171
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106985892"
---
# <a name="id3dxspriteflush-method"></a><span data-ttu-id="946e7-105">ID3DXSprite：： Flush 方法</span><span class="sxs-lookup"><span data-stu-id="946e7-105">ID3DXSprite::Flush method</span></span>

<span data-ttu-id="946e7-106">強制將所有批次中的 sprite 提交至裝置。</span><span class="sxs-lookup"><span data-stu-id="946e7-106">Forces all batched sprites to be submitted to the device.</span></span> <span data-ttu-id="946e7-107">裝置狀態會維持在最後一次呼叫 [**ID3DXSprite：： Begin**](id3dxsprite--begin.md)之後。</span><span class="sxs-lookup"><span data-stu-id="946e7-107">Device states remain as they were after the last call to [**ID3DXSprite::Begin**](id3dxsprite--begin.md).</span></span> <span data-ttu-id="946e7-108">然後會清除批次中的子後 sprite 清單。</span><span class="sxs-lookup"><span data-stu-id="946e7-108">The list of batched sprites is then cleared.</span></span>

## <a name="syntax"></a><span data-ttu-id="946e7-109">語法</span><span class="sxs-lookup"><span data-stu-id="946e7-109">Syntax</span></span>


```C++
HRESULT Flush();
```



## <a name="parameters"></a><span data-ttu-id="946e7-110">參數</span><span class="sxs-lookup"><span data-stu-id="946e7-110">Parameters</span></span>

<span data-ttu-id="946e7-111">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="946e7-111">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="946e7-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="946e7-112">Return value</span></span>

<span data-ttu-id="946e7-113">類型： **[ **HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span><span class="sxs-lookup"><span data-stu-id="946e7-113">Type: **[**HRESULT**](https://msdn.microsoft.com/library/Bb401631(v=MSDN.10).aspx)**</span></span>

<span data-ttu-id="946e7-114">如果方法成功，則傳回值為 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="946e7-114">If the method succeeds, the return value is S\_OK.</span></span> <span data-ttu-id="946e7-115">如果方法失敗，則會傳回下列值。D3DERR \_ INVALIDCALL</span><span class="sxs-lookup"><span data-stu-id="946e7-115">If the method fails, the following value will be returned.D3DERR\_INVALIDCALL</span></span>

## <a name="requirements"></a><span data-ttu-id="946e7-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="946e7-116">Requirements</span></span>



| <span data-ttu-id="946e7-117">需求</span><span class="sxs-lookup"><span data-stu-id="946e7-117">Requirement</span></span> | <span data-ttu-id="946e7-118">值</span><span class="sxs-lookup"><span data-stu-id="946e7-118">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="946e7-119">標頭</span><span class="sxs-lookup"><span data-stu-id="946e7-119">Header</span></span><br/>  | <dl> <span data-ttu-id="946e7-120"><dt>D3dx9core。h</dt></span><span class="sxs-lookup"><span data-stu-id="946e7-120"><dt>D3dx9core.h</dt></span></span> </dl> |
| <span data-ttu-id="946e7-121">程式庫</span><span class="sxs-lookup"><span data-stu-id="946e7-121">Library</span></span><br/> | <dl> <span data-ttu-id="946e7-122"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="946e7-122"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="946e7-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="946e7-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="946e7-124">ID3DXSprite</span><span class="sxs-lookup"><span data-stu-id="946e7-124">ID3DXSprite</span></span>](id3dxsprite.md)
</dt> <dt>

[<span data-ttu-id="946e7-125">**ID3DXSprite：： End**</span><span class="sxs-lookup"><span data-stu-id="946e7-125">**ID3DXSprite::End**</span></span>](id3dxsprite--end.md)
</dt> </dl>

 

 




