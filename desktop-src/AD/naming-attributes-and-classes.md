---
title: 命名屬性和類別
description: 本主題包含命名屬性和類別的指導方針。
ms.assetid: ccbc2859-332f-4ded-9125-5bf507cad960
ms.tgt_platform: multiple
keywords:
- 命名屬性和類別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 80bfd2614033e12f68ba2727cc7aec689c16071e
ms.sourcegitcommit: 02e6e0b58720bf6b77797dd7a9ddc11c95f42b33
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2020
ms.locfileid: "107001288"
---
# <a name="naming-attributes-and-classes"></a><span data-ttu-id="069fc-104">命名屬性和類別</span><span class="sxs-lookup"><span data-stu-id="069fc-104">Naming Attributes and Classes</span></span>

<span data-ttu-id="069fc-105">本主題包含命名屬性和類別的指導方針。</span><span class="sxs-lookup"><span data-stu-id="069fc-105">This topic includes guidelines for naming attributes and classes.</span></span>

<span data-ttu-id="069fc-106">若要建立新的類別或屬性，請遵循下列命名規則：</span><span class="sxs-lookup"><span data-stu-id="069fc-106">To create a new class or attribute, adhere to the following naming rules:</span></span>

-   <span data-ttu-id="069fc-107">新 **attributeSchema** 或 **classSchema** 物件的 **cn** 和 **lDAPDisplayName** 屬性都使用相同的名稱。</span><span class="sxs-lookup"><span data-stu-id="069fc-107">Use the same name for both the **cn** and **lDAPDisplayName** properties of a new **attributeSchema** or **classSchema** object.</span></span>
-   <span data-ttu-id="069fc-108">在名稱的第一個區段中，識別具有小寫前置詞的公司。</span><span class="sxs-lookup"><span data-stu-id="069fc-108">Identify the company with a lower-case prefix in the first section of the name.</span></span> <span data-ttu-id="069fc-109">這個前置詞可以是 DNS 名稱、縮略字或可唯一識別該公司的其他字串。</span><span class="sxs-lookup"><span data-stu-id="069fc-109">This prefix can be a DNS name, acronym, or other string that uniquely identifies the company.</span></span> <span data-ttu-id="069fc-110">前置詞可確保在流覽架構時，會連續顯示特定公司的所有屬性和類別。</span><span class="sxs-lookup"><span data-stu-id="069fc-110">The prefix ensures that all attributes and classes for a specific company are displayed consecutively when browsing the schema.</span></span>
-   <span data-ttu-id="069fc-111">如果您要將架構延伸開發為獨立軟體廠商，請新增前置詞的產品名稱縮寫。</span><span class="sxs-lookup"><span data-stu-id="069fc-111">If you are developing a schema extension as an independent software vendor, add an abbreviation of the product name of the prefix.</span></span> <span data-ttu-id="069fc-112">這會增加多個包含 LDAP 架構延伸的產品之間的差異。</span><span class="sxs-lookup"><span data-stu-id="069fc-112">This adds distinction between multiple products that contain LDAP schema extensions.</span></span>
-   <span data-ttu-id="069fc-113">使用連字號作為前置詞後面的下一個字元。</span><span class="sxs-lookup"><span data-stu-id="069fc-113">Use a hyphen as the next character after the prefix.</span></span>
-   <span data-ttu-id="069fc-114">在連字號之後的公司屬性中，指定唯一的屬性或類別名稱。</span><span class="sxs-lookup"><span data-stu-id="069fc-114">Specify an attribute or class name that is unique within the company's attributes after the hyphen.</span></span> <span data-ttu-id="069fc-115">一般名稱的這個部分應該是描述性的。</span><span class="sxs-lookup"><span data-stu-id="069fc-115">This part of the common-name should be descriptive.</span></span> <span data-ttu-id="069fc-116">請勿使用對架構開發人員和檢視器沒有意義的顯得不合理名稱。</span><span class="sxs-lookup"><span data-stu-id="069fc-116">Do not use illogical names that are meaningless to developers and viewers of the schema.</span></span>

<span data-ttu-id="069fc-117">例如，假設虛構的 Fabrikam 公司藉由新增用來儲存語音信箱識別碼的屬性來延伸架構，則新屬性的 **cn** 和 **lDAPDisplayName** 可能是 "Fabrikam-VoiceMailID"。</span><span class="sxs-lookup"><span data-stu-id="069fc-117">For example, if the fictitious Fabrikam company extended the schema by adding an attribute for storing a voice-mail identifier, the **cn** and **lDAPDisplayName** of the new attribute could be "fabrikam-VoiceMailID".</span></span>

<span data-ttu-id="069fc-118">如果未指定屬性或類別的 **lDAPDisplayName** ，系統會使用 **cn** 來產生一或多個。</span><span class="sxs-lookup"><span data-stu-id="069fc-118">If the **lDAPDisplayName** of an attribute or class is not specified, the system uses the **cn** to generate one.</span></span> <span data-ttu-id="069fc-119">不過，產生名稱的系統演算法可能會導致名稱衝突或難以讀取的名稱。</span><span class="sxs-lookup"><span data-stu-id="069fc-119">However, the system algorithm for generating the name may result in name collisions or names that are difficult to read.</span></span> <span data-ttu-id="069fc-120">若要避免這些問題，建議您為所有屬性和類別明確指定 **lDAPDisplayName** 。</span><span class="sxs-lookup"><span data-stu-id="069fc-120">To avoid these problems, it is recommended that an **lDAPDisplayName** be explicitly specified for all attributes and classes.</span></span>

<span data-ttu-id="069fc-121">針對開發和測試目的，您可能會想要將版本尾碼附加到 **cn** 和 **lDAPDisplayName**，例如 "fabrikam-VoiceMailID-001"。</span><span class="sxs-lookup"><span data-stu-id="069fc-121">For development and testing purposes, it may be desirable to append a version suffix to the **cn** and **lDAPDisplayName**, for example, "fabrikam-VoiceMailID-001".</span></span> <span data-ttu-id="069fc-122">在分散式開發/測試環境中，版本尾碼可讓開發人員同時執行其軟體的多個版本。</span><span class="sxs-lookup"><span data-stu-id="069fc-122">In a distributed development/test environment, a version suffix enables developers to run multiple versions of their software simultaneously.</span></span> <span data-ttu-id="069fc-123">測試完成之後，請重新命名屬性或類別以移除尾碼。</span><span class="sxs-lookup"><span data-stu-id="069fc-123">After testing is complete, rename the attribute or class to remove the suffix.</span></span>

<span data-ttu-id="069fc-124">您無法刪除架構延伸模組的無用版本，但可以將其停用，然後以隱匿的名稱重新命名。</span><span class="sxs-lookup"><span data-stu-id="069fc-124">It is not possible to delete defunct versions of a schema extensions, but it is possible to disable them and rename them with obscure names.</span></span> <span data-ttu-id="069fc-125">如需詳細資訊，請參閱 [停用現有的類別和屬性](disabling-existing-classes-and-attributes.md)。</span><span class="sxs-lookup"><span data-stu-id="069fc-125">For more information, see [Disabling Existing Classes and Attributes](disabling-existing-classes-and-attributes.md).</span></span>

 

 




