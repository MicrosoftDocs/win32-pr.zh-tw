---
description: 在完整系統管理員帳戶下執行的 c + + 應用程式和腳本，都可以變更命名空間安全描述項。
ms.assetid: d3e56b30-d5a8-446a-89aa-645b44a75af6
ms.tgt_platform: multiple
title: 設定命名空間安全描述項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4877b1dfc0ae1a9467b1beb7d169bfa31fdf7395
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107000190"
---
# <a name="setting-namespace-security-descriptors"></a><span data-ttu-id="b7ede-103">設定命名空間安全描述項</span><span class="sxs-lookup"><span data-stu-id="b7ede-103">Setting Namespace Security Descriptors</span></span>

<span data-ttu-id="b7ede-104">在完整系統管理員帳戶下執行的 c + + 應用程式和腳本，都可以變更命名空間安全描述項。</span><span class="sxs-lookup"><span data-stu-id="b7ede-104">Both C++ applications and scripts running under a full administrator account can change a namespace security descriptor.</span></span>

## <a name="namespace-security-descriptors"></a><span data-ttu-id="b7ede-105">命名空間安全描述項</span><span class="sxs-lookup"><span data-stu-id="b7ede-105">Namespace Security Descriptors</span></span>

<span data-ttu-id="b7ede-106">每個 WMI 命名空間都有一個 [*安全描述項*](/windows/desktop/SecGloss/s-gly)，可讓每個命名空間具有唯一的安全性設定，以決定誰可以存取命名空間資料和方法。</span><span class="sxs-lookup"><span data-stu-id="b7ede-106">Each WMI namespace has a [*security descriptor*](/windows/desktop/SecGloss/s-gly), which allows each namespace to have unique security settings that determine who has access to the namespace data and methods.</span></span> <span data-ttu-id="b7ede-107">如需 WMI 存取安全性的詳細資訊，請參閱 [存取 wmi 安全物件](access-to-wmi-securable-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="b7ede-107">For more information about WMI access security, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span> <span data-ttu-id="b7ede-108">Wmi[命名空間的存取權](access-to-wmi-namespaces.md)描述 WMI 中 wmi 命名空間和安全性審核的預設安全性設定。</span><span class="sxs-lookup"><span data-stu-id="b7ede-108">[Access to WMI Namespaces](access-to-wmi-namespaces.md) describes the default security settings for WMI namespaces and security auditing in WMI.</span></span>

<span data-ttu-id="b7ede-109">您可以透過下列方式，設定 WMI (CIM) 存放庫中每個 WMI 命名空間的帳戶許可權：</span><span class="sxs-lookup"><span data-stu-id="b7ede-109">You can set account permissions for each WMI namespace in the WMI (CIM) repository in the following ways:</span></span>

-   <span data-ttu-id="b7ede-110">在 MOF 檔案中建立命名空間時。</span><span class="sxs-lookup"><span data-stu-id="b7ede-110">When the namespace is created in the MOF file.</span></span> <span data-ttu-id="b7ede-111">如需詳細資訊，請參閱 [在建立命名空間時設定命名空間安全性](setting-namespace-security-when-the-namespace-is-created.md)。</span><span class="sxs-lookup"><span data-stu-id="b7ede-111">For more information, see [Setting Namespace Security When the Namespace is Created](setting-namespace-security-when-the-namespace-is-created.md).</span></span>
-   <span data-ttu-id="b7ede-112">使用 WMI 控制項手動進行。</span><span class="sxs-lookup"><span data-stu-id="b7ede-112">Manually, using the WMI Control.</span></span> <span data-ttu-id="b7ede-113">如需詳細資訊，請參閱 [使用 WMI 控制項設定命名空間安全性](setting-namespace-security-with-the-wmi-control.md)。</span><span class="sxs-lookup"><span data-stu-id="b7ede-113">For more information, see [Setting Namespace Security with the WMI Control](setting-namespace-security-with-the-wmi-control.md).</span></span>
-   <span data-ttu-id="b7ede-114">藉由呼叫 [**\_ \_ SystemSecurity**](--systemsecurity.md)類別的方法，以程式設計方式進行。</span><span class="sxs-lookup"><span data-stu-id="b7ede-114">Programmatically, by calling the methods of the [**\_\_SystemSecurity**](--systemsecurity.md) class.</span></span>

<span data-ttu-id="b7ede-115">與每個命名空間相關聯之 [**\_ \_ SystemSecurity**](--systemsecurity.md)物件的下列方法，可讓您讀取或變更命名空間的安全性。</span><span class="sxs-lookup"><span data-stu-id="b7ede-115">The following methods of the [**\_\_SystemSecurity**](--systemsecurity.md) object associated with each namespace allow you to read or change security on a namespace.</span></span>

<dl> <dt>

<span data-ttu-id="b7ede-116"><span id="GetCallerAccessRights"></span><span id="getcalleraccessrights"></span><span id="GETCALLERACCESSRIGHTS"></span>[**GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md)</span><span class="sxs-lookup"><span data-stu-id="b7ede-116"><span id="GetCallerAccessRights"></span><span id="getcalleraccessrights"></span><span id="GETCALLERACCESSRIGHTS"></span>[**GetCallerAccessRights**](--systemsecurity-getcalleraccessrights.md)</span></span>
</dt> <dd>

<span data-ttu-id="b7ede-117">將 *rights* 參數設定為點陣圖，每個位都對應至存取權限。</span><span class="sxs-lookup"><span data-stu-id="b7ede-117">Sets the *rights* parameter as a bitmap with each bit corresponding to an access right.</span></span>

</dd> <dt>

<span data-ttu-id="b7ede-118"><span id="GetSD"></span><span id="getsd"></span><span id="GETSD"></span>[**GetSD**](--systemsecurity-getsd.md)</span><span class="sxs-lookup"><span data-stu-id="b7ede-118"><span id="GetSD"></span><span id="getsd"></span><span id="GETSD"></span>[**GetSD**](--systemsecurity-getsd.md)</span></span>
</dt> <dd>

<span data-ttu-id="b7ede-119">取得使用者所連接之命名空間的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="b7ede-119">Gets the security descriptor for the namespace to which the user is connected.</span></span> <span data-ttu-id="b7ede-120">這個方法會以二進位位元組陣列格式傳回安全描述項。</span><span class="sxs-lookup"><span data-stu-id="b7ede-120">This method returns a security descriptor in binary byte array format.</span></span> <span data-ttu-id="b7ede-121">如果您要撰寫腳本，請使用 [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="b7ede-121">If you are writing a script, use the [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="b7ede-122"><span id="SetSD"></span><span id="setsd"></span><span id="SETSD"></span>[**SetSD**](--systemsecurity-setsd.md)</span><span class="sxs-lookup"><span data-stu-id="b7ede-122"><span id="SetSD"></span><span id="setsd"></span><span id="SETSD"></span>[**SetSD**](--systemsecurity-setsd.md)</span></span>
</dt> <dd>

<span data-ttu-id="b7ede-123">針對使用者所連接的命名空間，設定 (SD) 的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="b7ede-123">Sets the security descriptor (SD) for the namespace to which a user is connected.</span></span> <span data-ttu-id="b7ede-124">這個方法需要二進位位元組陣列格式的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="b7ede-124">This method requires a security descriptor in binary byte array format.</span></span> <span data-ttu-id="b7ede-125">如果您要撰寫腳本，請使用 [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) 方法。</span><span class="sxs-lookup"><span data-stu-id="b7ede-125">If you are writing a script, use the [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md) method.</span></span>

</dd> <dt>

<span data-ttu-id="b7ede-126"><span id="GetSecurityDescriptor"></span><span id="getsecuritydescriptor"></span><span id="GETSECURITYDESCRIPTOR"></span>[**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md)</span><span class="sxs-lookup"><span data-stu-id="b7ede-126"><span id="GetSecurityDescriptor"></span><span id="getsecuritydescriptor"></span><span id="GETSECURITYDESCRIPTOR"></span>[**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md)</span></span>
</dt> <dd>

<span data-ttu-id="b7ede-127">取得安全描述項，可控制與 [**\_ \_ SystemSecurity**](--systemsecurity.md)實例相關聯之 WMI 命名空間的存取權。</span><span class="sxs-lookup"><span data-stu-id="b7ede-127">Gets the security descriptor that controls access to the WMI namespace associated with the instance of [**\_\_SystemSecurity**](--systemsecurity.md).</span></span> <span data-ttu-id="b7ede-128">安全描述項會以 [**\_ \_ SecurityDescriptor**](--securitydescriptor.md)的實例傳回。</span><span class="sxs-lookup"><span data-stu-id="b7ede-128">The security descriptor is returned as an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7ede-129"><span id="SetSecurityDescriptor"></span><span id="setsecuritydescriptor"></span><span id="SETSECURITYDESCRIPTOR"></span>[**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md)</span><span class="sxs-lookup"><span data-stu-id="b7ede-129"><span id="SetSecurityDescriptor"></span><span id="setsecuritydescriptor"></span><span id="SETSECURITYDESCRIPTOR"></span>[**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md)</span></span>
</dt> <dd>

<span data-ttu-id="b7ede-130">寫入控制印表機存取權之安全描述項的更新版本。</span><span class="sxs-lookup"><span data-stu-id="b7ede-130">Writes an updated version of the security descriptor that controls access to the printer.</span></span> <span data-ttu-id="b7ede-131">安全描述項會以 [**\_ \_ SecurityDescriptor**](--securitydescriptor.md)的實例來表示。</span><span class="sxs-lookup"><span data-stu-id="b7ede-131">The security descriptor is represented by an instance of [**\_\_SecurityDescriptor**](--securitydescriptor.md).</span></span>

</dd> <dt>

<span data-ttu-id="b7ede-132"><span id="Get9XUserList"></span><span id="get9xuserlist"></span><span id="GET9XUSERLIST"></span>[**Get9XUserList**](--systemsecurity-get9xuserlist.md)</span><span class="sxs-lookup"><span data-stu-id="b7ede-132"><span id="Get9XUserList"></span><span id="get9xuserlist"></span><span id="GET9XUSERLIST"></span>[**Get9XUserList**](--systemsecurity-get9xuserlist.md)</span></span>
</dt> <dd>

<span data-ttu-id="b7ede-133">針對執行過時 Windows 的電腦上的個別使用者清單取得遠端存取許可權，但無法使用透過 Windows 安全描述項的存取控制。</span><span class="sxs-lookup"><span data-stu-id="b7ede-133">Gets the remote access rights for a list of individual users on computers running obsolete versions of Windows, where access control through Windows security descriptors is not available.</span></span>

</dd> <dt>

<span data-ttu-id="b7ede-134"><span id="Set9XUserList"></span><span id="set9xuserlist"></span><span id="SET9XUSERLIST"></span>[**Set9XUserList**](--systemsecurity-set9xuserlist.md)</span><span class="sxs-lookup"><span data-stu-id="b7ede-134"><span id="Set9XUserList"></span><span id="set9xuserlist"></span><span id="SET9XUSERLIST"></span>[**Set9XUserList**](--systemsecurity-set9xuserlist.md)</span></span>
</dt> <dd>

<span data-ttu-id="b7ede-135">針對執行過時 Windows 的電腦上的個別使用者清單設定遠端存取許可權，無法使用透過 Windows 安全描述項的存取控制。</span><span class="sxs-lookup"><span data-stu-id="b7ede-135">Sets the remote access rights for a list of individual users on computers running obsolete versions of Windows, where access control through Windows security descriptors is not available.</span></span>

</dd> </dl>

<span data-ttu-id="b7ede-136">如果您要撰寫腳本，請使用 [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) 和 [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md)。</span><span class="sxs-lookup"><span data-stu-id="b7ede-136">If you are writing scripts, use the [**GetSecurityDescriptor**](getsecuritydescriptor-method-in-class---systemsecurity-.md) and [**SetSecurityDescriptor**](setsecuritydescriptor-method-in-class---systemsecurity.md).</span></span> <span data-ttu-id="b7ede-137">您可以使用 [**Win32 \_ SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) 類別的方法來改變安全描述項。</span><span class="sxs-lookup"><span data-stu-id="b7ede-137">You can use the methods of the [**Win32\_SecurityDescriptorHelper**](/previous-versions/windows/desktop/secrcw32prov/win32-securitydescriptorhelper) class to alter the security descriptors.</span></span>

<span data-ttu-id="b7ede-138">如果您是使用 c + + 進行程式設計，您可以使用 [安全描述項定義語言 (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language)和轉換方法 [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) 和 [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora)，來操作二進位安全描述項。</span><span class="sxs-lookup"><span data-stu-id="b7ede-138">If you are programming in C++, you can manipulate the binary security descriptor using [Security Descriptor Definition Language (SDDL)](/windows/desktop/SecAuthZ/security-descriptor-definition-language), and the conversion methods [**ConvertSecurityDescriptorToStringSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertsecuritydescriptortostringsecuritydescriptora) and [**ConvertStringSecurityDescriptorToSecurityDescriptor**](/windows/desktop/api/sddl/nf-sddl-convertstringsecuritydescriptortosecuritydescriptora).</span></span>

<span data-ttu-id="b7ede-139">請注意，從 Windows Vista 開始， [使用者帳戶控制](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) (UAC) 會影響對 wmi 資料的存取權，以及可使用 [*wmi 控制項*](gloss-w.md)設定的內容。</span><span class="sxs-lookup"><span data-stu-id="b7ede-139">Be aware that, starting with Windows Vista, [User Account Control](https://www.microsoft.com/technet/windowsvista/security/uac.mspx) (UAC) affects access to WMI data and what can be configured with the [*WMI Control*](gloss-w.md).</span></span> <span data-ttu-id="b7ede-140">如需詳細資訊，請參閱 [使用者帳戶控制和 WMI](user-account-control-and-wmi.md)。</span><span class="sxs-lookup"><span data-stu-id="b7ede-140">For more information, see [User Account Control and WMI](user-account-control-and-wmi.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="b7ede-141">相關主題</span><span class="sxs-lookup"><span data-stu-id="b7ede-141">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b7ede-142">保護 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="b7ede-142">Securing WMI Namespaces</span></span>](securing-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="b7ede-143">WMI 安全性常數</span><span class="sxs-lookup"><span data-stu-id="b7ede-143">WMI Security Constants</span></span>](wmi-security-constants.md)
</dt> <dt>

[<span data-ttu-id="b7ede-144">存取 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="b7ede-144">Access to WMI Namespaces</span></span>](access-to-wmi-namespaces.md)
</dt> <dt>

[<span data-ttu-id="b7ede-145">WMI 安全描述項物件</span><span class="sxs-lookup"><span data-stu-id="b7ede-145">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
