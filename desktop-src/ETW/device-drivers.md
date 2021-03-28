---
description: 本檔適用于想要使用 ETW 進行事件追蹤的使用者模式應用程式。
ms.assetid: 4d5ae7f7-dd15-4940-bb92-277e80927da6
title: 設備磁碟機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f04cebec3e947da52c374b4ffe15f9a7ccaeb53d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972217"
---
# <a name="device-drivers"></a><span data-ttu-id="bafcd-103">設備磁碟機</span><span class="sxs-lookup"><span data-stu-id="bafcd-103">Device Drivers</span></span>

<span data-ttu-id="bafcd-104">本檔適用于想要使用 ETW 進行事件追蹤的使用者模式應用程式。</span><span class="sxs-lookup"><span data-stu-id="bafcd-104">This documentation is for user-mode applications that want to use ETW for event tracing.</span></span> <span data-ttu-id="bafcd-105">本檔不適用於以核心模式執行的設備磁碟機。</span><span class="sxs-lookup"><span data-stu-id="bafcd-105">This documentation is not for device drivers that run in kernel-mode.</span></span> <span data-ttu-id="bafcd-106">對於撰寫設備磁碟機和核心模式的應用程式，如果想要使用 ETW 作為低影響的偵錯工具來疑難排解時間相關問題，請參閱 Windows 驅動程式套件 (WDK) 的 [Windows 事件追蹤](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-)、 [WPP 軟體追蹤](/windows-hardware/drivers/devtest/wpp-software-tracing)，以及 [WMI 事件追蹤](/windows-hardware/drivers/kernel/wmi-event-tracing) 以瞭解檢測驅動程式的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="bafcd-106">For those writing device drivers and kernel-mode applications that want to use ETW as a low-impact debugger to troubleshoot timing-related problems, see [Event Tracing for Windows](/windows-hardware/drivers/devtest/event-tracing-for-windows--etw-), [WPP Software Tracing](/windows-hardware/drivers/devtest/wpp-software-tracing), and [WMI Event Tracing](/windows-hardware/drivers/kernel/wmi-event-tracing) in the Windows Driver Kit (WDK) for information on instrumenting your driver.</span></span>

 

 
