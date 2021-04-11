---
title: 使用 Visual Basic 存取 Active Directory
description: Microsoft Windows 2000 作業系統提供的其中一個最強大功能，就是 Microsoft Active Directory Directory 服務。
ms.assetid: b5021e38-92a2-43d2-b3cb-15ff5c74c1d8
ms.tgt_platform: multiple
keywords:
- 使用 Visual Basic ADSI 存取 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bbc469de112c37c1c2ea5865d88252c4bd98466
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020817"
---
# <a name="accessing-active-directory-using-visual-basic"></a><span data-ttu-id="2aca9-104">使用 Visual Basic 存取 Active Directory</span><span class="sxs-lookup"><span data-stu-id="2aca9-104">Accessing Active Directory Using Visual Basic</span></span>

<span data-ttu-id="2aca9-105">Microsoft Windows 2000 作業系統提供的其中一個最強大功能，就是 Microsoft Active Directory Directory 服務。</span><span class="sxs-lookup"><span data-stu-id="2aca9-105">One of the most powerful features that became available with the Microsoft Windows 2000 operating system is the Microsoft Active Directory directory service.</span></span> <span data-ttu-id="2aca9-106">當您登入 Windows 2000 網域時，Active Directory 會進入動作;若要在大樓中搜尋最接近的彩色印表機，您可以使用 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="2aca9-106">When you log on to a Windows 2000 domain, Active Directory is put into action; to search for the closest color printer in your building, you can use Active Directory.</span></span> <span data-ttu-id="2aca9-107">它可用於通訊錄查閱或搜尋大樓40中工作的使用者。</span><span class="sxs-lookup"><span data-stu-id="2aca9-107">It can be used for an address book lookup or a search for users who work in building 40.</span></span> <span data-ttu-id="2aca9-108">使用 Active Directory 時，您可以使用智慧卡來登入 Windows 2000 網域。</span><span class="sxs-lookup"><span data-stu-id="2aca9-108">With Active Directory, you can use a smart card to log on to a Windows 2000 domain.</span></span> <span data-ttu-id="2aca9-109">您甚至可以將 Microsoft SQL Server 資料庫軟體和 Active Directory 的資料聯結。</span><span class="sxs-lookup"><span data-stu-id="2aca9-109">You can even join data from Microsoft SQL Server database software and Active Directory.</span></span>

<span data-ttu-id="2aca9-110">許多其他的 Microsoft 技術（例如 Microsoft Message Queue Server (MSMQ) 、COM (類別存放區) 、網際網路通訊協定安全性 (IPsec) 、群組原則物件 (Gpo) 和 Exchange 都與 Active Directory 整合。</span><span class="sxs-lookup"><span data-stu-id="2aca9-110">Many other Microsoft technologies, such as Microsoft Message Queue Server (MSMQ), COM (Class Store), Internet Protocol security (IPsec), Group Policy Objects (GPOs), and Exchange are integrated with Active Directory.</span></span>

<span data-ttu-id="2aca9-111">本節討論如何使用 Active Directory 服務介面 (ADSI) 來存取 Active Directory。</span><span class="sxs-lookup"><span data-stu-id="2aca9-111">This section discusses how to use the Active Directory Service Interfaces (ADSI) to access Active Directory.</span></span> <span data-ttu-id="2aca9-112">針對虛構公司（Fabrikam Corporation）使用案例，您將瞭解如何執行一些基本的系統管理工作。</span><span class="sxs-lookup"><span data-stu-id="2aca9-112">Using a scenario for a fictitious company — the Fabrikam Corporation — you will learn how to perform some basic administrative tasks.</span></span>

<span data-ttu-id="2aca9-113">當您進行此案例時，每個區段中的程式碼範例都會自行建立。</span><span class="sxs-lookup"><span data-stu-id="2aca9-113">As you progress through this scenario, the code examples in each section build upon themselves.</span></span>

<span data-ttu-id="2aca9-114">為了簡潔起見，所有的程式碼範例都是使用 Microsoft Visual Basic 開發系統來撰寫。</span><span class="sxs-lookup"><span data-stu-id="2aca9-114">For brevity, all code examples are written with the Microsoft Visual Basic development system.</span></span> <span data-ttu-id="2aca9-115">如需 c + + 轉換的詳細資訊，請參閱 [將 ADSI Visual Basic 程式碼對應至 c + + 程式碼](mapping-adsi-visual-basic-code-to-c-code.md)。</span><span class="sxs-lookup"><span data-stu-id="2aca9-115">For more information about C++ conversion, see [Mapping ADSI Visual Basic Code to C++ Code](mapping-adsi-visual-basic-code-to-c-code.md).</span></span>

 

 




