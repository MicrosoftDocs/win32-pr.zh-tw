---
description: CAMMsgEvent 類別是執行訊息處理之事件物件的包裝函式。
ms.assetid: 4b94febe-169f-4f04-be93-043a8c75e3b4
title: 'CAMMsgEvent 類別 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CAMMsgEvent
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: 4ebac7aae11f7a7b7d6b846e262e93b5759210b0
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106997004"
---
# <a name="cammsgevent-class"></a><span data-ttu-id="7df9c-103">CAMMsgEvent 類別</span><span class="sxs-lookup"><span data-stu-id="7df9c-103">CAMMsgEvent class</span></span>

![cammsgevent 類別階層](images/util06.png)

<span data-ttu-id="7df9c-105">`CAMMsgEvent`類別是執行訊息處理之事件物件的包裝函式。</span><span class="sxs-lookup"><span data-stu-id="7df9c-105">The `CAMMsgEvent` class is a wrapper for event objects that perform message processing.</span></span>

<span data-ttu-id="7df9c-106">這個類別衍生自 [**CAMEvent**](camevent.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="7df9c-106">This class derives from the [**CAMEvent**](camevent.md) object.</span></span> <span data-ttu-id="7df9c-107">它會新增一個方法 [**CAMMsgEvent：： WaitMsg**](cammsgevent-waitmsg.md)，這會在等候時分派傳入訊息。</span><span class="sxs-lookup"><span data-stu-id="7df9c-107">It adds one method, [**CAMMsgEvent::WaitMsg**](cammsgevent-waitmsg.md), which dispatches incoming messages while waiting.</span></span>



| <span data-ttu-id="7df9c-108">公用方法</span><span class="sxs-lookup"><span data-stu-id="7df9c-108">Public Methods</span></span>                                 | <span data-ttu-id="7df9c-109">Description</span><span class="sxs-lookup"><span data-stu-id="7df9c-109">Description</span></span>                                                          |
|------------------------------------------------|----------------------------------------------------------------------|
| [<span data-ttu-id="7df9c-110">**CAMMsgEvent**</span><span class="sxs-lookup"><span data-stu-id="7df9c-110">**CAMMsgEvent**</span></span>](cammsgevent-cammsgevent.md) | <span data-ttu-id="7df9c-111">建構函式。</span><span class="sxs-lookup"><span data-stu-id="7df9c-111">Constructor.</span></span>                                                         |
| [<span data-ttu-id="7df9c-112">**WaitMsg**</span><span class="sxs-lookup"><span data-stu-id="7df9c-112">**WaitMsg**</span></span>](cammsgevent-waitmsg.md)         | <span data-ttu-id="7df9c-113">在分派傳送的訊息時，等候事件收到信號。</span><span class="sxs-lookup"><span data-stu-id="7df9c-113">Waits for the event to be signaled, while dispatching sent messages.</span></span> |



 

## <a name="requirements"></a><span data-ttu-id="7df9c-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="7df9c-114">Requirements</span></span>



| <span data-ttu-id="7df9c-115">需求</span><span class="sxs-lookup"><span data-stu-id="7df9c-115">Requirement</span></span> | <span data-ttu-id="7df9c-116">值</span><span class="sxs-lookup"><span data-stu-id="7df9c-116">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7df9c-117">標頭</span><span class="sxs-lookup"><span data-stu-id="7df9c-117">Header</span></span><br/>  | <dl> <span data-ttu-id="7df9c-118"><dt>Wxutil (包含： .h) </dt></span><span class="sxs-lookup"><span data-stu-id="7df9c-118"><dt>Wxutil.h (include Streams.h)</dt></span></span> </dl>                                                                                    |
| <span data-ttu-id="7df9c-119">程式庫</span><span class="sxs-lookup"><span data-stu-id="7df9c-119">Library</span></span><br/> | <dl> <span data-ttu-id="7df9c-120"><dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt></span><span class="sxs-lookup"><span data-stu-id="7df9c-120"><dt>Strmbase.lib (retail builds); </dt> <dt>Strmbasd.lib (debug builds)</dt></span></span> </dl> |



 

 




