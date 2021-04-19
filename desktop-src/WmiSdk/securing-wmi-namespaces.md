---
description: WMI 命名空間及其資料的存取權是由安全描述項控制。
ms.assetid: 3c2dc148-df6a-4bcb-a657-59b56c358d14
ms.tgt_platform: multiple
title: 保護 WMI 命名空間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f605a6cd1136e70d6c5243b9e143fdb167d41808
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106981491"
---
# <a name="securing-wmi-namespaces"></a><span data-ttu-id="b3495-103">保護 WMI 命名空間</span><span class="sxs-lookup"><span data-stu-id="b3495-103">Securing WMI Namespaces</span></span>

<span data-ttu-id="b3495-104">WMI 命名空間及其資料的存取權是由 [*安全描述項*](gloss-s.md)控制。</span><span class="sxs-lookup"><span data-stu-id="b3495-104">Access to WMI namespaces and their data is controlled by [*security descriptors*](gloss-s.md).</span></span> <span data-ttu-id="b3495-105">您可以藉由調整命名空間安全描述項來控制誰可以存取資料和方法，以保護 [*命名空間*](gloss-n.md) 中的資料。</span><span class="sxs-lookup"><span data-stu-id="b3495-105">You can protect data in your [*namespaces*](gloss-n.md) by adjusting the namespace security descriptor to control who has access to the data and methods.</span></span> <span data-ttu-id="b3495-106">如需詳細資訊，請參閱 [存取 WMI 安全物件](access-to-wmi-securable-objects.md)。</span><span class="sxs-lookup"><span data-stu-id="b3495-106">For more information, see [Access to WMI Securable Objects](access-to-wmi-securable-objects.md).</span></span>


<span data-ttu-id="b3495-107">下列主題將說明 WMI 命名空間安全性，以及如何控制對命名空間的存取。</span><span class="sxs-lookup"><span data-stu-id="b3495-107">The following topics describe WMI namespace security and how to control access to namespaces.</span></span>

<dl> <dt>

<span data-ttu-id="b3495-108"><span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[存取 WMI 命名空間](access-to-wmi-namespaces.md)</span><span class="sxs-lookup"><span data-stu-id="b3495-108"><span id="Access_to_WMI_Namespaces"></span><span id="access_to_wmi_namespaces"></span><span id="ACCESS_TO_WMI_NAMESPACES"></span>[Access to WMI Namespaces](access-to-wmi-namespaces.md)</span></span>
</dt> <dd>

<span data-ttu-id="b3495-109">WMI 命名空間安全性依賴標準的 Windows 使用者 [*安全識別碼*](/windows/desktop/SecGloss/s-gly) (sid) 和存取控制清單。</span><span class="sxs-lookup"><span data-stu-id="b3495-109">WMI namespace security relies on standard Windows user [*security identifiers*](/windows/desktop/SecGloss/s-gly) (SIDs) and access control lists.</span></span> <span data-ttu-id="b3495-110">系統管理員和使用者有不同的預設許可權。</span><span class="sxs-lookup"><span data-stu-id="b3495-110">Administrators and users have different default permissions.</span></span>

</dd> <dt>

<span data-ttu-id="b3495-111"><span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[設定命名空間安全描述項](setting-namespace-security-descriptors.md)</span><span class="sxs-lookup"><span data-stu-id="b3495-111"><span id="Setting_Namespace_Security_Descriptors"></span><span id="setting_namespace_security_descriptors"></span><span id="SETTING_NAMESPACE_SECURITY_DESCRIPTORS"></span>[Setting Namespace Security Descriptors](setting-namespace-security-descriptors.md)</span></span>
</dt> <dd>

<span data-ttu-id="b3495-112">在 wmi 存放庫中存在命名空間之後，您可以使用 wmi 控制項或呼叫 [**\_ \_ SystemSecurity**](--systemsecurity.md)的方法，變更命名空間上的安全性。</span><span class="sxs-lookup"><span data-stu-id="b3495-112">After a namespace exists in the WMI repository, you can change the security on the namespace by using the WMI Control or by calling the methods of [**\_\_SystemSecurity**](--systemsecurity.md).</span></span>

</dd> <dt>

<span data-ttu-id="b3495-113"><span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[需要命名空間的加密連接](requiring-an-encrypted-connection-to-a-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b3495-113"><span id="Requiring_an_Encrypted_Connection_to_a_Namespace"></span><span id="requiring_an_encrypted_connection_to_a_namespace"></span><span id="REQUIRING_AN_ENCRYPTED_CONNECTION_TO_A_NAMESPACE"></span>[Requiring an Encrypted Connection to a Namespace](requiring-an-encrypted-connection-to-a-namespace.md)</span></span>
</dt> <dd>

<span data-ttu-id="b3495-114">命名空間上的 **RequiresEncryption** 限定詞需要 WMI 用戶端應用程式或腳本，才能使用加密遠端程序呼叫的驗證層級。</span><span class="sxs-lookup"><span data-stu-id="b3495-114">The **RequiresEncryption** qualifier on a namespace requires the WMI client application or script to use the authentication level which encrypts remote procedure calls.</span></span> <span data-ttu-id="b3495-115">傳入的資料要求和非同步回呼都必須加密。</span><span class="sxs-lookup"><span data-stu-id="b3495-115">Both incoming data requests and asynchronous callbacks must be encrypted.</span></span>

</dd> <dt>

<span data-ttu-id="b3495-116"><span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[建立命名空間安全性的繼承](establishing-inheritance-of-namespace-security.md)</span><span class="sxs-lookup"><span data-stu-id="b3495-116"><span id="Establishing_Inheritance_of_Namespace_Security"></span><span id="establishing_inheritance_of_namespace_security"></span><span id="ESTABLISHING_INHERITANCE_OF_NAMESPACE_SECURITY"></span>[Establishing Inheritance of Namespace Security](establishing-inheritance-of-namespace-security.md)</span></span>
</dt> <dd>

<span data-ttu-id="b3495-117">您可以控制子命名空間是否繼承父命名空間的安全描述項。</span><span class="sxs-lookup"><span data-stu-id="b3495-117">You can control whether a child namespace inherits the security descriptor of the parent namespace.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="b3495-118">相關主題</span><span class="sxs-lookup"><span data-stu-id="b3495-118">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="b3495-119">維護 WMI 安全性</span><span class="sxs-lookup"><span data-stu-id="b3495-119">Maintaining WMI Security</span></span>](maintaining-wmi-security.md)
</dt> <dt>

[<span data-ttu-id="b3495-120">連接至遠端電腦上的 WMI</span><span class="sxs-lookup"><span data-stu-id="b3495-120">Connecting to WMI on a Remote Computer</span></span>](connecting-to-wmi-on-a-remote-computer.md)
</dt> <dt>

[<span data-ttu-id="b3495-121">使用 WMI API 建立命名空間</span><span class="sxs-lookup"><span data-stu-id="b3495-121">Creating a Namespace with the WMI API</span></span>](creating-a-namespace-with-the-wmi-api.md)
</dt> <dt>

[<span data-ttu-id="b3495-122">WMI 安全描述項物件</span><span class="sxs-lookup"><span data-stu-id="b3495-122">WMI Security Descriptor Objects</span></span>](wmi-security-descriptor-objects.md)
</dt> </dl>

 

 
