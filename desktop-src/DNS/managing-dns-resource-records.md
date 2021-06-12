---
title: 管理 DNS 資源記錄
description: 瞭解如何管理資源記錄。 資源記錄是 DNS 區域檔案中的資訊專案單位，用來解析所有 DNS 查詢。
ms.assetid: ddad5f14-5a2d-4966-87b7-b354666f9e24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ba6c818899414cc541a1c89bfd11747051b2f5f1
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011111"
---
# <a name="managing-dns-resource-records"></a><span data-ttu-id="43498-104">管理 DNS 資源記錄</span><span class="sxs-lookup"><span data-stu-id="43498-104">Managing DNS Resource Records</span></span>

<span data-ttu-id="43498-105">資源記錄（通常稱為 RR）是 DNS 區域檔案中的資訊專案單位。Rr 是主機名稱和 IP 資訊的基本組建區塊，可用來解析所有 DNS 查詢。</span><span class="sxs-lookup"><span data-stu-id="43498-105">A resource record, commonly referred to as an RR, is the unit of information entry in DNS zone files; RRs are the basic building blocks of host-name and IP information and are used to resolve all DNS queries.</span></span> <span data-ttu-id="43498-106">資源記錄會有相當廣泛的類型，以提供擴充的名稱解析服務。</span><span class="sxs-lookup"><span data-stu-id="43498-106">Resource records come in a fairly wide variety of types in order to provide extended name-resolution services.</span></span>

<span data-ttu-id="43498-107">不同類型的 Rr 具有不同的格式，因為它們包含不同的資料。</span><span class="sxs-lookup"><span data-stu-id="43498-107">Different types of RRs have different formats, as they contain different data.</span></span> <span data-ttu-id="43498-108">許多 Rr 共用一個通用的格式。</span><span class="sxs-lookup"><span data-stu-id="43498-108">Many RRs share a common format.</span></span> <span data-ttu-id="43498-109">每一部 DNS 伺服器都會包含其所授權之命名空間部分的 Rr。</span><span class="sxs-lookup"><span data-stu-id="43498-109">Each DNS Server contains RRs for the portion of the name space for which it is authoritative.</span></span>

<span data-ttu-id="43498-110">DNS WMI 提供者目前支援下列 RR 類型。</span><span class="sxs-lookup"><span data-stu-id="43498-110">The DNS WMI Provider currently supports the following RR types.</span></span> <span data-ttu-id="43498-111">按一下資源記錄的名稱，以跳至其參考頁面。</span><span class="sxs-lookup"><span data-stu-id="43498-111">Click the name of the resource record to jump to its reference page.</span></span>



| <span data-ttu-id="43498-112">提供者) 中的資源記錄 (</span><span class="sxs-lookup"><span data-stu-id="43498-112">Resource Record (in provider)</span></span>                             | <span data-ttu-id="43498-113">Description</span><span class="sxs-lookup"><span data-stu-id="43498-113">Description</span></span>                                                  |
|-----------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="43498-114">**MicrosoftDNS \_ AType**</span><span class="sxs-lookup"><span data-stu-id="43498-114">**MicrosoftDNS\_AType**</span></span>](microsoftdns-atype.md)         | <span data-ttu-id="43498-115">位址對應記錄的名稱</span><span class="sxs-lookup"><span data-stu-id="43498-115">Name to address mapping record</span></span>                               |
| [<span data-ttu-id="43498-116">**MicrosoftDNS \_ AAAAType**</span><span class="sxs-lookup"><span data-stu-id="43498-116">**MicrosoftDNS\_AAAAType**</span></span>](microsoftdns-aaaatype.md)   | <span data-ttu-id="43498-117">主機至 Ipv6 地址記錄</span><span class="sxs-lookup"><span data-stu-id="43498-117">Host to Ipv6 address record</span></span>                                  |
| [<span data-ttu-id="43498-118">**MicrosoftDNS \_ AFSDBType**</span><span class="sxs-lookup"><span data-stu-id="43498-118">**MicrosoftDNS\_AFSDBType**</span></span>](microsoftdns-afsdbtype.md) | <span data-ttu-id="43498-119">Andrew 檔案系統資料庫伺服器記錄</span><span class="sxs-lookup"><span data-stu-id="43498-119">Andrew File System Database Server record</span></span>                    |
| [<span data-ttu-id="43498-120">**MicrosoftDNS \_ ATMAType**</span><span class="sxs-lookup"><span data-stu-id="43498-120">**MicrosoftDNS\_ATMAType**</span></span>](microsoftdns-atmatype.md)   | <span data-ttu-id="43498-121">ATM 位址對名稱記錄</span><span class="sxs-lookup"><span data-stu-id="43498-121">ATM address-to-name record</span></span>                                   |
| [<span data-ttu-id="43498-122">**MicrosoftDNS \_ CNAMEType**</span><span class="sxs-lookup"><span data-stu-id="43498-122">**MicrosoftDNS\_CNAMEType**</span></span>](microsoftdns-cnametype.md) | <span data-ttu-id="43498-123">正式 [*名稱*](c-gly.md)記錄</span><span class="sxs-lookup"><span data-stu-id="43498-123">[*Canonical Name*](c-gly.md) record</span></span> |
| [<span data-ttu-id="43498-124">**MicrosoftDNS \_ HINFOType**</span><span class="sxs-lookup"><span data-stu-id="43498-124">**MicrosoftDNS\_HINFOType**</span></span>](microsoftdns-hinfotype.md) | <span data-ttu-id="43498-125">主機資訊記錄</span><span class="sxs-lookup"><span data-stu-id="43498-125">Host Information record</span></span>                                      |
| [<span data-ttu-id="43498-126">**MicrosoftDNS \_ ISDNType**</span><span class="sxs-lookup"><span data-stu-id="43498-126">**MicrosoftDNS\_ISDNType**</span></span>](microsoftdns-isdntype.md)   | <span data-ttu-id="43498-127">整合式服務數位網路記錄</span><span class="sxs-lookup"><span data-stu-id="43498-127">Integrated services digital network record</span></span>                   |
| [<span data-ttu-id="43498-128">**MicrosoftDNS \_ KEYType**</span><span class="sxs-lookup"><span data-stu-id="43498-128">**MicrosoftDNS\_KEYType**</span></span>](microsoftdns-keytype.md)     | <span data-ttu-id="43498-129">索引鍵記錄。</span><span class="sxs-lookup"><span data-stu-id="43498-129">KEY record.</span></span> <span data-ttu-id="43498-130">請參閱 RFC 2535</span><span class="sxs-lookup"><span data-stu-id="43498-130">See RFC 2535</span></span>                                     |
| [<span data-ttu-id="43498-131">**MicrosoftDNS \_ MBType**</span><span class="sxs-lookup"><span data-stu-id="43498-131">**MicrosoftDNS\_MBType**</span></span>](microsoftdns-mbtype.md)       | <span data-ttu-id="43498-132">信箱記錄</span><span class="sxs-lookup"><span data-stu-id="43498-132">Mailbox record</span></span>                                               |
| [<span data-ttu-id="43498-133">**MicrosoftDNS \_ MDType**</span><span class="sxs-lookup"><span data-stu-id="43498-133">**MicrosoftDNS\_MDType**</span></span>](microsoftdns-mdtype.md)       | <span data-ttu-id="43498-134">網域記錄的郵件代理程式</span><span class="sxs-lookup"><span data-stu-id="43498-134">Mail agent for the domain record</span></span>                             |
| [<span data-ttu-id="43498-135">**MicrosoftDNS \_ MFType**</span><span class="sxs-lookup"><span data-stu-id="43498-135">**MicrosoftDNS\_MFType**</span></span>](microsoftdns-mftype.md)       | <span data-ttu-id="43498-136">網域記錄的郵件轉送代理程式</span><span class="sxs-lookup"><span data-stu-id="43498-136">Mail forwarding agent for the domain record</span></span>                  |
| [<span data-ttu-id="43498-137">**MicrosoftDNS \_ MGType**</span><span class="sxs-lookup"><span data-stu-id="43498-137">**MicrosoftDNS\_MGType**</span></span>](microsoftdns-mgtype.md)       | <span data-ttu-id="43498-138">郵件群組記錄</span><span class="sxs-lookup"><span data-stu-id="43498-138">Mail group record</span></span>                                            |
| [<span data-ttu-id="43498-139">**MicrosoftDNS \_ MINFOType**</span><span class="sxs-lookup"><span data-stu-id="43498-139">**MicrosoftDNS\_MINFOType**</span></span>](microsoftdns-minfotype.md) | <span data-ttu-id="43498-140">郵件資訊記錄</span><span class="sxs-lookup"><span data-stu-id="43498-140">Mail information record</span></span>                                      |
| [<span data-ttu-id="43498-141">**MicrosoftDNS \_ MRType**</span><span class="sxs-lookup"><span data-stu-id="43498-141">**MicrosoftDNS\_MRType**</span></span>](microsoftdns-mrtype.md)       | <span data-ttu-id="43498-142">信箱重新命名記錄</span><span class="sxs-lookup"><span data-stu-id="43498-142">Mailbox rename record</span></span>                                        |
| [<span data-ttu-id="43498-143">**MicrosoftDNS \_ MXType**</span><span class="sxs-lookup"><span data-stu-id="43498-143">**MicrosoftDNS\_MXType**</span></span>](microsoftdns-mxtype.md)       | <span data-ttu-id="43498-144">郵件交換記錄</span><span class="sxs-lookup"><span data-stu-id="43498-144">Mail exchanger record</span></span>                                        |
| [<span data-ttu-id="43498-145">**MicrosoftDNS \_ NSType**</span><span class="sxs-lookup"><span data-stu-id="43498-145">**MicrosoftDNS\_NSType**</span></span>](microsoftdns-nstype.md)       | <span data-ttu-id="43498-146">名稱伺服器記錄</span><span class="sxs-lookup"><span data-stu-id="43498-146">Name server record</span></span>                                           |
| [<span data-ttu-id="43498-147">**MicrosoftDNS \_ NXTType**</span><span class="sxs-lookup"><span data-stu-id="43498-147">**MicrosoftDNS\_NXTType**</span></span>](microsoftdns-nxttype.md)     | <span data-ttu-id="43498-148">下一筆記錄</span><span class="sxs-lookup"><span data-stu-id="43498-148">Next record</span></span>                                                  |
| [<span data-ttu-id="43498-149">**MicrosoftDNS \_ PTRType**</span><span class="sxs-lookup"><span data-stu-id="43498-149">**MicrosoftDNS\_PTRType**</span></span>](microsoftdns-ptrtype.md)     | <span data-ttu-id="43498-150">名稱對應記錄的位址</span><span class="sxs-lookup"><span data-stu-id="43498-150">Address to name mapping record</span></span>                               |
| [<span data-ttu-id="43498-151">**MicrosoftDNS \_ RPType**</span><span class="sxs-lookup"><span data-stu-id="43498-151">**MicrosoftDNS\_RPType**</span></span>](microsoftdns-rptype.md)       | <span data-ttu-id="43498-152">負責任人員記錄</span><span class="sxs-lookup"><span data-stu-id="43498-152">Responsible person record</span></span>                                    |
| [<span data-ttu-id="43498-153">**MicrosoftDNS \_ RTType**</span><span class="sxs-lookup"><span data-stu-id="43498-153">**MicrosoftDNS\_RTType**</span></span>](microsoftdns-rttype.md)       | <span data-ttu-id="43498-154">路由傳送記錄</span><span class="sxs-lookup"><span data-stu-id="43498-154">Route through record</span></span>                                         |
| [<span data-ttu-id="43498-155">**MicrosoftDNS \_ SIGType**</span><span class="sxs-lookup"><span data-stu-id="43498-155">**MicrosoftDNS\_SIGType**</span></span>](microsoftdns-sigtype.md)     | <span data-ttu-id="43498-156">簽章記錄</span><span class="sxs-lookup"><span data-stu-id="43498-156">Signature record</span></span>                                             |
| [<span data-ttu-id="43498-157">**MicrosoftDNS \_ SOAType**</span><span class="sxs-lookup"><span data-stu-id="43498-157">**MicrosoftDNS\_SOAType**</span></span>](microsoftdns-soatype.md)     | <span data-ttu-id="43498-158">開始授權</span><span class="sxs-lookup"><span data-stu-id="43498-158">Start of authority</span></span>                                           |
| [<span data-ttu-id="43498-159">**MicrosoftDNS \_ SRVType**</span><span class="sxs-lookup"><span data-stu-id="43498-159">**MicrosoftDNS\_SRVType**</span></span>](microsoftdns-srvtype.md)     | <span data-ttu-id="43498-160">服務記錄</span><span class="sxs-lookup"><span data-stu-id="43498-160">Service record</span></span>                                               |
| [<span data-ttu-id="43498-161">**MicrosoftDNS \_ TXTType**</span><span class="sxs-lookup"><span data-stu-id="43498-161">**MicrosoftDNS\_TXTType**</span></span>](microsoftdns-txttype.md)     | <span data-ttu-id="43498-162">文字記錄</span><span class="sxs-lookup"><span data-stu-id="43498-162">Text record</span></span>                                                  |
| [<span data-ttu-id="43498-163">**MicrosoftDNS \_ WINSType**</span><span class="sxs-lookup"><span data-stu-id="43498-163">**MicrosoftDNS\_WINSType**</span></span>](microsoftdns-winstype.md)   | <span data-ttu-id="43498-164">WINS 伺服器記錄</span><span class="sxs-lookup"><span data-stu-id="43498-164">WINS server record</span></span>                                           |
| [<span data-ttu-id="43498-165">**MicrosoftDNS \_ WINSRType**</span><span class="sxs-lookup"><span data-stu-id="43498-165">**MicrosoftDNS\_WINSRType**</span></span>](microsoftdns-winsrtype.md) | <span data-ttu-id="43498-166">WINS 反向查閱記錄</span><span class="sxs-lookup"><span data-stu-id="43498-166">WINS reverse-lookup record</span></span>                                   |
| [<span data-ttu-id="43498-167">**MicrosoftDNS \_ WKSType**</span><span class="sxs-lookup"><span data-stu-id="43498-167">**MicrosoftDNS\_WKSType**</span></span>](microsoftdns-wkstype.md)     | <span data-ttu-id="43498-168">知名的服務記錄</span><span class="sxs-lookup"><span data-stu-id="43498-168">Well-known services record</span></span>                                   |
| [<span data-ttu-id="43498-169">**MicrosoftDNS \_ X25Type**</span><span class="sxs-lookup"><span data-stu-id="43498-169">**MicrosoftDNS\_X25Type**</span></span>](microsoftdns-x25type.md)     | <span data-ttu-id="43498-170">X.x.x.x 位址對名稱的對應記錄</span><span class="sxs-lookup"><span data-stu-id="43498-170">X.121 Address-to-name mapping record</span></span>                         |



 

## <a name="administration-steps"></a><span data-ttu-id="43498-171">管理步驟</span><span class="sxs-lookup"><span data-stu-id="43498-171">Administration Steps</span></span>

<span data-ttu-id="43498-172">DNS WMI 提供者可讓您從伺服器本身或從遠端主機管理 Rr。</span><span class="sxs-lookup"><span data-stu-id="43498-172">The DNS WMI Provider enables the administration of RRs from the server itself, or from remote hosts.</span></span> <span data-ttu-id="43498-173">使用 DNS WMI 提供者管理 Rr 所需的一般步驟如下：</span><span class="sxs-lookup"><span data-stu-id="43498-173">The general steps necessary to administer RRs using the DNS WMI Provider are:</span></span>

-   <span data-ttu-id="43498-174">連接到 DNS WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="43498-174">Connecting to the DNS WMI Provider</span></span>
-   <span data-ttu-id="43498-175">取得資源記錄實例</span><span class="sxs-lookup"><span data-stu-id="43498-175">Getting a resource record instance</span></span>
-   <span data-ttu-id="43498-176">列出或修改資源記錄屬性或使用方法</span><span class="sxs-lookup"><span data-stu-id="43498-176">Listing or modifying a resource record property or using a method</span></span>

<span data-ttu-id="43498-177">下列工作會連結到其相關聯的腳本範例。</span><span class="sxs-lookup"><span data-stu-id="43498-177">The following tasks are linked to their associated scripting samples.</span></span>

-   [<span data-ttu-id="43498-178">列出資源類型</span><span class="sxs-lookup"><span data-stu-id="43498-178">Listing Resource Types</span></span>](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [<span data-ttu-id="43498-179">新增資源記錄</span><span class="sxs-lookup"><span data-stu-id="43498-179">Adding a Resource Record</span></span>](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [<span data-ttu-id="43498-180">刪除資源記錄</span><span class="sxs-lookup"><span data-stu-id="43498-180">Deleting a Resource Record</span></span>](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [<span data-ttu-id="43498-181">修改資源記錄</span><span class="sxs-lookup"><span data-stu-id="43498-181">Modifying a Resource Record</span></span>](dns-wmi-provider-samples-managing-dns-resource-records.md)

 

 




