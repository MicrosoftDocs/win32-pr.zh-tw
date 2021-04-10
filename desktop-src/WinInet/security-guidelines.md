---
title: 安全性指導方針
description: 請務必讓使用者知道可能的安全性問題。
ms.assetid: f0c041fd-3cc5-491e-b088-6c93fcd61def
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4b3d4214ba4582394ed555bafd58551e8b047493
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104093068"
---
# <a name="security-guideline"></a><span data-ttu-id="e8e79-103">安全性指導方針</span><span class="sxs-lookup"><span data-stu-id="e8e79-103">Security Guideline</span></span>

<span data-ttu-id="e8e79-104">請務必讓使用者知道可能的安全性問題。</span><span class="sxs-lookup"><span data-stu-id="e8e79-104">It is important to keep the user informed about possible security issues.</span></span>

## <a name="notify-the-user-of-security-related-events"></a><span data-ttu-id="e8e79-105">通知使用者 Security-Related 事件</span><span class="sxs-lookup"><span data-stu-id="e8e79-105">Notify the User of Security-Related Events</span></span>

<span data-ttu-id="e8e79-106">一律通知使用者任何安全性變更、是否為與安全性相關的錯誤（例如憑證失敗），或基礎通訊協定安全性變更（例如從 HTTPS 網站變更為 HTTP 網站）。</span><span class="sxs-lookup"><span data-stu-id="e8e79-106">Always notify the user of any change in security, whether it is a security-related error such as a certificate failure, or a change in the security of the underlying protocol, such as change from an HTTPS site to an HTTP site.</span></span>

## <a name="notify-the-user-of-security-related-errors"></a><span data-ttu-id="e8e79-107">通知使用者 Security-Related 錯誤</span><span class="sxs-lookup"><span data-stu-id="e8e79-107">Notify the User of Security-Related Errors</span></span>

<span data-ttu-id="e8e79-108">當您的應用程式收到可能指出安全性問題的錯誤訊息時， **InternetErrorDlg** 函式會提供標準、熟悉的介面，在大部分情況下通知使用者。</span><span class="sxs-lookup"><span data-stu-id="e8e79-108">When your application receives an error message that may indicate a security problem, the **InternetErrorDlg** function provides a standard, familiar interface for notifying the user in most cases.</span></span>

<span data-ttu-id="e8e79-109">屬於此類別的錯誤包括：</span><span class="sxs-lookup"><span data-stu-id="e8e79-109">Among the errors that fall in this category are:</span></span>

<span data-ttu-id="e8e79-110">**\_ \_ \_ \_ \_ REDIR 上的網際網路 HTTP 至 \_ HTTPS 時發生錯誤**</span><span class="sxs-lookup"><span data-stu-id="e8e79-110">**ERROR\_INTERNET\_HTTP\_TO\_HTTPS\_ON\_REDIR**</span></span>

<span data-ttu-id="e8e79-111">**\_網際網路 \_ 不正確 \_ CA 錯誤**</span><span class="sxs-lookup"><span data-stu-id="e8e79-111">**ERROR\_INTERNET\_INVALID\_CA**</span></span>

<span data-ttu-id="e8e79-112">**錯誤 \_ 網際網路 \_ POST \_ 為 \_ 非 \_ 安全的**</span><span class="sxs-lookup"><span data-stu-id="e8e79-112">**ERROR\_INTERNET\_POST\_IS\_NON\_SECURE**</span></span>

<span data-ttu-id="e8e79-113">**\_INTERNET \_ SEC \_ CERT \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="e8e79-113">**ERROR\_INTERNET\_SEC\_CERT\_ERRORS**</span></span>

<span data-ttu-id="e8e79-114">**\_INTERNET \_ SEC \_ CERT \_ CN \_ 不正確錯誤**</span><span class="sxs-lookup"><span data-stu-id="e8e79-114">**ERROR\_INTERNET\_SEC\_CERT\_CN\_INVALID**</span></span>

<span data-ttu-id="e8e79-115">**錯誤 \_ 網際網路 \_ SEC \_ 憑證 \_ 日期 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="e8e79-115">**ERROR\_INTERNET\_SEC\_CERT\_DATE\_INVALID**</span></span>

<span data-ttu-id="e8e79-116">若無法通知使用者發生這類錯誤，可能會讓使用者暴露于各種不同的安全性漏洞，包括詐騙攻擊或非自願資訊洩漏。</span><span class="sxs-lookup"><span data-stu-id="e8e79-116">A failure to notify the user of errors such as these can expose the user to various sorts of security breaches, including spoofing attacks or involuntary information disclosure.</span></span>

## <a name="notify-the-user-when-connection-security-changes"></a><span data-ttu-id="e8e79-117">在連接安全性變更時通知使用者</span><span class="sxs-lookup"><span data-stu-id="e8e79-117">Notify the User When Connection Security Changes</span></span>

<span data-ttu-id="e8e79-118">當連線的安全性變更時（例如從 HTTPS 至 HTTP），一律會通知使用者。</span><span class="sxs-lookup"><span data-stu-id="e8e79-118">Always notify the user when the security of the connection changes, for example from HTTPS to HTTP.</span></span> <span data-ttu-id="e8e79-119">否則，除非使用者明確選擇不收到這類變更的通知，否則您會隱藏非自願資訊洩漏的風險。</span><span class="sxs-lookup"><span data-stu-id="e8e79-119">Otherwise, unless the user has explicitly chosen not to be notified of such changes, you are concealing the risks of involuntary information disclosure.</span></span>

<span data-ttu-id="e8e79-120">在連接安全性中報告這類變更的函式中， **InternetStatusCallback** 回呼函式和 **InternetConfirmZoneCrossing** 函式。</span><span class="sxs-lookup"><span data-stu-id="e8e79-120">Among the functions that report such a change in connection security are the **InternetStatusCallback** callback function and the **InternetConfirmZoneCrossing** function.</span></span>

> [!Note]  
> <span data-ttu-id="e8e79-121">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="e8e79-121">WinINet does not support server implementations.</span></span> <span data-ttu-id="e8e79-122">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="e8e79-122">In addition, it should not be used from a service.</span></span> <span data-ttu-id="e8e79-123">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="e8e79-123">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 