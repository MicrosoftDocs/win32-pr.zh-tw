---
title: 偵測網域的操作模式
description: 在 Windows 2000 中，網域可在混合和原生兩種作業模式中執行。
ms.assetid: c20dec14-50ad-4f63-bd5c-222c2f2c83e4
ms.tgt_platform: multiple
keywords:
- 偵測網域 AD 的操作模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d871bd50c9a7462972992685d4226963a3eaff
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103842096"
---
# <a name="detecting-the-operation-mode-of-a-domain"></a><span data-ttu-id="6c28f-104">偵測網域的操作模式</span><span class="sxs-lookup"><span data-stu-id="6c28f-104">Detecting the Operation Mode of a Domain</span></span>

<span data-ttu-id="6c28f-105">在 Windows 2000 中，網域可在兩種作業模式下執行：混合和原生。</span><span class="sxs-lookup"><span data-stu-id="6c28f-105">In Windows 2000, a domain can run in two operation modes: mixed and native.</span></span> <span data-ttu-id="6c28f-106">混合模式應該用來包含在 Windows 2000 網域中執行 Windows NT 4.0 的網域控制站。</span><span class="sxs-lookup"><span data-stu-id="6c28f-106">Mixed mode should be used to include domain controllers running Windows NT 4.0 in a Windows 2000 domain.</span></span> <span data-ttu-id="6c28f-107">混合模式不支援萬用群組或嵌套群組。</span><span class="sxs-lookup"><span data-stu-id="6c28f-107">Mixed mode does not support universal groups or nested groups.</span></span> <span data-ttu-id="6c28f-108">如果網域中的所有網域控制站都是執行 Windows 2000，您可以使用原生模式。</span><span class="sxs-lookup"><span data-stu-id="6c28f-108">If all domain controllers in the domain are running Windows 2000, you can use native mode.</span></span>

<span data-ttu-id="6c28f-109">若要以程式設計方式偵測 Windows 2000 網域的作業模式，請閱讀該網域之 [**domainDNS**](/windows/desktop/ADSchema/c-domaindns)物件的 [**ntMixedDomain**](/windows/desktop/ADSchema/a-ntmixeddomain)屬性。</span><span class="sxs-lookup"><span data-stu-id="6c28f-109">To programmatically detect the operation mode of a Windows 2000 domain, read the [**ntMixedDomain**](/windows/desktop/ADSchema/a-ntmixeddomain) property of the [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) object for that domain.</span></span> <span data-ttu-id="6c28f-110">值為零 (0) 表示該網域處於原生模式。</span><span class="sxs-lookup"><span data-stu-id="6c28f-110">A value of zero (0) means that the domain is in native mode.</span></span> <span data-ttu-id="6c28f-111">值 (1) 表示該網域處於混合模式。</span><span class="sxs-lookup"><span data-stu-id="6c28f-111">A value of one (1) indicates that the domain is in mixed mode.</span></span> <span data-ttu-id="6c28f-112">您也可以使用 [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation) 函式來取得作業模式，以及有關網域及其狀態的其他資料。</span><span class="sxs-lookup"><span data-stu-id="6c28f-112">You can also use the [**DsRoleGetPrimaryDomainInformation**](/windows/desktop/api/Dsrole/nf-dsrole-dsrolegetprimarydomaininformation) function to get the operation mode as well as other data about the domain and its state.</span></span>

<span data-ttu-id="6c28f-113">若要系結至您的應用程式執行所在的使用者帳戶之網域的 [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) 物件，請使用無伺服器系結和 rootDSE 來取得網域的辨別名稱，然後使用該辨別名稱系結至代表該網域的 **domainDNS** 物件。</span><span class="sxs-lookup"><span data-stu-id="6c28f-113">To bind to the [**domainDNS**](/windows/desktop/ADSchema/c-domaindns) object of the domain of the user account under which your application is running, use serverless binding and rootDSE to get the distinguished name for the domain and then use that distinguished name to bind to the **domainDNS** object that represents that domain.</span></span> <span data-ttu-id="6c28f-114">如需無伺服器系結和 rootDSE 的詳細資訊，請參閱 [無伺服器系結和 rootdse](serverless-binding-and-rootdse.md)。</span><span class="sxs-lookup"><span data-stu-id="6c28f-114">For more information about serverless binding and rootDSE, see [Serverless Binding and RootDSE](serverless-binding-and-rootdse.md).</span></span>

<span data-ttu-id="6c28f-115">如需詳細資訊和示範如何以程式設計方式偵測網域作業模式的程式碼範例，請參閱 [判斷作業模式的範例程式碼](example-code-for-determining-the-operation-mode.md)。</span><span class="sxs-lookup"><span data-stu-id="6c28f-115">For more information and a code example that shows how to programmatically detect the operation mode of a domain, see [Example Code for Determining the Operation Mode](example-code-for-determining-the-operation-mode.md).</span></span>

 

 