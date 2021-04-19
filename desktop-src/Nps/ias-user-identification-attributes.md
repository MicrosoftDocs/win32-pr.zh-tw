---
title: 使用者識別屬性
description: 要求驗證的使用者身分識別會以數個不同的屬性提供給 NPS 擴充 Dll。
ms.assetid: 2f741a81-e432-47fe-a14a-8b77ecd41e28
ms.tgt_platform: multiple
keywords:
- 屬性、使用者識別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 527bdffad376ce92fa2fd7c5d5330fb752fea6aa
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106968915"
---
# <a name="user-identification-attributes"></a><span data-ttu-id="25331-104">使用者識別屬性</span><span class="sxs-lookup"><span data-stu-id="25331-104">User Identification Attributes</span></span>

> [!Note]  
> <span data-ttu-id="25331-105">從 Windows Server 2008 開始， (IAS) 的網際網路驗證服務已重新命名為網路原則伺服器 (NPS) 。</span><span class="sxs-lookup"><span data-stu-id="25331-105">Internet Authentication Service (IAS) was renamed Network Policy Server (NPS) starting with Windows Server 2008.</span></span> <span data-ttu-id="25331-106">本主題的內容適用于 IAS 和 NPS。</span><span class="sxs-lookup"><span data-stu-id="25331-106">The content of this topic applies to both IAS and NPS.</span></span> <span data-ttu-id="25331-107">在整個文字中，NPS 是用來參考服務的所有版本，包括原本稱為 IAS 的版本。</span><span class="sxs-lookup"><span data-stu-id="25331-107">Throughout the text, NPS is used to refer to all versions of the service, including the versions originally referred to as IAS.</span></span>

 

<span data-ttu-id="25331-108">要求驗證的使用者身分識別會以數個不同的屬性提供給 NPS 擴充 Dll。</span><span class="sxs-lookup"><span data-stu-id="25331-108">The identity of the user requesting authentication is supplied to the NPS Extension DLLs in a number of different attributes.</span></span>

-   <span data-ttu-id="25331-109">**ratUserName**</span><span class="sxs-lookup"><span data-stu-id="25331-109">**ratUserName**</span></span>
-   <span data-ttu-id="25331-110">**ratStrippedUserName**</span><span class="sxs-lookup"><span data-stu-id="25331-110">**ratStrippedUserName**</span></span>
-   <span data-ttu-id="25331-111">**ratFQUserName**</span><span class="sxs-lookup"><span data-stu-id="25331-111">**ratFQUserName**</span></span>

<span data-ttu-id="25331-112">每個屬性都提供不同格式的使用者身分識別。</span><span class="sxs-lookup"><span data-stu-id="25331-112">Each attribute provides the user identity in a different format.</span></span> <span data-ttu-id="25331-113">一般情況下，開發人員應該使用 **ratStrippedUserName**。</span><span class="sxs-lookup"><span data-stu-id="25331-113">In general, developers should use **ratStrippedUserName**.</span></span> <span data-ttu-id="25331-114">**RatUserName** 和 **ratFQUserName** 屬性的用法更加特製化。</span><span class="sxs-lookup"><span data-stu-id="25331-114">The uses of the **ratUserName** and **ratFQUserName** attributes are more specialized.</span></span>

> [!Note]  
> <span data-ttu-id="25331-115">當 User-Password 屬性（ **ratUserPassword**）傳送至擴充 DLL 時，已經解密，而且可以在該表單中使用。</span><span class="sxs-lookup"><span data-stu-id="25331-115">The User-Password attribute, **ratUserPassword**, has already been decrypted when it is sent to the extension DLL and is usable in that form.</span></span>

 

## <a name="ratusername"></a><span data-ttu-id="25331-116">ratUserName</span><span class="sxs-lookup"><span data-stu-id="25331-116">ratUserName</span></span>

<span data-ttu-id="25331-117">**RatUserName** 屬性包含實際透過網路傳送的名稱。</span><span class="sxs-lookup"><span data-stu-id="25331-117">The **ratUserName** attribute contains the name that was actually sent "over the wire."</span></span> <span data-ttu-id="25331-118">NPS 未以任何方式處理或驗證此屬性的內容。</span><span class="sxs-lookup"><span data-stu-id="25331-118">NPS has not, in any way, processed or validated the contents of this attribute.</span></span> <span data-ttu-id="25331-119">這個屬性可能完全無法使用，因為使用者可能已經透過呼叫者識別碼之類的方法來識別。</span><span class="sxs-lookup"><span data-stu-id="25331-119">This attribute may not be available at all because the user may have been identified through a means such as caller ID.</span></span>

<span data-ttu-id="25331-120">使用 [**RadiusExtensionProcess/例如**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex)，如果這個屬性可供使用，它只能在驗證延伸模組 DLL 外掛程式點使用。</span><span class="sxs-lookup"><span data-stu-id="25331-120">When using [**RadiusExtensionProcess/Ex**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_ex), if this attribute is available, it is available only at the Authentication Extension DLL plug-in point.</span></span> <span data-ttu-id="25331-121">**RatUserName** 屬性無法在授權延伸模組 dll 外掛程式點使用，因為在授權延伸 dll 中， **RadiusExtensionProcess/Ex** 函式只會看到 "傳出" 屬性。</span><span class="sxs-lookup"><span data-stu-id="25331-121">The **ratUserName** attribute is not available at the Authorization Extension DLL plug-in point because in Authorization Extension DLLs the **RadiusExtensionProcess/Ex** functions see only the "outbound" attributes.</span></span>

<span data-ttu-id="25331-122">使用 [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2)時，如果此屬性可供使用，則可在驗證延伸模組 dll 外掛程式點和授權延伸模組 dll 外掛程式點上使用。</span><span class="sxs-lookup"><span data-stu-id="25331-122">When using [**RadiusExtensionProcess2**](/windows/desktop/api/authif/nc-authif-pradius_extension_process_2), if this attribute is available, it is available at both the Authentication Extension DLL plug-in point and the Authorization Extension DLL plug-in point.</span></span>

## <a name="ratstrippedusername"></a><span data-ttu-id="25331-123">ratStrippedUserName</span><span class="sxs-lookup"><span data-stu-id="25331-123">ratStrippedUserName</span></span>

<span data-ttu-id="25331-124">在「領域移除」之後， **ratStrippedUserName** 是使用者的身分識別。</span><span class="sxs-lookup"><span data-stu-id="25331-124">The **ratStrippedUserName** is the user's identity after "realm stripping."</span></span> <span data-ttu-id="25331-125">如需有關領域移除的詳細資訊，請參閱 HTTP： technet2.microsoft.com 的[領域名稱](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10))主題 \\ \\ 。</span><span class="sxs-lookup"><span data-stu-id="25331-125">For more information on realm stripping, see the [Realm names](/previous-versions/windows/it-pro/windows-server-2003/cc779938(v=ws.10)) topic on http:\\\\technet2.microsoft.com.</span></span>

<span data-ttu-id="25331-126">這個屬性可能存在於驗證延伸模組 DLL 外掛程式點、授權延伸模組 DLL 外掛程式點，或兩者。</span><span class="sxs-lookup"><span data-stu-id="25331-126">This attribute may be present at the Authentication Extension DLL plug-in point, the Authorization Extension DLL plug-in point, or both.</span></span> <span data-ttu-id="25331-127">這個屬性的格式保證如下：</span><span class="sxs-lookup"><span data-stu-id="25331-127">This attribute is guaranteed to have the format:</span></span>

<span data-ttu-id="25331-128">*網域使用者 ***\\*** 名稱*</span><span class="sxs-lookup"><span data-stu-id="25331-128">*Domain ***\\*** UserName*</span></span>

<span data-ttu-id="25331-129">其中 *網域* 是 NetBIOS 功能變數名稱。</span><span class="sxs-lookup"><span data-stu-id="25331-129">Where *Domain* is the NetBIOS domain name.</span></span>

## <a name="ratfqusername"></a><span data-ttu-id="25331-130">ratFQUserName</span><span class="sxs-lookup"><span data-stu-id="25331-130">ratFQUserName</span></span>

<span data-ttu-id="25331-131">**RatFQUserName** 屬性是「完整」使用者名稱。</span><span class="sxs-lookup"><span data-stu-id="25331-131">The **ratFQUserName** attribute is the "fully qualified" user name.</span></span>

<span data-ttu-id="25331-132">這個屬性可能存在於驗證延伸模組 DLL 外掛程式點、授權延伸模組 DLL 外掛程式點或兩者中。</span><span class="sxs-lookup"><span data-stu-id="25331-132">This attribute may be present in the Authentication Extension DLL plug-in point, the Authorization Extension DLL plug-in point, or both.</span></span> <span data-ttu-id="25331-133">不過，這兩個外掛程式點之間的屬性格式可能不同。</span><span class="sxs-lookup"><span data-stu-id="25331-133">However, the format of the attribute may differ between the two plug-in points.</span></span> <span data-ttu-id="25331-134">在驗證延伸模組 DLL 外掛程式點上，這個屬性一律會採用下列格式：</span><span class="sxs-lookup"><span data-stu-id="25331-134">At the Authentication Extension DLL plug-in point, this attribute will always be of the form:</span></span>

<span data-ttu-id="25331-135">*網域使用者 ***\\*** 名稱*</span><span class="sxs-lookup"><span data-stu-id="25331-135">*Domain ***\\*** UserName*</span></span>

<span data-ttu-id="25331-136">在授權延伸模組 DLL 外掛程式點的 **ratFQUserName** 屬性格式，取決於使用者是否為 Active Directory 的使用者。</span><span class="sxs-lookup"><span data-stu-id="25331-136">The format of the **ratFQUserName** attribute at the Authorization Extension DLL plug-in point depends on whether the user is an Active Directory user.</span></span>

-   <span data-ttu-id="25331-137">如果使用者是本機使用者 **ratFQUserName** 與驗證延伸模組 DLL 外掛程式點的格式相同：</span><span class="sxs-lookup"><span data-stu-id="25331-137">If the user is a local user **ratFQUserName** has the same format as for the Authentication Extension DLL plug-in point:</span></span>

    <span data-ttu-id="25331-138">*網域使用者 ***\\*** 名稱*</span><span class="sxs-lookup"><span data-stu-id="25331-138">*Domain ***\\*** UserName*</span></span>

    <span data-ttu-id="25331-139">.</span><span class="sxs-lookup"><span data-stu-id="25331-139">.</span></span>

-   <span data-ttu-id="25331-140">如果使用者是 Active Directory 使用者， **ratFQUserName** 可能會以「標準」格式包含使用者的名稱。</span><span class="sxs-lookup"><span data-stu-id="25331-140">If the user is an Active Directory user, **ratFQUserName** may contain the user's name in "canonical" format.</span></span> <span data-ttu-id="25331-141">標準格式是 Active Directory 用來識別使用者的格式。</span><span class="sxs-lookup"><span data-stu-id="25331-141">Canonical format is the format used by the Active Directory to identify the user.</span></span> <span data-ttu-id="25331-142">它是從 Active Directory 樹狀結構的根路徑，其中包含使用者的組織單位 (OU) 。</span><span class="sxs-lookup"><span data-stu-id="25331-142">It is the path from the root of the Active Directory tree, and includes the user's Organizational Unit (OU).</span></span>

## <a name="related-topics"></a><span data-ttu-id="25331-143">相關主題</span><span class="sxs-lookup"><span data-stu-id="25331-143">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="25331-144">設定延伸模組 Dll</span><span class="sxs-lookup"><span data-stu-id="25331-144">Setting Up the Extension DLLs</span></span>](/windows/desktop/Nps/ias-setting-up-the-extension-and-authorization-dlls)
</dt> <dt>

[<span data-ttu-id="25331-145">叫用擴充 Dll</span><span class="sxs-lookup"><span data-stu-id="25331-145">Invoking the Extension DLLs</span></span>](/windows/desktop/Nps/ias-authentication-and-authorization-process)
</dt> </dl>

 

 