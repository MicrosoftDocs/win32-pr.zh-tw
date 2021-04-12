---
title: 開發提供者
description: 若要寫入您在資訊清單中定義的事件，您可以使用事件追蹤 (ETW) API 中所含的函式。 如需撰寫提供者的詳細資訊，請參閱提供事件。
ms.assetid: 23de19c4-5f8d-4faa-acd9-fe6208ca17a9
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 83939429f1dc4d499e7c2d0e0c2bfa7a47522ffe
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093164"
---
# <a name="developing-a-provider"></a><span data-ttu-id="50e13-104">開發提供者</span><span class="sxs-lookup"><span data-stu-id="50e13-104">Developing a Provider</span></span>

<span data-ttu-id="50e13-105">若要寫入您在資訊清單中定義的事件，您可以使用 [事件追蹤](/windows/desktop/ETW/event-tracing-portal) (ETW) API 中所含的函式。</span><span class="sxs-lookup"><span data-stu-id="50e13-105">To write the events that you define in your manifest, you use the functions included in the [Event Tracing](/windows/desktop/ETW/event-tracing-portal) (ETW) API.</span></span> <span data-ttu-id="50e13-106">如需撰寫提供者的詳細資訊，請參閱 [提供事件](/windows/desktop/ETW/providing-events)。</span><span class="sxs-lookup"><span data-stu-id="50e13-106">For details on writing a provider, see [Providing Events](/windows/desktop/ETW/providing-events).</span></span>

<span data-ttu-id="50e13-107">撰寫提供者之後，請使用 WevtUtil.exe 工具來註冊提供者和架構。</span><span class="sxs-lookup"><span data-stu-id="50e13-107">After writing the provider, use the WevtUtil.exe tool to register the provider and schema.</span></span> <span data-ttu-id="50e13-108">如需使用 WevtUtil 的詳細資訊，請參閱 [Windows 事件記錄工具](windows-event-log-tools.md)。</span><span class="sxs-lookup"><span data-stu-id="50e13-108">For details on using WevtUtil, see [Windows Event Log Tools](windows-event-log-tools.md).</span></span> <span data-ttu-id="50e13-109">以下顯示如何使用 WevtUtil 來註冊提供者和移除註冊。</span><span class="sxs-lookup"><span data-stu-id="50e13-109">The following shows how to use WevtUtil to register a provider and to remove the registration.</span></span>


```cmd
wevtutil im provider.man

wevtutil um provider.man
```