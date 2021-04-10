---
title: XML 標準化
description: XML 標準化可解決將一組 XML 節點轉換為位元組的問題，這種方式可讓 XML (的簡單變更，例如變更元素中屬性的順序) 不會變更產生的位元組格式。
ms.assetid: a64303a1-efc4-4c91-ab8d-3e389a655b3e
keywords:
- 適用于 Windows 的 XML 標準化 Web 服務
- WWSAPI
- WWS
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bab8b1aa00b99b604276a479f1a47aacb5bd8b1e
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103842900"
---
# <a name="xml-canonicalization"></a><span data-ttu-id="f81be-106">XML 標準化</span><span class="sxs-lookup"><span data-stu-id="f81be-106">XML Canonicalization</span></span>

<span data-ttu-id="f81be-107">XML 標準化可解決將一組 XML 節點轉換為位元組的問題，這種方式可讓 XML (的簡單變更，例如變更元素中屬性的順序) 不會變更產生的位元組格式。</span><span class="sxs-lookup"><span data-stu-id="f81be-107">XML canonicalization solves the problem of converting a set of XML nodes into bytes in such a way that trivial changes to the XML (such as changing the order of attributes in an element) do not change the resulting byte form.</span></span> <span data-ttu-id="f81be-108">從標準化取得的位元組通常是用來透過 XML 內容產生密碼編譯簽章。</span><span class="sxs-lookup"><span data-stu-id="f81be-108">The bytes obtained from canonicalization are commonly used to generate a cryptographic signature over XML content.</span></span>


<span data-ttu-id="f81be-109">常用的 XML 標準化演算法可將下列層面標準化：</span><span class="sxs-lookup"><span data-stu-id="f81be-109">The commonly used XML canonicalization algorithms standardize the following aspects:</span></span>

-   <span data-ttu-id="f81be-110">不含前序) 的字元編碼 (UTF-8</span><span class="sxs-lookup"><span data-stu-id="f81be-110">Character encoding (UTF-8 without preamble)</span></span>
-   <span data-ttu-id="f81be-111">換行字元和其他字元形式</span><span class="sxs-lookup"><span data-stu-id="f81be-111">Linefeed and other character forms</span></span>
-   <span data-ttu-id="f81be-112">元素中的屬性順序</span><span class="sxs-lookup"><span data-stu-id="f81be-112">Attribute order in an element</span></span>
-   <span data-ttu-id="f81be-113">空白的元素表單</span><span class="sxs-lookup"><span data-stu-id="f81be-113">Empty element form</span></span>
-   <span data-ttu-id="f81be-114">轉譯命名空間宣告</span><span class="sxs-lookup"><span data-stu-id="f81be-114">Rendering namespace declarations</span></span>

<span data-ttu-id="f81be-115">[**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization)和 [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) api 會在讀取檔時提供 XML 標準化功能。</span><span class="sxs-lookup"><span data-stu-id="f81be-115">The APIs [**WsStartReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization) and [**WsEndReaderCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization) provide the XML canonicalization functionality while reading a document.</span></span>

<span data-ttu-id="f81be-116">[**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization)和 [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) api 會在寫入檔時提供 XML 標準化功能。</span><span class="sxs-lookup"><span data-stu-id="f81be-116">The APIs [**WsStartWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization) and [**WsEndWriterCanonicalization**](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization) provide the XML canonicalization functionality while writing a document.</span></span>

<span data-ttu-id="f81be-117">下列列舉適用于標準化：</span><span class="sxs-lookup"><span data-stu-id="f81be-117">The following enumerations are used with canonicalization:</span></span>

-   [<span data-ttu-id="f81be-118">**WS \_ XML \_ 標準化 \_ 演算法**</span><span class="sxs-lookup"><span data-stu-id="f81be-118">**WS\_XML\_CANONICALIZATION\_ALGORITHM**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_algorithm)
-   [<span data-ttu-id="f81be-119">**WS \_ XML \_ 標準化 \_ 屬性 \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="f81be-119">**WS\_XML\_CANONICALIZATION\_PROPERTY\_ID**</span></span>](/windows/desktop/api/WebServices/ne-webservices-ws_xml_canonicalization_property_id)

<span data-ttu-id="f81be-120">下列函式適用于標準化：</span><span class="sxs-lookup"><span data-stu-id="f81be-120">The following functions are used with canonicalization:</span></span>

-   [<span data-ttu-id="f81be-121">**WsEndReaderCanonicalization**</span><span class="sxs-lookup"><span data-stu-id="f81be-121">**WsEndReaderCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsendreadercanonicalization)
-   [<span data-ttu-id="f81be-122">**WsEndWriterCanonicalization**</span><span class="sxs-lookup"><span data-stu-id="f81be-122">**WsEndWriterCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsendwritercanonicalization)
-   [<span data-ttu-id="f81be-123">**WsStartReaderCanonicalization**</span><span class="sxs-lookup"><span data-stu-id="f81be-123">**WsStartReaderCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsstartreadercanonicalization)
-   [<span data-ttu-id="f81be-124">**WsStartWriterCanonicalization**</span><span class="sxs-lookup"><span data-stu-id="f81be-124">**WsStartWriterCanonicalization**</span></span>](/windows/desktop/api/WebServices/nf-webservices-wsstartwritercanonicalization)

<span data-ttu-id="f81be-125">下列結構適用于標準化：</span><span class="sxs-lookup"><span data-stu-id="f81be-125">The following structures are used with canonicalization:</span></span>

-   [<span data-ttu-id="f81be-126">**WS \_ XML \_ 標準化 \_ 內含 \_ 首碼**</span><span class="sxs-lookup"><span data-stu-id="f81be-126">**WS\_XML\_CANONICALIZATION\_INCLUSIVE\_PREFIXES**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_inclusive_prefixes)
-   [<span data-ttu-id="f81be-127">**WS \_ XML \_ 標準化 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="f81be-127">**WS\_XML\_CANONICALIZATION\_PROPERTY**</span></span>](/windows/desktop/api/WebServices/ns-webservices-ws_xml_canonicalization_property)

 

 




