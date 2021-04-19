---
description: 您可以在 Microsoft .NET Framework 3.0 和更新版本的 Microsoft .NET Framework，以及 Windows Vista 和更新版本的 Windows 中使用列印架構和相關技術。
ms.assetid: 98d5f8ec-54bd-4e88-b632-ed427b599cb6
title: 列印架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ae3ac50b9a2f2aba9cda7dc73f183e1f3571cc9d
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106993792"
---
# <a name="print-schema"></a><span data-ttu-id="15d09-103">列印架構</span><span class="sxs-lookup"><span data-stu-id="15d09-103">Print Schema</span></span>

<span data-ttu-id="15d09-104">您可以在 Microsoft .NET Framework 3.0 和更新版本的 Microsoft .NET Framework，以及 Windows Vista 和更新版本的 Windows 中使用列印架構和相關技術。</span><span class="sxs-lookup"><span data-stu-id="15d09-104">The Print Schema and related technologies are available in Microsoft .NET Framework 3.0 and later versions of Microsoft .NET Framework, and in Windows Vista and later versions of Windows.</span></span> <span data-ttu-id="15d09-105">XPS 檔和 XPS 物件模型可以使用列印 [架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)中描述的列印票證物件，指定檔對印表機和觀看應用程式的列印喜好設定。</span><span class="sxs-lookup"><span data-stu-id="15d09-105">XPS documents and the XPS Object Model can use the print ticket objects, which are described in the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip), to specify the printing preferences of a document to printers and viewing applications.</span></span>

<span data-ttu-id="15d09-106">[列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)是可下載的檔，其中包含列印架構的相關資訊，以及如何在檔和列印中使用它。</span><span class="sxs-lookup"><span data-stu-id="15d09-106">The [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip) is a downloadable document that contains information about the Print Schema and how to use it in documents and printing.</span></span> <span data-ttu-id="15d09-107">在線上提供的資訊僅供參考，網址為： [舊版列印架構參考](print-schema.md);但是，它可能不會正確地反映出目前版本的 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="15d09-107">Additional information is provided online for your information only, at [Legacy Print Schema Reference](print-schema.md); however, it might not accurately reflect the current version of the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span> <span data-ttu-id="15d09-108">如需最新的設計資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip) 。</span><span class="sxs-lookup"><span data-stu-id="15d09-108">Refer to the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip) for the most current design information.</span></span>

## <a name="print-schema-overview"></a><span data-ttu-id="15d09-109">列印架構總覽</span><span class="sxs-lookup"><span data-stu-id="15d09-109">Print Schema Overview</span></span>

<span data-ttu-id="15d09-110">列印架構是一種階層式結構化的 XML 架構，用來組織和描述印表機或列印工作的屬性。</span><span class="sxs-lookup"><span data-stu-id="15d09-110">The Print Schema is a hierarchically structured, XML-based schema that is used to organize and describe the properties of a printer or print job.</span></span> <span data-ttu-id="15d09-111">列印架構包含兩個元件： Print Schema 關鍵字和 Print Schema Framework。</span><span class="sxs-lookup"><span data-stu-id="15d09-111">The Print Schema includes two components: the Print Schema Keywords and the Print Schema Framework.</span></span> <span data-ttu-id="15d09-112">列印架構關鍵字是一組描述印表機屬性和列印工作格式化意圖的元素實例。</span><span class="sxs-lookup"><span data-stu-id="15d09-112">The Print Schema Keywords are a set of element instances that describe printer attributes and print job formatting intent.</span></span> <span data-ttu-id="15d09-113">Print Schema Framework 會定義 XML 專案型別的階層式結構化集合，以及如何搭配使用這些專案類型。</span><span class="sxs-lookup"><span data-stu-id="15d09-113">The Print Schema Framework defines a hierarchically structured collection of XML element types and how these element types can be used together.</span></span>

<span data-ttu-id="15d09-114">稱為 *PrintCapabilities* 和 *PrintTicket* 的列印架構技術，是使用 print schema Framework 所指定的 print schema 關鍵字來建立。</span><span class="sxs-lookup"><span data-stu-id="15d09-114">The Print Schema technologies, called *PrintCapabilities* and *PrintTicket*, are built using the Print Schema Keywords as specified by the Print Schema Framework.</span></span> <span data-ttu-id="15d09-115">列印架構規格支援協力廠商的架構延伸，讓列印架構使用者不受限於列印架構關鍵字所定義的屬性、功能、選項或 ParameterInit 實例。</span><span class="sxs-lookup"><span data-stu-id="15d09-115">The Print Schema Specification supports schema extensions by third parties, so that Print Schema users are not restricted to the Property, Feature, Option, or ParameterInit instances that are defined by the Print Schema Keywords.</span></span> <span data-ttu-id="15d09-116">協力廠商元素實例可以加入至由 Print Schema 關鍵字定義的元素實例;不過，私用的協力廠商屬性實例必須屬於與建立命名空間的協力廠商清楚相關聯的命名空間。</span><span class="sxs-lookup"><span data-stu-id="15d09-116">Third-party element instances can be added to element instances that are defined by the Print Schema Keywords; however, private, third-party Property instances must belong to a namespace that is clearly associated with the third party that created the namespace.</span></span>

## <a name="related-topics"></a><span data-ttu-id="15d09-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="15d09-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="15d09-118">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="15d09-118">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> <dt>

[<span data-ttu-id="15d09-119">舊版列印架構參考</span><span class="sxs-lookup"><span data-stu-id="15d09-119">Legacy Print Schema Reference</span></span>](print-schema.md)
</dt> <dt>

[<span data-ttu-id="15d09-120">雙向列印機通訊 (硬體開發人員中心) </span><span class="sxs-lookup"><span data-stu-id="15d09-120">Bidirectional printer communications (Hardware Dev Center)</span></span>](/windows-hardware/drivers/print/bidirectional-communication)
</dt> </dl>

 

 
