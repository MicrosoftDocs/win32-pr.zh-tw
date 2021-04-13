---
description: WMI 具有可讓您讀取和操作安全描述項的物件和方法，以決定誰可以存取安全物件。
ms.assetid: ce4b7c9e-2c16-40d4-8839-76e69ddb2d8c
ms.tgt_platform: multiple
title: WMI 安全描述項物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ddc315e955c2d449d0dea0db97684cc352257cd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104568476"
---
# <a name="wmi-security-descriptor-objects"></a><span data-ttu-id="e3137-103">WMI 安全描述項物件</span><span class="sxs-lookup"><span data-stu-id="e3137-103">WMI Security Descriptor Objects</span></span>

<span data-ttu-id="e3137-104">WMI 具有可讓您讀取和操作安全描述項的物件和方法，以決定誰可以存取安全物件。</span><span class="sxs-lookup"><span data-stu-id="e3137-104">WMI has objects and methods that allow you to read and manipulate security descriptors to determine who has access to securable objects.</span></span>

-   [<span data-ttu-id="e3137-105">安全描述項的角色</span><span class="sxs-lookup"><span data-stu-id="e3137-105">The Role of Security Descriptors</span></span>](#the-role-of-security-descriptors)
-   [<span data-ttu-id="e3137-106">存取控制和 WMI 安全性物件</span><span class="sxs-lookup"><span data-stu-id="e3137-106">Access Control and WMI Security Objects</span></span>](#access-control-and-wmi-security-objects)
-   [<span data-ttu-id="e3137-107">Win32 \_ SecurityDescriptor 物件</span><span class="sxs-lookup"><span data-stu-id="e3137-107">Win32\_SecurityDescriptor Object</span></span>](/windows)
-   [<span data-ttu-id="e3137-108">DACL 和 SACL</span><span class="sxs-lookup"><span data-stu-id="e3137-108">DACL and SACL</span></span>](#dacl-and-sacl)
-   [<span data-ttu-id="e3137-109">Win32 \_ ACE，win32 \_ 信任者，win32 \_ SID</span><span class="sxs-lookup"><span data-stu-id="e3137-109">Win32\_ACE, Win32\_Trustee, Win32\_SID</span></span>](/windows)
-   [<span data-ttu-id="e3137-110">範例：檢查誰有印表機的存取權</span><span class="sxs-lookup"><span data-stu-id="e3137-110">Example: Checking Who has Access to Printers</span></span>](#example-checking-who-has-access-to-printers)
-   [<span data-ttu-id="e3137-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="e3137-111">Related topics</span></span>](#related-topics)

## <a name="the-role-of-security-descriptors"></a><span data-ttu-id="e3137-112">安全描述項的角色</span><span class="sxs-lookup"><span data-stu-id="e3137-112">The Role of Security Descriptors</span></span>

<span data-ttu-id="e3137-113">安全描述項會定義安全物件的安全性屬性，例如檔案、登錄機碼、WMI 命名空間、印表機、服務或共用。</span><span class="sxs-lookup"><span data-stu-id="e3137-113">Security descriptors define the security attributes of securable objects such as files, registry keys, WMI namespaces, printers, services, or shares.</span></span> <span data-ttu-id="e3137-114">安全描述項包含物件的擁有者和主要群組的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="e3137-114">A security descriptor contains information about the owner and primary group of an object.</span></span> <span data-ttu-id="e3137-115">提供者可以比較資源安全描述項與提出要求之使用者的身分識別，並判斷使用者是否有許可權存取使用者要求的資源。</span><span class="sxs-lookup"><span data-stu-id="e3137-115">A provider can compare the resource security descriptor to the identity of a requesting user, and determine whether or not the user has the right to access the resource that a user is requesting.</span></span> <span data-ttu-id="e3137-116">如需詳細資訊，請參閱 [存取 WMI 安全物件](access-to-wmi-securable-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="e3137-116">For more information, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span>

<span data-ttu-id="e3137-117">某些 WMI 方法（例如 [**GetSD**](--systemsecurity-getsd.md)）會以二進位位元組陣列格式傳回安全描述項。</span><span class="sxs-lookup"><span data-stu-id="e3137-117">Some WMI methods, such as [**GetSD**](--systemsecurity-getsd.md), return a security descriptor in the binary byte array format.</span></span> <span data-ttu-id="e3137-118">從 Windows Vista 開始，使用 [**win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) 類別的方法，將二進位安全描述項轉換成 [**win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)的實例，這樣可以更輕鬆地操作。</span><span class="sxs-lookup"><span data-stu-id="e3137-118">Starting with Windows Vista, use the methods of the [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class to convert a binary security descriptor to an instance of [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor), which can be manipulated more easily.</span></span> <span data-ttu-id="e3137-119">如需詳細資訊，請參閱 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="e3137-119">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

## <a name="access-control-and-wmi-security-objects"></a><span data-ttu-id="e3137-120">存取控制和 WMI 安全性物件</span><span class="sxs-lookup"><span data-stu-id="e3137-120">Access Control and WMI Security Objects</span></span>

<span data-ttu-id="e3137-121">以下是 WMI 安全性物件的清單：</span><span class="sxs-lookup"><span data-stu-id="e3137-121">The following is a list of WMI security objects:</span></span>

-   [<span data-ttu-id="e3137-122">**Win32 \_ SecurityDescriptor**</span><span class="sxs-lookup"><span data-stu-id="e3137-122">**Win32\_SecurityDescriptor**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)
-   [<span data-ttu-id="e3137-123">**Win32 \_ ACE**</span><span class="sxs-lookup"><span data-stu-id="e3137-123">**Win32\_ACE**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-ace)
-   [<span data-ttu-id="e3137-124">**Win32 \_ 信任者**</span><span class="sxs-lookup"><span data-stu-id="e3137-124">**Win32\_Trustee**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)
-   [<span data-ttu-id="e3137-125">**Win32 \_ SID**</span><span class="sxs-lookup"><span data-stu-id="e3137-125">**Win32\_SID**</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-sid)

<span data-ttu-id="e3137-126">下圖顯示 WMI 安全性物件之間的關聯性。</span><span class="sxs-lookup"><span data-stu-id="e3137-126">The following diagram shows the relationships among WMI security objects.</span></span>

![wmi 安全性物件之間的關聯性](images/security-descriptor.png)

<span data-ttu-id="e3137-128">如需有關存取安全性角色的詳細資訊，請參閱 [安全性最佳作法](/windows/desktop/SecBP/best-practices-for-the-security-apis)、 [維護 WMI 安全性](maintaining-wmi-security.md)和 [存取控制](/windows/desktop/SecAuthZ/access-control)。</span><span class="sxs-lookup"><span data-stu-id="e3137-128">For more information about the role of access security, see [Security Best Practices](/windows/desktop/SecBP/best-practices-for-the-security-apis), [Maintaining WMI Security](maintaining-wmi-security.md), and [Access Control](/windows/desktop/SecAuthZ/access-control).</span></span>

## <a name="win32_securitydescriptor-object"></a><span data-ttu-id="e3137-129">Win32 \_ SecurityDescriptor 物件</span><span class="sxs-lookup"><span data-stu-id="e3137-129">Win32\_SecurityDescriptor Object</span></span>

<span data-ttu-id="e3137-130">下表列出 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) 類別屬性。</span><span class="sxs-lookup"><span data-stu-id="e3137-130">The following table lists the [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor) class properties.</span></span>



| <span data-ttu-id="e3137-131">屬性</span><span class="sxs-lookup"><span data-stu-id="e3137-131">Property</span></span>         | <span data-ttu-id="e3137-132">描述</span><span class="sxs-lookup"><span data-stu-id="e3137-132">Description</span></span>                                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="e3137-133">**ControlFlags**</span><span class="sxs-lookup"><span data-stu-id="e3137-133">**ControlFlags**</span></span> | <span data-ttu-id="e3137-134">限定 SD 或其個別成員意義的控制位集。</span><span class="sxs-lookup"><span data-stu-id="e3137-134">Set of control bits that qualify the meaning of an SD or its individual members.</span></span> <span data-ttu-id="e3137-135">如需設定 **ControlFlags** 位值的詳細資訊，請參閱 [**Win32 \_ SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor)。</span><span class="sxs-lookup"><span data-stu-id="e3137-135">For more information about setting the **ControlFlags** bit values, see [**Win32\_SecurityDescriptor**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptor).</span></span><br/>                                                                                                                                                                      |
| <span data-ttu-id="e3137-136">**Dacl**</span><span class="sxs-lookup"><span data-stu-id="e3137-136">**DACL**</span></span>         | <span data-ttu-id="e3137-137">[任意存取控制清單 (](/windows/desktop/SecAuthZ/access-control-lists) 使用者和群組的 ACL) ，以及其對受保護物件的存取權限。</span><span class="sxs-lookup"><span data-stu-id="e3137-137">[Discretionary Access Control List (ACL)](/windows/desktop/SecAuthZ/access-control-lists) of users and groups, and their access rights to a secured object.</span></span> <span data-ttu-id="e3137-138">這個屬性包含 [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) 實例的陣列，代表 [存取控制專案](/windows/desktop/SecAuthZ/access-control-entries)。</span><span class="sxs-lookup"><span data-stu-id="e3137-138">This property contains an array of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) instances that represent [Access Control Entries](/windows/desktop/SecAuthZ/access-control-entries).</span></span> <span data-ttu-id="e3137-139">如需詳細資訊，請參閱 [建立 DACL](/windows/desktop/SecBP/best-practices-for-the-security-apis)。</span><span class="sxs-lookup"><span data-stu-id="e3137-139">For more information, see [Creating a DACL](/windows/desktop/SecBP/best-practices-for-the-security-apis).</span></span><br/> |
| <span data-ttu-id="e3137-140">**群組**</span><span class="sxs-lookup"><span data-stu-id="e3137-140">**Group**</span></span>        | <span data-ttu-id="e3137-141">此受保護物件所屬的群組。</span><span class="sxs-lookup"><span data-stu-id="e3137-141">Group to which this secured object belongs.</span></span> <span data-ttu-id="e3137-142">這個屬性包含 [**Win32 \_ 信任者**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) 的實例，其中包含擁有者所屬群組的名稱、網域及安全識別碼 (SID) 。</span><span class="sxs-lookup"><span data-stu-id="e3137-142">This property contains an instance of [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) that contains the name, domain, and security identifier (SID) of the group to which the owner belongs.</span></span><br/>                                                                                                                                                             |
| <span data-ttu-id="e3137-143">**擁有者**</span><span class="sxs-lookup"><span data-stu-id="e3137-143">**Owner**</span></span>        | <span data-ttu-id="e3137-144">此受保護物件的擁有者。</span><span class="sxs-lookup"><span data-stu-id="e3137-144">Owner of this secured object.</span></span> <span data-ttu-id="e3137-145">此屬性包含 [Win32 \_ 信任者](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) 的實例，其中包含擁有者 (SID) 的名稱、網域及安全識別碼。</span><span class="sxs-lookup"><span data-stu-id="e3137-145">This property contains an instance of [Win32\_Trustee](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) that contains the name, domain, and security identifier (SID) of the owner.</span></span><br/>                                                                                                                                                                                                          |
| <span data-ttu-id="e3137-146">**SACL**</span><span class="sxs-lookup"><span data-stu-id="e3137-146">**SACL**</span></span>         | <span data-ttu-id="e3137-147">[系統存取控制清單 (ACL)](/windows/desktop/SecAuthZ/access-control-lists) 包含 [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) 實例陣列，代表為使用者或群組產生審核記錄的存取嘗試類型。</span><span class="sxs-lookup"><span data-stu-id="e3137-147">[System Access Control List (ACL)](/windows/desktop/SecAuthZ/access-control-lists) contains an array of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) instances that represent the type of access attempts that generate audit records for users or groups.</span></span> <span data-ttu-id="e3137-148">如需詳細資訊，請參閱 [SACL 的新物件](/windows/desktop/SecAuthZ/sacl-for-a-new-object)。</span><span class="sxs-lookup"><span data-stu-id="e3137-148">For more information, see [SACL for a New Object](/windows/desktop/SecAuthZ/sacl-for-a-new-object).</span></span><br/>                                                                        |



 

## <a name="dacl-and-sacl"></a><span data-ttu-id="e3137-149">DACL 和 SACL</span><span class="sxs-lookup"><span data-stu-id="e3137-149">DACL and SACL</span></span>

<span data-ttu-id="e3137-150">任意存取控制清單中的 [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) 物件陣列 (DACL) 和系統存取控制清單 {SACL) 建立使用者或群組之間的連結，以及其存取權限。</span><span class="sxs-lookup"><span data-stu-id="e3137-150">The arrays of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) objects in the discretionary access control list (DACL) and system access control list {SACL) create a link between a user or group and their access rights.</span></span>

<span data-ttu-id="e3137-151">當 DACL 屬性未包含 (ACE) 的存取控制專案時，不會授與存取權限，且拒絕存取物件。</span><span class="sxs-lookup"><span data-stu-id="e3137-151">When a DACL property does not contain an access control entry (ACE), access rights are not granted and access to the object is denied.</span></span>

> [!Note]  
> <span data-ttu-id="e3137-152">**Null** DACL 可提供所有人的完整存取權，這是嚴重的安全性風險。</span><span class="sxs-lookup"><span data-stu-id="e3137-152">A **NULL** DACL gives full access to everyone, which is a serious security risk.</span></span> <span data-ttu-id="e3137-153">如需詳細資訊，請參閱 [建立 DACL](/windows/desktop/SecBP/creating-a-dacl)。</span><span class="sxs-lookup"><span data-stu-id="e3137-153">For more information, see [Creating a DACL](/windows/desktop/SecBP/creating-a-dacl).</span></span>

 

## <a name="win32_ace-win32_trustee-win32_sid"></a><span data-ttu-id="e3137-154">Win32 \_ ACE，win32 \_ 信任者，win32 \_ SID</span><span class="sxs-lookup"><span data-stu-id="e3137-154">Win32\_ACE, Win32\_Trustee, Win32\_SID</span></span>

<span data-ttu-id="e3137-155">[**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)物件包含識別使用者或群組的 [**win32 \_ 受信任**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)類別的實例，而 **AccessMask** 屬性則是位元遮罩，可指定使用者或群組可以採取的動作。</span><span class="sxs-lookup"><span data-stu-id="e3137-155">A [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) object contains an instance of the [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) class that identifies a user or group, and an **AccessMask** property that is a bitmask, which specifies the actions that a user or group can take.</span></span> <span data-ttu-id="e3137-156">例如，使用者或群組可能會被授與讀取檔案的許可權，但無法寫入檔案。</span><span class="sxs-lookup"><span data-stu-id="e3137-156">For example, a user or group might be granted the right to read a file but not write to the file.</span></span> <span data-ttu-id="e3137-157">**Win32 \_ ACE** 物件也包含 ACE，指出它是允許或拒絕存取。</span><span class="sxs-lookup"><span data-stu-id="e3137-157">A **Win32\_ACE** object also contains an ACE that indicates whether or not it is an allow or a deny access.</span></span>

> [!Note]  
> <span data-ttu-id="e3137-158">DACL 中的 [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) 順序很重要，因為 dacl 中允許 (ACE) 允許和拒絕存取控制專案。</span><span class="sxs-lookup"><span data-stu-id="e3137-158">The [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) order in a DACL is important because both allow and deny access control entry (ACE) are permitted in a DACL.</span></span> <span data-ttu-id="e3137-159">如需詳細資訊，請參閱 [DACL 中的 Ace 順序](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl)。</span><span class="sxs-lookup"><span data-stu-id="e3137-159">For more information, see [Order of ACEs in a DACL](/windows/desktop/SecAuthZ/order-of-aces-in-a-dacl).</span></span>

 

<span data-ttu-id="e3137-160">由 [**Win32 \_ 信任者**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) 表示的每個使用者帳戶或群組都有安全識別碼 (SID) ，可唯一識別帳戶，並指定帳戶的存取權限。</span><span class="sxs-lookup"><span data-stu-id="e3137-160">Each user account or group represented by a [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) has a security identifier (SID) that uniquely identifies an account, and specifies the access privileges of the account.</span></span> <span data-ttu-id="e3137-161">您指定 SID 資料的方式取決於作業系統。</span><span class="sxs-lookup"><span data-stu-id="e3137-161">How you specify the SID data depends on the operating system.</span></span> <span data-ttu-id="e3137-162">如需詳細資訊，請參閱 [變更安全物件的存取安全性](changing-access-security-on-securable-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="e3137-162">For more information, see [Changing Access Security on Securable Objects](changing-access-security-on-securable-objects.md).</span></span>

<span data-ttu-id="e3137-163">下圖顯示一個 [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) 實例的內容。</span><span class="sxs-lookup"><span data-stu-id="e3137-163">The following diagram shows the contents of one [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace) instance.</span></span>

![一個 win32 \- ace 實例的內容](images/win32-ace.png)

## <a name="example-checking-who-has-access-to-printers"></a><span data-ttu-id="e3137-165">範例：檢查誰有印表機的存取權</span><span class="sxs-lookup"><span data-stu-id="e3137-165">Example: Checking Who has Access to Printers</span></span>

<span data-ttu-id="e3137-166">下列 VBScript 程式碼範例顯示如何使用印表機安全描述項。</span><span class="sxs-lookup"><span data-stu-id="e3137-166">The following VBScript code example shows how to use the printer security descriptor.</span></span> <span data-ttu-id="e3137-167">腳本會在 [**Win32 \_ 印表機**](/windows/desktop/CIMWin32Prov/win32-printer)類別中呼叫 [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer)方法，以取得描述項，然後判斷安全描述項中是否有任意的存取控制清單 (DACL) 存在。</span><span class="sxs-lookup"><span data-stu-id="e3137-167">The script calls the [**GetSecurityDescriptor**](/windows/desktop/CIMWin32Prov/getsecuritydescriptor-method-in-class-win32-printer) method in the [**Win32\_Printer**](/windows/desktop/CIMWin32Prov/win32-printer) class to obtain the descriptor then determines if there is a Discretionary Access Control List (DACL) present in the security descriptor.</span></span> <span data-ttu-id="e3137-168">如果有 DACL，則腳本會從 DACL 取得 (ACE) 存取控制專案的清單。</span><span class="sxs-lookup"><span data-stu-id="e3137-168">If there is a DACL, then the script obtains the list of Access Control Entries (ACE) from the DACL.</span></span> <span data-ttu-id="e3137-169">每個 ACE 都是由 [**Win32 \_ ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace)的實例表示。</span><span class="sxs-lookup"><span data-stu-id="e3137-169">Each ACE is represented by an instance of [**Win32\_ACE**](/previous-versions/windows/desktop/secrcw32prov/win32-ace).</span></span> <span data-ttu-id="e3137-170">腳本會檢查每個 ACE 來取得使用者的名稱，並判斷使用者是否具有印表機的存取權。</span><span class="sxs-lookup"><span data-stu-id="e3137-170">The script checks every ACE to get the name of the user and determine whether the user has access to the printer.</span></span> <span data-ttu-id="e3137-171">使用者會以內嵌在 **win32 \_ ACE** 實例中的 [**win32 \_ 受信任**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee)實例來表示。</span><span class="sxs-lookup"><span data-stu-id="e3137-171">The user is represented in by an instance of [**Win32\_Trustee**](/previous-versions/windows/desktop/secrcw32prov/win32-trustee) embedded in the **Win32\_ACE** instance.</span></span>


```VB
SE_DACL_PRESENT = &h4
ACCESS_ALLOWED_ACE_TYPE = &h0
ACCESS_DENIED_ACE_TYPE  = &h1

strComputer = "."
Set objWMIService = GetObject("winmgmts:" _
    & "{impersonationLevel=impersonate, (Security)}!\\" & strComputer & "\root\cimv2")

Set colInstalledPrinters =  objWMIService.ExecQuery _
    ("Select * from Win32_Printer")

For Each objPrinter in colInstalledPrinters
   Wscript.Echo "Name: " & objPrinter.Name 
' Get security descriptor for printer
    Return = objPrinter.GetSecurityDescriptor( objSD )
    If ( return <> 0 ) Then
 WScript.Echo "Could not get security descriptor: " & Return
 wscript.Quit Return
    End If
' Extract the security descriptor flags
    intControlFlags = objSD.ControlFlags
    If intControlFlags AND SE_DACL_PRESENT Then
' Get the ACE entries from security descriptor
        colACEs = objSD.DACL
    For Each objACE in colACEs
' Get all the trustees and determine which have access to printer
        WScript.Echo objACE.Trustee.Domain & "\" & objACE.Trustee.Name
        If objACE.AceType = ACCESS_ALLOWED_ACE_TYPE Then
            WScript.Echo vbTab & "User has access to printer"
        ElseIf objACE.AceType = ACCESS_DENIED_ACE_TYPE Then
            WScript.Echo vbTab & "User does not have access to the printer"
        End If
    Next
    Else
    WScript.Echo "No DACL found in security descriptor"
End If
Next
```



## <a name="related-topics"></a><span data-ttu-id="e3137-172">相關主題</span><span class="sxs-lookup"><span data-stu-id="e3137-172">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="e3137-173">變更安全物件的存取安全性</span><span class="sxs-lookup"><span data-stu-id="e3137-173">Changing Access Security on Securable Objects</span></span>](changing-access-security-on-securable-objects.md)
</dt> <dt>

[<span data-ttu-id="e3137-174">安全描述項協助程式類別</span><span class="sxs-lookup"><span data-stu-id="e3137-174">Security Descriptor Helper Class</span></span>](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper)
</dt> <dt>

[<span data-ttu-id="e3137-175">安全性最佳作法</span><span class="sxs-lookup"><span data-stu-id="e3137-175">Security Best Practices</span></span>](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> <dt>

[<span data-ttu-id="e3137-176">維護 WMI 安全性</span><span class="sxs-lookup"><span data-stu-id="e3137-176">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="e3137-177">存取控制</span><span class="sxs-lookup"><span data-stu-id="e3137-177">Access Control</span></span>](/windows/desktop/SecAuthZ/access-control)
</dt> <dt>

[<span data-ttu-id="e3137-178">存取 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="e3137-178">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> </dl>

 

