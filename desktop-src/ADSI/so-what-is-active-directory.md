---
title: 教學課程總覽與 Visual Basic 的 ADSI
description: Active Directory 是特殊用途的資料庫 \ 8212;它不是登錄取代。
ms.assetid: 899799e3-5ab9-4d19-883a-5bc9f20d2bad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6607d9da26d1c96d7cb6f83a799c7633404e5bb4
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "104566925"
---
# <a name="tutorial-overview-adsi-with-visual-basic"></a><span data-ttu-id="a3966-103">教學課程總覽： ADSI 與 Visual Basic</span><span class="sxs-lookup"><span data-stu-id="a3966-103">Tutorial Overview: ADSI with Visual Basic</span></span>

> [!Note]  
> <span data-ttu-id="a3966-104">下列檔是 Visual Basic 開發人員擴充案例描述的一部分。</span><span class="sxs-lookup"><span data-stu-id="a3966-104">The following documentation is part of an extended scenario description for Visual Basic developers.</span></span> <span data-ttu-id="a3966-105">如果您要尋找 Active Directory 的一般總覽，請參閱 [Technet 上的 IT 專業人員檔](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10))。</span><span class="sxs-lookup"><span data-stu-id="a3966-105">If you are looking for a general overview of Active Directory, see the [IT Pro docs on Technet](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10)).</span></span> <span data-ttu-id="a3966-106">若要深入瞭解 Active Directory 的開發端，請參閱 [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services)。</span><span class="sxs-lookup"><span data-stu-id="a3966-106">For a more in-depth look at the development side of Active Directory, see [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services).</span></span> <span data-ttu-id="a3966-107">如需 Active Directory 服務介面的更大介紹，請參閱本主題的父主題： [Active Directory 服務介面](active-directory-service-interfaces-adsi.md)，以及同級主題： [關於 Active Directory 服務介面](about-adsi.md)。</span><span class="sxs-lookup"><span data-stu-id="a3966-107">For a larger introduction to Active Directory Service Interfaces, see this topic's parent topic: [Active Directory Service Interfaces](active-directory-service-interfaces-adsi.md), as well as the sibling topic: [About Active Directory Service Interfaces](about-adsi.md).</span></span>

 

<span data-ttu-id="a3966-108">Active Directory 是特殊用途的資料庫，而不是登錄取代。</span><span class="sxs-lookup"><span data-stu-id="a3966-108">Active Directory is a special-purpose database — it is not a registry replacement.</span></span> <span data-ttu-id="a3966-109">目錄的設計目的是要處理大量的讀取和搜尋作業，並大幅減少變更和更新的數目。</span><span class="sxs-lookup"><span data-stu-id="a3966-109">The directory is designed to handle a large number of read and search operations and a significantly smaller number of changes and updates.</span></span> <span data-ttu-id="a3966-110">Active Directory 資料是階層式、複寫和可擴充的。</span><span class="sxs-lookup"><span data-stu-id="a3966-110">Active Directory data is hierarchical, replicated, and extensible.</span></span> <span data-ttu-id="a3966-111">因為它已複寫，所以您不想要儲存動態資料，例如公司股票價格或 CPU 效能。</span><span class="sxs-lookup"><span data-stu-id="a3966-111">Because it is replicated, you do not want to store dynamic data, such as corporate stock prices or CPU performance.</span></span> <span data-ttu-id="a3966-112">如果您的資料是電腦特有的，請將資料儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="a3966-112">If your data is machine-specific, store the data in the registry.</span></span> <span data-ttu-id="a3966-113">目錄中儲存的一般資料範例包括印表機佇列資料、使用者連絡人資料和網路/電腦設定資料。</span><span class="sxs-lookup"><span data-stu-id="a3966-113">Typical examples of data stored in the directory include printer queue data, user contact data, and network/computer configuration data.</span></span> <span data-ttu-id="a3966-114">Active Directory 資料庫是由物件和屬性所組成。</span><span class="sxs-lookup"><span data-stu-id="a3966-114">The Active Directory database consists of objects and attributes.</span></span> <span data-ttu-id="a3966-115">物件和屬性定義會儲存在 Active Directory 架構中。</span><span class="sxs-lookup"><span data-stu-id="a3966-115">Objects and attribute definitions are stored in the Active Directory schema.</span></span>

<span data-ttu-id="a3966-116">您可能想知道哪些物件目前儲存在 Active Directory 中。</span><span class="sxs-lookup"><span data-stu-id="a3966-116">You may be wondering what objects are currently stored in Active Directory.</span></span> <span data-ttu-id="a3966-117">Active Directory 有三個磁碟分割。</span><span class="sxs-lookup"><span data-stu-id="a3966-117">Active Directory has three partitions.</span></span> <span data-ttu-id="a3966-118">這些也稱為命名內容：網域、架構和設定。</span><span class="sxs-lookup"><span data-stu-id="a3966-118">These are also known as naming contexts: domain, schema, and configuration.</span></span> <span data-ttu-id="a3966-119">網域分割區包含使用者、群組、連絡人、電腦、組織單位以及許多其他物件類型。</span><span class="sxs-lookup"><span data-stu-id="a3966-119">The domain partition contains users, groups, contacts, computers, organizational units, and many other object types.</span></span> <span data-ttu-id="a3966-120">因為 Active Directory 可延伸，所以您也可以新增自己的類別及/或屬性。</span><span class="sxs-lookup"><span data-stu-id="a3966-120">Because Active Directory is extensible, you can also add your own classes and/or attributes.</span></span> <span data-ttu-id="a3966-121">架構分割區包含類別和屬性定義。</span><span class="sxs-lookup"><span data-stu-id="a3966-121">The schema partition contains classes and attribute definitions.</span></span> <span data-ttu-id="a3966-122">設定磁碟分割包含服務、磁碟分割和網站的設定資料。</span><span class="sxs-lookup"><span data-stu-id="a3966-122">The configuration partition includes configuration data for services, partitions, and sites.</span></span>

<span data-ttu-id="a3966-123">下列螢幕擷取畫面顯示 Active Directory 的網域分割區。</span><span class="sxs-lookup"><span data-stu-id="a3966-123">The following screen shot shows the Active Directory domain partition.</span></span>

![active directory 網域分割](images/adadsi1.png)

## <a name="related-topics"></a><span data-ttu-id="a3966-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="a3966-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="a3966-126">使用 Visual Basic 存取 Active Directory</span><span class="sxs-lookup"><span data-stu-id="a3966-126">Accessing Active Directory Using Visual Basic</span></span>](accessing-active-directory-using-visual-basic.md)
</dt> <dt>

[<span data-ttu-id="a3966-127">案例： Fabrikam Corporation</span><span class="sxs-lookup"><span data-stu-id="a3966-127">Scenario: The Fabrikam Corporation</span></span>](scenario--the-fabrikam-corporation.md)
</dt> <dt>

[<span data-ttu-id="a3966-128">Advanced 主題</span><span class="sxs-lookup"><span data-stu-id="a3966-128">Advanced Topics</span></span>](advanced-topics.md)
</dt> </dl>

 

 