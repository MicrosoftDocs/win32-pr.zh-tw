---
description: 抓取記憶體中用來儲存範例的色彩通道數目。
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
ms.openlocfilehash: 99456c6386a822489eca6beef41f639008007778
ms.sourcegitcommit: 14010c34b35fa268046c7683f021f86de08ddd0a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/15/2021
ms.locfileid: "106975715"
---
# <a name="id3dxprtbuffergetnumchannels-method"></a><span data-ttu-id="68709-103">ID3DXPRTBuffer：： GetNumChannels 方法</span><span class="sxs-lookup"><span data-stu-id="68709-103">ID3DXPRTBuffer::GetNumChannels method</span></span>

<span data-ttu-id="68709-104">抓取記憶體中用來儲存範例的色彩通道數目。</span><span class="sxs-lookup"><span data-stu-id="68709-104">Retrieves the number of color channels used in memory to store samples.</span></span>

## <a name="syntax"></a><span data-ttu-id="68709-105">語法</span><span class="sxs-lookup"><span data-stu-id="68709-105">Syntax</span></span>


```C++
UINT GetNumChannels();
```



## <a name="parameters"></a><span data-ttu-id="68709-106">參數</span><span class="sxs-lookup"><span data-stu-id="68709-106">Parameters</span></span>

<span data-ttu-id="68709-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="68709-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="68709-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="68709-108">Return value</span></span>

<span data-ttu-id="68709-109">類型： **[ **UINT**](../winprog/windows-data-types.md)**</span><span class="sxs-lookup"><span data-stu-id="68709-109">Type: **[**UINT**](../winprog/windows-data-types.md)**</span></span>

<span data-ttu-id="68709-110">傳回記憶體中用來儲存範例的色彩通道數目。</span><span class="sxs-lookup"><span data-stu-id="68709-110">Returns the number of color channels used in memory to store samples.</span></span> <span data-ttu-id="68709-111">此值通常會是1以表示亮度值，或3表示 RGB 值。</span><span class="sxs-lookup"><span data-stu-id="68709-111">The value generally will be either 1 to represent luminance values, or 3 to represent RGB values.</span></span>

## <a name="requirements"></a><span data-ttu-id="68709-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="68709-112">Requirements</span></span>



| <span data-ttu-id="68709-113">需求</span><span class="sxs-lookup"><span data-stu-id="68709-113">Requirement</span></span> | <span data-ttu-id="68709-114">值</span><span class="sxs-lookup"><span data-stu-id="68709-114">Value</span></span> |
|--------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="68709-115">標頭</span><span class="sxs-lookup"><span data-stu-id="68709-115">Header</span></span><br/>  | <dl> <span data-ttu-id="68709-116"><dt>D3DX9Mesh。h</dt></span><span class="sxs-lookup"><span data-stu-id="68709-116"><dt>D3DX9Mesh.h</dt></span></span> </dl> |
| <span data-ttu-id="68709-117">程式庫</span><span class="sxs-lookup"><span data-stu-id="68709-117">Library</span></span><br/> | <dl> <span data-ttu-id="68709-118"><dt>D3dx9 .lib</dt></span><span class="sxs-lookup"><span data-stu-id="68709-118"><dt>D3dx9.lib</dt></span></span> </dl>   |



## <a name="see-also"></a><span data-ttu-id="68709-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="68709-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="68709-120">ID3DXPRTBuffer</span><span class="sxs-lookup"><span data-stu-id="68709-120">ID3DXPRTBuffer</span></span>](id3dxprtbuffer.md)
</dt> </dl>

 

 
