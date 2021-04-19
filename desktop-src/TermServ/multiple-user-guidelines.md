---
title: 多使用者指導方針
description: 在遠端桌面服務環境中為多個使用者開發應用程式的指導方針。
ms.assetid: c7acbedb-3bf2-4519-ab11-a50bf071e757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a06db01da6d9413684e3197aa9758d6e5c04643f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966001"
---
# <a name="multiple-user-guidelines"></a><span data-ttu-id="f3099-103">多使用者指導方針</span><span class="sxs-lookup"><span data-stu-id="f3099-103">Multiple-user guidelines</span></span>

<span data-ttu-id="f3099-104">下列各節提供在遠端桌面服務環境中為多個使用者開發應用程式的指導方針。</span><span class="sxs-lookup"><span data-stu-id="f3099-104">The following sections provide guidelines for developing applications for multiple users in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="f3099-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="f3099-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="f3099-106">應用程式設定</span><span class="sxs-lookup"><span data-stu-id="f3099-106">Application setup</span></span>](application-setup-in-a-terminal-services-environment.md)
</dt> <dd>

<span data-ttu-id="f3099-107">針對單一使用者安裝應用程式，可能會在多使用者遠端桌面服務環境中產生問題。</span><span class="sxs-lookup"><span data-stu-id="f3099-107">Installing an application for a single user can create problems in a multiuser Remote Desktop Services environment.</span></span>

</dd> <dt>

[<span data-ttu-id="f3099-108">儲存使用者特定資訊</span><span class="sxs-lookup"><span data-stu-id="f3099-108">Storing user-specific information</span></span>](storing-user-specific-information.md)
</dt> <dd>

<span data-ttu-id="f3099-109">應用程式應在使用者特定位置中 儲存使用者專屬資訊 ，藉此與套用到所有使用者的全域資訊區隔。</span><span class="sxs-lookup"><span data-stu-id="f3099-109">Applications should store user-specific information in user-specific locations, separately from global information that applies to all users.</span></span>

</dd> <dt>

[<span data-ttu-id="f3099-110">核心物件命名空間</span><span class="sxs-lookup"><span data-stu-id="f3099-110">Kernel object namespaces</span></span>](kernel-object-namespaces.md)
</dt> <dd>

<span data-ttu-id="f3099-111">遠端桌面服務針對核心物件使用多個命名空間;全域命名空間主要是由用戶端/伺服器應用程式中的服務所使用。</span><span class="sxs-lookup"><span data-stu-id="f3099-111">Remote Desktop Services uses multiple namespaces for kernel objects; a global namespace is used primarily by services in client/server applications.</span></span>

</dd> <dt>

[<span data-ttu-id="f3099-112">IP 位址和電腦名稱稱</span><span class="sxs-lookup"><span data-stu-id="f3099-112">IP addresses and computer names</span></span>](ip-addresses-and-computer-names.md)
</dt> <dd>

<span data-ttu-id="f3099-113">假設指派給電腦的電腦名稱或 IP 位址 與單一使用者相關聯並不安全，因為多個使用者可以同時登入遠端桌面工作階段主機 (RD 工作階段主機) 伺服器。</span><span class="sxs-lookup"><span data-stu-id="f3099-113">It is not safe to assume that the computer name or the IP address assigned to the computer are associated with a single user because multiple users can be logged on simultaneously to a Remote Desktop Session Host (RD Session Host) server.</span></span>

</dd> </dl>

<span data-ttu-id="f3099-114">像往常一樣，在進行變更時鎖定檔案和資料庫，以防止意外遺失資料。</span><span class="sxs-lookup"><span data-stu-id="f3099-114">As always, lock files and databases while making changes to prevent inadvertent loss of data.</span></span>

<span data-ttu-id="f3099-115">您的應用程式不能鎖定不是每個使用者檔案的任何執行時間應用程式檔。</span><span class="sxs-lookup"><span data-stu-id="f3099-115">Your application must not lock any run-time application files that are not per-user files.</span></span> <span data-ttu-id="f3099-116">鎖定的執行時間檔案可以保留應用程式的多個實例，或應用程式（例如，嚮導）下的進程執行。</span><span class="sxs-lookup"><span data-stu-id="f3099-116">Locked run-time files can keep multiple instances of the application, or processes under the application such as wizards, from running.</span></span> <span data-ttu-id="f3099-117">測試哪些檔案是執行時間應用程式檔的好方法，就是追蹤應用程式安裝程式所安裝的檔案。</span><span class="sxs-lookup"><span data-stu-id="f3099-117">A good way to test which files are run-time application files is to track which files are installed by the application setup.</span></span> <span data-ttu-id="f3099-118">安裝程式很少會安裝每個使用者的檔案;因此，安裝程式安裝的大部分檔案都是執行時間的應用程式檔。</span><span class="sxs-lookup"><span data-stu-id="f3099-118">Per-user files are rarely installed by setup; therefore, most files installed by setup are run-time application files.</span></span>

 

 




