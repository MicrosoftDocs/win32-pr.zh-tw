---
title: 列舉本機群組
description: 在執行 Windows 2000 Professional 的成員伺服器和電腦上，您可以列舉所有本機群組。
ms.assetid: edbabbe5-13e1-42f6-8e73-f8e18ba4866b
ms.tgt_platform: multiple
keywords:
- 列舉本機群組 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e106fc2517cfedd8fb5fa40e4b99798ee32de8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681671"
---
# <a name="enumerating-local-groups"></a><span data-ttu-id="d0fa9-104">列舉本機群組</span><span class="sxs-lookup"><span data-stu-id="d0fa9-104">Enumerating Local Groups</span></span>

<span data-ttu-id="d0fa9-105">在執行 Windows 2000 Professional 的成員伺服器和電腦上，您可以列舉所有本機群組。</span><span class="sxs-lookup"><span data-stu-id="d0fa9-105">On member servers and computers running on Windows 2000 Professional, you can enumerate all local groups.</span></span>

<span data-ttu-id="d0fa9-106">只有本機群組可以在成員伺服器和 Windows 2000 Professional 上建立。</span><span class="sxs-lookup"><span data-stu-id="d0fa9-106">Only local groups can be created on member servers and Windows 2000 Professional.</span></span> <span data-ttu-id="d0fa9-107">不過，這些本機群組可以包含：</span><span class="sxs-lookup"><span data-stu-id="d0fa9-107">However, those local groups can contain:</span></span>

-   <span data-ttu-id="d0fa9-108">樹系中的通用和全域群組，其中包含電腦所屬的網域。</span><span class="sxs-lookup"><span data-stu-id="d0fa9-108">Universal and Global groups from the forest that contains the domain to which the computer is a member.</span></span>
-   <span data-ttu-id="d0fa9-109">來自該電腦網域的網域本機群組。</span><span class="sxs-lookup"><span data-stu-id="d0fa9-109">Domain local groups from that computer's domain.</span></span>
-   <span data-ttu-id="d0fa9-110">樹系中任何網域的使用者。</span><span class="sxs-lookup"><span data-stu-id="d0fa9-110">Users from any domain in the forest.</span></span>

<span data-ttu-id="d0fa9-111">**在成員伺服器或執行 Windows 2000 Professional 的電腦上列舉本機群組**</span><span class="sxs-lookup"><span data-stu-id="d0fa9-111">**To enumerate the local groups on a member server or computer running Windows 2000 Professional**</span></span>

1.  <span data-ttu-id="d0fa9-112">使用下列規則系結至電腦：</span><span class="sxs-lookup"><span data-stu-id="d0fa9-112">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="d0fa9-113">使用具有足夠許可權的帳戶來存取該電腦。</span><span class="sxs-lookup"><span data-stu-id="d0fa9-113">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="d0fa9-114">使用 WinNT 提供者、電腦名稱稱和額外的參數來使用下列系結字串格式，以指示 ADSI 系結至電腦： "WinNT://" <computer name> <computer> 。</span><span class="sxs-lookup"><span data-stu-id="d0fa9-114">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span>

        <span data-ttu-id="d0fa9-115">" <computer name> 參數是要存取的電腦群組名。</span><span class="sxs-lookup"><span data-stu-id="d0fa9-115">"The <computer name>" parameter is the name of the computer group to access.</span></span> <span data-ttu-id="d0fa9-116">此參數會指示 ADSI 系結至電腦，並允許 WinNT 提供者的剖析器略過一些不明確的解析查詢，以判斷您要系結到的物件類型。</span><span class="sxs-lookup"><span data-stu-id="d0fa9-116">This parameter instruct ADSI that it is binding to a computer and allows the WinNT provider's parser to skip some ambiguity-resolution queries to determine what type of object you are binding to.</span></span>

    3.  <span data-ttu-id="d0fa9-117">系結至 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 介面。</span><span class="sxs-lookup"><span data-stu-id="d0fa9-117">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>

2.  <span data-ttu-id="d0fa9-118">使用 [**IADsContainer. filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) 屬性設定包含 "groups" 的篩選準則。</span><span class="sxs-lookup"><span data-stu-id="d0fa9-118">Set a filter that contains "groups" using the [**IADsContainer.Filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) property.</span></span> <span data-ttu-id="d0fa9-119">這可讓您列舉容器，並只取得群組。</span><span class="sxs-lookup"><span data-stu-id="d0fa9-119">This enables you to enumerate the container and retrieve only groups.</span></span>
3.  <span data-ttu-id="d0fa9-120">使用 [**IADsContainer：： get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum)方法來列舉群組物件。</span><span class="sxs-lookup"><span data-stu-id="d0fa9-120">Enumerate the group objects, using the [**IADsContainer::get\_\_NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum) method.</span></span>
4.  <span data-ttu-id="d0fa9-121">針對每個群組物件，使用 [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) 介面讀取群組的名稱和成員。</span><span class="sxs-lookup"><span data-stu-id="d0fa9-121">For each the group object, use the [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) interface to read the name and members of the group.</span></span>

 

 