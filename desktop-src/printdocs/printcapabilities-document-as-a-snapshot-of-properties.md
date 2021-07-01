---
title: 做為屬性快照集的檔
description: 將 PrintCapabilities 檔視為屬性的快照集。 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 476c98e6-face-42cf-874d-cfa7a54b0666
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b399c82211c268a72ad2b67082c144c64e46a879
ms.sourcegitcommit: b32433cc0394159c7263809ae67615ab5792d40d
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/30/2021
ms.locfileid: "113118643"
---
# <a name="printcapabilities-document-as-a-snapshot-of-properties"></a><span data-ttu-id="646d3-105">將檔 PrintCapabilities 為屬性的快照集</span><span class="sxs-lookup"><span data-stu-id="646d3-105">PrintCapabilities Document as a Snapshot of Properties</span></span>

<span data-ttu-id="646d3-106">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="646d3-106">This topic is not current.</span></span> <span data-ttu-id="646d3-107">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="646d3-107">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="646d3-108">PrintCapabilities 所描述的裝置可能會有相依于裝置狀態或設定的屬性。</span><span class="sxs-lookup"><span data-stu-id="646d3-108">The device described by the PrintCapabilities might have properties that depend on the state or configuration of the device.</span></span> <span data-ttu-id="646d3-109">雖然 PrintCapabilities 代表裝置的完整設定空間，但 PrintCapabilities 提供者會產生名為 PrintCapabilities 檔之 PrintCapabilities 的設定相依實例。</span><span class="sxs-lookup"><span data-stu-id="646d3-109">While the PrintCapabilities represents the full configuration space of a device, the PrintCapabilities provider produces a configuration-dependent instance of the PrintCapabilities called the PrintCapabilities document.</span></span> <span data-ttu-id="646d3-110">這項與設定相依的 PrintCapabilities 檔可避免 PrintCapabilities 架構的負擔，以及表示多重值資料的複雜度。</span><span class="sxs-lookup"><span data-stu-id="646d3-110">This configuration-dependent PrintCapabilities document avoids burdening the PrintCapabilities Schema with the complexity of representing multivalued data.</span></span> <span data-ttu-id="646d3-111">更重要的是，若要減輕 PrintCapabilities 檔的取用者免于從多重值資料標記法中解壓縮適當值的負擔，PrintCapabilities 檔中的所有屬性和 ScoredProperty 實例都必須是單一值。</span><span class="sxs-lookup"><span data-stu-id="646d3-111">More importantly, to relieve a consumer of the PrintCapabilities document from the burden of extracting the appropriate value from a multivalued data representation, all Property and ScoredProperty instances in a PrintCapabilities document are required to be single-valued.</span></span> <span data-ttu-id="646d3-112">換句話說，PrintCapabilities 檔中的每個屬性和 ScoredProperty 實例都必須具有固定值（相對於輸入設定）。</span><span class="sxs-lookup"><span data-stu-id="646d3-112">In other words, each Property and ScoredProperty instance in a PrintCapabilities document must have a fixed Value, relative to the input configuration.</span></span> <span data-ttu-id="646d3-113">當裝置處於特定狀態時，可以將每個 PrintCapabilities 檔視為裝置屬性的快照集。</span><span class="sxs-lookup"><span data-stu-id="646d3-113">Each PrintCapabilities document can be thought of as a snapshot of the properties of the device when the device is in a particular state.</span></span> <span data-ttu-id="646d3-114">因此，在可以建立 PrintCapabilities 檔之前，必須先提供要使用的設定。</span><span class="sxs-lookup"><span data-stu-id="646d3-114">Consequently, before a PrintCapabilities document can be constructed, the configuration to be used must be provided.</span></span>

## <a name="related-topics"></a><span data-ttu-id="646d3-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="646d3-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="646d3-116">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="646d3-116">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



