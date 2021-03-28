---
description: 下列主題描述如何使用 ETW API 進行事件追蹤。
ms.assetid: 7362874a-8206-4973-bb79-a9eaff55feb4
title: 使用事件追蹤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5141c19838796c0ec29f9eb20add689d56b97757
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191609"
---
# <a name="using-event-tracing"></a><span data-ttu-id="0cded-103">使用事件追蹤</span><span class="sxs-lookup"><span data-stu-id="0cded-103">Using Event Tracing</span></span>

<span data-ttu-id="0cded-104">下列主題描述如何使用 ETW API 進行事件追蹤。</span><span class="sxs-lookup"><span data-stu-id="0cded-104">The following topics describe how to use the ETW API for event tracing.</span></span>



| <span data-ttu-id="0cded-105">主題</span><span class="sxs-lookup"><span data-stu-id="0cded-105">Topic</span></span>                                                                          | <span data-ttu-id="0cded-106">描述</span><span class="sxs-lookup"><span data-stu-id="0cded-106">Description</span></span>                                                                                                             |
|--------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="0cded-107">控制事件追蹤會話</span><span class="sxs-lookup"><span data-stu-id="0cded-107">Controlling Event Tracing Sessions</span></span>](controlling-event-tracing-sessions.md)   | <span data-ttu-id="0cded-108">說明如何管理事件追蹤會話。</span><span class="sxs-lookup"><span data-stu-id="0cded-108">Describes how to manage event tracing sessions.</span></span>                                                                         |
| [<span data-ttu-id="0cded-109">提供事件</span><span class="sxs-lookup"><span data-stu-id="0cded-109">Providing Events</span></span>](providing-events.md)                                       | <span data-ttu-id="0cded-110">說明如何註冊和檢測事件追蹤提供者。</span><span class="sxs-lookup"><span data-stu-id="0cded-110">Describes how to register and instrument an event trace provider.</span></span>                                                       |
| [<span data-ttu-id="0cded-111">使用事件</span><span class="sxs-lookup"><span data-stu-id="0cded-111">Consuming Events</span></span>](consuming-events.md)                                       | <span data-ttu-id="0cded-112">描述如何實回呼函式，用來從追蹤記錄檔或即時取用和處理事件。</span><span class="sxs-lookup"><span data-stu-id="0cded-112">Describes how to implement callback functions used to consume and process events from a trace log file or in real time.</span></span> |
| [<span data-ttu-id="0cded-113">Windows 軟體追蹤預處理器</span><span class="sxs-lookup"><span data-stu-id="0cded-113">Windows Software Trace Preprocessor</span></span>](windows-software-trace-preprocessor.md) | <span data-ttu-id="0cded-114">提供有效的機制來記錄和取用應用程式或驅動程式執行期間所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="0cded-114">Provides an efficient mechanism to log and consume events that occur during the execution of an application or driver.</span></span>  |



 

<span data-ttu-id="0cded-115">在包含 Evntrace .h 標頭檔之前，請先包含 Wmistr .h 標頭檔。</span><span class="sxs-lookup"><span data-stu-id="0cded-115">Include the Wmistr.h header file before including the Evntrace.h header file.</span></span>

 

 



