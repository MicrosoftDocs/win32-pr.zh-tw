---
title: BufferAverage
description: BufferAverage 屬性包含變數位元速率 (VBR) 資料流程所需的平均緩衝區大小。
ms.assetid: 5fd69534-6655-4c98-bf07-a694585fc9ae
keywords:
- BufferAverage windows Media 格式
topic_type:
- apiref
api_name:
- BufferAverage
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ce5767ed329fde43cc1022af54d937fc99e0e323
ms.sourcegitcommit: 57758ecb246c84d65e6e0e4bd5570d9176fa39cd
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/25/2019
ms.locfileid: "104092406"
---
# <a name="bufferaverage"></a><span data-ttu-id="9d6d4-104">BufferAverage</span><span class="sxs-lookup"><span data-stu-id="9d6d4-104">BufferAverage</span></span>

<span data-ttu-id="9d6d4-105">**BufferAverage** 屬性包含變數位元速率 (VBR) 資料流程所需的平均緩衝區大小。</span><span class="sxs-lookup"><span data-stu-id="9d6d4-105">The **BufferAverage** attribute contains the average buffer size needed for a variable bit rate (VBR) stream.</span></span>

## <a name="global-constant"></a><span data-ttu-id="9d6d4-106">全域常數</span><span class="sxs-lookup"><span data-stu-id="9d6d4-106">Global Constant</span></span>

<span data-ttu-id="9d6d4-107">g \_ wszBufferAverage</span><span class="sxs-lookup"><span data-stu-id="9d6d4-107">g\_wszBufferAverage</span></span>

## <a name="data-type"></a><span data-ttu-id="9d6d4-108">資料類型</span><span class="sxs-lookup"><span data-stu-id="9d6d4-108">Data Type</span></span>

<span data-ttu-id="9d6d4-109">**WMT \_ 類型 \_ DWORD**</span><span class="sxs-lookup"><span data-stu-id="9d6d4-109">**WMT\_TYPE\_DWORD**</span></span>

## <a name="remarks"></a><span data-ttu-id="9d6d4-110">備註</span><span class="sxs-lookup"><span data-stu-id="9d6d4-110">Remarks</span></span>

<span data-ttu-id="9d6d4-111">存取寫入器物件的 **IWMHeaderInfo3** 介面時，您可以加入或變更此值。</span><span class="sxs-lookup"><span data-stu-id="9d6d4-111">When accessing the **IWMHeaderInfo3** interface of the writer object, you can add or change this value.</span></span> <span data-ttu-id="9d6d4-112">在其他物件 (中繼資料編輯器、讀取器和同步讀取器) ，此值是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="9d6d4-112">In other objects (metadata editor, reader, and synchronous reader), this value is read-only.</span></span>

<span data-ttu-id="9d6d4-113">寫入器會自動為每個 VBR 串流寫入 **BufferAverage** 值。</span><span class="sxs-lookup"><span data-stu-id="9d6d4-113">The writer automatically writes a **BufferAverage** value for each VBR stream.</span></span>

## <a name="see-also"></a><span data-ttu-id="9d6d4-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d6d4-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d6d4-115">**屬性清單**</span><span class="sxs-lookup"><span data-stu-id="9d6d4-115">**Attribute List**</span></span>](attribute-list.md)
</dt> </dl>

 

 




