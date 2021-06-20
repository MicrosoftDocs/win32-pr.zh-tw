---
description: 當 PrintTicket 經過驗證之後，就可以用來建立 PrintCapabilities 的快照集。
ms.assetid: b49e20b7-bd9e-4b8f-bb4a-bb1e99b0c417
title: 建立 PrintCapabilities 檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b96ea51cef9dfd0f351704b3b71a7f6163737736
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409511"
---
# <a name="creating-a-printcapabilities-document"></a><span data-ttu-id="6ccc6-103">建立 PrintCapabilities 檔</span><span class="sxs-lookup"><span data-stu-id="6ccc6-103">Creating a PrintCapabilities Document</span></span>

<span data-ttu-id="6ccc6-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="6ccc6-104">This topic is not current.</span></span> <span data-ttu-id="6ccc6-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="6ccc6-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="6ccc6-106">當 PrintTicket 經過驗證之後，就可以用來建立 PrintCapabilities 的快照集。</span><span class="sxs-lookup"><span data-stu-id="6ccc6-106">After a PrintTicket is validated, it can be used to create a snapshot of the PrintCapabilities.</span></span> <span data-ttu-id="6ccc6-107">提供者必須有任何屬性的內部標記法，其值相依于裝置設定。</span><span class="sxs-lookup"><span data-stu-id="6ccc6-107">The provider must have an internal representation for any Property whose Value is dependent on the device configuration.</span></span> <span data-ttu-id="6ccc6-108">例如，如果 SpotDiameter 是一種相依于解析和媒體類型功能的屬性，則 SpotDiameter 的內部標記法會與不同的解析和媒體值相關聯，如下表所示：</span><span class="sxs-lookup"><span data-stu-id="6ccc6-108">For example, if SpotDiameter is a Property that is dependent on both the Resolution and MediaType Features, an internal representation of SpotDiameter as it relates to the various values for Resolution and MediaType might appear as in the following table:</span></span>



| <span data-ttu-id="6ccc6-109">解決方案</span><span class="sxs-lookup"><span data-stu-id="6ccc6-109">Resolution</span></span>      | <span data-ttu-id="6ccc6-110">MediaType</span><span class="sxs-lookup"><span data-stu-id="6ccc6-110">MediaType</span></span>         | <span data-ttu-id="6ccc6-111">SpotDiameter</span><span class="sxs-lookup"><span data-stu-id="6ccc6-111">SpotDiameter</span></span>   |
|-----------------|-------------------|----------------|
| <span data-ttu-id="6ccc6-112">300</span><span class="sxs-lookup"><span data-stu-id="6ccc6-112">300</span></span><br/>  | <span data-ttu-id="6ccc6-113">債券</span><span class="sxs-lookup"><span data-stu-id="6ccc6-113">Bond</span></span><br/>   | <span data-ttu-id="6ccc6-114">520</span><span class="sxs-lookup"><span data-stu-id="6ccc6-114">520</span></span><br/> |
| <span data-ttu-id="6ccc6-115">300</span><span class="sxs-lookup"><span data-stu-id="6ccc6-115">300</span></span><br/>  | <span data-ttu-id="6ccc6-116">光澤</span><span class="sxs-lookup"><span data-stu-id="6ccc6-116">Glossy</span></span><br/> | <span data-ttu-id="6ccc6-117">350</span><span class="sxs-lookup"><span data-stu-id="6ccc6-117">350</span></span><br/> |
| <span data-ttu-id="6ccc6-118">600</span><span class="sxs-lookup"><span data-stu-id="6ccc6-118">600</span></span><br/>  | <span data-ttu-id="6ccc6-119">債券</span><span class="sxs-lookup"><span data-stu-id="6ccc6-119">Bond</span></span><br/>   | <span data-ttu-id="6ccc6-120">330</span><span class="sxs-lookup"><span data-stu-id="6ccc6-120">330</span></span><br/> |
| <span data-ttu-id="6ccc6-121">600</span><span class="sxs-lookup"><span data-stu-id="6ccc6-121">600</span></span><br/>  | <span data-ttu-id="6ccc6-122">光澤</span><span class="sxs-lookup"><span data-stu-id="6ccc6-122">Glossy</span></span><br/> | <span data-ttu-id="6ccc6-123">180</span><span class="sxs-lookup"><span data-stu-id="6ccc6-123">180</span></span><br/> |
| <span data-ttu-id="6ccc6-124">1200</span><span class="sxs-lookup"><span data-stu-id="6ccc6-124">1200</span></span><br/> | <span data-ttu-id="6ccc6-125">債券</span><span class="sxs-lookup"><span data-stu-id="6ccc6-125">Bond</span></span><br/>   | <span data-ttu-id="6ccc6-126">250</span><span class="sxs-lookup"><span data-stu-id="6ccc6-126">250</span></span><br/> |
| <span data-ttu-id="6ccc6-127">1200</span><span class="sxs-lookup"><span data-stu-id="6ccc6-127">1200</span></span><br/> | <span data-ttu-id="6ccc6-128">光澤</span><span class="sxs-lookup"><span data-stu-id="6ccc6-128">Glossy</span></span><br/> | <span data-ttu-id="6ccc6-129">100</span><span class="sxs-lookup"><span data-stu-id="6ccc6-129">100</span></span><br/> |



 

<span data-ttu-id="6ccc6-130">在此範例中，PrintCapabilities 提供者必須使用提供的 PrintTicket，從內部資料表和報表中選取適當的專案，做為 SpotDiameter 屬性的值。</span><span class="sxs-lookup"><span data-stu-id="6ccc6-130">For this example, the PrintCapabilities provider must use the provided PrintTicket to select the proper entry from the internal table and report that as the Value for the SpotDiameter Property.</span></span> <span data-ttu-id="6ccc6-131">對於值相依于設定) 的每個屬性，每個多重值屬性 (都會重複此程式。</span><span class="sxs-lookup"><span data-stu-id="6ccc6-131">This process is repeated for every multi-valued Property (for every Property whose Value is dependent on the configuration).</span></span> <span data-ttu-id="6ccc6-132">[PrintCapabilities 架構和檔結構](printcapabilities-schema-and-document-construction.md)一節說明建立 PrintCapabilities 快照集時所牽涉到的其他步驟。</span><span class="sxs-lookup"><span data-stu-id="6ccc6-132">The [PrintCapabilities Schema and Document Construction](printcapabilities-schema-and-document-construction.md) section describes the other steps involved in creating a snapshot of the PrintCapabilities.</span></span>

<span data-ttu-id="6ccc6-133">若要建立預設 PrintCapabilities 檔的快照集，請提供預設的 PrintTicket (，而不是建立 PrintCapabilities 檔之方法的任意 PrintTicket) 。</span><span class="sxs-lookup"><span data-stu-id="6ccc6-133">To create a snapshot of the default PrintCapabilities document, provide a default PrintTicket (rather than an arbitrary PrintTicket) to the method that creates PrintCapabilities documents.</span></span>

## <a name="related-topics"></a><span data-ttu-id="6ccc6-134">相關主題</span><span class="sxs-lookup"><span data-stu-id="6ccc6-134">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="6ccc6-135">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="6ccc6-135">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 




