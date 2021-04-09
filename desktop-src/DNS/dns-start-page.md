---
title: 網域名稱系統
description: 網域名稱系統 (DNS) （Microsoft Windows 中的定位器服務）是一種業界標準的通訊協定，可在以 IP 為基礎的網路上尋找電腦。
ms.assetid: 4d1c2151-3995-4e7f-881b-4466bd7b7bb7
keywords:
- DNS
- 'DNS， (查看網域名稱系統) '
- 網域名稱系統
- 網域名稱系統，起始頁
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d705c15fccb0ab237bc610ae4129f6d7002c4a2a
ms.sourcegitcommit: 6515eef99ca0d1bbe3e27d4575e9986f5255f277
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/10/2021
ms.locfileid: "104035322"
---
# <a name="domain-name-system"></a><span data-ttu-id="6e2d8-107">網域名稱系統</span><span class="sxs-lookup"><span data-stu-id="6e2d8-107">Domain Name System</span></span>

## <a name="purpose"></a><span data-ttu-id="6e2d8-108">目的</span><span class="sxs-lookup"><span data-stu-id="6e2d8-108">Purpose</span></span>

<span data-ttu-id="6e2d8-109">網域名稱系統 (DNS) （Microsoft Windows 中的定位器服務）是一種業界標準的通訊協定，可在以 IP 為基礎的網路上尋找電腦。</span><span class="sxs-lookup"><span data-stu-id="6e2d8-109">Domain Name System (DNS), a locator service in Microsoft Windows, is an industry-standard protocol that locates computers on an IP-based network.</span></span> <span data-ttu-id="6e2d8-110">IP 網路（例如網際網路和 Windows 網路）依賴以數位為基礎的位址來處理資料。</span><span class="sxs-lookup"><span data-stu-id="6e2d8-110">IP networks, such as the Internet and Windows networks, rely on number-based addresses to process data.</span></span> <span data-ttu-id="6e2d8-111">不過，使用者可以更容易記住名稱位址，因此必須將使用者易記的 (名稱（例如) ）轉譯 `www.microsoft.com` 為網路可 (辨識的位址，例如 207.46.131.137) 簡單) 。</span><span class="sxs-lookup"><span data-stu-id="6e2d8-111">Users however, can more easily remember name addresses, so it is necessary to translate user-friendly names (such as `www.microsoft.com`) into addresses that the network can recognize (such as 207.46.131.137).</span></span>

## <a name="where-applicable"></a><span data-ttu-id="6e2d8-112">適用時</span><span class="sxs-lookup"><span data-stu-id="6e2d8-112">Where applicable</span></span>

<span data-ttu-id="6e2d8-113">Windows 和 Active Directory 使用 DNS。</span><span class="sxs-lookup"><span data-stu-id="6e2d8-113">Windows and Active Directory use DNS.</span></span> <span data-ttu-id="6e2d8-114">DNS 是網際網路和 Active Directory 的主要定位器服務，因此 DNS 被視為適用于 Windows 和 Active Directory 的基礎服務。</span><span class="sxs-lookup"><span data-stu-id="6e2d8-114">DNS is the primary locator service for the Internet and Active Directory, and therefore, DNS is considered a base service for Windows and Active Directory.</span></span>

## <a name="developer-audience"></a><span data-ttu-id="6e2d8-115">開發人員對象</span><span class="sxs-lookup"><span data-stu-id="6e2d8-115">Developer audience</span></span>

<span data-ttu-id="6e2d8-116">Windows 提供的函式可讓應用程式設計人員使用 DNS，例如程式設計 DNS 查詢、記錄比較和名稱查閱。</span><span class="sxs-lookup"><span data-stu-id="6e2d8-116">Windows provides functions that enable application programmers to use DNS, such as programmatic DNS query, record compare, and name lookup.</span></span>

<span data-ttu-id="6e2d8-117">可程式化 DNS 元件是設計來供 C/C++ 程式設計人員使用。</span><span class="sxs-lookup"><span data-stu-id="6e2d8-117">Programmable DNS components are designed for use by C/C++ programmers.</span></span> <span data-ttu-id="6e2d8-118">必須熟悉網路及 DNS。</span><span class="sxs-lookup"><span data-stu-id="6e2d8-118">Familiarity with networking and DNS is required.</span></span> <span data-ttu-id="6e2d8-119">程式設計人員應該熟悉 IP 通訊協定套件，以及 DNS 通訊協定和 DNS 作業。</span><span class="sxs-lookup"><span data-stu-id="6e2d8-119">Programmers should be familiar with the IP-protocol suite, as well as the DNS protocol and DNS operations.</span></span>

## <a name="run-time-requirements"></a><span data-ttu-id="6e2d8-120">執行階段需求求</span><span class="sxs-lookup"><span data-stu-id="6e2d8-120">Run-time requirements</span></span>

<span data-ttu-id="6e2d8-121">所有需要網際網路相容定位器服務的 IP 網路都會使用 DNS。</span><span class="sxs-lookup"><span data-stu-id="6e2d8-121">DNS is used on all IP networks that require an Internet-compatible locator service.</span></span> <span data-ttu-id="6e2d8-122">不過，DNS API 需要 Windows 2000 或更新版本。</span><span class="sxs-lookup"><span data-stu-id="6e2d8-122">However, the DNS API requires Windows 2000 or later.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="6e2d8-123">本節內容</span><span class="sxs-lookup"><span data-stu-id="6e2d8-123">In this section</span></span>



| <span data-ttu-id="6e2d8-124">主題</span><span class="sxs-lookup"><span data-stu-id="6e2d8-124">Topic</span></span>                                                             | <span data-ttu-id="6e2d8-125">描述</span><span class="sxs-lookup"><span data-stu-id="6e2d8-125">Description</span></span>                                                                          |
|-------------------------------------------------------------------|--------------------------------------------------------------------------------------|
| [<span data-ttu-id="6e2d8-126">DNS 標準檔</span><span class="sxs-lookup"><span data-stu-id="6e2d8-126">DNS Standards Documents</span></span>](dns-standards-documents.md)<br/> | <span data-ttu-id="6e2d8-127">公用 DNS 標準檔的連結。</span><span class="sxs-lookup"><span data-stu-id="6e2d8-127">Links to public DNS standards documents.</span></span><br/>                                  |
| [<span data-ttu-id="6e2d8-128">關於 DNS</span><span class="sxs-lookup"><span data-stu-id="6e2d8-128">About DNS</span></span>](about-dns.md)<br/>                             | <span data-ttu-id="6e2d8-129">關於 DNS 的一般資訊。</span><span class="sxs-lookup"><span data-stu-id="6e2d8-129">General information about DNS.</span></span><br/>                                            |
| [<span data-ttu-id="6e2d8-130">DNS 參考</span><span class="sxs-lookup"><span data-stu-id="6e2d8-130">DNS Reference</span></span>](dns-reference.md)<br/>                     | <span data-ttu-id="6e2d8-131">DNS 的參考檔。</span><span class="sxs-lookup"><span data-stu-id="6e2d8-131">Reference documentation for DNS.</span></span><br/>                                          |
| [<span data-ttu-id="6e2d8-132">DNS WMI 提供者</span><span class="sxs-lookup"><span data-stu-id="6e2d8-132">DNS WMI Provider</span></span>](dns-wmi-provider.md)<br/>               | <span data-ttu-id="6e2d8-133">DNS WMI 提供者的一般資訊和參考檔。</span><span class="sxs-lookup"><span data-stu-id="6e2d8-133">General information and reference documentation for the DNS WMI provider.</span></span><br/> |
| [<span data-ttu-id="6e2d8-134">詞彙</span><span class="sxs-lookup"><span data-stu-id="6e2d8-134">Glossary</span></span>](glossary-gly.md)<br/>                           | <span data-ttu-id="6e2d8-135">DNS 詞彙和定義的詞彙。</span><span class="sxs-lookup"><span data-stu-id="6e2d8-135">Glossary of DNS terms and definitions.</span></span><br/>                                    |



 

## <a name="related-topics"></a><span data-ttu-id="6e2d8-136">相關主題</span><span class="sxs-lookup"><span data-stu-id="6e2d8-136">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6e2d8-137">DHCP</span><span class="sxs-lookup"><span data-stu-id="6e2d8-137">DHCP</span></span>](/previous-versions/windows/desktop/dhcp/dhcp-start-page)
</dt> <dt>

[<span data-ttu-id="6e2d8-138">網際網路通訊協定協助程式</span><span class="sxs-lookup"><span data-stu-id="6e2d8-138">Internet Protocol Helper</span></span>](/windows/desktop/IpHlp/ip-helper-start-page)
</dt> <dt>

<span data-ttu-id="6e2d8-139">[目錄服務](https://msdn.microsoft.com/library/Dd425378(v=VS.85).aspx)</span><span class="sxs-lookup"><span data-stu-id="6e2d8-139">[Directory Services](https://msdn.microsoft.com/library/Dd425378(v=VS.85).aspx)</span></span>
</dt> </dl>

 

