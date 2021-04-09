---
title: 管理 DNS 資源記錄
description: 資源記錄（通常稱為 RR）是 DNS 區域檔案中的資訊專案單位。Rr 是主機名稱和 IP 資訊的基本組建區塊，可用來解析所有 DNS 查詢。
ms.assetid: ddad5f14-5a2d-4966-87b7-b354666f9e24
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99edffa52b5137858468fd64122d2af826a896ad
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840404"
---
# <a name="managing-dns-resource-records"></a><span data-ttu-id="f9d06-103">管理 DNS 資源記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-103">Managing DNS Resource Records</span></span>

<span data-ttu-id="f9d06-104">資源記錄（通常稱為 RR）是 DNS 區域檔案中的資訊專案單位。Rr 是主機名稱和 IP 資訊的基本組建區塊，可用來解析所有 DNS 查詢。</span><span class="sxs-lookup"><span data-stu-id="f9d06-104">A resource record, commonly referred to as an RR, is the unit of information entry in DNS zone files; RRs are the basic building blocks of host-name and IP information and are used to resolve all DNS queries.</span></span> <span data-ttu-id="f9d06-105">資源記錄會有相當廣泛的類型，以提供擴充的名稱解析服務。</span><span class="sxs-lookup"><span data-stu-id="f9d06-105">Resource records come in a fairly wide variety of types in order to provide extended name-resolution services.</span></span>

<span data-ttu-id="f9d06-106">不同類型的 Rr 具有不同的格式，因為它們包含不同的資料。</span><span class="sxs-lookup"><span data-stu-id="f9d06-106">Different types of RRs have different formats, as they contain different data.</span></span> <span data-ttu-id="f9d06-107">許多 Rr 共用一個通用的格式。</span><span class="sxs-lookup"><span data-stu-id="f9d06-107">Many RRs share a common format.</span></span> <span data-ttu-id="f9d06-108">每一部 DNS 伺服器都會包含其所授權之命名空間部分的 Rr。</span><span class="sxs-lookup"><span data-stu-id="f9d06-108">Each DNS Server contains RRs for the portion of the name space for which it is authoritative.</span></span>

<span data-ttu-id="f9d06-109">DNS WMI 提供者目前支援下列 RR 類型。</span><span class="sxs-lookup"><span data-stu-id="f9d06-109">The DNS WMI Provider currently supports the following RR types.</span></span> <span data-ttu-id="f9d06-110">按一下資源記錄的名稱，以跳至其參考頁面。</span><span class="sxs-lookup"><span data-stu-id="f9d06-110">Click the name of the resource record to jump to its reference page.</span></span>



| <span data-ttu-id="f9d06-111">提供者) 中的資源記錄 (</span><span class="sxs-lookup"><span data-stu-id="f9d06-111">Resource Record (in provider)</span></span>                             | <span data-ttu-id="f9d06-112">Description</span><span class="sxs-lookup"><span data-stu-id="f9d06-112">Description</span></span>                                                  |
|-----------------------------------------------------------|--------------------------------------------------------------|
| [<span data-ttu-id="f9d06-113">**MicrosoftDNS \_ AType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-113">**MicrosoftDNS\_AType**</span></span>](microsoftdns-atype.md)         | <span data-ttu-id="f9d06-114">位址對應記錄的名稱</span><span class="sxs-lookup"><span data-stu-id="f9d06-114">Name to address mapping record</span></span>                               |
| [<span data-ttu-id="f9d06-115">**MicrosoftDNS \_ AAAAType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-115">**MicrosoftDNS\_AAAAType**</span></span>](microsoftdns-aaaatype.md)   | <span data-ttu-id="f9d06-116">主機至 Ipv6 地址記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-116">Host to Ipv6 address record</span></span>                                  |
| [<span data-ttu-id="f9d06-117">**MicrosoftDNS \_ AFSDBType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-117">**MicrosoftDNS\_AFSDBType**</span></span>](microsoftdns-afsdbtype.md) | <span data-ttu-id="f9d06-118">Andrew 檔案系統資料庫伺服器記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-118">Andrew File System Database Server record</span></span>                    |
| [<span data-ttu-id="f9d06-119">**MicrosoftDNS \_ ATMAType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-119">**MicrosoftDNS\_ATMAType**</span></span>](microsoftdns-atmatype.md)   | <span data-ttu-id="f9d06-120">ATM 位址對名稱記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-120">ATM address-to-name record</span></span>                                   |
| [<span data-ttu-id="f9d06-121">**MicrosoftDNS \_ CNAMEType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-121">**MicrosoftDNS\_CNAMEType**</span></span>](microsoftdns-cnametype.md) | <span data-ttu-id="f9d06-122">正式 [*名稱*](c-gly.md)記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-122">[*Canonical Name*](c-gly.md) record</span></span> |
| [<span data-ttu-id="f9d06-123">**MicrosoftDNS \_ HINFOType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-123">**MicrosoftDNS\_HINFOType**</span></span>](microsoftdns-hinfotype.md) | <span data-ttu-id="f9d06-124">主機資訊記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-124">Host Information record</span></span>                                      |
| [<span data-ttu-id="f9d06-125">**MicrosoftDNS \_ ISDNType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-125">**MicrosoftDNS\_ISDNType**</span></span>](microsoftdns-isdntype.md)   | <span data-ttu-id="f9d06-126">整合式服務數位網路記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-126">Integrated services digital network record</span></span>                   |
| [<span data-ttu-id="f9d06-127">**MicrosoftDNS \_ KEYType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-127">**MicrosoftDNS\_KEYType**</span></span>](microsoftdns-keytype.md)     | <span data-ttu-id="f9d06-128">索引鍵記錄。</span><span class="sxs-lookup"><span data-stu-id="f9d06-128">KEY record.</span></span> <span data-ttu-id="f9d06-129">請參閱 RFC 2535</span><span class="sxs-lookup"><span data-stu-id="f9d06-129">See RFC 2535</span></span>                                     |
| [<span data-ttu-id="f9d06-130">**MicrosoftDNS \_ MBType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-130">**MicrosoftDNS\_MBType**</span></span>](microsoftdns-mbtype.md)       | <span data-ttu-id="f9d06-131">信箱記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-131">Mailbox record</span></span>                                               |
| [<span data-ttu-id="f9d06-132">**MicrosoftDNS \_ MDType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-132">**MicrosoftDNS\_MDType**</span></span>](microsoftdns-mdtype.md)       | <span data-ttu-id="f9d06-133">網域記錄的郵件代理程式</span><span class="sxs-lookup"><span data-stu-id="f9d06-133">Mail agent for the domain record</span></span>                             |
| [<span data-ttu-id="f9d06-134">**MicrosoftDNS \_ MFType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-134">**MicrosoftDNS\_MFType**</span></span>](microsoftdns-mftype.md)       | <span data-ttu-id="f9d06-135">網域記錄的郵件轉送代理程式</span><span class="sxs-lookup"><span data-stu-id="f9d06-135">Mail forwarding agent for the domain record</span></span>                  |
| [<span data-ttu-id="f9d06-136">**MicrosoftDNS \_ MGType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-136">**MicrosoftDNS\_MGType**</span></span>](microsoftdns-mgtype.md)       | <span data-ttu-id="f9d06-137">郵件群組記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-137">Mail group record</span></span>                                            |
| [<span data-ttu-id="f9d06-138">**MicrosoftDNS \_ MINFOType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-138">**MicrosoftDNS\_MINFOType**</span></span>](microsoftdns-minfotype.md) | <span data-ttu-id="f9d06-139">郵件資訊記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-139">Mail information record</span></span>                                      |
| [<span data-ttu-id="f9d06-140">**MicrosoftDNS \_ MRType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-140">**MicrosoftDNS\_MRType**</span></span>](microsoftdns-mrtype.md)       | <span data-ttu-id="f9d06-141">信箱重新命名記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-141">Mailbox rename record</span></span>                                        |
| [<span data-ttu-id="f9d06-142">**MicrosoftDNS \_ MXType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-142">**MicrosoftDNS\_MXType**</span></span>](microsoftdns-mxtype.md)       | <span data-ttu-id="f9d06-143">郵件交換記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-143">Mail exchanger record</span></span>                                        |
| [<span data-ttu-id="f9d06-144">**MicrosoftDNS \_ NSType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-144">**MicrosoftDNS\_NSType**</span></span>](microsoftdns-nstype.md)       | <span data-ttu-id="f9d06-145">名稱伺服器記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-145">Name server record</span></span>                                           |
| [<span data-ttu-id="f9d06-146">**MicrosoftDNS \_ NXTType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-146">**MicrosoftDNS\_NXTType**</span></span>](microsoftdns-nxttype.md)     | <span data-ttu-id="f9d06-147">下一筆記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-147">Next record</span></span>                                                  |
| [<span data-ttu-id="f9d06-148">**MicrosoftDNS \_ PTRType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-148">**MicrosoftDNS\_PTRType**</span></span>](microsoftdns-ptrtype.md)     | <span data-ttu-id="f9d06-149">名稱對應記錄的位址</span><span class="sxs-lookup"><span data-stu-id="f9d06-149">Address to name mapping record</span></span>                               |
| [<span data-ttu-id="f9d06-150">**MicrosoftDNS \_ RPType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-150">**MicrosoftDNS\_RPType**</span></span>](microsoftdns-rptype.md)       | <span data-ttu-id="f9d06-151">負責任人員記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-151">Responsible person record</span></span>                                    |
| [<span data-ttu-id="f9d06-152">**MicrosoftDNS \_ RTType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-152">**MicrosoftDNS\_RTType**</span></span>](microsoftdns-rttype.md)       | <span data-ttu-id="f9d06-153">路由傳送記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-153">Route through record</span></span>                                         |
| [<span data-ttu-id="f9d06-154">**MicrosoftDNS \_ SIGType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-154">**MicrosoftDNS\_SIGType**</span></span>](microsoftdns-sigtype.md)     | <span data-ttu-id="f9d06-155">簽章記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-155">Signature record</span></span>                                             |
| [<span data-ttu-id="f9d06-156">**MicrosoftDNS \_ SOAType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-156">**MicrosoftDNS\_SOAType**</span></span>](microsoftdns-soatype.md)     | <span data-ttu-id="f9d06-157">開始授權</span><span class="sxs-lookup"><span data-stu-id="f9d06-157">Start of authority</span></span>                                           |
| [<span data-ttu-id="f9d06-158">**MicrosoftDNS \_ SRVType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-158">**MicrosoftDNS\_SRVType**</span></span>](microsoftdns-srvtype.md)     | <span data-ttu-id="f9d06-159">服務記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-159">Service record</span></span>                                               |
| [<span data-ttu-id="f9d06-160">**MicrosoftDNS \_ TXTType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-160">**MicrosoftDNS\_TXTType**</span></span>](microsoftdns-txttype.md)     | <span data-ttu-id="f9d06-161">文字記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-161">Text record</span></span>                                                  |
| [<span data-ttu-id="f9d06-162">**MicrosoftDNS \_ WINSType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-162">**MicrosoftDNS\_WINSType**</span></span>](microsoftdns-winstype.md)   | <span data-ttu-id="f9d06-163">WINS 伺服器記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-163">WINS server record</span></span>                                           |
| [<span data-ttu-id="f9d06-164">**MicrosoftDNS \_ WINSRType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-164">**MicrosoftDNS\_WINSRType**</span></span>](microsoftdns-winsrtype.md) | <span data-ttu-id="f9d06-165">WINS 反向查閱記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-165">WINS reverse-lookup record</span></span>                                   |
| [<span data-ttu-id="f9d06-166">**MicrosoftDNS \_ WKSType**</span><span class="sxs-lookup"><span data-stu-id="f9d06-166">**MicrosoftDNS\_WKSType**</span></span>](microsoftdns-wkstype.md)     | <span data-ttu-id="f9d06-167">知名的服務記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-167">Well-known services record</span></span>                                   |
| [<span data-ttu-id="f9d06-168">**MicrosoftDNS \_ X25Type**</span><span class="sxs-lookup"><span data-stu-id="f9d06-168">**MicrosoftDNS\_X25Type**</span></span>](microsoftdns-x25type.md)     | <span data-ttu-id="f9d06-169">X.x.x.x 位址對名稱的對應記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-169">X.121 Address-to-name mapping record</span></span>                         |



 

## <a name="administration-steps"></a><span data-ttu-id="f9d06-170">管理步驟</span><span class="sxs-lookup"><span data-stu-id="f9d06-170">Administration Steps</span></span>

<span data-ttu-id="f9d06-171">DNS WMI 提供者可讓您從伺服器本身或從遠端主機管理 Rr。</span><span class="sxs-lookup"><span data-stu-id="f9d06-171">The DNS WMI Provider enables the administration of RRs from the server itself, or from remote hosts.</span></span> <span data-ttu-id="f9d06-172">使用 DNS WMI 提供者管理 Rr 所需的一般步驟如下：</span><span class="sxs-lookup"><span data-stu-id="f9d06-172">The general steps necessary to administer RRs using the DNS WMI Provider are:</span></span>

-   <span data-ttu-id="f9d06-173">連接到 DNS WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="f9d06-173">Connecting to the DNS WMI Provider</span></span>
-   <span data-ttu-id="f9d06-174">取得資源記錄實例</span><span class="sxs-lookup"><span data-stu-id="f9d06-174">Getting a resource record instance</span></span>
-   <span data-ttu-id="f9d06-175">列出或修改資源記錄屬性或使用方法</span><span class="sxs-lookup"><span data-stu-id="f9d06-175">Listing or modifying a resource record property or using a method</span></span>

<span data-ttu-id="f9d06-176">下列工作會連結到其相關聯的腳本範例。</span><span class="sxs-lookup"><span data-stu-id="f9d06-176">The following tasks are linked to their associated scripting samples.</span></span>

-   [<span data-ttu-id="f9d06-177">列出資源類型</span><span class="sxs-lookup"><span data-stu-id="f9d06-177">Listing Resource Types</span></span>](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [<span data-ttu-id="f9d06-178">新增資源記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-178">Adding a Resource Record</span></span>](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [<span data-ttu-id="f9d06-179">刪除資源記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-179">Deleting a Resource Record</span></span>](dns-wmi-provider-samples-managing-dns-resource-records.md)
-   [<span data-ttu-id="f9d06-180">修改資源記錄</span><span class="sxs-lookup"><span data-stu-id="f9d06-180">Modifying a Resource Record</span></span>](dns-wmi-provider-samples-managing-dns-resource-records.md)

 

 




