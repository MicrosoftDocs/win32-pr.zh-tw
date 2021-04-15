---
title: 將許可權設定為特定物件類型的特定屬性
description: 屬性特定的許可權可以與物件特定繼承搭配使用，以提供功能強大且詳細的管理委派。
ms.assetid: d2ebbe3a-78f7-4bb5-bac0-13236031b7b1
ms.tgt_platform: multiple
keywords:
- 將許可權設定為特定物件類型的特定屬性（AD）
- Active Directory，使用，安全性，設定特定屬性的許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 79bfa24b574639e64fbb17c33fabee1185cc014c
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104462816"
---
# <a name="setting-rights-to-specific-properties-of-specific-types-of-objects"></a><span data-ttu-id="4bf3f-105">將許可權設定為特定物件類型的特定屬性</span><span class="sxs-lookup"><span data-stu-id="4bf3f-105">Setting Rights to Specific Properties of Specific Types of Objects</span></span>

<span data-ttu-id="4bf3f-106">屬性特定的許可權可以與物件特定繼承搭配使用，以提供功能強大且詳細的管理委派。</span><span class="sxs-lookup"><span data-stu-id="4bf3f-106">Property-specific permissions can be used in combination with object specific inheritance to provide the powerful and detailed delegation of administration.</span></span> <span data-ttu-id="4bf3f-107">您可以設定屬性特定的物件-可繼承的 ACE，以允許指定的使用者或群組在容器中的特定子物件類別上讀取和/或寫入特定屬性。</span><span class="sxs-lookup"><span data-stu-id="4bf3f-107">You can set a property-specific object-inheritable ACE to allow a specified user or group to read and/or write a specific attribute on a specified class of child objects in a container.</span></span> <span data-ttu-id="4bf3f-108">例如，您可以在組織單位上設定 ACE (OU) ，讓群組能夠讀取和寫入 OU 中所有使用者物件的電話號碼屬性。</span><span class="sxs-lookup"><span data-stu-id="4bf3f-108">For example, you can set an ACE on an organizational unit (OU) to enable a group to read and write the telephone number attribute of all user objects in the OU.</span></span>

<span data-ttu-id="4bf3f-109">**設定屬性特定物件-可繼承的 Ace**</span><span class="sxs-lookup"><span data-stu-id="4bf3f-109">**To set property-specific object-inheritable ACEs**</span></span>

1.  <span data-ttu-id="4bf3f-110">將 [**IADsAccessControlEntry AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 設定為 **ADS \_ AceType \_ 存取 \_ 允許的 \_ 物件** 或 **ads \_ AceType \_ \_ 拒絕存取 \_ 物件**。</span><span class="sxs-lookup"><span data-stu-id="4bf3f-110">Set [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
2.  <span data-ttu-id="4bf3f-111">將 [**IADsAccessControlEntry**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 設定為屬性的 **schemaIDGUID** 。</span><span class="sxs-lookup"><span data-stu-id="4bf3f-111">Set [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to the **schemaIDGUID** of the attribute.</span></span> <span data-ttu-id="4bf3f-112">例如， **telephoneNumber** 屬性的 **schemaIDGUID** 是 {bf967a49-0de6-11d0-a285-00aa003049e2}。</span><span class="sxs-lookup"><span data-stu-id="4bf3f-112">For example, the **schemaIDGUID** of the **telephoneNumber** attribute is {bf967a49-0de6-11d0-a285-00aa003049e2}.</span></span>
3.  <span data-ttu-id="4bf3f-113">將 [**IADsAccessControlEntry AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 設定為 **ADS \_ ACEFLAG \_ INHERIT \_ ACE**。</span><span class="sxs-lookup"><span data-stu-id="4bf3f-113">Set [**IADsAccessControlEntry.AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_ACEFLAG\_INHERIT\_ACE**.</span></span>
4.  <span data-ttu-id="4bf3f-114">將 [**IADsAccessControlEntry. InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 設定為可繼承 ACE 之物件類別的 **schemaIDGUID** 。</span><span class="sxs-lookup"><span data-stu-id="4bf3f-114">Set [**IADsAccessControlEntry.InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to the **schemaIDGUID** of the object class that can inherit the ACE.</span></span> <span data-ttu-id="4bf3f-115">例如，**使用者** 類別的 **schemaIDGUID** 是 {bf967aba-0de6-11d0-a285-00aa003049e2}。</span><span class="sxs-lookup"><span data-stu-id="4bf3f-115">For example, the **schemaIDGUID** of the **user** class is {bf967aba-0de6-11d0-a285-00aa003049e2}.</span></span>
5.  <span data-ttu-id="4bf3f-116">將 [**IADsAccessControlEntry**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 設定為 **ads \_ 旗標 \_ 物件 \_ 類型 \_ 存在** ， **廣告 \_ 旗標繼承的 \_ \_ 物件 \_ 類型 \_ 存在**。</span><span class="sxs-lookup"><span data-stu-id="4bf3f-116">Set [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_FLAG\_OBJECT\_TYPE\_PRESENT** and **ADS\_FLAG\_INHERITED\_OBJECT\_TYPE\_PRESENT**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="4bf3f-117">Set ADS \_ ACEFLAG \_ INHERIT \_ ACE，使 ace 成為繼承的。</span><span class="sxs-lookup"><span data-stu-id="4bf3f-117">Set ADS\_ACEFLAG\_INHERIT\_ACE to cause the ACE to be inherited.</span></span> <span data-ttu-id="4bf3f-118">此外， \_ \_ \_ \_ 如果套用此 ace 的物件類型不符合指定 ace 之容器的物件類型，則設定 ADS ACEFLAG 只會繼承 ace。</span><span class="sxs-lookup"><span data-stu-id="4bf3f-118">In addition, set ADS\_ACEFLAG\_INHERIT\_ONLY\_ACE if the object type this ACE applies to does not match the object type of the container where the ACE is specified.</span></span> <span data-ttu-id="4bf3f-119">如果未這麼做，ACE 也會在容器上生效，而且可以授與非預期的許可權。</span><span class="sxs-lookup"><span data-stu-id="4bf3f-119">If this is not done, the ACE will also become effective on the container and can grant unexpected rights.</span></span>

 

<span data-ttu-id="4bf3f-120">如需可用來設定這類 ACE 的詳細資訊和程式碼範例，請參閱 [在目錄物件上設定 ACE 的範例程式碼](example-code-for-setting-an-ace-on-a-directory-object.md)。</span><span class="sxs-lookup"><span data-stu-id="4bf3f-120">For more information and code examples that can be used to set this kind of ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 