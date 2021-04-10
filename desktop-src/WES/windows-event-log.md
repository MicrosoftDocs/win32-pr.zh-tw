---
title: Windows 事件記錄檔
description: Windows 事件記錄檔 API 會定義您用來撰寫檢測資訊清單的架構。
ms.assetid: 738c8afa-4714-4d4f-9231-b8fbdb5159c5
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9df51efc878af2770ad056e6e1f84b8f4f2566
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103842707"
---
# <a name="windows-event-log"></a><span data-ttu-id="8f60b-103">Windows 事件記錄檔</span><span class="sxs-lookup"><span data-stu-id="8f60b-103">Windows Event Log</span></span>

## <a name="purpose"></a><span data-ttu-id="8f60b-104">目的</span><span class="sxs-lookup"><span data-stu-id="8f60b-104">Purpose</span></span>

<span data-ttu-id="8f60b-105">Windows 事件記錄檔 API 會定義您用來撰寫檢測資訊清單的架構。</span><span class="sxs-lookup"><span data-stu-id="8f60b-105">The Windows Event Log API defines the schema that you use to write an instrumentation manifest.</span></span> <span data-ttu-id="8f60b-106">檢測資訊清單會識別您的事件提供者和其所記錄的事件。</span><span class="sxs-lookup"><span data-stu-id="8f60b-106">An instrumentation manifest identifies your event provider and the events that it logs.</span></span> <span data-ttu-id="8f60b-107">此 API 也包含事件取用者（例如 [事件檢視器](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11))）將用來讀取和轉譯事件的函式。</span><span class="sxs-lookup"><span data-stu-id="8f60b-107">The API also includes the functions that an event consumer, such as the [Event Viewer](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc766042(v=ws.11)), would use to read and render the events.</span></span> <span data-ttu-id="8f60b-108">若要寫入資訊清單中定義的事件，請使用 [事件追蹤](/windows/desktop/ETW/event-tracing-portal) (ETW) API 中包含的函式。</span><span class="sxs-lookup"><span data-stu-id="8f60b-108">To write the events defined in the manifest, use the functions included in the [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) API.</span></span>

<span data-ttu-id="8f60b-109">Windows 事件記錄檔會取代從 Windows Vista 作業系統開始的 [事件記錄](/windows/desktop/EventLog/event-logging) API。</span><span class="sxs-lookup"><span data-stu-id="8f60b-109">Windows Event Log supersedes the [Event Logging](/windows/desktop/EventLog/event-logging) API beginning with the Windows Vista operating system.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="8f60b-110">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="8f60b-110">Developer audience</span></span>

<span data-ttu-id="8f60b-111">Windows 事件記錄檔是針對 C/c + + 程式設計人員所設計。</span><span class="sxs-lookup"><span data-stu-id="8f60b-111">Windows Event Log is designed for C/C++ programmers.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="8f60b-112">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="8f60b-112">Run-time requirements</span></span>

<span data-ttu-id="8f60b-113">從 Windows Vista 和 Windows Server 2008 開始，windows 事件記錄檔已包含在作業系統中。</span><span class="sxs-lookup"><span data-stu-id="8f60b-113">Windows Event Log is included in the operating system beginning with Windows Vista and Windows Server 2008.</span></span>

<span data-ttu-id="8f60b-114">如需特定程式設計專案之執行時間需求的詳細資訊，請參閱該元素之 [參考] 頁面的 [需求] 區段。</span><span class="sxs-lookup"><span data-stu-id="8f60b-114">For information about run-time requirements for a particular programming element, see the Requirements section of the reference page for that element.</span></span>

<span data-ttu-id="8f60b-115">如需完整的版本歷程記錄，請參閱 [新功能](what-s-new.md)。</span><span class="sxs-lookup"><span data-stu-id="8f60b-115">For complete version history, see [What's New](what-s-new.md).</span></span>

## <a name="in-this-section"></a><span data-ttu-id="8f60b-116">本節內容</span><span class="sxs-lookup"><span data-stu-id="8f60b-116">In this section</span></span>


| <span data-ttu-id="8f60b-117">主題</span><span class="sxs-lookup"><span data-stu-id="8f60b-117">Topic</span></span>                                                        | <span data-ttu-id="8f60b-118">描述</span><span class="sxs-lookup"><span data-stu-id="8f60b-118">Description</span></span>                                                                                       |
|--------------------------------------------------------------|---------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="8f60b-119">使用 Windows 事件記錄檔</span><span class="sxs-lookup"><span data-stu-id="8f60b-119">Using Windows Event Log</span></span>](using-windows-event-log.md)        | <span data-ttu-id="8f60b-120">說明如何使用 Windows 事件記錄檔 API 的程式指南。</span><span class="sxs-lookup"><span data-stu-id="8f60b-120">Procedural guide that shows how to use the Windows Event Log API.</span></span>                                 |
| [<span data-ttu-id="8f60b-121">Windows 事件記錄檔參考</span><span class="sxs-lookup"><span data-stu-id="8f60b-121">Windows Event Log Reference</span></span>](windows-event-log-reference.md)| <span data-ttu-id="8f60b-122">API 包含的資料類型、函數、列舉、結構、常數和架構。</span><span class="sxs-lookup"><span data-stu-id="8f60b-122">The data types, functions, enumerations, structures, constants, and schemas that the API includes.</span></span>|