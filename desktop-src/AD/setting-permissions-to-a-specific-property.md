---
title: 設定特定屬性的許可權
description: 許可權可以設定為套用至物件的特定屬性。
ms.assetid: 7bafba5a-a437-4777-98a0-f478b738a8ca
ms.tgt_platform: multiple
keywords:
- 設定特定屬性 AD 的許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99dbfc3dc682103166b41957a3f52206d84fe671
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023215"
---
# <a name="setting-permissions-to-a-specific-property"></a><span data-ttu-id="09132-104">設定特定屬性的許可權</span><span class="sxs-lookup"><span data-stu-id="09132-104">Setting Permissions to a Specific Property</span></span>

<span data-ttu-id="09132-105">許可權可以設定為套用至物件的特定屬性。</span><span class="sxs-lookup"><span data-stu-id="09132-105">Permissions can be set to apply to a specific property of an object.</span></span>

<span data-ttu-id="09132-106">**若要設定套用至物件之特定屬性的許可權**</span><span class="sxs-lookup"><span data-stu-id="09132-106">**To set permissions that apply to a specific property of an object**</span></span>

1.  <span data-ttu-id="09132-107">將 [**IADsAccessControlEntry. AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 屬性設定為 **ads \_ right \_ ds \_ 讀取 \_** 屬性和/或 **ads \_ right \_ ds \_ 寫入 \_** 屬性。</span><span class="sxs-lookup"><span data-stu-id="09132-107">Set the [**IADsAccessControlEntry.AccessMask**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_RIGHT\_DS\_READ\_PROP** and/or **ADS\_RIGHT\_DS\_WRITE\_PROP**.</span></span>
2.  <span data-ttu-id="09132-108">將 [**IADsAccessControlEntry AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 屬性設定為 **ADS \_ AceType \_ 存取允許的 \_ \_ 物件** 或 **ads \_ AceType \_ 拒絕存取 \_ \_ 物件**。</span><span class="sxs-lookup"><span data-stu-id="09132-108">Set the [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
3.  <span data-ttu-id="09132-109">將 [ [**IADsAccessControlEntry**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) ] 屬性設定為屬性的 **schemaIDGUID** 。</span><span class="sxs-lookup"><span data-stu-id="09132-109">Set the [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to the **schemaIDGUID** of the property.</span></span> <span data-ttu-id="09132-110">這是在架構中定義屬性之 **attributeSchema** 物件的 **schemaIDGUID** 。</span><span class="sxs-lookup"><span data-stu-id="09132-110">This is the **schemaIDGUID** of the **attributeSchema** object that defines the property in the schema.</span></span> <span data-ttu-id="09132-111">GUID 必須指定為 COM 程式庫中 [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) 函式所產生的格式字串。</span><span class="sxs-lookup"><span data-stu-id="09132-111">The GUID must be specified as a string of the form produced by the [**StringFromGUID2**](/windows/win32/api/combaseapi/nf-combaseapi-stringfromguid2) function in the COM library.</span></span>
4.  <span data-ttu-id="09132-112">將 [**IADsAccessControlEntry**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 設定為 **ADS \_ 旗標 \_ 物件 \_ 類型 \_**。</span><span class="sxs-lookup"><span data-stu-id="09132-112">Set [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) to **ADS\_FLAG\_OBJECT\_TYPE\_PRESENT**.</span></span>

<span data-ttu-id="09132-113">如需預先定義之屬性 **schemaIDGUID** 的詳細資訊，請參閱 [Active Directory Domain Services 參考](active-directory-domain-services-reference.md)。</span><span class="sxs-lookup"><span data-stu-id="09132-113">For more information about the **schemaIDGUID** of a predefined attribute, see [Active Directory Domain Services Reference](active-directory-domain-services-reference.md).</span></span>

<span data-ttu-id="09132-114">如需可用來取出 schemaIDGUID 的詳細資訊和程式碼範例，請參閱 [讀取 attributeSchema 和 ClassSchema 物件](reading-attributeschema-and-classschema-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="09132-114">For more information and a code example that can be used to retrieve a schemaIDGUID, see [Reading attributeSchema and classSchema Objects](reading-attributeschema-and-classschema-objects.md).</span></span>

<span data-ttu-id="09132-115">如需有關如何建立 ACE 的詳細資訊，請參閱 [設定物件的存取權限](setting-access-rights-on-an-object.md)。</span><span class="sxs-lookup"><span data-stu-id="09132-115">For more information about how to create an ACE, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="09132-116">如需可用來設定屬性特定 ACE 的詳細資訊和程式碼範例，請參閱 [在目錄物件上設定 ACE 的範例程式碼](example-code-for-setting-an-ace-on-a-directory-object.md)。</span><span class="sxs-lookup"><span data-stu-id="09132-116">For more information and a code example that can be used to set a property-specific ACE, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 