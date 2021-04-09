---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 193dd600-7cbb-4f4e-bb7d-7f7117e9d16a
title: 列印架構背景
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93280b6c8de62c76acdd59e2e596a0f600702451
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "103696326"
---
# <a name="print-schema-background"></a><span data-ttu-id="2c7b2-104">列印架構背景</span><span class="sxs-lookup"><span data-stu-id="2c7b2-104">Print Schema Background</span></span>

<span data-ttu-id="2c7b2-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="2c7b2-105">This topic is not current.</span></span> <span data-ttu-id="2c7b2-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="2c7b2-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="2c7b2-107">列印架構的目的是要解決與列印子系統元件之間的內部通訊相關的 opaqueness 和不明確的問題，以及列印子系統和應用程式之間的外部通訊。</span><span class="sxs-lookup"><span data-stu-id="2c7b2-107">The Print Schema is intended to address the problems of opaqueness and ambiguity associated with internal communication between the components of the print subsystem, and external communication between the print subsystem and applications.</span></span>

<span data-ttu-id="2c7b2-108">目前的列印子系統與應用程式和硬體廠商的外掛程式互動會使用二進位、以索引為基礎的 DEVMODE 結構和二進位 DevCaps。</span><span class="sxs-lookup"><span data-stu-id="2c7b2-108">The current print subsystem interaction with applications and hardware vendors' plug-ins uses the binary, index-based DEVMODE structure and binary DevCaps.</span></span> <span data-ttu-id="2c7b2-109">每個元件所做的設定，對其他元件來說大多是不透明的，防止裝置之間的設定可攜性，甚至在相同裝置上的不同驅動程式版本之間可移植。</span><span class="sxs-lookup"><span data-stu-id="2c7b2-109">Settings made by each component are largely opaque to other components, preventing portability of settings between devices or even between different driver versions on the same device.</span></span> <span data-ttu-id="2c7b2-110">此外，用戶端應用程式不需要對裝置有專屬的知識，或使用驅動程式使用者介面 (UI) ，就不容易利用 PrintCapabilities。</span><span class="sxs-lookup"><span data-stu-id="2c7b2-110">Furthermore, PrintCapabilities cannot easily be leveraged by client applications without either proprietary knowledge of the device or using the driver user interface (UI).</span></span> <span data-ttu-id="2c7b2-111">除了這些限制之外，沒有定義完善的語言來描述一般裝置屬性、PrintCapabilities、裝置設定或作業格式。</span><span class="sxs-lookup"><span data-stu-id="2c7b2-111">In addition to these limitations, in a broader sense there is no well-defined language to describe general device attributes, PrintCapabilities, device configurations, or job formatting.</span></span> <span data-ttu-id="2c7b2-112">列印架構及其相關技術的設計目的是要解決這些限制，並以合併和邏輯的方式，提供一致、明確且可擴充的設定與功能通訊方法。</span><span class="sxs-lookup"><span data-stu-id="2c7b2-112">The Print Schema and its related technologies are designed to address these limitations, providing a consistent, unambiguous and extensible method of communication of settings and capabilities in a consolidated and logical manner.</span></span>

<span data-ttu-id="2c7b2-113">Print Schema 關鍵字和 Print Schema Framework 的概念基礎是一致的，缺乏不明確的擴充性。</span><span class="sxs-lookup"><span data-stu-id="2c7b2-113">The conceptual foundations of the Print Schema Keywords and the Print Schema Framework are consistency, lack of ambiguity and extensibility.</span></span> <span data-ttu-id="2c7b2-114">一致性是透過使用 Print Schema 關鍵字和 Print Schema Framework 來達成，以作為下一代列印元件之間的通訊基礎結構。</span><span class="sxs-lookup"><span data-stu-id="2c7b2-114">Consistency is achieved through the use of the Print Schema Keywords and Print Schema Framework as the building blocks for the communication between next-generation printing components.</span></span> <span data-ttu-id="2c7b2-115">應用程式、Microsoft Windows 列印子系統以及 IHV 外掛程式和驅動程式都會使用此常見機制進行互動。</span><span class="sxs-lookup"><span data-stu-id="2c7b2-115">Applications, the Microsoft Windows printing subsystem, and IHV plug-ins and drivers interact using this common mechanism.</span></span> <span data-ttu-id="2c7b2-116">這些關鍵字、其結構和其意義將由公用架構妥善定義。</span><span class="sxs-lookup"><span data-stu-id="2c7b2-116">These keywords, their structure and their meaning will be well-defined by the public schema.</span></span> <span data-ttu-id="2c7b2-117">這可防止特定關鍵字的意義不明確，並可避免重複或重複的關鍵字。</span><span class="sxs-lookup"><span data-stu-id="2c7b2-117">This prevents ambiguity in the meaning of a particular keyword, and prevents redundant or duplicate keywords.</span></span> <span data-ttu-id="2c7b2-118">所有元件都可以依賴使用特定關鍵字來傳達特定意圖，並讓收件者充分瞭解該意圖。</span><span class="sxs-lookup"><span data-stu-id="2c7b2-118">All components can rely on using a particular keyword to convey a certain intent and have that intent be well-understood by the recipient.</span></span> <span data-ttu-id="2c7b2-119">擴充性的關鍵是列印架構關鍵字的壽命，以確保公用架構為動態實體。</span><span class="sxs-lookup"><span data-stu-id="2c7b2-119">Extensibility is vital to be the longevity of the Print Schema Keywords, ensuring that the public schema is a dynamic entity.</span></span> <span data-ttu-id="2c7b2-120">此結構也允許私用延伸模組，可授與 Ihv 可依需求創新的彈性，並記得未來將私用關鍵字納入公用架構中，是保留一致性和避免混淆的必要。</span><span class="sxs-lookup"><span data-stu-id="2c7b2-120">The structure also allows private extensions, which grants IHVs the flexibility to innovate as desired, keeping in mind future inclusion of a private keyword into the public schema is essential to preserving consistency and preventing ambiguity.</span></span>

## <a name="related-topics"></a><span data-ttu-id="2c7b2-121">相關主題</span><span class="sxs-lookup"><span data-stu-id="2c7b2-121">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="2c7b2-122">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="2c7b2-122">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



