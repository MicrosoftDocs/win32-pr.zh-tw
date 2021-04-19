---
description: 疑難排解
ms.assetid: e3576161-fc04-47e0-b6b8-75af33fe87ff
title: 疑難排解
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f5dcc9814353f9c19a8f5005a3ee8fe461c37a93
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972774"
---
# <a name="troubleshooting"></a><span data-ttu-id="59efc-103">疑難排解</span><span class="sxs-lookup"><span data-stu-id="59efc-103">Troubleshooting</span></span>

<span data-ttu-id="59efc-104">如果您在診斷應用程式錯誤時遇到問題，請參閱下列疑難排解秘訣：</span><span class="sxs-lookup"><span data-stu-id="59efc-104">If you are having trouble diagnosing your application errors, refer to the following of troubleshooting tips:</span></span>

-   <span data-ttu-id="59efc-105">確定分散式交易協調器 (DTC) 正在所有伺服器上執行。</span><span class="sxs-lookup"><span data-stu-id="59efc-105">Make sure that the Distributed Transaction Coordinator (DTC) is running on all servers.</span></span>
-   <span data-ttu-id="59efc-106">先在本機電腦上測試以確認應用程式可運作，以檢查網路通訊。</span><span class="sxs-lookup"><span data-stu-id="59efc-106">Check network communication by first testing on a local computer to verify that the application works.</span></span> <span data-ttu-id="59efc-107">如果您在網路上執行 TCP/IP，則可以使用 ping.exe 公用程式來確認電腦是否在網路上。</span><span class="sxs-lookup"><span data-stu-id="59efc-107">If you are running TCP/IP on your network, you can use the ping.exe utility to verify that the machines are on the network.</span></span>
-   <span data-ttu-id="59efc-108">請確定 SQL 和 DTC 位於相同的電腦上，或者 DTC 用戶端設定程式指定 DTC 位於另一部電腦上。</span><span class="sxs-lookup"><span data-stu-id="59efc-108">Make sure that SQL and DTC are located on the same computer or that the DTC Client Configuration program specifies that the DTC is on another computer.</span></span> <span data-ttu-id="59efc-109">如果沒有，SQLConnect 會在從交易元件呼叫時，從內部傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="59efc-109">If not, SQLConnect will return an error internally when called from a transactional component.</span></span>
-   <span data-ttu-id="59efc-110">將交易超時設定為比預設60秒更高的數位。</span><span class="sxs-lookup"><span data-stu-id="59efc-110">Set the transaction time-out to a higher number than the default 60 seconds.</span></span> <span data-ttu-id="59efc-111">交易超時經過之後，COM + 會中止交易。</span><span class="sxs-lookup"><span data-stu-id="59efc-111">After the transaction time-out has elapsed, COM+ aborts the transaction.</span></span> <span data-ttu-id="59efc-112">元件的所有後續呼叫都會立即傳回，內容 \_ E 會 \_ 中止。</span><span class="sxs-lookup"><span data-stu-id="59efc-112">All subsequent calls to the component return immediately with CONTEXT\_E\_ABORTED.</span></span>
-   <span data-ttu-id="59efc-113">確定您的 ODBC 驅動程式是安全線程，而且沒有線程親和性。</span><span class="sxs-lookup"><span data-stu-id="59efc-113">Make sure that your ODBC drivers are thread-safe and do not have thread affinity.</span></span>
-   <span data-ttu-id="59efc-114">如果您無法讓應用程式在數部伺服器上運作，請重新開機用戶端，然後確認您的網域控制站已正確設定。</span><span class="sxs-lookup"><span data-stu-id="59efc-114">If you have difficulty getting an application to work over several servers, reboot the client and then verify that your domain controller is configured properly.</span></span>

## <a name="related-topics"></a><span data-ttu-id="59efc-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="59efc-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="59efc-116">錯誤隔離和 Failfast 原則</span><span class="sxs-lookup"><span data-stu-id="59efc-116">Fault Isolation and Failfast Policy</span></span>](fault-isolation-and-failfast-policy.md)
</dt> <dt>

[<span data-ttu-id="59efc-117">找出錯誤的來源</span><span class="sxs-lookup"><span data-stu-id="59efc-117">Finding the Source of an Error</span></span>](finding-the-source-of-an-error.md)
</dt> <dt>

[<span data-ttu-id="59efc-118">COM + 如何修改傳回值</span><span class="sxs-lookup"><span data-stu-id="59efc-118">How COM+ Modifies Return Values</span></span>](how-com--modifies-return-values.md)
</dt> <dt>

[<span data-ttu-id="59efc-119">解讀錯誤碼</span><span class="sxs-lookup"><span data-stu-id="59efc-119">Interpreting Error Codes</span></span>](interpreting-error-codes.md)
</dt> <dt>

[<span data-ttu-id="59efc-120">在 COM + 中處理錯誤的策略</span><span class="sxs-lookup"><span data-stu-id="59efc-120">Strategies for Handling Errors in COM+</span></span>](strategies-for-handling-errors-in-com-.md)
</dt> </dl>

 

 



