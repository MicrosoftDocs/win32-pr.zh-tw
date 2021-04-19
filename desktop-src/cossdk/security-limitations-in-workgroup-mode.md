---
description: 工作組模式中的安全性限制
ms.assetid: 05c0aba7-b94b-49d4-a0fc-1ff0a23550b3
title: 工作組模式中的安全性限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eabe38b8d05c49382ae6dd8337b883a6f4a8079a
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966635"
---
# <a name="security-limitations-in-workgroup-mode"></a><span data-ttu-id="12e83-103">工作組模式中的安全性限制</span><span class="sxs-lookup"><span data-stu-id="12e83-103">Security Limitations in Workgroup Mode</span></span>

<span data-ttu-id="12e83-104">[訊息佇列](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85))工作組設定不允許 com + 佇列元件服務支援應用程式安全性。</span><span class="sxs-lookup"><span data-stu-id="12e83-104">The [Message Queuing](/previous-versions/windows/desktop/legacy/ms711472(v=vs.85)) workgroup configuration does not permit the COM+ queued components service to support application security.</span></span> <span data-ttu-id="12e83-105">如果您已安裝含有工作組設定的訊息佇列，您必須在 [COM + 應用程式內容] 對話方塊的 [**佇列**] 索引標籤上，使用 [元件 **服務] 系統** 管理工具選取 [不要 **驗證訊息**]，以停用此設定中所存取之每個佇列應用程式的 [安全性](specifying-the-authentication-protocol.md)。</span><span class="sxs-lookup"><span data-stu-id="12e83-105">If you've installed Message Queuing with the workgroup configuration, you must [disable security](specifying-the-authentication-protocol.md) on each queued application accessed in this configuration by selecting **Do not authenticate messages** on the **Queuing** tab for the COM+ application's **Properties** dialog, using the Component Services administrative tool.</span></span> <span data-ttu-id="12e83-106">這應該只在信任的網路上完成，而且必須在用戶端和伺服器上執行（如果已匯出應用程式的話）。</span><span class="sxs-lookup"><span data-stu-id="12e83-106">This should be done only on a trusted network and must be done at both client and server if the application has already been exported.</span></span>

 

 



