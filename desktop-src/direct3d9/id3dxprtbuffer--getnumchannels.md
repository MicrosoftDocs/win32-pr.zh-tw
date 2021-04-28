---
description: ID3DXPRTBuffer：： GetNumChannels 方法-抓取記憶體中用來儲存範例的色彩通道數目。
ms.assetid: dd1e3590-78e1-41a2-9f15-79389d9a210a
title: 'ID3DXPRTBuffer：： GetNumChannels 方法 (D3DX9Mesh .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ID3DXPRTBuffer.GetNumChannels
api_type:
- COM
api_location:
- d3dx9.lib
- d3dx9.dll
ms.openlocfilehash: 5dab8491128a242116c48a58e8edba1be9eb51b6
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108107336"
---
# <a name="id3dxprtbuffergetnumchannels-method"></a><span data-ttu-id="bb140-103">ID3DXPRTBuffer：： GetNumChannels 方法</span><span class="sxs-lookup"><span data-stu-id="bb140-103">ID3DXPRTBuffer::GetNumChannels method</span></span>

<span data-ttu-id="bb140-104">抓取記憶體中用來儲存範例的色彩通道數目。</span><span class="sxs-lookup"><span data-stu-id="bb140-104">Retrieves the number of color channels used in memory to store samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="bb140-105">語法</span><span class="sxs-lookup"><span data-stu-id="bb140-105">Syntax</span></span>


```C++
UINT GetNumChannels();
```



## <a name="parameters"></a><span data-ttu-id="bb140-106">參數</span><span class="sxs-lookup"><span data-stu-id="bb140-106">Parameters</span></span>

<span data-ttu-id="bb140-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="bb140-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="bb140-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="bb140-108">Return value</span></span>

<span data-ttu-id="bb140-109">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="bb140-109">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="bb140-110">傳回記憶體中用來儲存範例的色彩通道數目。</span><span class="sxs-lookup"><span data-stu-id="bb140-110">Returns the number of color channels used in memory to store samples.</span></span> <span data-ttu-id="bb140-111">此值通常會是1以表示亮度值，或3表示 RGB 值。</span><span class="sxs-lookup"><span data-stu-id="bb140-111">The value generally will be either 1 to represent luminance values, or 3 to represent RGB values.</span></span>

## <a name="requirements"></a><span data-ttu-id="bb140-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="bb140-112">Requirements</span></span>



| <span data-ttu-id="bb140-113">需求</span><span class="sxs-lookup"><span data-stu-id="bb140-113">Requirement</span></span> | <span data-ttu-id="bb140-114">值</span><span class="sxs-lookup"><span data-stu-id="bb140-114">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="bb140-115">標頭</span><span class="sxs-lookup"><span data-stu-id="bb140-115">Header</span></span><br/>  | <dl> <span data-ttu-id="bb140-116"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="bb140-116"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="bb140-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="bb140-117">Library</span></span><br/> | <dl> <span data-ttu-id="bb140-118"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="bb140-118"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="bb140-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bb140-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bb140-120">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="bb140-120">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
