---
title: RAS 伺服器安全性驗證
description: 當 Windows NT/Windows 2000 RAS 伺服器接收到呼叫時，它會叫用已註冊的 RAS 安全性 DLL 的 RasSecurityDialogBegin 函式（如果有的話）。
ms.assetid: dd9469ec-9bb1-4444-af5b-72e3ba8b4cb2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 27184388b418e0fec2a1988fd9e693e942c08e03
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021356"
---
# <a name="ras-server-security-authentication"></a><span data-ttu-id="e1659-103">RAS 伺服器安全性驗證</span><span class="sxs-lookup"><span data-stu-id="e1659-103">RAS Server Security Authentication</span></span>

<span data-ttu-id="e1659-104">當 Windows NT/Windows 2000 RAS 伺服器接收到呼叫時，它會叫用已註冊的 RAS 安全性 DLL 的 [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) 函式（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="e1659-104">When a Windows NT/Windows 2000 RAS server receives a call, it invokes the [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) function of the registered RAS security DLL, if there is one.</span></span> <span data-ttu-id="e1659-105">此呼叫會通知安全性 DLL 開始其遠端使用者的驗證。</span><span class="sxs-lookup"><span data-stu-id="e1659-105">This call notifies the security DLL to begin its authentication of the remote user.</span></span> <span data-ttu-id="e1659-106">RAS 伺服器會先呼叫 **RasSecurityDialogBegin** ，然後再執行其 PPP 或 RAS 驗證。</span><span class="sxs-lookup"><span data-stu-id="e1659-106">The RAS server calls **RasSecurityDialogBegin** before performing its PPP or RAS authentication.</span></span>

<span data-ttu-id="e1659-107">[**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin)呼叫會將下列資訊傳遞給安全性 DLL：</span><span class="sxs-lookup"><span data-stu-id="e1659-107">The [**RasSecurityDialogBegin**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogbegin) call passes the following information to the security DLL:</span></span>

-   <span data-ttu-id="e1659-108">用來識別連接的通訊埠控制碼。</span><span class="sxs-lookup"><span data-stu-id="e1659-108">A port handle to identify the connection.</span></span>
-   <span data-ttu-id="e1659-109">與遠端使用者通訊時所要使用之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="e1659-109">Pointers to buffers to use when communicating with the remote user.</span></span>
-   <span data-ttu-id="e1659-110">完成驗證時要呼叫之 [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) 函數的指標。</span><span class="sxs-lookup"><span data-stu-id="e1659-110">A pointer to a [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) function to call when the authentication has been completed.</span></span>

<span data-ttu-id="e1659-111">埠控制碼和緩衝區指標都有效，直到安全性 DLL 呼叫 [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) 終止驗證交易為止。</span><span class="sxs-lookup"><span data-stu-id="e1659-111">The port handle and buffer pointers are valid until the security DLL calls [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) to terminate the authentication transaction.</span></span>

<span data-ttu-id="e1659-112">[**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete)會向 RAS 伺服器通知遠端使用者的安全性 DLL 驗證結果。</span><span class="sxs-lookup"><span data-stu-id="e1659-112">The [**RasSecurityDialogComplete**](/windows/desktop/api/Rasshost/nf-rasshost-rassecuritydialogcomplete) notifies the RAS server of the results of the security DLL's authentication of the remote user.</span></span> <span data-ttu-id="e1659-113">如果安全性 DLL 報告成功，RAS 伺服器會繼續進行其 PPP 和遠端使用者的 RAS 驗證。</span><span class="sxs-lookup"><span data-stu-id="e1659-113">If the security DLL reports success, the RAS server proceeds with its PPP and RAS authentication of the remote user.</span></span> <span data-ttu-id="e1659-114">如果安全性 DLL 報告遠端使用者驗證失敗，或發生錯誤，RAS 伺服器將會停止回應，並在事件記錄檔中記錄錯誤或驗證失敗。</span><span class="sxs-lookup"><span data-stu-id="e1659-114">If the security DLL reports that the remote user failed the authentication, or that an error occurred, the RAS server hangs up and logs the error or failed authentication in the event log.</span></span>

 

 




