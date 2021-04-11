---
description: 列印票證 API 可讓應用程式管理和轉換列印票證。
ms.assetid: 4f854c1a-f2e1-48c4-9cc1-8a0fcf1bebed
title: 列印票證 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e19cfd8d624a1390b8afacd625e92fcee2704dd
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "104027694"
---
# <a name="print-ticket-api"></a><span data-ttu-id="f89ec-103">列印票證 API</span><span class="sxs-lookup"><span data-stu-id="f89ec-103">Print Ticket API</span></span>

<span data-ttu-id="f89ec-104">列印票證 API 可讓應用程式管理和轉換列印票證。</span><span class="sxs-lookup"><span data-stu-id="f89ec-104">The Print Ticket API provides enables applications to manage and convert print tickets.</span></span>

<span data-ttu-id="f89ec-105">列印票證是 XPS 檔元件，其中包含檔中頁面的慣用印表機設定、整份檔，或包含一或多個檔的列印工作。</span><span class="sxs-lookup"><span data-stu-id="f89ec-105">A print ticket is an XPS document component that contains the preferred printer settings for a page in a document, or for an entire document, or for a print job that contains one or more documents.</span></span> <span data-ttu-id="f89ec-106">請注意，列印票證只會在 XPS 檔中找到。</span><span class="sxs-lookup"><span data-stu-id="f89ec-106">Note that print tickets are only found in XPS documents.</span></span>

<span data-ttu-id="f89ec-107">在印表機可以使用列印票證之前，必須先針對印表機的特性（在印表機的列印功能中定義）驗證列印票證。</span><span class="sxs-lookup"><span data-stu-id="f89ec-107">Before the printer can use the print ticket, the print ticket must be validated against the printer's characteristics, which are defined in the printer's Print Capabilities.</span></span> <span data-ttu-id="f89ec-108">應用程式會藉由呼叫 Print Ticket API 來執行該驗證。</span><span class="sxs-lookup"><span data-stu-id="f89ec-108">The application performs that validation by calling the Print Ticket API.</span></span>

<span data-ttu-id="f89ec-109">您可以使用 print [Schema 規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)所定義的列印架構元素來描述 PrintTicket 和 PrintCapabilities。</span><span class="sxs-lookup"><span data-stu-id="f89ec-109">The PrintTicket and PrintCapabilities are described by using elements of the Print Schema, which is defined by the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="f89ec-110">本主題包含下列 API 元素的相關資訊：</span><span class="sxs-lookup"><span data-stu-id="f89ec-110">This topic contains information about the following API elements:</span></span>

-   [<span data-ttu-id="f89ec-111">列印票證 API 函式</span><span class="sxs-lookup"><span data-stu-id="f89ec-111">Print Ticket API Functions</span></span>](print-ticket-api-functions.md)
-   [<span data-ttu-id="f89ec-112">列印票證 API 列舉</span><span class="sxs-lookup"><span data-stu-id="f89ec-112">Print Ticket API Enumerations</span></span>](print-ticket-api-enumerations.md)

<span data-ttu-id="f89ec-113">下圖顯示 Print Ticket API 與原生 Windows 應用程式可以使用的其他列印 Api 的關聯性。</span><span class="sxs-lookup"><span data-stu-id="f89ec-113">The following diagram shows the relationship of the Print Ticket API to the other Print APIs that a native Windows application can use.</span></span>

![此圖表顯示列印票證 api 與原生 windows 應用程式可以使用的其他列印 api 的關聯性](images/print-apis-pt.png)

## <a name="related-topics"></a><span data-ttu-id="f89ec-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="f89ec-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="f89ec-116">XPS 列印 API</span><span class="sxs-lookup"><span data-stu-id="f89ec-116">XPS Print API</span></span>](xps-printing.md)
</dt> <dt>

[<span data-ttu-id="f89ec-117">列印多工緩衝處理器 API</span><span class="sxs-lookup"><span data-stu-id="f89ec-117">Print Spooler API</span></span>](print-spooler-api.md)
</dt> <dt>

[<span data-ttu-id="f89ec-118">GDI 列印 API</span><span class="sxs-lookup"><span data-stu-id="f89ec-118">GDI Print API</span></span>](gdi-printing.md)
</dt> <dt>

[<span data-ttu-id="f89ec-119">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="f89ec-119">Print Schema Specification</span></span>](https://go.microsoft.com/fwlink/?linkid=2022117)
</dt> <dt>

[<span data-ttu-id="f89ec-120">XML Paper Specification</span><span class="sxs-lookup"><span data-stu-id="f89ec-120">XML Paper Specification</span></span>](https://go.microsoft.com/fwlink/?linkid=2022122)
</dt> </dl>

 

 



