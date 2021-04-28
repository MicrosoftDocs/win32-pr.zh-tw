---
description: OPM 憑證撤銷
ms.assetid: 21faf809-1335-4d93-be06-628c5a05a4c8
title: OPM 憑證撤銷
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47ebf38a3fa6bd2b61a756d6103453fd0356f693
ms.sourcegitcommit: 95685061d5b0333bbf9e6ebd208dde8190f97005
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "108092726"
---
# <a name="opm-certificate-revocation"></a><span data-ttu-id="3ee84-103">OPM 憑證撤銷</span><span class="sxs-lookup"><span data-stu-id="3ee84-103">OPM Certificate Revocation</span></span>

<span data-ttu-id="3ee84-104">OPM) 憑證的輸出保護管理員 (可由 Microsoft 撤銷。</span><span class="sxs-lookup"><span data-stu-id="3ee84-104">An output protection manager (OPM) certificate can be revoked by Microsoft.</span></span> <span data-ttu-id="3ee84-105">撤銷的憑證清單會儲存在全域撤銷清單中， (GRL) 。</span><span class="sxs-lookup"><span data-stu-id="3ee84-105">The list of revoked certificates is stored in a global revocation list (GRL).</span></span> <span data-ttu-id="3ee84-106">GRL 的格式如下：</span><span class="sxs-lookup"><span data-stu-id="3ee84-106">The GRL has the following format:</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3ee84-107">區段</span><span class="sxs-lookup"><span data-stu-id="3ee84-107">Section</span></span></th>
<th><span data-ttu-id="3ee84-108">描述</span><span class="sxs-lookup"><span data-stu-id="3ee84-108">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="3ee84-109">標頭</span><span class="sxs-lookup"><span data-stu-id="3ee84-109">Header</span></span></td>
<td><span data-ttu-id="3ee84-110"><a href="grl-header.md"><strong>GRL_HEADER</strong></a>結構。</span><span class="sxs-lookup"><span data-stu-id="3ee84-110">A <a href="grl-header.md"><strong>GRL_HEADER</strong></a> structure.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ee84-111">核心</span><span class="sxs-lookup"><span data-stu-id="3ee84-111">Core</span></span></td>
<td><span data-ttu-id="3ee84-112">包含下列撤銷清單：</span><span class="sxs-lookup"><span data-stu-id="3ee84-112">Contains the following revocation lists:</span></span>
<ul>
<li><span data-ttu-id="3ee84-113">核心二進位檔撤銷</span><span class="sxs-lookup"><span data-stu-id="3ee84-113">Kernel binary revocations</span></span></li>
<li><span data-ttu-id="3ee84-114">使用者模式二進位撤銷</span><span class="sxs-lookup"><span data-stu-id="3ee84-114">User-mode binary revocations</span></span></li>
<li><span data-ttu-id="3ee84-115">憑證撤銷</span><span class="sxs-lookup"><span data-stu-id="3ee84-115">Certificate revocations</span></span></li>
<li><span data-ttu-id="3ee84-116">受信任的根 (保留) </span><span class="sxs-lookup"><span data-stu-id="3ee84-116">Trusted roots (reserved)</span></span></li>
</ul>
<span data-ttu-id="3ee84-117">受信任的根目錄清單目前未使用，並保留供日後使用。</span><span class="sxs-lookup"><span data-stu-id="3ee84-117">The list of trusted roots is currently not used, and is reserved for future use.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ee84-118">可擴充專案</span><span class="sxs-lookup"><span data-stu-id="3ee84-118">Extensible entries</span></span></td>
<td><span data-ttu-id="3ee84-119">包含其他元件所使用的資訊。</span><span class="sxs-lookup"><span data-stu-id="3ee84-119">Contains information used by other components.</span></span> <span data-ttu-id="3ee84-120">本節與 OPM 無關。</span><span class="sxs-lookup"><span data-stu-id="3ee84-120">This section is not relevant to OPM.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ee84-121">更新：</span><span class="sxs-lookup"><span data-stu-id="3ee84-121">Renewals:</span></span></td>
<td><span data-ttu-id="3ee84-122">包含定義 Windows Update 識別碼的 Guid。</span><span class="sxs-lookup"><span data-stu-id="3ee84-122">Contains GUIDs that define Windows Update identifiers.</span></span> <span data-ttu-id="3ee84-123">本節包含下列清單的識別碼：</span><span class="sxs-lookup"><span data-stu-id="3ee84-123">This section contains identifiers for the following lists:</span></span>
<ul>
<li><span data-ttu-id="3ee84-124">核心二進位檔撤銷</span><span class="sxs-lookup"><span data-stu-id="3ee84-124">Kernel binary revocations</span></span></li>
<li><span data-ttu-id="3ee84-125">使用者模式二進位撤銷</span><span class="sxs-lookup"><span data-stu-id="3ee84-125">User-mode binary revocations</span></span></li>
<li><span data-ttu-id="3ee84-126">憑證撤銷</span><span class="sxs-lookup"><span data-stu-id="3ee84-126">Certificate revocations</span></span></li>
</ul>
<span data-ttu-id="3ee84-127">應用程式可以使用這些識別碼來要求已撤銷之二進位檔的更新版本（如果有的話）。</span><span class="sxs-lookup"><span data-stu-id="3ee84-127">An application can use these identifiers to request a renewed version of a revoked binary, if one is available.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="3ee84-128">簽名：核心區段</span><span class="sxs-lookup"><span data-stu-id="3ee84-128">Signature: Core section</span></span></td>
<td><span data-ttu-id="3ee84-129">簽署標頭和核心區段。</span><span class="sxs-lookup"><span data-stu-id="3ee84-129">Signs the header and core sections.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="3ee84-130">簽名：可擴充區段</span><span class="sxs-lookup"><span data-stu-id="3ee84-130">Signature: Extensible section</span></span></td>
<td><span data-ttu-id="3ee84-131">簽署標頭和可擴充區段。</span><span class="sxs-lookup"><span data-stu-id="3ee84-131">Signs the header and extensible sections.</span></span></td>
</tr>
</tbody>
</table>



 

<span data-ttu-id="3ee84-132">GRL 標頭是一個 [**grl \_ 標頭**](grl-header.md) 結構。</span><span class="sxs-lookup"><span data-stu-id="3ee84-132">The GRL header is a [**GRL\_HEADER**](grl-header.md) structure.</span></span> <span data-ttu-id="3ee84-133">結構的 **dwSequenceNumber** 成員包含 GRL 版本號碼。</span><span class="sxs-lookup"><span data-stu-id="3ee84-133">The **dwSequenceNumber** member of the structure contains the GRL version number.</span></span> <span data-ttu-id="3ee84-134">每次更新 GRL 並將新版本放置在使用者的電腦上時，這個數位就會遞增。</span><span class="sxs-lookup"><span data-stu-id="3ee84-134">This number is incremented whenever the GRL is updated and a new version placed on the user's computer.</span></span>

<span data-ttu-id="3ee84-135">已撤銷的 OPM 憑證會列在 [核心] 區段的 [憑證撤銷] 清單中。</span><span class="sxs-lookup"><span data-stu-id="3ee84-135">Revoked OPM certificates are listed in the certificate revocations list of the Core section.</span></span> <span data-ttu-id="3ee84-136">在 GRL 中的每個核心專案都是一個20位元組陣列，其中包含已撤銷憑證之公開金鑰的 SHA-1 雜湊。</span><span class="sxs-lookup"><span data-stu-id="3ee84-136">Each Core entry in the GRL is a 20-byte array that contains the SHA-1 hash of the public key of the revoked certificate.</span></span>

<span data-ttu-id="3ee84-137">簽章區段包含簽章，可用來驗證 GRL 是否未遭到篡改。</span><span class="sxs-lookup"><span data-stu-id="3ee84-137">The Signature sections contains signatures that can be used to verify that the GRL has not been tampered with.</span></span> <span data-ttu-id="3ee84-138">每個簽章區段都包含 MF 簽章結構。 [**\_**](mf-signature.md)</span><span class="sxs-lookup"><span data-stu-id="3ee84-138">Each Signature sections contains am [**MF\_SIGNATURE**](mf-signature.md) structure.</span></span> <span data-ttu-id="3ee84-139">第一個簽章會將標頭加上核心區段。</span><span class="sxs-lookup"><span data-stu-id="3ee84-139">The first signature signs the header plus the Core section.</span></span> <span data-ttu-id="3ee84-140">第二個簽章會簽署標頭加上可延伸區段;此簽章與 OPM 無關。</span><span class="sxs-lookup"><span data-stu-id="3ee84-140">The second signature signs the header plus the Extensible section; this signature is not relevant to OPM.</span></span>

<span data-ttu-id="3ee84-141">若要確定 GRL 本身尚未遭篡改，請驗證簽章，如下所示：</span><span class="sxs-lookup"><span data-stu-id="3ee84-141">To ensure that the GRL itself has not been tampered with, verify the signature as follows:</span></span>

1.  <span data-ttu-id="3ee84-142">找出 MF 簽章 [**結構 \_**](mf-signature.md) 的開始。</span><span class="sxs-lookup"><span data-stu-id="3ee84-142">Find the start of the [**MF\_SIGNATURE**](mf-signature.md) structure.</span></span> <span data-ttu-id="3ee84-143">在 [**GRL \_ 標頭**](grl-header.md)結構的 **cbSignatureCoreOffset** 成員中會提供 MF 簽章結構的位置。 **\_**</span><span class="sxs-lookup"><span data-stu-id="3ee84-143">The location of the **MF\_SIGNATURE** structure is given in the **cbSignatureCoreOffset** member of the [**GRL\_HEADER**](grl-header.md) structure.</span></span> <span data-ttu-id="3ee84-144">位置會指定為從 GRL 開頭算起的位移（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="3ee84-144">The location is specified as an offset in bytes from the start of the GRL.</span></span>
2.  <span data-ttu-id="3ee84-145">使用憑證鏈將 MF 簽章結構剖析為 PKCS 7 簽章 [**\_**](mf-signature.md) \# 。</span><span class="sxs-lookup"><span data-stu-id="3ee84-145">Parse the [**MF\_SIGNATURE**](mf-signature.md) structure as a PKCS \#7 signature with a certificate chain.</span></span>
3.  <span data-ttu-id="3ee84-146">確認憑證鏈對受信任的根。</span><span class="sxs-lookup"><span data-stu-id="3ee84-146">Verify the certificate chain up to a trusted root.</span></span>
4.  <span data-ttu-id="3ee84-147">確認在 EKU 中的分葉憑證具有下列物件識別碼： "1.3.6.1.4.1.311.10.5.4"。</span><span class="sxs-lookup"><span data-stu-id="3ee84-147">Verify that the leaf certificate has the following object identifier in the EKU: "1.3.6.1.4.1.311.10.5.4".</span></span>
5.  <span data-ttu-id="3ee84-148">計算包含標頭的位元組雜湊以及 GRL 的核心區段。</span><span class="sxs-lookup"><span data-stu-id="3ee84-148">Compute a hash of the bytes that include the header and the core sections of the GRL.</span></span>
6.  <span data-ttu-id="3ee84-149">確認雜湊符合分葉憑證中的簽章。</span><span class="sxs-lookup"><span data-stu-id="3ee84-149">Verify that the hash matches the signature in the leaf certificate.</span></span>

## <a name="related-topics"></a><span data-ttu-id="3ee84-150">相關主題</span><span class="sxs-lookup"><span data-stu-id="3ee84-150">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="3ee84-151">輸出保護管理員</span><span class="sxs-lookup"><span data-stu-id="3ee84-151">Output Protection Manager</span></span>](output-protection-manager.md)
</dt> <dt>

[<span data-ttu-id="3ee84-152">**GRL \_ 標頭**</span><span class="sxs-lookup"><span data-stu-id="3ee84-152">**GRL\_HEADER**</span></span>](grl-header.md)
</dt> <dt>

[<span data-ttu-id="3ee84-153">**MF \_ 簽章**</span><span class="sxs-lookup"><span data-stu-id="3ee84-153">**MF\_SIGNATURE**</span></span>](mf-signature.md)
</dt> </dl>

 

 



