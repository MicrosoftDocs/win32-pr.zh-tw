---
title: 設定子物件作業的許可權
description: 您也可以針對特定類別的所有子系或子系上的作業，授與或拒絕許可權，例如「建立子系」和「刪除子系」。
ms.assetid: fe2f8939-7562-4c03-a7a9-3ac5fc3e81bb
ms.tgt_platform: multiple
keywords:
- 設定子物件作業的許可權 AD
- 物件 AD、子系、設定子物件作業的許可權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d407e9b0db865c5df8d5dab53bd97f9f1afa1497
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104092621"
---
# <a name="setting-permissions-on-child-object-operations"></a><span data-ttu-id="d0434-105">設定子物件作業的許可權</span><span class="sxs-lookup"><span data-stu-id="d0434-105">Setting Permissions on Child Object Operations</span></span>

<span data-ttu-id="d0434-106">您也可以針對特定類別的所有子系或子系上的作業，授與或拒絕許可權，例如「建立子系」和「刪除子系」。</span><span class="sxs-lookup"><span data-stu-id="d0434-106">Permissions, such as Create Child and Delete Child, can also be granted or denied for operations on all subobjects or subobjects of a specific class.</span></span>

<span data-ttu-id="d0434-107">下列程式可以用來設定特定子物件類型的許可權。</span><span class="sxs-lookup"><span data-stu-id="d0434-107">The following procedure can be used to set permissions for a specific subobject type.</span></span>

<span data-ttu-id="d0434-108">**若要設定特定子物件類型的許可權**</span><span class="sxs-lookup"><span data-stu-id="d0434-108">**To set permissions for a specific subobject type**</span></span>

1.  <span data-ttu-id="d0434-109">將 [**IADsAccessControlEntry AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) 屬性設定為 **ADS \_ AceType \_ 存取允許的 \_ \_ 物件** 或 **ads \_ AceType \_ 拒絕存取 \_ \_ 物件**。</span><span class="sxs-lookup"><span data-stu-id="d0434-109">Set the [**IADsAccessControlEntry.AceType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_ACETYPE\_ACCESS\_ALLOWED\_OBJECT** or **ADS\_ACETYPE\_ACCESS\_DENIED\_OBJECT**.</span></span>
2.  <span data-ttu-id="d0434-110">將 [ [**IADsAccessControlEntry**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) ] 屬性設定為物件類別的 GUID。</span><span class="sxs-lookup"><span data-stu-id="d0434-110">Set the [**IADsAccessControlEntry.ObjectType**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to the GUID for object class.</span></span> <span data-ttu-id="d0434-111">這是定義物件類別之 classSchema 物件的 **schemaIDGUID** 屬性。</span><span class="sxs-lookup"><span data-stu-id="d0434-111">This is the **schemaIDGUID** property of the classSchema object that defines the object class.</span></span> <span data-ttu-id="d0434-112">如果 **ObjectType** 屬性為 **Null**，ACE 會套用至任何類別的子物件。</span><span class="sxs-lookup"><span data-stu-id="d0434-112">If the **ObjectType** property is **NULL**, the ACE applies to subobjects of any class.</span></span>
3.  <span data-ttu-id="d0434-113">將 [ [**IADsAccessControlEntry**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) ] 屬性設定為 [ **ADS \_ 旗標 \_ 物件 \_ 類型 \_**]。</span><span class="sxs-lookup"><span data-stu-id="d0434-113">Set the [**IADsAccessControlEntry.Flags**](/windows/desktop/ADSI/iadsaccesscontrolentry-property-methods) property to **ADS\_FLAG\_OBJECT\_TYPE\_PRESENT**.</span></span>

<span data-ttu-id="d0434-114">如需建立 ACE 的詳細資訊和程式，請參閱 [設定物件的存取權限](setting-access-rights-on-an-object.md)。</span><span class="sxs-lookup"><span data-stu-id="d0434-114">For more information and a procedure for creating an ACE, see [Setting Access Rights on an Object](setting-access-rights-on-an-object.md).</span></span>

<span data-ttu-id="d0434-115">如需可用於設定可控制子物件作業之 ACE 的詳細資訊和程式碼範例，請參閱 [在目錄物件上設定 ace 的範例程式碼](example-code-for-setting-an-ace-on-a-directory-object.md)。</span><span class="sxs-lookup"><span data-stu-id="d0434-115">For more information and a code example that can be used to set an ACE that controls child object operations, see [Example Code for Setting an ACE on a Directory Object](example-code-for-setting-an-ace-on-a-directory-object.md).</span></span>

 

 