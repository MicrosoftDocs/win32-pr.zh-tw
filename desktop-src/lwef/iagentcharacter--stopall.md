---
title: IAgentCharacter StopAll
description: IAgentCharacter StopAll
ms.assetid: cb0ce220-7b35-45c0-b587-30939d26740f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9bbe745f0611d184fefd729c04e50635bc4006e8
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106967633"
---
# <a name="iagentcharacterstopall"></a><span data-ttu-id="d1d18-103">IAgentCharacter::StopAll</span><span class="sxs-lookup"><span data-stu-id="d1d18-103">IAgentCharacter::StopAll</span></span>

<span data-ttu-id="d1d18-104">\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="d1d18-104">\[Microsoft Agent is deprecated as of Windows 7, and may be unavailable in subsequent versions of Windows.\]</span></span>

``` syntax
HRESULT StopAll();
   long lType,  // request type
```

<span data-ttu-id="d1d18-105">停止 (要求) 的所有動畫，並將其從字元的動畫佇列中移除。</span><span class="sxs-lookup"><span data-stu-id="d1d18-105">Stops all animations (requests) and removes them from the character's animation queue.</span></span>

<dl> <dt>

<span data-ttu-id="d1d18-106"><span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*</span><span class="sxs-lookup"><span data-stu-id="d1d18-106"><span id="lType"></span><span id="ltype"></span><span id="LTYPE"></span>*lType*</span></span>
</dt> <dd>

<span data-ttu-id="d1d18-107">代表要停止 (的要求類型，並從字元的佇列) 移除的位位，由下列所組成：</span><span class="sxs-lookup"><span data-stu-id="d1d18-107">A bitfield that indicates the types of requests to stop (and remove from the character's queue), comprised from the following:</span></span>



|                                                                                   |                                                                                                          |
|-----------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1d18-108">**const 不帶正負號的 long** **STOP \_ TYPE \_ ALL = 0xffffffff;**</span><span class="sxs-lookup"><span data-stu-id="d1d18-108">**const unsigned long** **STOP\_TYPE\_ALL = 0xFFFFFFFF;**</span></span><br/>              | <span data-ttu-id="d1d18-109">停止所有的動畫要求，包括未排入佇列的 [**準備**](iagentcharacter--prepare.md) 要求。</span><span class="sxs-lookup"><span data-stu-id="d1d18-109">Stops all animation requests, including non-queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span> |
| <span data-ttu-id="d1d18-110">**const 不帶正負號的 long** **STOP \_ 類型 \_ PLAY = 0x00000001;**</span><span class="sxs-lookup"><span data-stu-id="d1d18-110">**const unsigned long** **STOP\_TYPE\_PLAY = 0x00000001;**</span></span><br/>             | <span data-ttu-id="d1d18-111">停止所有播放要求。</span><span class="sxs-lookup"><span data-stu-id="d1d18-111">Stops all Play requests.</span></span>                                                                                 |
| <span data-ttu-id="d1d18-112">**const 不帶正負號的 long** **STOP \_ 類型 \_ MOVE = 0x00000002;**</span><span class="sxs-lookup"><span data-stu-id="d1d18-112">**const unsigned long** **STOP\_TYPE\_MOVE = 0x00000002;**</span></span><br/>             | <span data-ttu-id="d1d18-113">停止所有 [**移動**](https://www.bing.com/search?q=**Move**) 要求。</span><span class="sxs-lookup"><span data-stu-id="d1d18-113">Stops all [**Move**](https://www.bing.com/search?q=**Move**) requests.</span></span>                                               |
| <span data-ttu-id="d1d18-114">**const 不帶正負號的 long** **STOP \_ 類型 \_ 話 = 0x00000004;**</span><span class="sxs-lookup"><span data-stu-id="d1d18-114">**const unsigned long** **STOP\_TYPE\_SPEAK = 0x00000004;**</span></span><br/>            | <span data-ttu-id="d1d18-115">停止所有 [**朗讀**](iagentcharacter--speak.md) 的要求。</span><span class="sxs-lookup"><span data-stu-id="d1d18-115">Stops all [**Speak**](iagentcharacter--speak.md) requests.</span></span>                                              |
| <span data-ttu-id="d1d18-116">**const 不帶正負號的 long** **STOP \_ TYPE \_ PREPARE = 0x00000008;**</span><span class="sxs-lookup"><span data-stu-id="d1d18-116">**const unsigned long** **STOP\_TYPE\_PREPARE = 0x00000008;**</span></span><br/>          | <span data-ttu-id="d1d18-117">停止所有已排入佇列的 [**準備**](iagentcharacter--prepare.md) 要求。</span><span class="sxs-lookup"><span data-stu-id="d1d18-117">Stops all queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span>                                   |
| <span data-ttu-id="d1d18-118">**const 不帶正負號的 long** **STOP \_ 類型 \_ NONQUEUEDPREPARE = 0x00000010;**</span><span class="sxs-lookup"><span data-stu-id="d1d18-118">**const unsigned long** **STOP\_TYPE\_NONQUEUEDPREPARE = 0x00000010;**</span></span><br/> | <span data-ttu-id="d1d18-119">停止所有未排入佇列的 [**準備**](iagentcharacter--prepare.md) 要求。</span><span class="sxs-lookup"><span data-stu-id="d1d18-119">Stops all non-queued [**Prepare**](iagentcharacter--prepare.md) requests.</span></span>                               |
| <span data-ttu-id="d1d18-120">**const 不帶正負號的 long** **STOP \_ 類型 \_ VISIBLE = 0x00000020;**</span><span class="sxs-lookup"><span data-stu-id="d1d18-120">**const unsigned long** **STOP\_TYPE\_VISIBLE = 0x00000020;**</span></span><br/>          | <span data-ttu-id="d1d18-121">停止所有 [**隱藏**](iagentcharacter--hide.md) 或 [**顯示**](iagentcharacter--show.md) 要求。</span><span class="sxs-lookup"><span data-stu-id="d1d18-121">Stops all [**Hide**](iagentcharacter--hide.md) or [**Show**](iagentcharacter--show.md) requests.</span></span>       |



 

</dd> </dl>

## <a name="see-also"></a><span data-ttu-id="d1d18-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1d18-122">See Also</span></span>

[<span data-ttu-id="d1d18-123">**IAgentCharacter：： Stop**</span><span class="sxs-lookup"><span data-stu-id="d1d18-123">**IAgentCharacter::Stop**</span></span>](iagentcharacter--stop.md)


 

 





