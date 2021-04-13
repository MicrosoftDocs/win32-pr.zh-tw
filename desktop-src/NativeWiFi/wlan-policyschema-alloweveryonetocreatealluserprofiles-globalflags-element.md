---
description: 指定任何使用者是否可以建立所有使用者設定檔。
ms.assetid: b9bdfe85-b9d5-4dcc-a7f8-05cce9702ec3
title: allowEveryoneToCreateAllUserProfiles (globalFlags) 元素
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- allowEveryoneToCreateAllUserProfiles
api_type:
- Schema
api_location: ''
ms.openlocfilehash: 63bc4c76ccecd8c7f774dc0e73621ef3f9b19877
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511184"
---
# <a name="alloweveryonetocreatealluserprofiles-globalflags-element"></a><span data-ttu-id="4d029-103">allowEveryoneToCreateAllUserProfiles (globalFlags) 元素</span><span class="sxs-lookup"><span data-stu-id="4d029-103">allowEveryoneToCreateAllUserProfiles (globalFlags) Element</span></span>

<span data-ttu-id="4d029-104">**AllowEveryoneToCreateAllUserProfiles** (globalFlags) 元素會指定任何使用者是否可以建立所有使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="4d029-104">The **allowEveryoneToCreateAllUserProfiles** (globalFlags) element specifies whether any user can create an all-user profile.</span></span> <span data-ttu-id="4d029-105">電腦上的任何使用者都可以使用所有使用者設定檔，以連線到與設定檔相關聯的無線網路。</span><span class="sxs-lookup"><span data-stu-id="4d029-105">An all-user profile can be used by any user on the machine to connect to the wireless network associated with the profile.</span></span>

<span data-ttu-id="4d029-106">如果 **allowEveryoneToCreateAllUserProfiles** 為 TRUE，則任何使用者都可以建立所有使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="4d029-106">If **allowEveryoneToCreateAllUserProfiles** is TRUE, than any user can create an all-user profile.</span></span> <span data-ttu-id="4d029-107">如果 **allowEveryoneToCreateAllUserProfiles** 為 FALSE，則不是所有使用者都可以建立所有使用者設定檔，而且會有與 [wlan 安全新增 \_ \_ \_ \_ 所有使用者設定檔] 安全性物件相關聯的 DACL， \_ \_ 其中指定具有建立所有使用者設定檔許可權的使用者或使用者群組。</span><span class="sxs-lookup"><span data-stu-id="4d029-107">If **allowEveryoneToCreateAllUserProfiles** is FALSE, then not all users can create an all-user profile, and there is a DACL associated with the wlan\_secure\_add\_new\_all\_user\_profiles security object that specifies the users or user groups with permission to create all-user profiles.</span></span> <span data-ttu-id="4d029-108">預設的 DACL 指定只有登入為 Administrators 群組成員的使用者可以建立所有使用者設定檔。</span><span class="sxs-lookup"><span data-stu-id="4d029-108">The default DACL specifies that only users that are logged on as a member of the Administrators group can create an all-user profile.</span></span> <span data-ttu-id="4d029-109">您可以藉由呼叫 [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings)來變更預設安全性設定。</span><span class="sxs-lookup"><span data-stu-id="4d029-109">The default security settings can be changed by calling [**WlanSetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlansetsecuritysettings).</span></span> <span data-ttu-id="4d029-110">若要取得目前的安全性設定，請呼叫 [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings)。</span><span class="sxs-lookup"><span data-stu-id="4d029-110">To get the current security settings, call [**WlanGetSecuritySettings**](/windows/desktop/api/wlanapi/nf-wlanapi-wlangetsecuritysettings).</span></span>

<span data-ttu-id="4d029-111">此為必要元素。</span><span class="sxs-lookup"><span data-stu-id="4d029-111">This element is mandatory.</span></span> <span data-ttu-id="4d029-112">當設定檔由自動設定服務建立時，此元素的預設值會是 TRUE。</span><span class="sxs-lookup"><span data-stu-id="4d029-112">When a profile is created by the AutoConfig service, this element will have the default value of TRUE.</span></span>

``` syntax
<xs:element name="allowEveryoneToCreateAllUserProfiles"
    type="boolean"
 />
```

<span data-ttu-id="4d029-113">**AllowEveryoneToCreateAllUserProfiles** 元素是由 [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md)元素定義。</span><span class="sxs-lookup"><span data-stu-id="4d029-113">The **allowEveryoneToCreateAllUserProfiles** element is defined by the [**globalFlags**](wlan-policyschema-globalflags-wlanpolicy-element.md) element.</span></span>

## <a name="requirements"></a><span data-ttu-id="4d029-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d029-114">Requirements</span></span>



| <span data-ttu-id="4d029-115">需求</span><span class="sxs-lookup"><span data-stu-id="4d029-115">Requirement</span></span> | <span data-ttu-id="4d029-116">值</span><span class="sxs-lookup"><span data-stu-id="4d029-116">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="4d029-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d029-117">Minimum supported client</span></span><br/> | <span data-ttu-id="4d029-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d029-118">Windows Vista \[desktop apps only\]</span></span><br/>       |
| <span data-ttu-id="4d029-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d029-119">Minimum supported server</span></span><br/> | <span data-ttu-id="4d029-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d029-120">Windows Server 2008 \[desktop apps only\]</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4d029-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d029-121">See also</span></span>

<dl> <dt>

<span data-ttu-id="4d029-122">**架構中的元素定義內容**</span><span class="sxs-lookup"><span data-stu-id="4d029-122">**Definition context of element in schema**</span></span>
</dt> <dt>

[<span data-ttu-id="4d029-123">**globalFlags**</span><span class="sxs-lookup"><span data-stu-id="4d029-123">**globalFlags**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> <dt>

<span data-ttu-id="4d029-124">**架構實例中可能的直屬父元素**</span><span class="sxs-lookup"><span data-stu-id="4d029-124">**Possible immediate parent element in schema instance**</span></span>
</dt> <dt>

[<span data-ttu-id="4d029-125">**globalFlags (WLANPolicy)**</span><span class="sxs-lookup"><span data-stu-id="4d029-125">**globalFlags (WLANPolicy)**</span></span>](wlan-policyschema-globalflags-wlanpolicy-element.md)
</dt> </dl>

 

 




