---
description: 這項 PrintTicket 功能的總覽說明用來表示裝置設定資訊和使用 PrintTicket 的格式。
ms.assetid: c48b9821-9194-47d9-a3ec-b10dbbdf14cc
title: PrintTicket 功能總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e90aa6f967f5fce25977b52a4d0bec7e9e1ea705
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112408541"
---
# <a name="overview-of-printticket-functionality"></a><span data-ttu-id="bdb4c-103">PrintTicket 功能總覽</span><span class="sxs-lookup"><span data-stu-id="bdb4c-103">Overview of PrintTicket Functionality</span></span>

<span data-ttu-id="bdb4c-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="bdb4c-104">This topic is not current.</span></span> <span data-ttu-id="bdb4c-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="bdb4c-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="bdb4c-106">PrintTicket 使用以 XML 為基礎的格式來表示裝置設定資訊，方法是使用 Print Schema Framework 的功能/選項和參數結構。</span><span class="sxs-lookup"><span data-stu-id="bdb4c-106">The PrintTicket utilizes an XML-based format for expressing device configuration information using the Feature/Option and parameter constructs of the Print Schema Framework.</span></span> <span data-ttu-id="bdb4c-107">這包括所有標準專案類型，以及 Print Schema Framework 的擴充性功能。</span><span class="sxs-lookup"><span data-stu-id="bdb4c-107">This includes all of the standard element types as well as the extensibility capabilities of the Print Schema Framework.</span></span> <span data-ttu-id="bdb4c-108">若要將 PrintTicket 視為單一頁面處理方式的獨立描述，則會假設為。</span><span class="sxs-lookup"><span data-stu-id="bdb4c-108">A PrintTicket is assumed to be a self-contained description of how a single page is to be processed.</span></span> <span data-ttu-id="bdb4c-109">此處未涵蓋從特定檔案格式解壓縮和建立這類 PrintTicket 的相關步驟。</span><span class="sxs-lookup"><span data-stu-id="bdb4c-109">The steps involved in extracting and constructing such a PrintTicket from a particular document format are not covered here.</span></span>

<span data-ttu-id="bdb4c-110">您可以使用 PrintTicket 來取得 PrintCapabilities 檔，以描述特定設定的裝置特性。</span><span class="sxs-lookup"><span data-stu-id="bdb4c-110">A PrintTicket can be used to obtain a PrintCapabilities document describing the characteristics of the device for a particular configuration.</span></span> <span data-ttu-id="bdb4c-111">或者，您可以使用一組轉譯指令來提交 PrintTicket，以根據 PrintTicket 中指定的設定產生轉譯和處理的輸出頁面。</span><span class="sxs-lookup"><span data-stu-id="bdb4c-111">Alternatively, the PrintTicket can be submitted with a set of rendering instructions to produce a page of output rendered and processed according to the configuration specified in the PrintTicket.</span></span>

## <a name="related-topics"></a><span data-ttu-id="bdb4c-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="bdb4c-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="bdb4c-113">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="bdb4c-113">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



