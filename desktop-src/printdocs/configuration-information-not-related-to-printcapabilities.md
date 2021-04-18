---
description: 本主題並非最新的。 如需最新資訊，請參閱列印架構規格。
ms.assetid: 00f1d2c4-3c71-4b64-b689-83b4399aa61d
title: 與 PrintCapabilities 無關的設定資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 26bbc1b37d430158d6e8c020aa5994fe4e28f4af
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106976410"
---
# <a name="configuration-information-not-related-to-printcapabilities"></a><span data-ttu-id="7b892-104">與 PrintCapabilities 無關的設定資訊</span><span class="sxs-lookup"><span data-stu-id="7b892-104">Configuration Information Not Related to PrintCapabilities</span></span>

<span data-ttu-id="7b892-105">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="7b892-105">This topic is not current.</span></span> <span data-ttu-id="7b892-106">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="7b892-106">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="7b892-107">除了提供 PrintCapabilities 中所定義之裝置屬性的選項之外，PrintTicket 還可讓用戶端以屬性專案的形式加入其他資訊。</span><span class="sxs-lookup"><span data-stu-id="7b892-107">In addition to providing selections for the device attributes defined in the PrintCapabilities, the PrintTicket allows additional information to be added by clients in the form of Property elements.</span></span> <span data-ttu-id="7b892-108">列印架構會定義一些標準的屬性實例，而介面提供者也可以自由地引進私用屬性實例。</span><span class="sxs-lookup"><span data-stu-id="7b892-108">The Print Schema defines a number of standard Property instances, and the interface provider is free to introduce private Property instances as well.</span></span> <span data-ttu-id="7b892-109">例如，如果組織的成員將大部分的列印工作傳送至中央批次設備，則可以為每個作業指定包含傳回位址的私用屬性實例。</span><span class="sxs-lookup"><span data-stu-id="7b892-109">For example, if members of an organization send most of their print jobs to a central batch facility, they can specify for each job a private Property instance that contains a return address.</span></span> <span data-ttu-id="7b892-110">這個屬性可讓您更輕鬆地傳遞完成的作業。</span><span class="sxs-lookup"><span data-stu-id="7b892-110">This Property can make it easier to deliver the completed job can be delivered to the originator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="7b892-111">相關主題</span><span class="sxs-lookup"><span data-stu-id="7b892-111">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7b892-112">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="7b892-112">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



