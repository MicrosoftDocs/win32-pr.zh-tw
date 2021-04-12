---
description: IPv4 的壽命導致硬式編碼許多知名的 IPv4 位址，例如 (127. x. x. x) 的回送位址、整數常數（例如 INADDR \_ 回送）等等。
ms.assetid: adb39f27-c219-43cd-9e86-b2d3b663c79c
title: 使用硬式編碼的 IPv4 位址
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8205840b1c79afcaf375b81f3223a1c780cc03d5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318359"
---
# <a name="use-of-hardcoded-ipv4-addresses"></a><span data-ttu-id="47812-103">使用硬式編碼的 IPv4 位址</span><span class="sxs-lookup"><span data-stu-id="47812-103">Use of Hardcoded IPv4 Addresses</span></span>

<span data-ttu-id="47812-104">IPv4 的壽命導致硬式編碼許多知名的 IPv4 位址，例如 (127. x. x. x) 的回送位址、整數常數（例如 INADDR \_ 回送）等等。</span><span class="sxs-lookup"><span data-stu-id="47812-104">The longevity of IPv4 resulted in hard coding many well-known IPv4 addresses, such as loopback addresses (127.x.x.x), integer constants such as INADDR\_LOOPBACK, among others.</span></span> <span data-ttu-id="47812-105">在修改和現有的應用程式以支援 IPv6 或建立與新的 IP 版本無關的程式時，將這些位址進行硬式編碼的做法會帶來明顯的問題。</span><span class="sxs-lookup"><span data-stu-id="47812-105">The practice of hard coding these addresses presents obvious problems when modifying and existing application to support IPv6 or creating new IP version-independent programs.</span></span>

<span data-ttu-id="47812-106">最佳做法</span><span class="sxs-lookup"><span data-stu-id="47812-106">Best Practice</span></span>

-   <span data-ttu-id="47812-107">最好的方法是避免硬式編碼任何位址。</span><span class="sxs-lookup"><span data-stu-id="47812-107">The best approach is to avoid hardcoding any addresses.</span></span>

<span data-ttu-id="47812-108">要避免的程式碼</span><span class="sxs-lookup"><span data-stu-id="47812-108">Code To Avoid</span></span>

-   <span data-ttu-id="47812-109">避免在程式碼中使用硬式編碼的位址。</span><span class="sxs-lookup"><span data-stu-id="47812-109">Avoid using hardcoded addresses in code.</span></span>

<span data-ttu-id="47812-110">**從 IPv4 將現有的程式碼基底修改為 IPv4 和 IPv6 互通性**</span><span class="sxs-lookup"><span data-stu-id="47812-110">**To modify your existing code base from IPv4 to IPv4- and IPv6-interoperability**</span></span>

1.  <span data-ttu-id="47812-111">取得 *Checkv4.exe* 公用程式。</span><span class="sxs-lookup"><span data-stu-id="47812-111">Acquire the *Checkv4.exe* utility.</span></span> <span data-ttu-id="47812-112">*Checkv4.exe* 公用程式會安裝為 Windows Vista 和更新版本的 Microsoft WINDOWS 軟體開發套件 (SDK) 所發行的一部分。</span><span class="sxs-lookup"><span data-stu-id="47812-112">The *Checkv4.exe* utility is installed as part of the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later.</span></span> <span data-ttu-id="47812-113">Windows SDK 可透過 MSDN 訂閱取得，也可以從 Microsoft 網站 (下載 https://msdn.microsoft.com) 。</span><span class="sxs-lookup"><span data-stu-id="47812-113">The Windows SDK is available through an MSDN subscription and can also be downloaded from the Microsoft website (https://msdn.microsoft.com).</span></span>
2.  <span data-ttu-id="47812-114">針對您的程式碼執行 *Checkv4.exe* 公用程式。</span><span class="sxs-lookup"><span data-stu-id="47812-114">Run the *Checkv4.exe* utility against your code.</span></span> <span data-ttu-id="47812-115">瞭解如何在 [使用 Checkv4.exe 公用程式](using-the-checkv4-exe-utility-2.md)一節中，針對您的檔案執行 *Checkv4.exe* 公用程式。</span><span class="sxs-lookup"><span data-stu-id="47812-115">Learn about how to run the *Checkv4.exe* utility against your files in the section on [Using the Checkv4.exe Utility](using-the-checkv4-exe-utility-2.md).</span></span>
3.  <span data-ttu-id="47812-116">*Checkv4.exe* 公用程式會警示您是否有 IPv4 位址的通用定義，例如 INADDR \_ 回送。</span><span class="sxs-lookup"><span data-stu-id="47812-116">The *Checkv4.exe* utility alerts you to the presence of common defines for IPv4 addresses, such as INADDR\_LOOPBACK.</span></span> <span data-ttu-id="47812-117">修改任何使用常值字串的程式碼，以及與通訊協定版本無關的程式碼。</span><span class="sxs-lookup"><span data-stu-id="47812-117">Modify any code that uses literal strings with code that is protocol-version agnostic.</span></span>
4.  <span data-ttu-id="47812-118">視需要在您的程式碼基底中搜尋其他可能的常值字串。</span><span class="sxs-lookup"><span data-stu-id="47812-118">Search your code base for other potential literal strings, as appropriate.</span></span>

<span data-ttu-id="47812-119">*Checkv4.exe* 公用程式可協助您尋找常見的常值字串，但您的應用程式可能會有其他特定字串。</span><span class="sxs-lookup"><span data-stu-id="47812-119">The *Checkv4.exe* utility can help you find common literal strings, but there may be others that are specific to your application.</span></span> <span data-ttu-id="47812-120">您應執行完整的搜尋和測試，以確保您的程式碼基底已 eradicated 與常值字串相關聯的潛在問題。</span><span class="sxs-lookup"><span data-stu-id="47812-120">You should perform thorough searching and testing to ensure your code base has eradicated potential problems associated with literal strings.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47812-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="47812-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47812-122">適用于 Windows 通訊端應用程式的 IPv6 指南</span><span class="sxs-lookup"><span data-stu-id="47812-122">IPv6 Guide for Windows Sockets Applications</span></span>](ipv6-guide-for-windows-sockets-applications-2.md)
</dt> <dt>

[<span data-ttu-id="47812-123">變更 IPv6 Winsock Html5 應用程式的資料結構</span><span class="sxs-lookup"><span data-stu-id="47812-123">Changing Data Structures for IPv6 Winsock Appications</span></span>](changing-data-structures-2.md)
</dt> <dt>

[<span data-ttu-id="47812-124">IPv6 Winsock 應用程式的雙重堆疊通訊端</span><span class="sxs-lookup"><span data-stu-id="47812-124">Dual-Stack Sockets for IPv6 Winsock Applications</span></span>](dual-stack-sockets.md)
</dt> <dt>

[<span data-ttu-id="47812-125">IPv6 Winsock 應用程式的函式呼叫</span><span class="sxs-lookup"><span data-stu-id="47812-125">Function Calls for IPv6 Winsock Applications</span></span>](function-calls-2.md)
</dt> <dt>

[<span data-ttu-id="47812-126">IPv6 Winsock 應用程式的消費者介面問題</span><span class="sxs-lookup"><span data-stu-id="47812-126">User Interface Issues for IPv6 Winsock Applications</span></span>](user-interface-issues-2.md)
</dt> <dt>

[<span data-ttu-id="47812-127">IPv6 Winsock 應用程式的基礎通訊協定</span><span class="sxs-lookup"><span data-stu-id="47812-127">Underlying Protocols for IPv6 Winsock Applications</span></span>](underlying-protocols-2.md)
</dt> </dl>

 

 



