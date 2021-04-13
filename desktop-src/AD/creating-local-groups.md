---
title: 建立本機群組
description: 只有本機群組可以針對成員伺服器和 Windows 2000 Professional 建立。
ms.assetid: 76cbac51-d8ba-4114-9951-060273be52f3
ms.tgt_platform: multiple
keywords:
- 建立本機群組 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 705902b0066913fcd6eed56ba7c74e299144595f
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104314638"
---
# <a name="creating-local-groups"></a><span data-ttu-id="d6d9e-104">建立本機群組</span><span class="sxs-lookup"><span data-stu-id="d6d9e-104">Creating Local Groups</span></span>

<span data-ttu-id="d6d9e-105">只有本機群組可以針對成員伺服器和 Windows 2000 Professional 建立。</span><span class="sxs-lookup"><span data-stu-id="d6d9e-105">Only local groups can be created for member servers and Windows 2000 Professional.</span></span>

<span data-ttu-id="d6d9e-106">**為執行 Windows 2000 Professional 的成員伺服器或電腦建立本機群組**</span><span class="sxs-lookup"><span data-stu-id="d6d9e-106">**To create a local group for a member server or computer running Windows 2000 Professional**</span></span>

1.  <span data-ttu-id="d6d9e-107">使用下列規則系結至電腦：</span><span class="sxs-lookup"><span data-stu-id="d6d9e-107">Bind to the computer using the following rules:</span></span>
    1.  <span data-ttu-id="d6d9e-108">使用具有足夠許可權的帳戶來存取該電腦。</span><span class="sxs-lookup"><span data-stu-id="d6d9e-108">Use an account with sufficient rights to access that computer.</span></span>
    2.  <span data-ttu-id="d6d9e-109">使用 WinNT 提供者、電腦名稱稱和額外的參數來使用下列系結字串格式，以指示 ADSI 系結至電腦： "WinNT://" <computer name> <computer> 。</span><span class="sxs-lookup"><span data-stu-id="d6d9e-109">Use the following binding string format using the WinNT provider, computer name, and an extra parameter to instruct ADSI that it is binding to a computer: "WinNT://<computer name>,<computer>".</span></span>

        <span data-ttu-id="d6d9e-110">「 &lt; 電腦名稱稱」 &gt; 參數是要存取的電腦群組名。</span><span class="sxs-lookup"><span data-stu-id="d6d9e-110">The "&lt;computer name&gt;" parameter is the name of the computer groups to access.</span></span>

        <span data-ttu-id="d6d9e-111">在系結字串中，" &lt; computer &gt; " 參數會指示 ADSI 系結至電腦。</span><span class="sxs-lookup"><span data-stu-id="d6d9e-111">In the binding string, the "&lt;computer&gt;" parameter instructs ADSI that it is binding to a computer.</span></span> <span data-ttu-id="d6d9e-112">ADSI 會將此資料提供給 WinNT 提供者的剖析器，讓它可以略過一些明確的解析查詢，以判斷您要系結到的物件類型。</span><span class="sxs-lookup"><span data-stu-id="d6d9e-112">ADSI makes this data available to the WinNT provider's parser so that it can skip some ambiguity-resolution queries to determine what type of object you are binding to.</span></span>

    3.  <span data-ttu-id="d6d9e-113">系結至 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 介面。</span><span class="sxs-lookup"><span data-stu-id="d6d9e-113">Bind to the [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) interface.</span></span>

2.  <span data-ttu-id="d6d9e-114">使用 [**IADsContainer**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) 指定 "localGroup" 作為類別，以新增群組。</span><span class="sxs-lookup"><span data-stu-id="d6d9e-114">Specify "localGroup" as the class using [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) to add the group.</span></span>
    > [!Note]  
    > <span data-ttu-id="d6d9e-115">如果您指定 "group" 作為類別，ADSI 會使用 "localGroup"。</span><span class="sxs-lookup"><span data-stu-id="d6d9e-115">If you specify "group" as the class, ADSI uses "localGroup".</span></span> <span data-ttu-id="d6d9e-116">請勿將類別指定為 "globalGroup"。</span><span class="sxs-lookup"><span data-stu-id="d6d9e-116">Do not specify the class as "globalGroup".</span></span> <span data-ttu-id="d6d9e-117">無法在成員伺服器或執行 Windows NT 工作站/Windows 2000 Professional 的電腦上建立類別 "globalGroup" 的群組。</span><span class="sxs-lookup"><span data-stu-id="d6d9e-117">Groups of class "globalGroup" cannot be created on member servers or a computer running Windows NT Workstation/Windows 2000 Professional.</span></span> <span data-ttu-id="d6d9e-118">如果您指定 "globalGroup"， [**IADsContainer**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) 就會在屬性快取中建立群組，但是 [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) 不會將群組寫入安全性資料庫，而且不會傳回錯誤。</span><span class="sxs-lookup"><span data-stu-id="d6d9e-118">If you specify "globalGroup", [**IADsContainer.Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) creates the group in the property cache, but [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) does not write the group to the security database and it does not return an error.</span></span>

     

3.  <span data-ttu-id="d6d9e-119">使用 [**IADs SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo)將群組寫入電腦安全性性資料庫。</span><span class="sxs-lookup"><span data-stu-id="d6d9e-119">Write the group to the computer security database using [**IADs.SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo).</span></span>

 

 