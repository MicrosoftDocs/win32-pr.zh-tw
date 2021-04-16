---
title: 物件名稱和身分識別
description: Active Directory Domain Services 中的物件有數個身分識別，包括下列各項。
ms.assetid: ad8bc74d-45a8-4df3-bfb8-35dd376b9c0b
ms.tgt_platform: multiple
keywords:
- 物件名稱和身分識別 Active Directory
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a803b4cc068a3ee0f9e2a75f61ff239c1d971bf3
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462844"
---
# <a name="object-names-and-identities"></a><span data-ttu-id="c9c20-104">物件名稱和身分識別</span><span class="sxs-lookup"><span data-stu-id="c9c20-104">Object Names and Identities</span></span>

<span data-ttu-id="c9c20-105">Active Directory Domain Services 中的物件有數個身分識別，包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="c9c20-105">An object in Active Directory Domain Services has several identities, including the following.</span></span>

## <a name="relative-distinguished-name"></a><span data-ttu-id="c9c20-106">相對辨別名稱</span><span class="sxs-lookup"><span data-stu-id="c9c20-106">Relative Distinguished Name</span></span>

<span data-ttu-id="c9c20-107">相對分辨名稱是物件命名屬性所定義的名稱。</span><span class="sxs-lookup"><span data-stu-id="c9c20-107">The relative distinguished name is the name defined by an object's naming attribute.</span></span> <span data-ttu-id="c9c20-108">**ClassSchema** 物件的 **rDnAttID** 屬性會識別類別實例的命名屬性。</span><span class="sxs-lookup"><span data-stu-id="c9c20-108">The **rDnAttID** attribute of a **classSchema** object identifies the naming attribute for instances of the class.</span></span> <span data-ttu-id="c9c20-109">大部分的物件類別都會使用 **cn** (一般名稱) 屬性做為命名屬性。</span><span class="sxs-lookup"><span data-stu-id="c9c20-109">Most object classes use the **cn** (Common-Name) attribute as the naming attribute.</span></span> <span data-ttu-id="c9c20-110">物件的相對辨別名稱在物件所在的容器中必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="c9c20-110">An object's relative distinguished name must be unique in the container where the object resides.</span></span> <span data-ttu-id="c9c20-111">您可以有多個具有相同相對分辨名稱的物件實例，但在相同的容器中不能有兩個。</span><span class="sxs-lookup"><span data-stu-id="c9c20-111">There can be many object instances with the same relative distinguished name, but no two can be in same container.</span></span> <span data-ttu-id="c9c20-112">如需 **rDnAttID** 屬性和 **classSchema** 物件的詳細資訊，請參閱 [物件類別的特性](characteristics-of-object-classes.md)。</span><span class="sxs-lookup"><span data-stu-id="c9c20-112">For more information about the **rDnAttID** attribute and **classSchema** objects, see [Characteristics of Object Classes](characteristics-of-object-classes.md).</span></span>

## <a name="distinguished-name"></a><span data-ttu-id="c9c20-113">辨別名稱</span><span class="sxs-lookup"><span data-stu-id="c9c20-113">Distinguished Name</span></span>

<span data-ttu-id="c9c20-114">[*辨別名稱*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85))是物件的目前名稱，並且包含在物件的 **distinguishedName** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="c9c20-114">The [*distinguished name*](/previous-versions/windows/desktop/legacy/ms681901(v=vs.85)) is the current name of the object and is contained in the **distinguishedName** attribute of the object.</span></span> <span data-ttu-id="c9c20-115">辨別名稱是一個字串，其中包含物件的位置，而是藉由將物件的相對辨別名稱和每個祖系串連至根目錄來形成。</span><span class="sxs-lookup"><span data-stu-id="c9c20-115">The distinguished name is a string that includes the location of the object and is formed by concatenating the relative distinguished name of the object and each of its ancestors all the way to root.</span></span> <span data-ttu-id="c9c20-116">例如，Fabrikam.com 網域中使用者容器的分辨名稱將會是 "CN = Users，DC = Fabrikam，DC = com"。</span><span class="sxs-lookup"><span data-stu-id="c9c20-116">For example, the distinguished name of the Users container in the Fabrikam.com domain would be "CN=Users,DC=Fabrikam,DC=com".</span></span> <span data-ttu-id="c9c20-117">辨別名稱在樹系中是唯一的。</span><span class="sxs-lookup"><span data-stu-id="c9c20-117">Distinguished names are unique within a forest.</span></span> <span data-ttu-id="c9c20-118">移動或重新命名物件時，物件的辨別名稱會變更。</span><span class="sxs-lookup"><span data-stu-id="c9c20-118">An object's distinguished name changes when the object is moved or renamed.</span></span>

## <a name="object-guid"></a><span data-ttu-id="c9c20-119">物件 GUID</span><span class="sxs-lookup"><span data-stu-id="c9c20-119">Object GUID</span></span>

<span data-ttu-id="c9c20-120">物件 GUID 是物件實例建立時，由 Active Directory Domain Services 指派的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="c9c20-120">The object GUID is a globally unique identifier assigned by Active Directory Domain Services when the object instance is created.</span></span> <span data-ttu-id="c9c20-121">物件 GUID 包含在物件的 **objectGUID** 屬性中。</span><span class="sxs-lookup"><span data-stu-id="c9c20-121">The object GUID is contained in the **objectGUID** attribute of the object.</span></span> <span data-ttu-id="c9c20-122">GUID 是在空間和時間中保證是唯一的128位數位。</span><span class="sxs-lookup"><span data-stu-id="c9c20-122">A GUID is a 128-bit number guaranteed to be unique in space and time.</span></span> <span data-ttu-id="c9c20-123">物件 Guid 永遠不會變更，因此，如果物件已重新命名或移至企業樹系中的任何位置，物件 GUID 會維持不變。</span><span class="sxs-lookup"><span data-stu-id="c9c20-123">Object GUIDs never change, so if an object is renamed or moved anywhere in the enterprise forest, the object GUID remains the same.</span></span> <span data-ttu-id="c9c20-124">在 Active Directory Domain Services 中儲存物件參考的應用程式必須使用物件 GUID，以確保物件參考在物件重新命名後仍然存在。</span><span class="sxs-lookup"><span data-stu-id="c9c20-124">Applications that save references to objects in Active Directory Domain Services must use the object GUID to ensure that the object reference will survive a rename of the object.</span></span> <span data-ttu-id="c9c20-125">物件的分辨名稱可能會變更，但物件 GUID 則不會變更。</span><span class="sxs-lookup"><span data-stu-id="c9c20-125">The distinguished name for an object might change, but the object GUID will not.</span></span>

## <a name="other-identities"></a><span data-ttu-id="c9c20-126">其他身分識別</span><span class="sxs-lookup"><span data-stu-id="c9c20-126">Other Identities</span></span>

<span data-ttu-id="c9c20-127">物件實例可以有許多其他屬性，而這些屬性可用於應用程式的識別。</span><span class="sxs-lookup"><span data-stu-id="c9c20-127">Object instances can have many other attributes, and the attributes can be used for identification by applications.</span></span> <span data-ttu-id="c9c20-128">例如， **使用者**、 **電腦** 和 **群組** 物件類別 (實例的安全性主體物件) 有 **userPrincipalName**、 **sAMAccountName** 和 **objectSid** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c9c20-128">For example, security principal objects (instances of the **user**, **computer**, and **group** object classes) have **userPrincipalName**, **sAMAccountName**, and **objectSid** attributes.</span></span> <span data-ttu-id="c9c20-129">這些屬性對於 Windows 2000 而言是很重要的「名稱」，但是這些屬性不是來自目錄觀點的物件身分識別的一部分。</span><span class="sxs-lookup"><span data-stu-id="c9c20-129">These attributes are very important "names" for Windows 2000, but these are not part of the object identity from the directory's perspective.</span></span>

 

 