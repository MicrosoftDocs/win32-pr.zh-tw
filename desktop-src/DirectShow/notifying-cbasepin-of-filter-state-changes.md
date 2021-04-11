---
description: 通知 CBasePin 篩選狀態變更
ms.assetid: 521ba95b-1f2d-4ad0-ab9b-4f1e3343a2d3
title: 通知 CBasePin 篩選狀態變更
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 49dad6fabc162eb2384283ce2fc8914f76707036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104317676"
---
# <a name="notifying-cbasepin-of-filter-state-changes"></a><span data-ttu-id="70523-103">通知 CBasePin 篩選狀態變更</span><span class="sxs-lookup"><span data-stu-id="70523-103">Notifying CBasePin of Filter State Changes</span></span>

<span data-ttu-id="70523-104">當擁有篩選準則的狀態變更時，就會通知 **CBasePin** 類別。</span><span class="sxs-lookup"><span data-stu-id="70523-104">The **CBasePin** class is notified whenever the state of the owning filter changes.</span></span> <span data-ttu-id="70523-105">針對每個狀態轉換，篩選準則會在 pin 上呼叫對應的方法，如下表所示。</span><span class="sxs-lookup"><span data-stu-id="70523-105">For each state transition, the filter calls a corresponding method on the pin, as shown in the following table.</span></span>



| <span data-ttu-id="70523-106">新的篩選準則狀態</span><span class="sxs-lookup"><span data-stu-id="70523-106">New Filter State</span></span> | <span data-ttu-id="70523-107">CBasePin 方法</span><span class="sxs-lookup"><span data-stu-id="70523-107">CBasePin Method</span></span>                                 |
|------------------|-------------------------------------------------|
| <span data-ttu-id="70523-108">已停止</span><span class="sxs-lookup"><span data-stu-id="70523-108">Stopped</span></span>          | [<span data-ttu-id="70523-109">**CBasePin：：非使用中**</span><span class="sxs-lookup"><span data-stu-id="70523-109">**CBasePin::Inactive**</span></span>](cbasepin-inactive.md) |
| <span data-ttu-id="70523-110">已暫停</span><span class="sxs-lookup"><span data-stu-id="70523-110">Paused</span></span>           | [<span data-ttu-id="70523-111">**CBasePin：： Active**</span><span class="sxs-lookup"><span data-stu-id="70523-111">**CBasePin::Active**</span></span>](cbasepin-active.md)     |
| <span data-ttu-id="70523-112">執行中</span><span class="sxs-lookup"><span data-stu-id="70523-112">Running</span></span>          | [<span data-ttu-id="70523-113">**CBasePin：： Run**</span><span class="sxs-lookup"><span data-stu-id="70523-113">**CBasePin::Run**</span></span>](cbasepin-run.md)           |



 

<span data-ttu-id="70523-114">衍生類別應該覆寫這些方法，以回應狀態變更。</span><span class="sxs-lookup"><span data-stu-id="70523-114">The derived class should override these methods to respond to the state change.</span></span> <span data-ttu-id="70523-115">根據篩選準則，pin 可能會啟動可傳遞範例、認可或取消認可其記憶體配置器等的工作者執行緒。</span><span class="sxs-lookup"><span data-stu-id="70523-115">Depending on the filter, the pin might start a worker thread that delivers samples, commit or decommit its memory allocator, and so forth.</span></span>

 

 



