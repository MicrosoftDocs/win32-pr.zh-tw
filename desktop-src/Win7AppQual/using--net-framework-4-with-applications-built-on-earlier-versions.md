---
description: 搭配使用 .NET Framework 4 與舊版的應用程式
ms.assetid: 287E25AD-A560-40DA-A4E6-C46A3123914E
title: 搭配使用 .NET Framework 4 與舊版的應用程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b30eb8f4be1c50904b8d5760f456f3fe20bdd3da
ms.sourcegitcommit: 78b64f3865e64768b5319d4f010032ee68924a98
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/13/2021
ms.locfileid: "107314941"
---
# <a name="using-net-framework-4-with-applications-built-on-earlier-versions"></a><span data-ttu-id="94ca8-103">搭配使用 .NET Framework 4 與舊版的應用程式</span><span class="sxs-lookup"><span data-stu-id="94ca8-103">Using .NET Framework 4 with Applications Built on Earlier Versions</span></span>

## <a name="platform"></a><span data-ttu-id="94ca8-104">平台</span><span class="sxs-lookup"><span data-stu-id="94ca8-104">Platform</span></span>

 <span data-ttu-id="94ca8-105">**客戶** 端-windows XP、windows Vista、windows 7</span><span class="sxs-lookup"><span data-stu-id="94ca8-105">**Clients** - Windows XP, Windows Vista, Windows 7</span></span>  
<span data-ttu-id="94ca8-106">**伺服器** -windows server 2003、windows server 2008、windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="94ca8-106">**Servers** - Windows Server 2003, Windows Server 2008, Windows Server 2008 R2</span></span>  


## <a name="feature-impact"></a><span data-ttu-id="94ca8-107">功能影響</span><span class="sxs-lookup"><span data-stu-id="94ca8-107">Feature Impact</span></span>

 <span data-ttu-id="94ca8-108">**嚴重性** -低</span><span class="sxs-lookup"><span data-stu-id="94ca8-108">**Severity** - Low</span></span>  
<span data-ttu-id="94ca8-109">**頻率** -高</span><span class="sxs-lookup"><span data-stu-id="94ca8-109">**Frequency** - High</span></span>  






## <a name="description"></a><span data-ttu-id="94ca8-110">描述</span><span class="sxs-lookup"><span data-stu-id="94ca8-110">Description</span></span>

<span data-ttu-id="94ca8-111">.NET Framework 4 與使用先前的 .NET Framework 版本所建立的應用程式具有高度相容性。</span><span class="sxs-lookup"><span data-stu-id="94ca8-111">The .NET Framework 4 is highly compatible with applications that are built by using earlier .NET Framework versions.</span></span> <span data-ttu-id="94ca8-112">.NET Framework 4 的主要變更是改善安全性、標準合規性、正確性、可靠性和效能。</span><span class="sxs-lookup"><span data-stu-id="94ca8-112">The primary changes in .NET Framework 4 are to improve security, standards compliance, correctness, reliability, and performance.</span></span>

<span data-ttu-id="94ca8-113">不過，.NET Framework 4 不會自動使用它的 common language runtime 版本 (CLR) 來執行使用舊版 .NET Framework 所建立的應用程式。</span><span class="sxs-lookup"><span data-stu-id="94ca8-113">However, .NET Framework 4 does not automatically use its version of the common language runtime (CLR) to run applications that are built by using earlier versions of the .NET Framework.</span></span>

## <a name="manifestation"></a><span data-ttu-id="94ca8-114">表現</span><span class="sxs-lookup"><span data-stu-id="94ca8-114">Manifestation</span></span>

<span data-ttu-id="94ca8-115">如果您使用較早的 .NET Framework 建立應用程式，而且使用者在已安裝 .NET Framework 4 和舊版 .NET Framework 的電腦上開啟該應用程式，則應用程式會使用較早的 CLR 版本。</span><span class="sxs-lookup"><span data-stu-id="94ca8-115">If you built an application by using an earlier .NET Framework and a user opens that application on a computer that has both .NET Framework 4 and the earlier version of the .NET Framework installed, the application uses the earlier CLR version.</span></span>

<span data-ttu-id="94ca8-116">但是，如果 .NET Framework 4 是安裝在電腦上的唯一執行階段版本，則應用程式會擲回例外狀況，並要求使用者安裝您為應用程式建立的執行階段版本。</span><span class="sxs-lookup"><span data-stu-id="94ca8-116">However, if the .NET Framework 4 is the only runtime version that is installed on the computer, the application throws an exception and asks the user to install the runtime version that you built the application against.</span></span>

## <a name="solution"></a><span data-ttu-id="94ca8-117">解決方法</span><span class="sxs-lookup"><span data-stu-id="94ca8-117">Solution</span></span>

<span data-ttu-id="94ca8-118">若要執行使用 .NET Framework 4 .NET Framework 版本所建立的應用程式，您必須將應用程式編譯為以 .NET Framework 4 版本為目標，方法是在 Microsoft Visual Studio 的專案屬性中指定該應用程式，或者您可以在應用程式佈建檔的 [**<supportedRuntime> 元素**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))中指定 .NET Framework 4。</span><span class="sxs-lookup"><span data-stu-id="94ca8-118">To run applications that are built with earlier .NET Framework versions with .NET Framework 4, you must compile your application to target the .NET Framework 4 version by specifying it in the properties for your project in Microsoft Visual Studio, or you can specify .NET Framework 4 in the [**<supportedRuntime> element**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71)) in an application configuration file.</span></span>

<span data-ttu-id="94ca8-119">如需如何遷移至 .NET Framework 4 的詳細資訊，請參閱 .NET Framework 中 .NET Framework 4 和[版本相容性](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))的[遷移指南](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))。</span><span class="sxs-lookup"><span data-stu-id="94ca8-119">For more information about how to migrate to the .NET Framework 4, see [Migration Guide to the .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100)) and [Version Compatibility in the .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100)).</span></span>

## <a name="compatibility-tests"></a><span data-ttu-id="94ca8-120">相容性測試</span><span class="sxs-lookup"><span data-stu-id="94ca8-120">Compatibility Tests</span></span>

<span data-ttu-id="94ca8-121">進行變更之後，請測試您的應用程式，以確定它會正確執行。</span><span class="sxs-lookup"><span data-stu-id="94ca8-121">After you make the changes, test your application to make sure that it runs correctly.</span></span> <span data-ttu-id="94ca8-122">您可以如 [.NET Framework 4 應用程式相容性](/previous-versions/dd889541(v=msdn.10)) 主題所述，測試相容性。</span><span class="sxs-lookup"><span data-stu-id="94ca8-122">You can test compatibility as described in the [.NET Framework 4 Application Compatibility](/previous-versions/dd889541(v=msdn.10)) topic.</span></span>

<span data-ttu-id="94ca8-123">如果您的應用程式或元件在安裝 .NET Framework 4 之後無法運作，請透過 [Microsoft Connect](https://connect.microsoft.com/visualstudio) 網站提交 bug。</span><span class="sxs-lookup"><span data-stu-id="94ca8-123">If your application or component does not work after .NET Framework 4 is installed, submit a bug through the [Microsoft Connect](https://connect.microsoft.com/visualstudio) website.</span></span>

## <a name="links-to-other-resources"></a><span data-ttu-id="94ca8-124">其他資源的連結</span><span class="sxs-lookup"><span data-stu-id="94ca8-124">Links to Other Resources</span></span>

-   <span data-ttu-id="94ca8-125">[**<supportedRuntime> 元素**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))</span><span class="sxs-lookup"><span data-stu-id="94ca8-125">[**<supportedRuntime> element**](/previous-versions/dotnet/netframework-1.1/w4atty68(v=vs.71))</span></span>
-   <span data-ttu-id="94ca8-126">[.NET Framework 4 移轉手冊](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="94ca8-126">[Migration Guide to the .NET Framework 4](/previous-versions/dotnet/netframework-4.0/ff657133(v=vs.100))</span></span>
-   <span data-ttu-id="94ca8-127">[.NET Framework 的版本相容性](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))</span><span class="sxs-lookup"><span data-stu-id="94ca8-127">[Version Compatibility in the .NET Framework](/previous-versions/dotnet/netframework-4.0/ff602939(v=vs.100))</span></span>
-   <span data-ttu-id="94ca8-128">**.NET Framework 4 RTM 應用程式相容性逐步解說：**<https://msdn.microsoft.com/library/dd889541.aspx></span><span class="sxs-lookup"><span data-stu-id="94ca8-128">**.NET Framework 4 RTM Application Compatibility Walkthrough:**<https://msdn.microsoft.com/library/dd889541.aspx></span></span>
-   [<span data-ttu-id="94ca8-129">Microsoft Connect</span><span class="sxs-lookup"><span data-stu-id="94ca8-129">Microsoft Connect</span></span>](https://connect.microsoft.com/)

 

 
