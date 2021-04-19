---
description: CMsgThread 類別支援工作者執行緒，要求可以用非同步方式張貼，而不是直接傳送。
ms.assetid: 1cf159c9-80d0-4e3b-88d8-2ba4cd18e768
title: CMsg 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CMsg
api_type:
- COM
api_location: ''
ms.openlocfilehash: a57a841b9c36a21895099c931acbf18a1e01ea0f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106972311"
---
# <a name="cmsg-class"></a><span data-ttu-id="44b08-103">CMsg 類別</span><span class="sxs-lookup"><span data-stu-id="44b08-103">CMsg class</span></span>

<span data-ttu-id="44b08-104">[**CMsgThread**](cmsgthread.md)類別支援工作者執行緒，要求可以用非同步方式張貼，而不是直接傳送。</span><span class="sxs-lookup"><span data-stu-id="44b08-104">The [**CMsgThread**](cmsgthread.md) class provides support for a worker thread to which requests can be posted asynchronously instead of sent directly.</span></span> <span data-ttu-id="44b08-105">[**CAMThread**](camthread.md)類別提供可傳送單一要求的工作者執行緒。</span><span class="sxs-lookup"><span data-stu-id="44b08-105">The [**CAMThread**](camthread.md) class provides a worker thread to which single requests can be sent.</span></span> <span data-ttu-id="44b08-106">一次只能有一個用戶端提出要求，而用戶端會封鎖，直到工作者執行緒完成要求為止。</span><span class="sxs-lookup"><span data-stu-id="44b08-106">Only one client can make a request at a time, and the client blocks until the worker thread has completed the request.</span></span> <span data-ttu-id="44b08-107">相反地， **CMsgThread** 類別會提供可以張貼任意數量要求的工作者執行緒。</span><span class="sxs-lookup"><span data-stu-id="44b08-107">By contrast, the **CMsgThread** class provides a worker thread to which any number of requests can be posted.</span></span> <span data-ttu-id="44b08-108">以物件) 形式 (的要求 `CMsg` 會以非同步方式排入佇列並依序執行。</span><span class="sxs-lookup"><span data-stu-id="44b08-108">The requests (in the form of a `CMsg` object) are queued and executed in order, asynchronously.</span></span> <span data-ttu-id="44b08-109">未收到回復或傳回值。</span><span class="sxs-lookup"><span data-stu-id="44b08-109">No reply or return value is received.</span></span>



| <span data-ttu-id="44b08-110">資料成員</span><span class="sxs-lookup"><span data-stu-id="44b08-110">Data Members</span></span>              | <span data-ttu-id="44b08-111">Description</span><span class="sxs-lookup"><span data-stu-id="44b08-111">Description</span></span>                                                                                                                                                                       |
|---------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="44b08-112">dwFlags</span><span class="sxs-lookup"><span data-stu-id="44b08-112">dwFlags</span></span>                   | <span data-ttu-id="44b08-113">要求碼的旗標參數。</span><span class="sxs-lookup"><span data-stu-id="44b08-113">Flag parameter to the request code.</span></span>                                                                                                                                               |
| <span data-ttu-id="44b08-114">lpParam</span><span class="sxs-lookup"><span data-stu-id="44b08-114">lpParam</span></span>                   | <span data-ttu-id="44b08-115">背景工作執行緒所需的資料做為參數或傳回值。</span><span class="sxs-lookup"><span data-stu-id="44b08-115">Data required by the worker thread as parameter or return values.</span></span> <span data-ttu-id="44b08-116">此資料不應以堆疊為基礎，因為它會在完成佇列作業之後被參考一段時間。</span><span class="sxs-lookup"><span data-stu-id="44b08-116">This data should not be stack-based, as it will be referenced some time after completing the queuing operation.</span></span> |
| <span data-ttu-id="44b08-117">pEvent</span><span class="sxs-lookup"><span data-stu-id="44b08-117">pEvent</span></span>                    | <span data-ttu-id="44b08-118">背景工作執行緒可以指示的事件物件，表示作業已完成。</span><span class="sxs-lookup"><span data-stu-id="44b08-118">Event object that a worker thread can signal to indicate the completion of the operation.</span></span>                                                                                         |
| <span data-ttu-id="44b08-119">uMsg</span><span class="sxs-lookup"><span data-stu-id="44b08-119">uMsg</span></span>                      | <span data-ttu-id="44b08-120">由執行緒類別的用戶端所定義，且由覆寫的背景工作執行緒函數所瞭解的要求程式碼。</span><span class="sxs-lookup"><span data-stu-id="44b08-120">Request code that is defined by the client of the thread class and understood by the overridden worker thread function.</span></span>                                                           |
| <span data-ttu-id="44b08-121">成員函數</span><span class="sxs-lookup"><span data-stu-id="44b08-121">Member Functions</span></span>          | <span data-ttu-id="44b08-122">Description</span><span class="sxs-lookup"><span data-stu-id="44b08-122">Description</span></span>                                                                                                                                                                       |
| [<span data-ttu-id="44b08-123">**CMsg**</span><span class="sxs-lookup"><span data-stu-id="44b08-123">**CMsg**</span></span>](cmsg-cmsg.md) | <span data-ttu-id="44b08-124">結構 [**CMsg**](cmsg-cmsg.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="44b08-124">Constructs a [**CMsg**](cmsg-cmsg.md) object.</span></span>                                                                                                                                    |



 

 

 



