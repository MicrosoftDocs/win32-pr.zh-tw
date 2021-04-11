---
description: Active Directory 是 Windows 的目錄服務，是 Windows 分散式網路的基礎。
ms.assetid: e7569754-87c3-4a18-bfed-a03a32a2ee22
ms.tgt_platform: multiple
title: 存取 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3bbad433f1f189d68c8a7ab2f312cbb678b15ee2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194713"
---
# <a name="accessing-active-directory"></a><span data-ttu-id="a5959-103">存取 Active Directory</span><span class="sxs-lookup"><span data-stu-id="a5959-103">Accessing Active Directory</span></span>

<span data-ttu-id="a5959-104">Active Directory 是 Windows 的目錄服務，是 Windows 分散式網路的基礎。</span><span class="sxs-lookup"><span data-stu-id="a5959-104">Active Directory is the directory service for Windows and is the foundation of Windows distributed networks.</span></span> <span data-ttu-id="a5959-105">您可以使用 Active Directory 來找出電腦網路網域中的物件，例如使用者、安全性原則、印表機、分散式元件及其他資源。</span><span class="sxs-lookup"><span data-stu-id="a5959-105">You can use Active Directory to locate objects in a computer network domain, such as users, security policies, printers, distributed components, and other resources.</span></span> <span data-ttu-id="a5959-106">名稱 Active Directory 指的是目錄服務和目錄本身。</span><span class="sxs-lookup"><span data-stu-id="a5959-106">The name Active Directory refers both to the directory service and the directory itself.</span></span>

> [!Note]  
> <span data-ttu-id="a5959-107">如需有關在特定作業系統上支援和安裝此元件的詳細資訊，請參閱 [WMI 元件的作業系統可用性](operating-system-availability-of-wmi-components.md)。</span><span class="sxs-lookup"><span data-stu-id="a5959-107">For more information about support and installation of this component on a specific operating system, see [Operating System Availability of WMI Components](operating-system-availability-of-wmi-components.md).</span></span>

 

<span data-ttu-id="a5959-108">Windows 透過建立一組包含在 Active Directory 中的類別和物件的參考，讓 Active Directory 可透過 WMI 存取。</span><span class="sxs-lookup"><span data-stu-id="a5959-108">Windows makes Active Directory accessible through WMI by creating a set of references to every class and object contained in Active Directory.</span></span> <span data-ttu-id="a5959-109">藉由透過 WMI 存取目錄服務提供者，您可以建立啟用 WMI 的應用程式，以存取 Active Directory 中包含的豐富資訊。</span><span class="sxs-lookup"><span data-stu-id="a5959-109">By accessing the Directory Services provider through WMI, you can create WMI-enabled applications that can access the wealth of information contained in Active Directory.</span></span>

<span data-ttu-id="a5959-110">使用這些介面，您可以：</span><span class="sxs-lookup"><span data-stu-id="a5959-110">With these interfaces, you can:</span></span>

-   <span data-ttu-id="a5959-111">取出類別和實例。</span><span class="sxs-lookup"><span data-stu-id="a5959-111">Retrieve classes and instances.</span></span>
-   <span data-ttu-id="a5959-112">列舉類別和實例。</span><span class="sxs-lookup"><span data-stu-id="a5959-112">Enumerate classes and instances.</span></span>
-   <span data-ttu-id="a5959-113">建立新的實例。</span><span class="sxs-lookup"><span data-stu-id="a5959-113">Create new instances.</span></span>
-   <span data-ttu-id="a5959-114">修改現有的實例。</span><span class="sxs-lookup"><span data-stu-id="a5959-114">Modify existing instances.</span></span>
-   <span data-ttu-id="a5959-115">刪除現有的實例。</span><span class="sxs-lookup"><span data-stu-id="a5959-115">Delete existing instances.</span></span>
-   <span data-ttu-id="a5959-116">查詢 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="a5959-116">Query Active Directory.</span></span>

<span data-ttu-id="a5959-117">下列主題可協助您搭配使用 Active Directory 與 WMI：</span><span class="sxs-lookup"><span data-stu-id="a5959-117">The following topics can assist you in using Active Directory with WMI:</span></span>

-   [<span data-ttu-id="a5959-118">使用適當的 Active Directory 語法</span><span class="sxs-lookup"><span data-stu-id="a5959-118">Using the Proper Active Directory Syntax</span></span>](using-the-proper-active-directory-syntax.md)
-   [<span data-ttu-id="a5959-119">將 Active Directory 對應至 WMI</span><span class="sxs-lookup"><span data-stu-id="a5959-119">Mapping Active Directory to WMI</span></span>](mapping-active-directory-to-wmi.md)

 

 



