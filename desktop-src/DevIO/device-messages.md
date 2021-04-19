---
description: 裝置訊息是通知應用程式和其他裝置變更事件功能的系統訊息。
ms.assetid: 4d1ace87-2d02-4ba4-9bcc-da86cf3481db
title: 裝置訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e22fe5b9f8b3f9fcc2a075767aa684bd92962f32
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973178"
---
# <a name="device-messages"></a><span data-ttu-id="f27b7-103">裝置訊息</span><span class="sxs-lookup"><span data-stu-id="f27b7-103">Device Messages</span></span>

<span data-ttu-id="f27b7-104">裝置訊息是通知應用程式和其他裝置變更事件功能的系統訊息。</span><span class="sxs-lookup"><span data-stu-id="f27b7-104">Device messages are system messages that notify applications and other features of device change events.</span></span> <span data-ttu-id="f27b7-105">當系統偵測到系統硬體有變更時，就會發生這些事件，例如當使用者將膝上型電腦停駐和取消停用，或是插入或移除裝置（例如 PCMCIA 卡）時。</span><span class="sxs-lookup"><span data-stu-id="f27b7-105">These events occur whenever the system detects a change to the system hardware, such as when the user docks and undocks a laptop computer, or inserts or removes a device such as a PCMCIA card.</span></span> <span data-ttu-id="f27b7-106">裝置事件可能會在系統執行時，或在暫時擱置後系統繼續操作時發生。</span><span class="sxs-lookup"><span data-stu-id="f27b7-106">Device events can occur while the system is running or when the system resumes operation after temporarily being suspended.</span></span>

<span data-ttu-id="f27b7-107">為了確保應用程式在裝置無法使用時不會遺失資料，系統會監視硬體設定，並將裝置訊息傳送至應用程式，以通知這些變更，並讓他們有機會在變更發生前加以準備。</span><span class="sxs-lookup"><span data-stu-id="f27b7-107">To help ensure that applications do not lose data when devices become unavailable, the system monitors the hardware configuration and sends device messages to the applications to notify them of the changes and to give them the opportunity to prepare for the changes before they occur.</span></span>

<span data-ttu-id="f27b7-108">針對每個裝置事件，系統會將 [**WM \_ DEVICECHANGE**](wm-devicechange.md) 訊息廣播至所有應用程式。</span><span class="sxs-lookup"><span data-stu-id="f27b7-108">For each device event, the system broadcasts a [**WM\_DEVICECHANGE**](wm-devicechange.md) message to all applications.</span></span> <span data-ttu-id="f27b7-109">在此訊息中， *wParam* 參數會識別 [裝置事件種類](device-event-types.md) ，而 *lParam* 參數是事件特定資料的指標。</span><span class="sxs-lookup"><span data-stu-id="f27b7-109">In this message, the *wParam* parameter identifies the [device event type](device-event-types.md) and the *lParam* parameter is a pointer to event-specific data.</span></span>

 

 



