---
description: 瞭解如何加入屬性實例。 列印架構可讓屬性實例存在於選項實例中。
ms.assetid: dac287a9-77ca-44d8-8019-b05e4c61dc52
title: 加入屬性實例
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8085fa10f824f32dc76aef0f1e5f78ca05b22b93
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409691"
---
# <a name="adding-property-instances"></a><span data-ttu-id="13163-104">加入屬性實例</span><span class="sxs-lookup"><span data-stu-id="13163-104">Adding Property Instances</span></span>

<span data-ttu-id="13163-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="13163-105">This topic is not current.</span></span> <span data-ttu-id="13163-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="13163-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="13163-107">列印架構可讓屬性實例存在於選項實例中。</span><span class="sxs-lookup"><span data-stu-id="13163-107">The Print Schema allows Property instances to be present in an Option instance.</span></span> <span data-ttu-id="13163-108">PrintCapabilities 檔中定義的屬性實例不會傳播至儲存在 PrintTicket 中的選項實例。</span><span class="sxs-lookup"><span data-stu-id="13163-108">The Property instances defined in the PrintCapabilities document are not propagated to the Option instances saved in the PrintTicket.</span></span> <span data-ttu-id="13163-109">比較兩個選項實例時，屬性專案不會影響評分進程的結果，但 ScoredProperty 實例會影響此程式。</span><span class="sxs-lookup"><span data-stu-id="13163-109">Property elements do not affect the result of the scoring process when two Option instances are compared, but ScoredProperty instances do affect this process.</span></span> <span data-ttu-id="13163-110">所有執行評分演算法的設備磁碟機都應該遵守此慣例。</span><span class="sxs-lookup"><span data-stu-id="13163-110">All device drivers that implement a scoring algorithm should observe this convention.</span></span> <span data-ttu-id="13163-111">如果這些實例是特定選項以外的特定選項，或如果提供者打算針對功能中的每個選項顯示這個屬性的值，則 PrintCapabilities 提供者可以將屬性實例加入至選項。</span><span class="sxs-lookup"><span data-stu-id="13163-111">PrintCapabilities providers are permitted to add Property instances to an Option if these instances are specific to that particular Option and no others, or if the provider intends for the value of this Property to appear for every Option in the Feature.</span></span> <span data-ttu-id="13163-112">例如，假設 PrintRate 屬性相依于針對 PageResolution 功能選取的選項。</span><span class="sxs-lookup"><span data-stu-id="13163-112">For example, suppose that the PrintRate Property is dependent on the Option selected for the PageResolution Feature.</span></span> <span data-ttu-id="13163-113">如果 PrintRate 屬性是放在 PrintCapabilities 檔的根層級，它會是單一值，而且只會反映目前所選解析度的列印速率。</span><span class="sxs-lookup"><span data-stu-id="13163-113">If the PrintRate Property were placed at the root level of the PrintCapabilities document, it would be single-valued and would reflect only the print rate for the currently selected resolution.</span></span> <span data-ttu-id="13163-114">但是，如果 PrintRate 屬性是放置在每個 PageResolution 選項內，則 PrintRate 屬性的每個實例都可以反映包含它之 PageResolution 選項的列印速率。</span><span class="sxs-lookup"><span data-stu-id="13163-114">However, if the PrintRate Property were placed within each PageResolution Option, each instance of the PrintRate Property could reflect the print rate for the PageResolution Option that contained it.</span></span> <span data-ttu-id="13163-115">PrintCapabilities 檔會包含 PrintRate 的多個定義，一個對應至每個 PageResolution 選項。</span><span class="sxs-lookup"><span data-stu-id="13163-115">The PrintCapabilities document would contain multiple definitions for PrintRate, one corresponding to each PageResolution Option.</span></span> <span data-ttu-id="13163-116">使用速記標記法時，PrintCapabilities 會包含：</span><span class="sxs-lookup"><span data-stu-id="13163-116">Using a shorthand representation, the PrintCapabilities would contain:</span></span>

``` syntax
<psf:Feature name="psk:PageResolution">
  <psf:Property name="psf:SelectionType">
    <psf:Value xsi:type="xs:string">psk:PickOne</psf:Value>
  </psf:Property>
  <psf:Option>
    <psf:ScoredProperty name="psk:ResolutionX">
      <psf:Value xsi:type="xs:string">800dpi</psf:Value>
    </psf:ScoredProperty>
    <psf:ScoredProperty name="psk:ResolutionY">
      <psf:Value xsi:type="xs:string">600dpi</psf:Value>
    </psf:ScoredProperty>
    <!-- Note: The following Property is not part of the Print Schema Framework -->
    <!-- It is included for illustration purposes. -->
    <!-- It is shown as a privately defined implementation-->
    <Property name="FabrikamES500:PrintRate">
      <Value xsi:type="string">20ppm</Value>
    </psf:Property>
  </psf:Option>
</psf:Feature>
```

<span data-ttu-id="13163-117">在某些情況下，在每個解析度選項中放置列印速率屬性，對於用戶端來說更方便，因為用戶端可以判斷每個解析度選項對列印速率的影響，而不需要為每個解析度設定取得新的 PrintCapabilities 檔。</span><span class="sxs-lookup"><span data-stu-id="13163-117">In some situations, placing a print rate Property within each resolution Option is more convenient for the client, because the client can determine at a glance the effect that each resolution Option has on the print rate, without the need for obtaining a new PrintCapabilities document for each resolution setting.</span></span>

<span data-ttu-id="13163-118">另外也請注意，屬性實例也可以新增為功能專案的子項目。</span><span class="sxs-lookup"><span data-stu-id="13163-118">Note also that Property instances can also be added as child elements of Feature elements.</span></span> <span data-ttu-id="13163-119">如果每個功能都有特定屬性實例或屬性實例的值，這就很有用。</span><span class="sxs-lookup"><span data-stu-id="13163-119">This is useful if there are Property instances or values of Property instances that are specific to each Feature.</span></span> <span data-ttu-id="13163-120">例如，可能會有一個屬性，指定某項功能一次只允許選取一個選項，還是可以選取多個選項。</span><span class="sxs-lookup"><span data-stu-id="13163-120">For example, there might be a Property that specifies whether only one Option is permitted to be selected at one time for a Feature, or whether multiple Options may be selected.</span></span> <span data-ttu-id="13163-121">這是挑選 \_ 一個，挑選 \_ 許多用於 PPD 和 GPD 檔案的屬性。</span><span class="sxs-lookup"><span data-stu-id="13163-121">This is the PICK\_ONE, PICK\_MANY property used in PPD and GPD files.</span></span> <span data-ttu-id="13163-122">因為某些功能實例可能會被識別為挑選 \_ 一個，而有些則可能被視為挑選 \_ 許多，所以必須為每項功能定義這個屬性。</span><span class="sxs-lookup"><span data-stu-id="13163-122">Because some Feature instances might be identified as PICK\_ONE, while others might be identified as PICK\_MANY, this Property must be defined for each Feature.</span></span> <span data-ttu-id="13163-123">將屬性尋找為功能的子專案，會產生屬性和功能之間的關聯。</span><span class="sxs-lookup"><span data-stu-id="13163-123">Locating the Property as a child element of the Feature produces the association between the Property and the Feature.</span></span>

## <a name="related-topics"></a><span data-ttu-id="13163-124">相關主題</span><span class="sxs-lookup"><span data-stu-id="13163-124">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="13163-125">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="13163-125">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



