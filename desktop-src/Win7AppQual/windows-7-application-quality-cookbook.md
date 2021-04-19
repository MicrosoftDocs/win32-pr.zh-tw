---
description: Windows 7 和 Windows Server 2008 R2 應用程式品質指南讓熟悉應用程式開發人員如何驗證其應用程式與新作業系統之間的相容性，並概述 Windows 7 和 Windows Server 2008 R2 中一些已知的應用程式相容性問題。 它也指出效能、可靠性和使用性方面的差異，並提供詳細白皮書和其他開發人員指南的連結。
ms.assetid: 68fe0b82-b6b3-4766-9699-3f2892d3f8e5
title: Windows 7 和 Windows Server 2008 R2 應用程式品質操作手冊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6c2e57912ea57f61c0ab62a00fbb3c6e8b2a57c9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978162"
---
# <a name="windows-7-and-windows-server-2008-r2-application-quality-cookbook"></a><span data-ttu-id="c6e4b-104">Windows 7 和 Windows Server 2008 R2 應用程式品質操作手冊</span><span class="sxs-lookup"><span data-stu-id="c6e4b-104">Windows 7 and Windows Server 2008 R2 Application Quality Cookbook</span></span>

<span data-ttu-id="c6e4b-105">*Windows 7 和 Windows server 2008 R2 應用程式品質指南* 讓熟悉應用程式開發人員如何驗證其應用程式與新作業系統之間的相容性，並概述 Windows 7 和 windows Server 2008 R2 中一些已知的應用程式相容性問題。</span><span class="sxs-lookup"><span data-stu-id="c6e4b-105">The *Windows 7 and Windows Server 2008 R2 Application Quality Cookbook* familiarizes application developers with how to verify the compatibility of their applications with the new operating system and provides an overview of the few known application compatibility issues in Windows 7 and Windows Server 2008 R2.</span></span> <span data-ttu-id="c6e4b-106">它也指出效能、可靠性和使用性方面的差異，並提供詳細白皮書和其他開發人員指南的連結。</span><span class="sxs-lookup"><span data-stu-id="c6e4b-106">It also points out differences in performance, reliability, and usability, and provides links to detailed white papers and other developer guidance.</span></span>

## <a name="overview"></a><span data-ttu-id="c6e4b-107">概觀</span><span class="sxs-lookup"><span data-stu-id="c6e4b-107">Overview</span></span>

<span data-ttu-id="c6e4b-108">Windows 7 和 Windows Server 2008 R2 引進最新的作業系統技術和軟體發展平臺，供全球的應用程式開發人員和企業使用。</span><span class="sxs-lookup"><span data-stu-id="c6e4b-108">Windows 7 and Windows Server 2008 R2 introduce the latest operating system technology and software development platform for use by application developers and enterprises worldwide.</span></span> <span data-ttu-id="c6e4b-109">在進一步增強 Windows 的安全性、可靠性、效能和使用者體驗的過程中，已引進許多新功能，已改善現有功能，且已移除一些功能。</span><span class="sxs-lookup"><span data-stu-id="c6e4b-109">As part of further enhancing the security, reliability, performance, and user experience of Windows, many new features have been introduced, existing features have been improved, and some features have been removed.</span></span>

<span data-ttu-id="c6e4b-110">雖然 Windows 7 和 Windows Server 2008 R2 與大部分專為 Windows XP、Windows Server 2003、Windows Vista、Windows Server 2008、Windows Server 2008 R2 及其 service pack 所撰寫的應用程式高度相容，但由於創新、安全性擴大和可靠性的緣故，某些相容性中斷是不可避免的。</span><span class="sxs-lookup"><span data-stu-id="c6e4b-110">While Windows 7 and Windows Server 2008 R2 are highly compatible with most of their respective applications written for Windows XP, Windows Server 2003, Windows Vista, Windows Server 2008, Windows Server 2008 R2 and their service packs, some compatibility breaks are inevitable due to innovations, security tightening, and increased reliability.</span></span> <span data-ttu-id="c6e4b-111">總而言之，Windows 7 和 Windows Server 2008 R2 與現有應用程式的相容性很高。</span><span class="sxs-lookup"><span data-stu-id="c6e4b-111">Overall, the compatibility of Windows 7 and Windows Server 2008 R2 with existing applications is high.</span></span>

<span data-ttu-id="c6e4b-112">本檔是以 [Windows Vista 和 Windows Server 2008 應用程式相容性指南](/previous-versions/bb757005(v=msdn.10))中所述的概念為基礎。</span><span class="sxs-lookup"><span data-stu-id="c6e4b-112">This document builds on the concepts embodied in the [Windows Vista and Windows Server 2008 Application Compatibility Cookbook](/previous-versions/bb757005(v=msdn.10)).</span></span> <span data-ttu-id="c6e4b-113"> (這項資源可能無法在某些語言及國家/地區使用。 ) 這份檔可讓您熟悉如何驗證應用程式與新作業系統之間的相容性，並概述 Windows 7 和 Windows Server 2008 R2 中一些已知的應用程式不相容問題。</span><span class="sxs-lookup"><span data-stu-id="c6e4b-113">(This resource may not be available in some languages and countries/regions.) Like it, this document provides you with the means to become familiar with how to verify the compatibility of your applications with the new operating system and provides an overview of the few known application incompatibility issues in Windows 7 and Windows Server 2008 R2.</span></span> <span data-ttu-id="c6e4b-114">但是，它也會指出效能、可靠性和使用性方面的差異，並提供詳細白皮書和其他開發人員指南的連結。</span><span class="sxs-lookup"><span data-stu-id="c6e4b-114">But more than that, it also points out differences in performance, reliability, and usability, and provides links to detailed white papers and other developer guidance.</span></span>

<span data-ttu-id="c6e4b-115">此外，Microsoft 還投資了數個新功能和增強功能，可讓您建立更高品質的應用程式，並在 Windows 7 和 Windows Server 2008 R2 上的應用程式無法正常運作時進行疑難排解。</span><span class="sxs-lookup"><span data-stu-id="c6e4b-115">In addition, Microsoft is investing in several new and enhanced features and tools to enable you to build higher quality applications and to troubleshoot when applications do not function properly on Windows 7 and Windows Server 2008 R2.</span></span> <span data-ttu-id="c6e4b-116">這些工具組括如何限定您的用戶端和伺服器應用程式參與 Windows 標誌計畫的指示。</span><span class="sxs-lookup"><span data-stu-id="c6e4b-116">Included among these tools are instructions for how to qualify your client and server applications for participating in the Windows Logo Program.</span></span>

<span data-ttu-id="c6e4b-117">此操作 *手冊* 包含三個以上的主題，分為三個主要區段：</span><span class="sxs-lookup"><span data-stu-id="c6e4b-117">This *Cookbook* contains more than three dozen topics divided into three major sections:</span></span>

-   <span data-ttu-id="c6e4b-118">一般和伺服器特定) 的[相容性](compatibility.md) (</span><span class="sxs-lookup"><span data-stu-id="c6e4b-118">[Compatibility](compatibility.md) (both General and Server-specific)</span></span>
-   [<span data-ttu-id="c6e4b-119">新功能和增強功能</span><span class="sxs-lookup"><span data-stu-id="c6e4b-119">New Features and Enhancements</span></span>](new-features-and-enhancements.md)
-   [<span data-ttu-id="c6e4b-120">工具、最佳作法和指導方針</span><span class="sxs-lookup"><span data-stu-id="c6e4b-120">Tools, Best Practices, and Guidance</span></span>](tools--resources--and-guidance.md)

<span data-ttu-id="c6e4b-121">我們邀請您查看這些主題，以瞭解如何將您的應用程式優化，以充分利用 Windows 7 提供的功能。</span><span class="sxs-lookup"><span data-stu-id="c6e4b-121">We invite you to check out these topics to learn how to optimize your application to take advantage of what Windows 7 has to offer.</span></span>

<span data-ttu-id="c6e4b-122">我們會將您對此檔的改進建議列入考慮。</span><span class="sxs-lookup"><span data-stu-id="c6e4b-122">We take your suggestions for improvements to this document seriously.</span></span>

 

 



