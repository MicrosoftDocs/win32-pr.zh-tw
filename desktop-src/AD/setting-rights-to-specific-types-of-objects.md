---
title: 設定特定物件類型的許可權
description: 下列程式顯示如何設定只能由特定物件類別繼承的 ACE。
ms.assetid: 42712458-69c7-4fe1-bfb3-b3fb28092a56
ms.tgt_platform: multiple
keywords:
- 將許可權設定為物件的類型
- 物件 AD，將許可權設定為
- Active Directory，使用，安全性，將許可權設定為物件的類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e6f44cfbe753e6f92787f8269eab1f4eab4c2e98
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103933042"
---
# <a name="setting-rights-to-specific-types-of-objects"></a><span data-ttu-id="0f104-106">設定特定物件類型的許可權</span><span class="sxs-lookup"><span data-stu-id="0f104-106">Setting Rights to Specific Types of Objects</span></span>

<span data-ttu-id="0f104-107">下列程式顯示如何設定只能由特定物件類別繼承的 ACE。</span><span class="sxs-lookup"><span data-stu-id="0f104-107">The following procedure shows how to set an ACE that can be inherited only by a specific class of objects.</span></span>

 <span data-ttu-id="0f104-108">**設定只能由特定物件類別繼承的 ACE**</span><span class="sxs-lookup"><span data-stu-id="0f104-108">**To set an ACE that can be inherited only by a specific class of objects**</span></span>

1.  <span data-ttu-id="0f104-109">將 [**IADsAccessControlEntry AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 屬性設定為 **ADS \_ AceType \_ 存取允許的 \_ \_ 物件** 或 **ads \_ AceType \_ 拒絕存取 \_ \_ 物件**。</span><span class="sxs-lookup"><span data-stu-id="0f104-109">Set the [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
2.  <span data-ttu-id="0f104-110">將 [**IADsAccessControlEntry AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 屬性設定為包含 ADS \_ ACEFLAG \_ INHERIT \_ ACE 旗標。</span><span class="sxs-lookup"><span data-stu-id="0f104-110">Set the [**IADsAccessControlEntry.AceFlags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to include the ADS\_ACEFLAG\_INHERIT\_ACE flag.</span></span>
3.  <span data-ttu-id="0f104-111">將 [**IADsAccessControlEntry. InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 屬性設定為可以繼承 ACE 之物件類別的 **schemaIDGUID** 。</span><span class="sxs-lookup"><span data-stu-id="0f104-111">Set the [**IADsAccessControlEntry.InheritedObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to the **schemaIDGUID** of the object class that can inherit the ACE.</span></span>
4.  <span data-ttu-id="0f104-112">將 [ [**IADsAccessControlEntry**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) ] 屬性設定為 [ **ADS \_ 旗標繼承的 \_ 物件 \_ 類型 \_**]。</span><span class="sxs-lookup"><span data-stu-id="0f104-112">Set the [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_FLAG\_INHERITED OBJECT\_TYPE\_PRESENT**.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="0f104-113">Set **ADS \_ ACEFLAG \_ INHERIT \_ ace** ，使 ace 成為繼承的。</span><span class="sxs-lookup"><span data-stu-id="0f104-113">Set **ADS\_ACEFLAG\_INHERIT\_ACE** to cause the ACE to be inherited.</span></span> <span data-ttu-id="0f104-114">此外，如果套用此 ACE 的物件類型不符合指定 ACE 之容器的物件類型，則您必須設定 **ADS \_ ACEFLAG \_ \_ 僅繼承 \_ ace** 。</span><span class="sxs-lookup"><span data-stu-id="0f104-114">In addition, you must set **ADS\_ACEFLAG\_INHERIT\_ONLY\_ACE** if the object type this ACE applies to does not match the object type of the container where the ACE is specified.</span></span> <span data-ttu-id="0f104-115">如果未這麼做，ACE 也會在容器上生效，而且可以授與非預期的許可權。</span><span class="sxs-lookup"><span data-stu-id="0f104-115">If this is not done, the ACE will also become effective on the container and can grant unintended rights.</span></span>

 

<span data-ttu-id="0f104-116">如需可用來設定這類 ACE 的詳細資訊和程式碼範例，請參閱 [在目錄物件上設定 ACE 的範例程式碼](example-code-for-setting-an-ace-on-a-directory-object.md)。</span><span class="sxs-lookup"><span data-stu-id="0f104-116">For more information and code examples that can be used to set this type of ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 