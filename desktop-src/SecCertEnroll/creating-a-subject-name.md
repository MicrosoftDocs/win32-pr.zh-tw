---
description: 您可以使用 IX500DistinguishedName 介面，從辨別名稱字串建立主體名稱。
ms.assetid: 78fbf15a-678f-4d87-a309-e70374e3ecee
title: 建立主體名稱
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7fe512be48c9a727857c4fac4abc6e04a705b7f6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104510961"
---
# <a name="creating-a-subject-name"></a><span data-ttu-id="60071-103">建立主體名稱</span><span class="sxs-lookup"><span data-stu-id="60071-103">Creating a Subject Name</span></span>

<span data-ttu-id="60071-104">您可以使用 [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) 介面，從辨別名稱字串建立主體名稱。</span><span class="sxs-lookup"><span data-stu-id="60071-104">You can use the [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) interface to create a subject name from a distinguished name string.</span></span> <span data-ttu-id="60071-105">字串是由 (RDNs) 的串連相對辨別名稱所組成。</span><span class="sxs-lookup"><span data-stu-id="60071-105">The string consists of concatenated relative distinguished names (RDNs).</span></span> <span data-ttu-id="60071-106">憑證註冊 API 支援下列 RDN 金鑰。</span><span class="sxs-lookup"><span data-stu-id="60071-106">The following RDN keys are supported by the Certificate Enrollment API.</span></span>

| <span data-ttu-id="60071-107">答案</span><span class="sxs-lookup"><span data-stu-id="60071-107">Key</span></span>                               | <span data-ttu-id="60071-108">OID</span><span class="sxs-lookup"><span data-stu-id="60071-108">OID</span></span>                                             | <span data-ttu-id="60071-109">Description</span><span class="sxs-lookup"><span data-stu-id="60071-109">Description</span></span>                                                                                        |
|-----------------------------------|-------------------------------------------------|----------------------------------------------------------------------------------------------------|
| <span data-ttu-id="60071-110">C</span><span class="sxs-lookup"><span data-stu-id="60071-110">C</span></span><br/>                      | <span data-ttu-id="60071-111">XCN \_ OID \_ 國家/地區 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="60071-111">XCN\_OID\_COUNTRY\_NAME</span></span><br/>              | <span data-ttu-id="60071-112">包含兩個字母的 ISO 3166 國家或地區碼。</span><span class="sxs-lookup"><span data-stu-id="60071-112">Contains a two-letter ISO 3166 country or region code.</span></span><br/>                                  |
| <span data-ttu-id="60071-113">CN</span><span class="sxs-lookup"><span data-stu-id="60071-113">CN</span></span><br/>                     | <span data-ttu-id="60071-114">XCN \_ OID \_ 一般 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="60071-114">XCN\_OID\_COMMON\_NAME</span></span><br/>               | <span data-ttu-id="60071-115">包含一般名稱。</span><span class="sxs-lookup"><span data-stu-id="60071-115">Contains a common name.</span></span><br/>                                                                 |
| <span data-ttu-id="60071-116">E</span><span class="sxs-lookup"><span data-stu-id="60071-116">E</span></span><br/> <span data-ttu-id="60071-117">電子郵件</span><span class="sxs-lookup"><span data-stu-id="60071-117">EMAIL</span></span><br/>     | <span data-ttu-id="60071-118">XCN \_ OID \_ RSA \_ emailAddr</span><span class="sxs-lookup"><span data-stu-id="60071-118">XCN\_OID\_RSA\_emailAddr</span></span><br/>             | <span data-ttu-id="60071-119">包含電子郵件地址。</span><span class="sxs-lookup"><span data-stu-id="60071-119">Contains an email address.</span></span><br/>                                                              |
| <span data-ttu-id="60071-120">DC</span><span class="sxs-lookup"><span data-stu-id="60071-120">DC</span></span><br/>                     | <span data-ttu-id="60071-121">XCN \_ OID \_ 網域 \_ 元件</span><span class="sxs-lookup"><span data-stu-id="60071-121">XCN\_OID\_DOMAIN\_COMPONENT</span></span><br/>          | <span data-ttu-id="60071-122">包含網域名稱系統 (DNS) 名稱的其中一個部分。</span><span class="sxs-lookup"><span data-stu-id="60071-122">Contains one part of a Domain Name System (DNS) name.</span></span><br/>                                   |
| <span data-ttu-id="60071-123">G</span><span class="sxs-lookup"><span data-stu-id="60071-123">G</span></span><br/> <span data-ttu-id="60071-124">GivenName</span><span class="sxs-lookup"><span data-stu-id="60071-124">GivenName</span></span><br/> | <span data-ttu-id="60071-125">XCN \_ \_ 指定 \_ 名稱的 OID</span><span class="sxs-lookup"><span data-stu-id="60071-125">XCN\_OID\_GIVEN\_NAME</span></span><br/>                | <span data-ttu-id="60071-126">包含個人名稱中不是姓氏的部分。</span><span class="sxs-lookup"><span data-stu-id="60071-126">Contains the part of a person's name that is not a surname.</span></span><br/>                             |
| <span data-ttu-id="60071-127">I</span><span class="sxs-lookup"><span data-stu-id="60071-127">I</span></span><br/>                      | <span data-ttu-id="60071-128">XCN \_ OID \_ 縮寫</span><span class="sxs-lookup"><span data-stu-id="60071-128">XCN\_OID\_INITIALS</span></span><br/>                   | <span data-ttu-id="60071-129">包含人員的縮寫。</span><span class="sxs-lookup"><span data-stu-id="60071-129">Contains a person's initials.</span></span><br/>                                                           |
| <span data-ttu-id="60071-130">L</span><span class="sxs-lookup"><span data-stu-id="60071-130">L</span></span><br/>                      | <span data-ttu-id="60071-131">XCN \_ OID \_ 位置 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="60071-131">XCN\_OID\_LOCALITY\_NAME</span></span><br/>             | <span data-ttu-id="60071-132">包含識別城市、國家/地區或其他地理區域的位置名稱。</span><span class="sxs-lookup"><span data-stu-id="60071-132">Contains the locality name that identifies a city, country, or other geographic region.</span></span><br/> |
| <span data-ttu-id="60071-133">O</span><span class="sxs-lookup"><span data-stu-id="60071-133">O</span></span><br/>                      | <span data-ttu-id="60071-134">XCN \_ OID \_ 組織 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="60071-134">XCN\_OID\_ORGANIZATION\_NAME</span></span><br/>         | <span data-ttu-id="60071-135">包含組織的名稱。</span><span class="sxs-lookup"><span data-stu-id="60071-135">Contains the name of an organization.</span></span><br/>                                                   |
| <span data-ttu-id="60071-136">OU</span><span class="sxs-lookup"><span data-stu-id="60071-136">OU</span></span><br/>                     | <span data-ttu-id="60071-137">XCN \_ OID \_ 組織 \_ 單位 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="60071-137">XCN\_OID\_ORGANIZATIONAL\_UNIT\_NAME</span></span><br/> | <span data-ttu-id="60071-138">包含組織內單位細分的名稱。</span><span class="sxs-lookup"><span data-stu-id="60071-138">Contains the name of a unit subdivision within an organization.</span></span><br/>                         |
| <span data-ttu-id="60071-139">S</span><span class="sxs-lookup"><span data-stu-id="60071-139">S</span></span><br/> <span data-ttu-id="60071-140">ST</span><span class="sxs-lookup"><span data-stu-id="60071-140">ST</span></span><br/>        | <span data-ttu-id="60071-141">XCN \_ OID \_ 州名 \_ 或 \_ 省份 \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="60071-141">XCN\_OID\_STATE\_OR\_PROVINCE\_NAME</span></span><br/>  | <span data-ttu-id="60071-142">包含州或省的完整名稱。</span><span class="sxs-lookup"><span data-stu-id="60071-142">Contains the full name of a state or province.</span></span><br/>                                          |
| <span data-ttu-id="60071-143">STREET</span><span class="sxs-lookup"><span data-stu-id="60071-143">STREET</span></span><br/>                 | <span data-ttu-id="60071-144">XCN \_ OID \_ 街道 \_ 位址</span><span class="sxs-lookup"><span data-stu-id="60071-144">XCN\_OID\_STREET\_ADDRESS</span></span><br/>            | <span data-ttu-id="60071-145">包含實體位址。</span><span class="sxs-lookup"><span data-stu-id="60071-145">Contains the physical address.</span></span><br/>                                                          |
| <span data-ttu-id="60071-146">SN</span><span class="sxs-lookup"><span data-stu-id="60071-146">SN</span></span><br/>                     | <span data-ttu-id="60071-147">XCN \_ OID \_ SUR \_ 名稱</span><span class="sxs-lookup"><span data-stu-id="60071-147">XCN\_OID\_SUR\_NAME</span></span><br/>                  | <span data-ttu-id="60071-148">包含人員的系列名稱。</span><span class="sxs-lookup"><span data-stu-id="60071-148">Contains the family name of a person.</span></span><br/>                                                   |
| <span data-ttu-id="60071-149">T</span><span class="sxs-lookup"><span data-stu-id="60071-149">T</span></span><br/> <span data-ttu-id="60071-150">TITLE</span><span class="sxs-lookup"><span data-stu-id="60071-150">TITLE</span></span><br/>     | <span data-ttu-id="60071-151">XCN \_ OID \_ 標題</span><span class="sxs-lookup"><span data-stu-id="60071-151">XCN\_OID\_TITLE</span></span><br/>                      | <span data-ttu-id="60071-152">包含組織中人員的標題。</span><span class="sxs-lookup"><span data-stu-id="60071-152">Contains the title of a person in the organization.</span></span><br/>                                     |



 

<span data-ttu-id="60071-153">當您初始化 [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) 物件時，您可以藉由指定 [**X500NameFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-x500nameflags) 列舉型別中的值，來識別辨別名稱的格式。</span><span class="sxs-lookup"><span data-stu-id="60071-153">When you initialize an [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object, you can identify the format of the distinguished name by specifying a value from the [**X500NameFlags**](/windows/desktop/api/CertEnroll/ne-certenroll-x500nameflags) enumeration type.</span></span> <span data-ttu-id="60071-154">例如，假設主體辨別名稱是由下列 RDNs 所組成：</span><span class="sxs-lookup"><span data-stu-id="60071-154">For example, assume that the subject distinguished name consists of the following RDNs:</span></span><dl> <span data-ttu-id="60071-155">CN = 系統管理員</span><span class="sxs-lookup"><span data-stu-id="60071-155">CN=Administrator</span></span>  
<span data-ttu-id="60071-156">CN = Users</span><span class="sxs-lookup"><span data-stu-id="60071-156">CN=Users</span></span>  
<span data-ttu-id="60071-157">DC = jdomcsc</span><span class="sxs-lookup"><span data-stu-id="60071-157">DC=jdomcsc</span></span>  
<span data-ttu-id="60071-158">DC = nttest</span><span class="sxs-lookup"><span data-stu-id="60071-158">DC=nttest</span></span>  
<span data-ttu-id="60071-159">DC = microsoft</span><span class="sxs-lookup"><span data-stu-id="60071-159">DC=microsoft</span></span>  
<span data-ttu-id="60071-160">DC = com</span><span class="sxs-lookup"><span data-stu-id="60071-160">DC=com</span></span>  
</dl>

<span data-ttu-id="60071-161">如果您將這些 RDNs 串連成下列以逗號分隔的辨別名稱字串，您可以在初始化 [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname)物件時，指定 **XCN \_ CERT \_ name \_ STR \_ 逗點 \_ 旗** 標值。</span><span class="sxs-lookup"><span data-stu-id="60071-161">If you concatenate these RDNs into the following comma-delimited distinguished name string, you can specify the **XCN\_CERT\_NAME\_STR\_COMMA\_FLAG** value when initializing an [**IX500DistinguishedName**](/windows/desktop/api/CertEnroll/nn-certenroll-ix500distinguishedname) object.</span></span>

``` syntax
CN=Administrator,CN=Users,DC=jdomcsc,DC=nttest,DC=microsoft,DC=com
```

## <a name="related-topics"></a><span data-ttu-id="60071-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="60071-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="60071-163">編碼主體名稱</span><span class="sxs-lookup"><span data-stu-id="60071-163">Encoding a Subject Name</span></span>](encoding-a-subject-name.md)
</dt> <dt>

[<span data-ttu-id="60071-164">主體名稱</span><span class="sxs-lookup"><span data-stu-id="60071-164">Subject Names</span></span>](subject-names.md)
</dt> </dl>

 

 




