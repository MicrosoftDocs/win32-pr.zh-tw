---
description: Windows 公開金鑰基礎結構 (PKI) 將憑證儲存在裝載證書 (頒發機構單位的伺服器上) 以及本機電腦或裝置上。
ms.assetid: b6aaafeb-30d1-453e-a70c-dcaa01fea1cf
title: 憑證目錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee525e4d910de1c75516c6aaa27ca41a6cfa17c3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195410"
---
# <a name="certificate-directory"></a><span data-ttu-id="66201-103">憑證目錄</span><span class="sxs-lookup"><span data-stu-id="66201-103">Certificate Directory</span></span>

<span data-ttu-id="66201-104">Windows 公開金鑰基礎結構 (PKI) 將憑證儲存在裝載證書 (頒發機構單位的伺服器上) 以及本機電腦或裝置上。</span><span class="sxs-lookup"><span data-stu-id="66201-104">A Windows public key infrastructure (PKI) saves certificates on the server that hosts the certification authority (CA) and on the local computer or device.</span></span> <span data-ttu-id="66201-105">CA 儲存體通常稱為憑證資料庫，而本機儲存體則稱為「憑證存放區」。</span><span class="sxs-lookup"><span data-stu-id="66201-105">CA storage is typically referred to as the certificate database, and local storage is known as the certificate store.</span></span>

## <a name="certificate-database"></a><span data-ttu-id="66201-106">憑證資料庫</span><span class="sxs-lookup"><span data-stu-id="66201-106">Certificate Database</span></span>

<span data-ttu-id="66201-107">當您在 Windows server 上新增憑證服務並設定 CA 時，會建立憑證資料庫。</span><span class="sxs-lookup"><span data-stu-id="66201-107">When you add Certificate Services on a Windows server and configure a CA, a certificate database is created.</span></span> <span data-ttu-id="66201-108">根據預設，資料庫會包含在 *% SystemRoot%* \\ System32 \\ Certlog 資料夾中，而且名稱會以 .edb 副檔名的 CA 名稱為基礎。</span><span class="sxs-lookup"><span data-stu-id="66201-108">By default, the database is contained in the *%SystemRoot%*\\System32\\Certlog folder, and the name is based on the CA name with an .edb extension.</span></span> <span data-ttu-id="66201-109">資料庫可包含：</span><span class="sxs-lookup"><span data-stu-id="66201-109">The database can contain:</span></span>

-   <span data-ttu-id="66201-110">發行的憑證</span><span class="sxs-lookup"><span data-stu-id="66201-110">Issued certificates</span></span>
-   <span data-ttu-id="66201-111">撤銷的憑證</span><span class="sxs-lookup"><span data-stu-id="66201-111">Revoked certificates</span></span>
-   <span data-ttu-id="66201-112">封存的私密金鑰</span><span class="sxs-lookup"><span data-stu-id="66201-112">Archived private keys</span></span>
-   <span data-ttu-id="66201-113">憑證要求</span><span class="sxs-lookup"><span data-stu-id="66201-113">Certificate requests</span></span>

<span data-ttu-id="66201-114">您無法使用憑證註冊 API 來運算元據庫。</span><span class="sxs-lookup"><span data-stu-id="66201-114">You cannot use the Certificate Enrollment API to manipulate the database.</span></span> <span data-ttu-id="66201-115">註冊程式會自動建立所需的專案。</span><span class="sxs-lookup"><span data-stu-id="66201-115">The enrollment process automatically creates the necessary entries.</span></span>

## <a name="certificate-stores"></a><span data-ttu-id="66201-116">憑證存放區</span><span class="sxs-lookup"><span data-stu-id="66201-116">Certificate Stores</span></span>

<span data-ttu-id="66201-117">Microsoft 憑證服務會將發出的憑證和擱置或拒絕的要求複製到本機電腦和裝置。</span><span class="sxs-lookup"><span data-stu-id="66201-117">Microsoft Certificate Services copies issued certificates and pending or rejected requests to local computers and devices.</span></span> <span data-ttu-id="66201-118">儲存位置稱為憑證存放區，並由下列邏輯存放區所組成。</span><span class="sxs-lookup"><span data-stu-id="66201-118">The storage location is called the certificate store and consists of the following logical stores.</span></span>

| <span data-ttu-id="66201-119">邏輯存放區</span><span class="sxs-lookup"><span data-stu-id="66201-119">Logical store</span></span>                                         | <span data-ttu-id="66201-120">Description</span><span class="sxs-lookup"><span data-stu-id="66201-120">Description</span></span>                                                                                                            |
|-------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="66201-121">個人</span><span class="sxs-lookup"><span data-stu-id="66201-121">Personal</span></span><br/>                                   | <span data-ttu-id="66201-122">包含與使用者或電腦所控制之私密金鑰相關聯的憑證。</span><span class="sxs-lookup"><span data-stu-id="66201-122">Contains certificates associated with a private key controlled by the user or computer.</span></span><br/>                     |
| <span data-ttu-id="66201-123">可信任的根憑證授權單位</span><span class="sxs-lookup"><span data-stu-id="66201-123">Trusted Root Certification Authorities</span></span><br/>     | <span data-ttu-id="66201-124">包含隱含信任的憑證授權單位單位)  (Ca 的憑證。</span><span class="sxs-lookup"><span data-stu-id="66201-124">Contains certificates from implicitly trusted certification authorities (CAs).</span></span><br/>                              |
| <span data-ttu-id="66201-125">企業信任</span><span class="sxs-lookup"><span data-stu-id="66201-125">Enterprise Trust</span></span><br/>                           | <span data-ttu-id="66201-126">包含通常用來信任來自其他組織之自我簽署憑證的憑證信任清單。</span><span class="sxs-lookup"><span data-stu-id="66201-126">Contains certificate trust lists typically used to trust self-signed certificates from other organizations.</span></span><br/> |
| <span data-ttu-id="66201-127">中繼憑證授權單位</span><span class="sxs-lookup"><span data-stu-id="66201-127">Intermediate Certification Authorities</span></span><br/>     | <span data-ttu-id="66201-128">包含對證書階層中的次級 Ca 發出的憑證。</span><span class="sxs-lookup"><span data-stu-id="66201-128">Contains certificates issued to subordinate CAs in the certification hierarchy.</span></span><br/>                             |
| <span data-ttu-id="66201-129">Active Directory 使用者物件</span><span class="sxs-lookup"><span data-stu-id="66201-129">Active Directory User Object</span></span><br/>               | <span data-ttu-id="66201-130">包含 Active Directory 中發佈的使用者物件憑證或憑證。</span><span class="sxs-lookup"><span data-stu-id="66201-130">Contains the user object certificate or certificates published in Active Directory.</span></span><br/>                         |
| <span data-ttu-id="66201-131">受信任的發行者</span><span class="sxs-lookup"><span data-stu-id="66201-131">Trusted Publishers</span></span><br/>                         | <span data-ttu-id="66201-132">包含來自信任的 Ca 的憑證。</span><span class="sxs-lookup"><span data-stu-id="66201-132">Contains certificates from trusted CAs.</span></span><br/>                                                                     |
| <span data-ttu-id="66201-133">未受信任的憑證</span><span class="sxs-lookup"><span data-stu-id="66201-133">Untrusted Certificates</span></span><br/>                     | <span data-ttu-id="66201-134">包含已明確識別為未受信任的憑證。</span><span class="sxs-lookup"><span data-stu-id="66201-134">Contains certificates that have been explicitly identified as untrusted.</span></span><br/>                                    |
| <span data-ttu-id="66201-135">第三方根憑證授權單位</span><span class="sxs-lookup"><span data-stu-id="66201-135">Third-Party Root Certification Authorities</span></span><br/> | <span data-ttu-id="66201-136">包含來自內部憑證階層以外之 Ca 的受信任根憑證。</span><span class="sxs-lookup"><span data-stu-id="66201-136">Contains trusted root certificates from CAs outside the internal certificate hierarchy.</span></span><br/>                     |
| <span data-ttu-id="66201-137">受信任的人</span><span class="sxs-lookup"><span data-stu-id="66201-137">Trusted People</span></span><br/>                             | <span data-ttu-id="66201-138">包含發給已明確信任之使用者或實體的憑證。</span><span class="sxs-lookup"><span data-stu-id="66201-138">Contains certificates issued to users or entities that have been explicitly trusted.</span></span><br/>                        |
| <span data-ttu-id="66201-139">其他人</span><span class="sxs-lookup"><span data-stu-id="66201-139">Other People</span></span><br/>                               | <span data-ttu-id="66201-140">包含發給已隱含信任之使用者或實體的憑證。</span><span class="sxs-lookup"><span data-stu-id="66201-140">Contains certificates issued to users or entities that have been implicitly trusted.</span></span><br/>                        |
| <span data-ttu-id="66201-141">憑證註冊要求</span><span class="sxs-lookup"><span data-stu-id="66201-141">Certificate Enrollment Requests</span></span><br/>            | <span data-ttu-id="66201-142">包含暫止或已拒絕的憑證要求。</span><span class="sxs-lookup"><span data-stu-id="66201-142">Contains pending or rejected certificate requests.</span></span><br/>                                                          |



 

<span data-ttu-id="66201-143">您無法使用憑證註冊 API 來指定或抓取存放區屬性，或將憑證複製到特定存放區。</span><span class="sxs-lookup"><span data-stu-id="66201-143">You cannot use the Certificate Enrollment API to specify or retrieve store properties or copy certificates to specific stores.</span></span>

## <a name="related-topics"></a><span data-ttu-id="66201-144">相關主題</span><span class="sxs-lookup"><span data-stu-id="66201-144">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="66201-145">PKI 元素</span><span class="sxs-lookup"><span data-stu-id="66201-145">PKI Elements</span></span>](about-pki-components.md)
</dt> </dl>

 

 




