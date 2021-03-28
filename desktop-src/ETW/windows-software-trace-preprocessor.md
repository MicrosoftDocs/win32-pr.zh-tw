---
description: Windows 軟體追蹤處理器 (的 WPP) 提供有效的機制，可記錄應用程式或驅動程式執行期間所發生的事件。 WPP 使用 ETW API。
ms.assetid: 3a6f441a-ae36-4cce-aa83-78a4e53c9b1a
title: 寫入 WPP 事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c0f0d4deb580a3f81f3c6c87f6ca5ca4518f735e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972260"
---
# <a name="writing-wpp-events"></a><span data-ttu-id="dd295-104">寫入 WPP 事件</span><span class="sxs-lookup"><span data-stu-id="dd295-104">Writing WPP Events</span></span>

<span data-ttu-id="dd295-105">Windows 軟體追蹤處理器 (的 WPP) 提供有效的機制，可記錄應用程式或驅動程式執行期間所發生的事件。</span><span class="sxs-lookup"><span data-stu-id="dd295-105">The Windows software trace processor (WPP) provides an efficient mechanism to log events that occur during the execution of an application or driver.</span></span> <span data-ttu-id="dd295-106">WPP 使用 ETW API。</span><span class="sxs-lookup"><span data-stu-id="dd295-106">WPP uses the ETW API.</span></span>

<span data-ttu-id="dd295-107">如需使用 WPP 來記錄事件的詳細資訊，請參閱 Microsoft Windows 驅動程式開發工具組中的 [WPP 軟體追蹤](/windows-hardware/drivers/devtest/wpp-software-tracing) 和 [軟體追蹤常見問題](/windows-hardware/drivers/devtest/software-tracing-faq) (DDK) 。</span><span class="sxs-lookup"><span data-stu-id="dd295-107">For details on using WPP to log events, see [WPP Software Tracing](/windows-hardware/drivers/devtest/wpp-software-tracing) and [Software Tracing FAQ](/windows-hardware/drivers/devtest/software-tracing-faq) in the Microsoft Windows Driver Development Kit (DDK).</span></span>

 

 
