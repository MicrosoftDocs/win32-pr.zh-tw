---
description: 在電腦升級或電腦對電腦的遷移期間，將會遷移特定憑證存放區中的憑證。
ms.assetid: fe81d578-f2f6-41f0-9ebf-e7bd5532bed9
title: 憑證存放區遷移
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a31b42b83718aa1cab786ad79cc2df754b8fd9b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027241"
---
# <a name="certificate-store-migration"></a><span data-ttu-id="6984b-103">憑證存放區遷移</span><span class="sxs-lookup"><span data-stu-id="6984b-103">Certificate Store Migration</span></span>

<span data-ttu-id="6984b-104">在電腦升級或電腦對電腦的遷移期間，將會遷移特定憑證存放區中的憑證。</span><span class="sxs-lookup"><span data-stu-id="6984b-104">During a computer upgrade or a computer-to-computer migration, the certificates in certain certificate stores will be migrated.</span></span> <span data-ttu-id="6984b-105">下表列出預設遷移的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="6984b-105">The following table lists the certificate stores that are migrated by default.</span></span> <span data-ttu-id="6984b-106">對於系統自動憑證要求設定 (ACR) 存放區，只會遷移 (Ctl) 的 [*憑證信任清單*](../secgloss/c-gly.md) 。</span><span class="sxs-lookup"><span data-stu-id="6984b-106">For the system Automatic Certificate Request Settings (ACRS) store, only the [*certificate trust lists*](../secgloss/c-gly.md) (CTLs) are migrated.</span></span> <span data-ttu-id="6984b-107">針對以下列出的所有其他存放區，只會遷移憑證。</span><span class="sxs-lookup"><span data-stu-id="6984b-107">For all other stores listed below, only the certificates are migrated.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="6984b-108">系統/使用者</span><span class="sxs-lookup"><span data-stu-id="6984b-108">System/user</span></span></th>
<th><span data-ttu-id="6984b-109">市集</span><span class="sxs-lookup"><span data-stu-id="6984b-109">Store</span></span></th>
<th><span data-ttu-id="6984b-110">儲存位置</span><span class="sxs-lookup"><span data-stu-id="6984b-110">Storage location</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="6984b-111">$ {ROWSPAN8} $System $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="6984b-111">${ROWSPAN8}$System${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="6984b-112">ROOT</span><span class="sxs-lookup"><span data-stu-id="6984b-112">ROOT</span></span></td>
<td><span data-ttu-id="6984b-113"><strong>HKEY_LOCAL_MACHINE</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \<strong>根目錄</strong> \<strong>憑證</strong></span><span class="sxs-lookup"><span data-stu-id="6984b-113"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Root</strong>\<strong>Certificates</strong></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6984b-114">MY</span><span class="sxs-lookup"><span data-stu-id="6984b-114">MY</span></span></td>
<td><span data-ttu-id="6984b-115"><strong>HKEY_LOCAL_MACHINE</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \<strong>我</strong> \ 的<strong>憑證</strong></span><span class="sxs-lookup"><span data-stu-id="6984b-115"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>My</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6984b-116">請求</span><span class="sxs-lookup"><span data-stu-id="6984b-116">REQUEST</span></span></td>
<td><span data-ttu-id="6984b-117"><strong>HKEY_LOCAL_MACHINE</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \<strong>要求</strong> \<strong>憑證</strong></span><span class="sxs-lookup"><span data-stu-id="6984b-117"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Request</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="6984b-118">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="6984b-118">TrustedPublisher</span></span></td>
<td><span data-ttu-id="6984b-119"><strong>HKEY_LOCAL_MACHINE</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \<strong>TrustedPublisher</strong> \<strong>憑證</strong></span><span class="sxs-lookup"><span data-stu-id="6984b-119"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPublisher</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6984b-120">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="6984b-120">TrustedPeople</span></span></td>
<td><span data-ttu-id="6984b-121"><strong>HKEY_LOCAL_MACHINE</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \<strong>TrustedPeople</strong> \<strong>憑證</strong></span><span class="sxs-lookup"><span data-stu-id="6984b-121"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPeople</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="6984b-122">不允許</span><span class="sxs-lookup"><span data-stu-id="6984b-122">Disallowed</span></span></td>
<td><span data-ttu-id="6984b-123"><strong>HKEY_LOCAL_MACHINE</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \不<strong>允許</strong> \<strong>憑證</strong></span><span class="sxs-lookup"><span data-stu-id="6984b-123"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Disallowed</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6984b-124">CA</span><span class="sxs-lookup"><span data-stu-id="6984b-124">CA</span></span></td>
<td><span data-ttu-id="6984b-125"><strong>HKEY_LOCAL_MACHINE</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \<strong>CA</strong> \<strong>憑證</strong></span><span class="sxs-lookup"><span data-stu-id="6984b-125"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>CA</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="6984b-126">ACR</span><span class="sxs-lookup"><span data-stu-id="6984b-126">ACRS</span></span></td>
<td><span data-ttu-id="6984b-127"><strong>HKEY_LOCAL_MACHINE</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \<strong>Acr</strong> \<strong>Ctl</strong></span><span class="sxs-lookup"><span data-stu-id="6984b-127"><strong>HKEY_LOCAL_MACHINE</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>ACRS</strong>\<strong>CTLs</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td rowspan="7"><span data-ttu-id="6984b-128">使用者 $ {REMOVE} $</span><span class="sxs-lookup"><span data-stu-id="6984b-128">User${REMOVE}$</span></span><br />
</td>
<td><span data-ttu-id="6984b-129">ROOT</span><span class="sxs-lookup"><span data-stu-id="6984b-129">ROOT</span></span></td>
<td><span data-ttu-id="6984b-130"><strong>HKEY_CURRENT_USER</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \<strong>根目錄</strong> \<strong>憑證</strong></span><span class="sxs-lookup"><span data-stu-id="6984b-130"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Root</strong>\<strong>Certificates</strong></span></span><br/></td>
</tr>
<tr class="even">
<td><span data-ttu-id="6984b-131">MY</span><span class="sxs-lookup"><span data-stu-id="6984b-131">MY</span></span></td>
<td><span data-ttu-id="6984b-132">file： \\ %APPDATA%\Microsoft\SystemCertificates\My\Certificates</span><span class="sxs-lookup"><span data-stu-id="6984b-132">file:\\%APPDATA%\Microsoft\SystemCertificates\My\Certificates</span></span></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6984b-133">請求</span><span class="sxs-lookup"><span data-stu-id="6984b-133">REQUEST</span></span></td>
<td><span data-ttu-id="6984b-134">file： \\ %APPDATA%\Microsoft\SystemCertificates\Request\Certificates</span><span class="sxs-lookup"><span data-stu-id="6984b-134">file:\\%APPDATA%\Microsoft\SystemCertificates\Request\Certificates</span></span></td>

</tr>
<tr class="even">
<td><span data-ttu-id="6984b-135">TrustedPublisher</span><span class="sxs-lookup"><span data-stu-id="6984b-135">TrustedPublisher</span></span></td>
<td><span data-ttu-id="6984b-136"><strong>HKEY_CURRENT_USER</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \<strong>TrustedPublisher</strong> \<strong>憑證</strong></span><span class="sxs-lookup"><span data-stu-id="6984b-136"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPublisher</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6984b-137">TrustedPeople</span><span class="sxs-lookup"><span data-stu-id="6984b-137">TrustedPeople</span></span></td>
<td><span data-ttu-id="6984b-138"><strong>HKEY_CURRENT_USER</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \<strong>TrustedPeople</strong> \<strong>憑證</strong></span><span class="sxs-lookup"><span data-stu-id="6984b-138"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>TrustedPeople</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="even">
<td><span data-ttu-id="6984b-139">不允許</span><span class="sxs-lookup"><span data-stu-id="6984b-139">Disallowed</span></span></td>
<td><span data-ttu-id="6984b-140"><strong>HKEY_CURRENT_USER</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \不<strong>允許</strong> \<strong>憑證</strong></span><span class="sxs-lookup"><span data-stu-id="6984b-140"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>Disallowed</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
<tr class="odd">
<td><span data-ttu-id="6984b-141">CA</span><span class="sxs-lookup"><span data-stu-id="6984b-141">CA</span></span></td>
<td><span data-ttu-id="6984b-142"><strong>HKEY_CURRENT_USER</strong> \<strong>軟體</strong> \<strong>Microsoft</strong> \<strong>SystemCertificates</strong> \<strong>CA</strong> \<strong>憑證</strong></span><span class="sxs-lookup"><span data-stu-id="6984b-142"><strong>HKEY_CURRENT_USER</strong>\<strong>SOFTWARE</strong>\<strong>Microsoft</strong>\<strong>SystemCertificates</strong>\<strong>CA</strong>\<strong>Certificates</strong></span></span><br/></td>

</tr>
</tbody>
</table>



 

<span data-ttu-id="6984b-143">依預設，應用程式所建立的其他憑證存放區不會遷移。</span><span class="sxs-lookup"><span data-stu-id="6984b-143">Other certificate stores created by applications are not migrated by default.</span></span> <span data-ttu-id="6984b-144">建立自己的存放區的應用程式會負責遷移其所建立的存放區。</span><span class="sxs-lookup"><span data-stu-id="6984b-144">Applications that create their own stores are responsible for migration of the stores that they create.</span></span> <span data-ttu-id="6984b-145">若要建立存放區，建議您在應用程式設定中定義登錄機碼，並使用 **CERT \_ store \_ >prov \_ REG** 存放區提供者在登錄設定中建立存放區。</span><span class="sxs-lookup"><span data-stu-id="6984b-145">To create stores, we recommend that you define a registry key in the application settings and create a store within the registry settings by using the **CERT\_STORE\_PROV\_REG** store provider.</span></span> <span data-ttu-id="6984b-146">如需有關遷移應用程式設定的詳細資訊，請參閱 *使用 USMT 3.0* 指南中的 *如何建立自訂 .xml* 檔案主題 [消費者狀態移轉工具 3.0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx)。</span><span class="sxs-lookup"><span data-stu-id="6984b-146">For more information about migrating application settings, see the *How To Create a Custom .xml File* topic in the *Using USMT 3.0* guide at [User State Migration Tool 3.0](https://www.microsoft.com/technet/windowsvista/library/91f62fc4-621f-4537-b311-1307df010561.mspx).</span></span> <span data-ttu-id="6984b-147"> (此資源可能無法在某些語言及國家或地區使用。 ) </span><span class="sxs-lookup"><span data-stu-id="6984b-147">(This resource may not be available in some languages and countries or regions.)</span></span>

 

 
