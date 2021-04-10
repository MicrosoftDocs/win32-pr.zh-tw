---
title: 存取控制和物件建立
description: 如果呼叫端沒有 ADS \_ RIGHT \_ DS 在 \_ \_ 父容器上為該物件類型建立子系，Active Directory 伺服器將無法建立子物件。
ms.assetid: 52f56e2a-580c-44b5-ba97-21388f6258bc
ms.tgt_platform: multiple
keywords:
- 存取控制和物件建立廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 71ac54c1fe71a1821d3a02db383ca95606ae360d
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104092611"
---
# <a name="access-control-and-object-creation"></a><span data-ttu-id="c4ceb-104">存取控制和物件建立</span><span class="sxs-lookup"><span data-stu-id="c4ceb-104">Access Control and Object Creation</span></span>

<span data-ttu-id="c4ceb-105">如果呼叫端沒有 ADS RIGHT DS 在父容器上為該物件類型 **\_ \_ \_ 建立 \_ 子** 系，Active Directory 伺服器將無法建立子物件。</span><span class="sxs-lookup"><span data-stu-id="c4ceb-105">The Active Directory server will fail to create a child object if the caller does not have the **ADS\_RIGHT\_DS\_CREATE\_CHILD** for that object type on the parent container.</span></span> <span data-ttu-id="c4ceb-106">若要判斷呼叫者可以在目錄物件中建立的子物件類型，請讀取物件的 **allowedChildClassesEffective** 屬性。</span><span class="sxs-lookup"><span data-stu-id="c4ceb-106">To determine the types of child objects that the caller can create in a directory object, read the object's **allowedChildClassesEffective** attribute.</span></span>

<span data-ttu-id="c4ceb-107">當您使用 [**IADsContainer：： create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) 方法來建立子物件時，除非在新的物件上呼叫 [**IADs：： SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) ，否則物件不會成為持續性。</span><span class="sxs-lookup"><span data-stu-id="c4ceb-107">When you use the [**IADsContainer::Create**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) method to create a child object, the object is not made persistent until [**IADs::SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) is called on the new object.</span></span> <span data-ttu-id="c4ceb-108">在 **Create** 和 **SetInfo** 呼叫之間，建立執行緒可以將值放入任何新物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="c4ceb-108">Between the **Create** and **SetInfo** calls, the creating thread can put values into any of the new object's properties.</span></span> <span data-ttu-id="c4ceb-109">在 **SetInfo** 呼叫之後，建立執行緒不一定具有存取權來設定新物件的屬性。</span><span class="sxs-lookup"><span data-stu-id="c4ceb-109">After the **SetInfo** call, the creating thread does not necessarily have the access rights to set the new object's properties.</span></span> <span data-ttu-id="c4ceb-110">若要確保呼叫端具有這些許可權，請在建立期間指定明確的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="c4ceb-110">To ensure that the caller has these rights, specify an explicit security descriptor during creation.</span></span> <span data-ttu-id="c4ceb-111">DACL 應該有一個 ACE，讓呼叫端具有物件的必要存取權限。</span><span class="sxs-lookup"><span data-stu-id="c4ceb-111">The DACL should have an ACE that gives the caller the necessary access rights on the object.</span></span>

<span data-ttu-id="c4ceb-112">如需存取控制和建立物件的詳細資訊，請參閱 [如何在新的目錄物件上設定安全描述項](how-security-descriptors-are-set-on-new-directory-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="c4ceb-112">For more information about access control and object creation, see [How Security Descriptors are Set on New Directory Objects](how-security-descriptors-are-set-on-new-directory-objects.md).</span></span>

 

 