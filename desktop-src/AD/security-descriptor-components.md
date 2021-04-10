---
title: 安全描述項元件
description: 使用 IADs 取得方法來取出 IADsSecurityDescriptor 介面指標，您可以使用 IADsSecurityDescriptor 屬性來讀取或寫入目錄物件之安全描述項的元件。
ms.assetid: 35d3d16b-d7fc-4967-ba5c-5a77e058a9ae
ms.tgt_platform: multiple
keywords:
- 安全性描述項元件廣告
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ef87b0e23f60fdbb4d0b03b421012d5918ed3c83
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681638"
---
# <a name="security-descriptor-components"></a><span data-ttu-id="e2681-104">安全描述項元件</span><span class="sxs-lookup"><span data-stu-id="e2681-104">Security Descriptor Components</span></span>

<span data-ttu-id="e2681-105">使用 [**IADs 取得**](/windows/desktop/api/iads/nf-iads-iads-get) 方法來取出 [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) 介面指標，您可以使用 **IADsSecurityDescriptor** 屬性來讀取或寫入目錄物件之安全描述項的元件。</span><span class="sxs-lookup"><span data-stu-id="e2681-105">Having used the [**IADs.Get**](/windows/desktop/api/iads/nf-iads-iads-get) method to retrieve an [**IADsSecurityDescriptor**](/windows/desktop/api/iads/nn-iads-iadssecuritydescriptor) interface pointer, you can use the **IADsSecurityDescriptor** properties to read or write the components of a directory object's security descriptor.</span></span> <span data-ttu-id="e2681-106">例如，若要取得或設定物件的 DACL，請使用 [**objdescriptor.discretionaryacl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) 屬性。</span><span class="sxs-lookup"><span data-stu-id="e2681-106">For example, to get or set the object's DACL, use the [**DiscretionaryAcl**](/windows/desktop/ADSI/iadssecuritydescriptor-property-methods) property.</span></span>

<span data-ttu-id="e2681-107">安全描述項可以儲存下列資料：</span><span class="sxs-lookup"><span data-stu-id="e2681-107">A security descriptor can store the following data:</span></span>

-   <span data-ttu-id="e2681-108">識別物件擁有者的安全識別碼 (SID) ：物件的擁有者具有在物件的安全描述項中修改 DACL 和擁有者資料的隱含許可權。</span><span class="sxs-lookup"><span data-stu-id="e2681-108">A security identifier (SID) that identifies the owner of the object: The owner of an object has the implicit right to modify the DACL and owner data in the object's security descriptor.</span></span>
-   <span data-ttu-id="e2681-109"> (DACL) 的任意存取控制清單，識別可對物件執行各種作業的使用者和群組： DACL 包含存取控制專案清單 (Ace) 。</span><span class="sxs-lookup"><span data-stu-id="e2681-109">A discretionary access-control list (DACL) that identifies the users and groups who can perform various operations on the object: A DACL contains a list of access-control entries (ACEs).</span></span> <span data-ttu-id="e2681-110">每個 ACE 都允許或拒絕指定之使用者帳戶、群組帳戶或其他受信任者的指定存取權限集。</span><span class="sxs-lookup"><span data-stu-id="e2681-110">Each ACE allows or denies a specified set of access rights to a specified user account, group account, or other trustee.</span></span> <span data-ttu-id="e2681-111">如需詳細資訊，請參閱 [取出物件的 DACL](retrieving-an-objectampaposs-dacl.md)。</span><span class="sxs-lookup"><span data-stu-id="e2681-111">For more information, see [Retrieving an Object's DACL](retrieving-an-objectampaposs-dacl.md).</span></span>
-   <span data-ttu-id="e2681-112">系統存取控制清單 (SACL) ，可控制系統如何嘗試存取物件： SACL 中的每個 ACE 都會指定針對指定的使用者帳戶、群組帳戶或其他信任者產生審核記錄專案的存取嘗試類型。</span><span class="sxs-lookup"><span data-stu-id="e2681-112">A system access-control list (SACL) that controls how the system audits attempts to access the object: Each ACE in a SACL specifies the types of access attempts that generate an audit log entry for a specified user account, group account, or other trustee.</span></span> <span data-ttu-id="e2681-113">如需詳細資訊，請參閱 [取出物件的 SACL](retrieving-an-objectampaposs-sacl.md)。</span><span class="sxs-lookup"><span data-stu-id="e2681-113">For more information, see [Retrieving an Object's SACL](retrieving-an-objectampaposs-sacl.md).</span></span>
-   <span data-ttu-id="e2681-114">一組 **安全性 \_ 描述項 \_ 控制** 旗標，可限定安全描述項或其元件的意義：例如， **SE \_ DACL \_ PROTECTED** 旗標會保護安全描述項的 DACL，使其無法繼承其父物件的 ace。</span><span class="sxs-lookup"><span data-stu-id="e2681-114">A set of **SECURITY\_DESCRIPTOR\_CONTROL** control flags that qualify the meaning of a security descriptor or its components: For example, the **SE\_DACL\_PROTECTED** flag protects the security descriptor's DACL from inheriting ACEs from its parent object.</span></span>
-   <span data-ttu-id="e2681-115">識別物件主要群組 (SID) 的安全識別碼： Active Directory Domain Services 不使用此元件。</span><span class="sxs-lookup"><span data-stu-id="e2681-115">A security identifier (SID) that identifies the primary group of the object: Active Directory Domain Services do not use this component.</span></span>

<span data-ttu-id="e2681-116">如需可用來讀取和顯示物件安全描述項和 DACL 中資料的詳細資訊和程式碼範例，請參閱 [讀取物件的安全描述項](reading-an-objectampaposs-security-descriptor.md)。</span><span class="sxs-lookup"><span data-stu-id="e2681-116">For more information and a code example that can be used to read and display the data in an object security descriptor and DACL, see [Reading an Object's Security Descriptor](reading-an-objectampaposs-security-descriptor.md).</span></span>

 

 