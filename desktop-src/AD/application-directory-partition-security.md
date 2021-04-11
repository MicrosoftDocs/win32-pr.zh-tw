---
title: 應用程式目錄分割安全性
description: 應用程式目錄分割的安全性與存取控制模型與 Active Directory Domain Services 中的其他分割區相同。
ms.assetid: 3e14b31a-524e-4b38-957f-166e80b35b31
ms.tgt_platform: multiple
keywords:
- 應用程式目錄分割安全性 AD
- 應用程式目錄分割 AD，安全性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80da4ce1b8d4e3604b8e546d79003f4d3719223d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933090"
---
# <a name="application-directory-partition-security"></a><span data-ttu-id="649a6-105">應用程式目錄分割安全性</span><span class="sxs-lookup"><span data-stu-id="649a6-105">Application Directory Partition Security</span></span>

<span data-ttu-id="649a6-106">應用程式目錄分割的安全性與存取控制模型與 Active Directory Domain Services 中的其他分割區相同。</span><span class="sxs-lookup"><span data-stu-id="649a6-106">The security and access control model for application directory partitions is the same as that for other partitions in Active Directory Domain Services.</span></span> <span data-ttu-id="649a6-107">一般使用者可以存取應用程式目錄分割中的物件，這些物件會受限於放在這些物件上的 Acl。</span><span class="sxs-lookup"><span data-stu-id="649a6-107">Normal users can access objects in an application directory partition subject to the ACLs placed on those objects.</span></span> <span data-ttu-id="649a6-108">如需詳細資訊，請參閱 [控制 Active Directory Domain Services 中的物件存取](controlling-access-to-objects-in-active-directory-domain-services.md)。</span><span class="sxs-lookup"><span data-stu-id="649a6-108">For more information, see [Controlling Access to Objects in Active Directory Domain Services](controlling-access-to-objects-in-active-directory-domain-services.md).</span></span>

<span data-ttu-id="649a6-109">不過，由於應用程式目錄分割可以跨目錄服務中的多個安全性網域，因此在應用程式目錄分割中建立物件時，會在物件的架構類別 [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) 中，解釋與網域相關的已知 SID 字串常數的問題。</span><span class="sxs-lookup"><span data-stu-id="649a6-109">However, because application directory partitions can span multiple security domains in a directory service, there arises the question of how to interpret domain-relative well-known SID string constants in the [**defaultSecurityDescriptor**](/windows/desktop/ADSchema/a-defaultsecuritydescriptor) of an object's schema class at the time of object creation in an application directory partition.</span></span> <span data-ttu-id="649a6-110">例如，如果 "DA" 指的是網域系統管理員群組，但在應用程式目錄分割中，則不知道 "DA" 群組所指的是哪個網域。</span><span class="sxs-lookup"><span data-stu-id="649a6-110">For example, if "DA" refers to the domain administrators group, but in an application directory partition, it is not known which domain the "DA" group refers to.</span></span>

<span data-ttu-id="649a6-111">若要解決這個問題，應用程式目錄分割的 [**交叉**](/windows/desktop/ADSchema/c-crossref) 參考物件具有 [**SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) 屬性，其中包含該應用程式目錄分割之參考功能變數名稱的分辨名稱。</span><span class="sxs-lookup"><span data-stu-id="649a6-111">To solve this problem, the [**crossRef**](/windows/desktop/ADSchema/c-crossref) object of an application directory partition has an [**msDS-SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) attribute that contains the distinguished name of the reference domain for that application directory partition.</span></span> <span data-ttu-id="649a6-112">安全性系統使用指定的網域來解讀本機網域參考，以取得附加至該應用程式目錄分割中所建立物件的預設安全描述項。</span><span class="sxs-lookup"><span data-stu-id="649a6-112">The security system uses the specified domain to interpret local domain references for default security descriptors attached to objects created in that application directory partition.</span></span> <span data-ttu-id="649a6-113">當建立應用程式目錄分割的 **交叉** 參考物件時，可以指定參考網域。</span><span class="sxs-lookup"><span data-stu-id="649a6-113">The reference domain can be specified when the **crossRef** object for an application directory partition is created.</span></span> <span data-ttu-id="649a6-114">不過，這需要針對應用程式目錄分割預先建立 **交叉引用** 物件。</span><span class="sxs-lookup"><span data-stu-id="649a6-114">This requires, however, that a **crossRef** object be pre-created for the application directory partition.</span></span> <span data-ttu-id="649a6-115">如果未指定任何參考網域，系統就會根據下列其中一個條件來自動設定參考網域：</span><span class="sxs-lookup"><span data-stu-id="649a6-115">If no reference domain is specified, the system automatically sets the reference domain based on one of the following conditions:</span></span>

-   <span data-ttu-id="649a6-116">如果應用程式目錄分割物件的父系是另一個應用程式目錄分割，則會將父應用程式目錄分割的 [**SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) 屬性用於參考網域。</span><span class="sxs-lookup"><span data-stu-id="649a6-116">If the parent of the application directory partition object is another application directory partition, then the [**msDS-SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) attribute of the parent application directory partition is used for the reference domain.</span></span>
-   <span data-ttu-id="649a6-117">如果父物件是網域，則會將該網域用於參考網域。</span><span class="sxs-lookup"><span data-stu-id="649a6-117">If the parent object is a domain, then that domain is used for the reference domain.</span></span>
-   <span data-ttu-id="649a6-118">如果沒有父物件，則會使用樹系根域作為參考網域。</span><span class="sxs-lookup"><span data-stu-id="649a6-118">If there is no parent object, then the forest root domain is used for the reference domain.</span></span>

<span data-ttu-id="649a6-119">建立分割區之後， **交叉** 參考屬性也可以變更為參考定義域，但不建議這樣做。</span><span class="sxs-lookup"><span data-stu-id="649a6-119">The **crossRef** attribute can also be changed to the reference domain after the partition is created, but this is not recommended.</span></span>

<span data-ttu-id="649a6-120">如果在應用程式目錄分割中的物件 ACL 中指定了本機群組，就會發生類似的問題。</span><span class="sxs-lookup"><span data-stu-id="649a6-120">A similar issue arises if a local group is specified in an ACL for an object in an application directory partition.</span></span> <span data-ttu-id="649a6-121">在此情況下， [**SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) 屬性不能用來解讀本機群組的參考網域。</span><span class="sxs-lookup"><span data-stu-id="649a6-121">In this case, the [**msDS-SDReferenceDomain**](/windows/desktop/ADSchema/a-msds-sdreferencedomain) attribute cannot be used to interpret the reference domain for a local group.</span></span> <span data-ttu-id="649a6-122">若要避免這個問題，請不要在應用程式目錄分割物件的 Acl 中使用本機群組。</span><span class="sxs-lookup"><span data-stu-id="649a6-122">To avoid this problem, local groups should not be used in the ACLs of application directory partition objects.</span></span>

 

 