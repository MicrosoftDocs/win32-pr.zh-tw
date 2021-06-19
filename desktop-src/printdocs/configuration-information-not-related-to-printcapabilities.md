---
description: 除了 PrintCapabilities 之外，PrintTicket 還可讓用戶端以屬性專案的形式加入其他資訊。
ms.assetid: 00f1d2c4-3c71-4b64-b689-83b4399aa61d
title: 與 PrintCapabilities 無關的設定資訊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 40e4ac332d6e9b106ab9d68c29d03366761c01d5
ms.sourcegitcommit: 5d4e99f4c8f42f5f543e52cb9beb9fb13ec56c5f
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/19/2021
ms.locfileid: "112409651"
---
# <a name="configuration-information-not-related-to-printcapabilities"></a><span data-ttu-id="ffc52-103">與 PrintCapabilities 無關的設定資訊</span><span class="sxs-lookup"><span data-stu-id="ffc52-103">Configuration Information Not Related to PrintCapabilities</span></span>

<span data-ttu-id="ffc52-104">本主題並非最新的。</span><span class="sxs-lookup"><span data-stu-id="ffc52-104">This topic is not current.</span></span> <span data-ttu-id="ffc52-105">如需最新資訊，請參閱 [列印架構規格](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)。</span><span class="sxs-lookup"><span data-stu-id="ffc52-105">For the most current information, see the [Print Schema Specification](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip).</span></span>

<span data-ttu-id="ffc52-106">除了提供 PrintCapabilities 中所定義之裝置屬性的選項之外，PrintTicket 還可讓用戶端以屬性專案的形式加入其他資訊。</span><span class="sxs-lookup"><span data-stu-id="ffc52-106">In addition to providing selections for the device attributes defined in the PrintCapabilities, the PrintTicket allows additional information to be added by clients in the form of Property elements.</span></span> <span data-ttu-id="ffc52-107">列印架構會定義一些標準的屬性實例，而介面提供者也可以自由地引進私用屬性實例。</span><span class="sxs-lookup"><span data-stu-id="ffc52-107">The Print Schema defines a number of standard Property instances, and the interface provider is free to introduce private Property instances as well.</span></span> <span data-ttu-id="ffc52-108">例如，如果組織的成員將大部分的列印工作傳送至中央批次設備，則可以為每個作業指定包含傳回位址的私用屬性實例。</span><span class="sxs-lookup"><span data-stu-id="ffc52-108">For example, if members of an organization send most of their print jobs to a central batch facility, they can specify for each job a private Property instance that contains a return address.</span></span> <span data-ttu-id="ffc52-109">這個屬性可讓您更輕鬆地傳遞完成的作業。</span><span class="sxs-lookup"><span data-stu-id="ffc52-109">This Property can make it easier to deliver the completed job can be delivered to the originator.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ffc52-110">相關主題</span><span class="sxs-lookup"><span data-stu-id="ffc52-110">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ffc52-111">列印架構規格</span><span class="sxs-lookup"><span data-stu-id="ffc52-111">Print Schema Specification</span></span>](https://download.microsoft.com/download/D/E/C/DECA6E6B-3E81-48E7-B7EF-6D92A547D03C/print-schema-spec-2-0.zip)
</dt> </dl>

 

 



