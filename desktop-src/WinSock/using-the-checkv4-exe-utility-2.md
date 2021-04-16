---
description: 使用 Checkv4.exe 公用程式來修改您的 IPv4 應用程式，以支援 IPv6。
ms.assetid: 36b72e4f-133d-4d96-a3c9-86a852d3a479
title: 使用 Checkv4.exe 公用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2fc9eca96b2138f9950b157a4b7690dc382f273e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104571622"
---
# <a name="using-the-checkv4exe-utility"></a><span data-ttu-id="96e6b-103">使用 Checkv4.exe 公用程式</span><span class="sxs-lookup"><span data-stu-id="96e6b-103">Using the Checkv4.exe utility</span></span>

> [!IMPORTANT]
> <span data-ttu-id="96e6b-104">*Checkv4.exe* 公用程式不會隨附于 Windows 8 的 WINDOWS 軟體開發套件 (SDK) ，也不會隨附于較新版本的 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="96e6b-104">The *Checkv4.exe* utility doesn't ship in the Windows Software Development Kit (SDK) for Windows 8, nor in later versions of the Windows SDK.</span></span>

<span data-ttu-id="96e6b-105">*Checkv4.exe* 公用程式是設計來提供程式碼移植夥伴;此公用程式會逐步引導您使用您的程式碼基底、找出潛在的問題，或反白顯示可受益于支援 IPv6 的函式或結構的程式碼，並提出建議。</span><span class="sxs-lookup"><span data-stu-id="96e6b-105">The *Checkv4.exe* utility is designed to provide you with a code porting partner; a utility that steps through your code base with you, identifies potential problems or highlights code that could benefit from IPv6-capable functions or structures, and makes recommendations.</span></span> <span data-ttu-id="96e6b-106">使用 Checkv4.exe 公用程式，修改現有 IPv4 應用程式以支援 IPv6 的工作會變得更容易。</span><span class="sxs-lookup"><span data-stu-id="96e6b-106">With the Checkv4.exe utility, the task of modifying an existing IPv4 application to support IPv6 becomes much easier.</span></span>

<span data-ttu-id="96e6b-107">*Checkv4.exe* 公用程式會安裝為 Windows Vista 和更新版本的 Microsoft WINDOWS 軟體開發套件 (SDK) 的一部分， (Windows 軟體開發套件 (的) Windows 8 SDK) 。</span><span class="sxs-lookup"><span data-stu-id="96e6b-107">The *Checkv4.exe* utility is installed as part of the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later SDKs (up to, but not including, the Windows Software Development Kit (SDK) for Windows 8).</span></span>

<span data-ttu-id="96e6b-108">舊版具有更有限功能的 *Checkv4.exe* 公用程式，也可在舊版 Microsoft IPv6 technical Preview for Windows 2000 中取得。</span><span class="sxs-lookup"><span data-stu-id="96e6b-108">An earlier version of the *Checkv4.exe* utility with more limited features was also made available as part of the earlier Microsoft IPv6 Technology Preview for Windows 2000.</span></span>

<span data-ttu-id="96e6b-109">下列各節說明如何使用 *Checkv4.exe* 公用程式，然後說明修改現有 IPv4 應用程式以支援 IPv6 的建議方法。</span><span class="sxs-lookup"><span data-stu-id="96e6b-109">The following sections describe how to use the *Checkv4.exe* utility, then explain the recommended approach for modifying an existing IPv4 application to support IPv6.</span></span>

## <a name="recommendations-for-running-checkv4exe"></a><span data-ttu-id="96e6b-110">執行 Checkv4.exe 的建議</span><span class="sxs-lookup"><span data-stu-id="96e6b-110">Recommendations for Running Checkv4.exe</span></span>

-   <span data-ttu-id="96e6b-111">*Checkv4.exe* 公用程式很簡單。</span><span class="sxs-lookup"><span data-stu-id="96e6b-111">The *Checkv4.exe* utility is straightforward.</span></span> <span data-ttu-id="96e6b-112">只要在命令列上執行 *Checkv4.exe* ，並以您想要檢查的檔案名作為參數。</span><span class="sxs-lookup"><span data-stu-id="96e6b-112">Simply execute *Checkv4.exe* at the command line with the name of the file you want to check as the parameter.</span></span> <span data-ttu-id="96e6b-113">*Checkv4.exe* 會剖析檔案，並提供該檔案中的 IPv6 移植問題所在的意見反應。</span><span class="sxs-lookup"><span data-stu-id="96e6b-113">*Checkv4.exe* parses the file and provides feedback as to where IPv6 porting issues exist in that file.</span></span> <span data-ttu-id="96e6b-114">將 *Checkv4.exe* 放入電腦的路徑，可讓您更輕鬆地從原始程式碼目錄結構中的任何位置執行 *Checkv4.exe* 公用程式。</span><span class="sxs-lookup"><span data-stu-id="96e6b-114">Placing the *Checkv4.exe* into your computer's path makes running the *Checkv4.exe* utility from anywhere in your source code directory structure much easier.</span></span> <span data-ttu-id="96e6b-115">例如，將 *Checkv4.exe* 放入% windir%，可讓您從電腦上的任何目錄啟動 *Checkv4.exe* ，而不包含其路徑。</span><span class="sxs-lookup"><span data-stu-id="96e6b-115">For example, placing *Checkv4.exe* into %windir% enables you to launch *Checkv4.exe* from any directory on your computer without including its path.</span></span>

-   <span data-ttu-id="96e6b-116">在命令提示字元中發出下列命令，以剖析 Simplec 檔案：</span><span class="sxs-lookup"><span data-stu-id="96e6b-116">Issue the following command at the command prompt to parse the file Simplec.c:</span></span>

    <span data-ttu-id="96e6b-117">**Checkv4 simplec c。**</span><span class="sxs-lookup"><span data-stu-id="96e6b-117">**Checkv4 simplec.c**</span></span>

    <span data-ttu-id="96e6b-118">請注意， *Checkv4.exe* 公用程式所做的某些建議只需要最新版本的 *Ws2tcpip .h* 標頭檔中的結構，例如 **SOCKADDR \_ IN6** 結構。</span><span class="sxs-lookup"><span data-stu-id="96e6b-118">Note that some of the recommendations made by the *Checkv4.exe* utility require structures available only in recent versions of the *Ws2tcpip.h* header file, such as the **SOCKADDR\_IN6** structure.</span></span> <span data-ttu-id="96e6b-119">這些標頭檔包含在 Windows Vista 和更新版本中發行的 Windows SDK。</span><span class="sxs-lookup"><span data-stu-id="96e6b-119">These header files are included in the Windows SDK released for Windows Vista and later.</span></span> <span data-ttu-id="96e6b-120">這些標頭檔也包含在舊版平臺軟體發展工具組中， (SDK) 發行給 Windows Server 2003。</span><span class="sxs-lookup"><span data-stu-id="96e6b-120">These header files are also included in the earlier Platform Software Development Kit (SDK) released for Windows Server 2003.</span></span> <span data-ttu-id="96e6b-121">這些標頭檔也會包含在 MSDN 訂用帳戶或下載中。</span><span class="sxs-lookup"><span data-stu-id="96e6b-121">These header files are also included as part of an MSDN subscription or by download.</span></span>

    <span data-ttu-id="96e6b-122">下列螢幕擷取畫面顯示在附錄 A 中所包含的 Simplec 檔案上使用 *Checkv4.exe* 公用程式的結果：</span><span class="sxs-lookup"><span data-stu-id="96e6b-122">The following screen shot displays the results of using the *Checkv4.exe* utility on the Simplec.c file included in Appendix A:</span></span>

    ![checkv4.exe 報告 simplec 中的 ipv6 不相容問題](images/portingguide002.jpg)

    <span data-ttu-id="96e6b-124">下列螢幕擷取畫面顯示在 Simples 上使用 *Checkv4.exe* 公用程式的結果，也包含在附錄 A：</span><span class="sxs-lookup"><span data-stu-id="96e6b-124">The following screen shot displays the results of using the *Checkv4.exe* utility on the Simples.c file, which is also included in Appendix A:</span></span>

    ![checkv4.exe 報告 simples 中的 ipv6 不相容問題](images/portingguide003.jpg)

## <a name="the-application-modification-process-where-to-start"></a><span data-ttu-id="96e6b-126">應用程式修改程式：要從何處著手</span><span class="sxs-lookup"><span data-stu-id="96e6b-126">The Application Modification Process: Where to Start</span></span>

<span data-ttu-id="96e6b-127">有一個建議的程式，與將 IPv6 功能新增至應用程式相關聯。</span><span class="sxs-lookup"><span data-stu-id="96e6b-127">There is a recommended procedure associated with adding IPv6 capability to applications.</span></span> <span data-ttu-id="96e6b-128">遵循此順序會很有説明，因為它可讓開發人員確保修改現有 IPv4 應用程式所需的所有步驟都是採用 IPv6。</span><span class="sxs-lookup"><span data-stu-id="96e6b-128">Following this sequence is beneficial, because it enables developers to ensure that all steps necessary to modify an existing IPv4 application to support IPv6 are taken.</span></span> <span data-ttu-id="96e6b-129">某些應用程式可能需要更廣泛地注意其中一個序列;例如，系統服務可能會有比圖形檔案傳輸程式 (FTP) 更少的使用者介面問題。</span><span class="sxs-lookup"><span data-stu-id="96e6b-129">Certain applications may require more extensive attention to one of these sequences; for example, a system service would likely have less user interface issues than a graphical file transfer program (FTP).</span></span>

<span data-ttu-id="96e6b-130">**修改 IPv4 應用程式以支援 IPv6**</span><span class="sxs-lookup"><span data-stu-id="96e6b-130">**To modify IPv4 applications to support IPv6**</span></span>

1.  <span data-ttu-id="96e6b-131">修正結構和宣告，以啟用 IPv6 和 IPv4 相容性。</span><span class="sxs-lookup"><span data-stu-id="96e6b-131">Fix structures and declarations to enable IPv6 and IPv4 compatibility.</span></span>
2.  <span data-ttu-id="96e6b-132">修改函式呼叫以利用具備 IPv6 功能的函式，例如 [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) 和 [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) 函數。</span><span class="sxs-lookup"><span data-stu-id="96e6b-132">Modify function calls to take advantage of IPv6-enabled functions, such as the [**getaddrinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getaddrinfo) and [**getnameinfo**](/windows/desktop/api/Ws2tcpip/nf-ws2tcpip-getnameinfo) functions.</span></span>
3.  <span data-ttu-id="96e6b-133">請參閱原始程式碼，以使用硬式編碼的 IPv4 位址，例如回送位址，或使用其他常值字串。</span><span class="sxs-lookup"><span data-stu-id="96e6b-133">Review source code for the use of hard-coded IPv4 addresses such as the loopback address, or the use of other literal strings.</span></span>
4.  <span data-ttu-id="96e6b-134">執行完整的使用者介面檢查，包括資訊對話方塊。</span><span class="sxs-lookup"><span data-stu-id="96e6b-134">Perform a thorough review of the user interface, including informational dialog boxes.</span></span> <span data-ttu-id="96e6b-135">請考慮它是否適用于已啟用 IPv6 的應用程式，以指定或提供以 IP 位址為基礎的資訊。</span><span class="sxs-lookup"><span data-stu-id="96e6b-135">Give thought to whether it is appropriate for IPv6-enabled applications to specify or provide IP-address based information.</span></span>
5.  <span data-ttu-id="96e6b-136">判斷您的應用程式是否依賴基礎通訊協定（例如 RPC），並進行適當的程式設計變更來處理 IPv6 位址。</span><span class="sxs-lookup"><span data-stu-id="96e6b-136">Determine whether your application relies on underlying protocols, such as RPC, and make appropriate programmatic changes to handle IPv6 addresses.</span></span>
6.  <span data-ttu-id="96e6b-137">在 Windows XP 和更新版本上編譯應用程式時，請使用編譯時間旗標 IPV6STRICT。</span><span class="sxs-lookup"><span data-stu-id="96e6b-137">Use the compile-time flag IPV6STRICT when compiling applications on Windows XP and later.</span></span> <span data-ttu-id="96e6b-138">此旗標會導致不相容的程式碼編譯失敗，如下所示：</span><span class="sxs-lookup"><span data-stu-id="96e6b-138">This flag results in incompatible code failing to compile, as follows:</span></span>

    <span data-ttu-id="96e6b-139">具有不相容程式碼的 Windows 通訊端1.x 應用程式無法進行編譯，並傳回錯誤訊息「需要的 WINSOCK2」。</span><span class="sxs-lookup"><span data-stu-id="96e6b-139">Windows Sockets 1.x applications with incompatible code fail to compile and return the error message "WINSOCK2 Required."</span></span>

    <span data-ttu-id="96e6b-140">具有不相容程式碼的 Windows 通訊端2.x 應用程式，會導致每個不相容程式碼實例發生編譯時間錯誤。</span><span class="sxs-lookup"><span data-stu-id="96e6b-140">Windows Sockets 2.x applications with incompatible code cause a compile time error for each instance of incompatible code.</span></span> <span data-ttu-id="96e6b-141">系統會以下列格式產生錯誤訊息：</span><span class="sxs-lookup"><span data-stu-id="96e6b-141">An error message is generated in the following format:</span></span>

    `[file name] ([line number]) : [error message] '[symbol]_IPV6INCOMPATIBLE'`

    <span data-ttu-id="96e6b-142">例如：</span><span class="sxs-lookup"><span data-stu-id="96e6b-142">For example:</span></span>

    `sample.c(8) : error C2065: 'gethostbyaddr_IPV6INCOMPATIBLE' : undeclared identifier`

 

 



