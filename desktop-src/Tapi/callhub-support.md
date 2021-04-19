---
description: CallHub 追蹤是 TAPI 3.0 版中的新功能。
ms.assetid: 29b6e585-6da8-46a2-a612-f42d0f65f68e
title: CallHub 支援
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9efe6891cfdad956a87745f8e4b35dd117fe775e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987677"
---
# <a name="callhub-support"></a><span data-ttu-id="b5d75-103">CallHub 支援</span><span class="sxs-lookup"><span data-stu-id="b5d75-103">CallHub Support</span></span>

<span data-ttu-id="b5d75-104">CallHub 追蹤是 TAPI 3.0 版中的新功能。</span><span class="sxs-lookup"><span data-stu-id="b5d75-104">CallHub tracking is a new feature in TAPI version 3.0.</span></span> <span data-ttu-id="b5d75-105">CallHub 功能已新增至 TAPI 2.1 程式設計項目，並提供 Windows 2000。</span><span class="sxs-lookup"><span data-stu-id="b5d75-105">CallHub functionality was added to the TAPI 2.1 programming elements with the delivery of Windows 2000.</span></span> <span data-ttu-id="b5d75-106">*CallHub* 代表呼叫的協力廠商觀點，而 TAPI 的呼叫控制碼則代表來電的第一方觀點。</span><span class="sxs-lookup"><span data-stu-id="b5d75-106">A *CallHub* represents a third-party view of a call, and TAPI's call handles represent the first-party view of a call.</span></span> <span data-ttu-id="b5d75-107">使用 CallHub 追蹤時，會要求服務提供者遵循 CallHubs，並在 CallHub 的存留期內提供呼叫的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="b5d75-107">With CallHub tracking, the service provider is requested to follow CallHubs and give information about the call during the lifetime of a CallHub.</span></span> <span data-ttu-id="b5d75-108">當新的當事人加入並離開 CallHub 時，服務提供者應該告知 TAPI。</span><span class="sxs-lookup"><span data-stu-id="b5d75-108">As new parties join and leave the CallHub, the service provider should inform TAPI.</span></span>

<span data-ttu-id="b5d75-109">服務提供者不需要執行任何新的函數，就能支援 CallHub。</span><span class="sxs-lookup"><span data-stu-id="b5d75-109">A service provider does not need to implement any new functions in order to support CallHub.</span></span> <span data-ttu-id="b5d75-110">它只需要填入 [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)結構的 **dwCallID** 成員。</span><span class="sxs-lookup"><span data-stu-id="b5d75-110">It simply needs to fill in the **dwCallID** member of the [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) structure.</span></span> <span data-ttu-id="b5d75-111">在 TAPI 3 中，TAPI 會收集所有具有相同 **dwCallID** 的呼叫，並建立應用程式可用來追蹤通話的 CallHub 控制碼。</span><span class="sxs-lookup"><span data-stu-id="b5d75-111">In TAPI 3, TAPI collects all calls with the same **dwCallID** and creates a CallHub handle that the application can use to track the call.</span></span>

 

 
