---
description: 憑證的數目、憑證撤銷清單 (Crl) ，以及使用者集合中 (Ctl) 的憑證信任清單成長時，這些憑證的組織就會變成問題。
ms.assetid: 13e7e077-e8be-4ba4-99e1-08421fd2452e
title: 集合存放區
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bfeb8ef071d7a5ccf6bc7ce43ba418117879536
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851043"
---
# <a name="collection-stores"></a><span data-ttu-id="ee89a-103">集合存放區</span><span class="sxs-lookup"><span data-stu-id="ee89a-103">Collection Stores</span></span>

<span data-ttu-id="ee89a-104">[*憑證的數目、*](../secgloss/c-gly.md)[*憑證撤銷清單*](../secgloss/c-gly.md) (crl) ，以及使用者集合中 (ctl) 的 [*憑證信任清單*](../secgloss/c-gly.md)成長時，這些憑證的組織就會變成問題。</span><span class="sxs-lookup"><span data-stu-id="ee89a-104">As the number of [*certificates*](../secgloss/c-gly.md), [*certificate revocation lists*](../secgloss/c-gly.md) (CRLs), and [*certificate trust list*](../secgloss/c-gly.md) (CTLs) in a user's collection grows, the organization of those certificates becomes an issue.</span></span> <span data-ttu-id="ee89a-105">其中一個可能的解決方法是建立不同的憑證存放區，以保留不同類型的憑證。</span><span class="sxs-lookup"><span data-stu-id="ee89a-105">One possible solution is to create separate certificate stores to keep different kinds of certificates.</span></span> <span data-ttu-id="ee89a-106">此解決方案會建立新的問題，因為應用程式可能需要搜尋數個不同的商店來尋找特定的憑證。</span><span class="sxs-lookup"><span data-stu-id="ee89a-106">This solution creates a new problem because an application might need to search several different stores to find a specific certificate.</span></span> <span data-ttu-id="ee89a-107">使用邏輯或集合存放區可解決此問題。</span><span class="sxs-lookup"><span data-stu-id="ee89a-107">The use of logical or collection stores solves this problem.</span></span>

<span data-ttu-id="ee89a-108">[*邏輯存放區*](../secgloss/l-gly.md)和集合憑證存放區是以單一存放區形式出現在應用程式中的實體存放區群組。</span><span class="sxs-lookup"><span data-stu-id="ee89a-108">A [*logical store*](../secgloss/l-gly.md) and a collection certificate store are groups of physical stores that appears to an application as a single store.</span></span> <span data-ttu-id="ee89a-109">您可以使用對 [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) 或 [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore)的單一函數呼叫來搜尋或列舉邏輯或集合存放區的所有成員存放區。</span><span class="sxs-lookup"><span data-stu-id="ee89a-109">All member stores of a logical or collection store can be searched or enumerated with a single function call to either [**CertFindCertificateInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certfindcertificateinstore) or [**CertEnumCertificatesInStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certenumcertificatesinstore).</span></span>

<span data-ttu-id="ee89a-110">使用「邏輯」或「收集」存放區也可提供難以使用紙張記錄來達成的彈性。</span><span class="sxs-lookup"><span data-stu-id="ee89a-110">The use of logical or collection stores also provides flexibility that is difficult to achieve with paper records.</span></span> <span data-ttu-id="ee89a-111">單一實體存放區中的憑證可能必須是數個不同邏輯群組的成員。</span><span class="sxs-lookup"><span data-stu-id="ee89a-111">A certificate in a single physical store might need to be a member of several different logical groups.</span></span> <span data-ttu-id="ee89a-112">因此，個別的實體存放區可以是一個以上的邏輯或集合存放區成員，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="ee89a-112">Therefore, an individual physical store can be a member of more than one logical or collection store as shown in the following illustration.</span></span>

![集合存放區](images/mancert.png)

<span data-ttu-id="ee89a-114">下圖顯示下列基本的邏輯憑證存放區概念：</span><span class="sxs-lookup"><span data-stu-id="ee89a-114">This illustration presents the following basic, logical certificate store concepts:</span></span>

-   <span data-ttu-id="ee89a-115">集合憑證存放區有指向該集合存放區之第一個指標區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="ee89a-115">A collection certificate store has a pointer to the first pointer block for that collection store.</span></span>
-   <span data-ttu-id="ee89a-116">集合存放區的每個指標區塊都有指向同級存放區的指標，以及該集合下一個指標區塊的指標。</span><span class="sxs-lookup"><span data-stu-id="ee89a-116">Each pointer block of a collection store has a pointer to a sibling store and a pointer to the next pointer block of the collection.</span></span>
-   <span data-ttu-id="ee89a-117">集合中的每個同級存放區都是簡單的實體憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="ee89a-117">Each sibling store in a collection is a simple physical certificate store.</span></span>
-   <span data-ttu-id="ee89a-118">簡單的憑證存放區可以是許多不同收集存放區中的成員同級存放區。</span><span class="sxs-lookup"><span data-stu-id="ee89a-118">A simple certificate store can be a member sibling store in many different collection stores.</span></span>
-   <span data-ttu-id="ee89a-119">新增至集合存放區的憑證會實際新增至集合中的其中一個同級存放區。</span><span class="sxs-lookup"><span data-stu-id="ee89a-119">Certificates added to a collection store are physically added to one of the sibling stores in the collection.</span></span>
-   <span data-ttu-id="ee89a-120">在同級存放區中的憑證，可以由任何屬於該成員的集合存放區存取。</span><span class="sxs-lookup"><span data-stu-id="ee89a-120">Certificates in a sibling store can be accessed by any collection store in which the sibling store is a member.</span></span>

<span data-ttu-id="ee89a-121">收集存放區是在應用程式內建立的，方法是使用 [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) 開啟集合存放區，然後使用 [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection) 將開啟的同級存放區加入至集合存放區。</span><span class="sxs-lookup"><span data-stu-id="ee89a-121">Collection stores are built within an application by opening a collection store by using [**CertOpenStore**](/windows/desktop/api/Wincrypt/nf-wincrypt-certopenstore) and then using [**CertAddStoreToCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certaddstoretocollection) to add an open sibling store to the collection store.</span></span> <span data-ttu-id="ee89a-122">您可以藉由呼叫 [**CertRemoveStoreFromCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremovestorefromcollection)，從集合存放區刪除同級存放區。</span><span class="sxs-lookup"><span data-stu-id="ee89a-122">A sibling store can be deleted from a collection store by calling [**CertRemoveStoreFromCollection**](/windows/desktop/api/Wincrypt/nf-wincrypt-certremovestorefromcollection).</span></span>

 

 
