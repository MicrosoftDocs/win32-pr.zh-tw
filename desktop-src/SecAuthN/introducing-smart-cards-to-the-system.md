---
description: 在智慧卡子系統可以找到智慧卡之前，必須先將智慧卡引入系統。
ms.assetid: 5b331d7d-9440-4e0d-a73b-48a2a556c31c
title: 將智慧卡引入系統
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6b9134dd9efce17b60f3495bf7bfc36b03c34ed3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194510"
---
# <a name="introducing-smart-cards-to-the-system"></a><span data-ttu-id="4415f-103">將智慧卡引入系統</span><span class="sxs-lookup"><span data-stu-id="4415f-103">Introducing Smart Cards to the System</span></span>

<span data-ttu-id="4415f-104">在 [*智慧卡子系統*](../secgloss/s-gly.md) 可以找到 [*智慧卡*](../secgloss/s-gly.md)之前，必須先將智慧卡引入系統。</span><span class="sxs-lookup"><span data-stu-id="4415f-104">Before the [*smart card subsystem*](../secgloss/s-gly.md) can find a [*smart card*](../secgloss/s-gly.md), the smart card must be introduced to the system.</span></span> <span data-ttu-id="4415f-105">這通常是透過卡片製造商提供的智慧卡設定工具來完成。</span><span class="sxs-lookup"><span data-stu-id="4415f-105">This is typically done with a smart card setup tool provided by the card manufacturer.</span></span> <span data-ttu-id="4415f-106">此工具可能是磁片磁碟機上的一種程式， (與智慧卡) 、網站上可用的 ActiveX 控制項等等。</span><span class="sxs-lookup"><span data-stu-id="4415f-106">The tool could come as a program on a floppy disk (with the smart card), an ActiveX control available on a website, and so on.</span></span>

<span data-ttu-id="4415f-107">安裝工具必須提供下列有關卡片的資訊：</span><span class="sxs-lookup"><span data-stu-id="4415f-107">The setup tool must provide the following pieces of information about the card:</span></span>

-   <span data-ttu-id="4415f-108">它的 [*ATR 字串*](../secgloss/a-gly.md)，以及選用的遮罩，用來做為識別卡片的輔助工具。</span><span class="sxs-lookup"><span data-stu-id="4415f-108">Its [*ATR string*](../secgloss/a-gly.md), and an optional mask to use as an aid in identifying the card.</span></span>
-   <span data-ttu-id="4415f-109">卡片所支援的智慧卡介面清單。</span><span class="sxs-lookup"><span data-stu-id="4415f-109">A list of smart card interfaces supported by the card.</span></span>
-   <span data-ttu-id="4415f-110">卡片的顯示名稱，用來識別使用者的卡片。</span><span class="sxs-lookup"><span data-stu-id="4415f-110">A display name for the card, to be used in identifying the card to the user.</span></span> <span data-ttu-id="4415f-111">在大部分的情況下，使用者會將它提供給安裝工具。</span><span class="sxs-lookup"><span data-stu-id="4415f-111">In most cases, the user will supply this to the setup tool.</span></span>
-   <span data-ttu-id="4415f-112">與卡片相關聯的 [*主要服務提供者*](../secgloss/p-gly.md) (選擇性) ，可在透過 COM 介面存取卡片時使用。</span><span class="sxs-lookup"><span data-stu-id="4415f-112">The [*primary service provider*](../secgloss/p-gly.md) associated with the card (optional), to be used when accessing the card through COM interfaces.</span></span>

<span data-ttu-id="4415f-113">為了簡化安裝工具，以及確保 [*智慧卡資料庫*](../secgloss/s-gly.md)的完整性，智慧卡子系統提供下列兩個功能。</span><span class="sxs-lookup"><span data-stu-id="4415f-113">To simplify setup tools, and to ensure the integrity of the [*smart card database*](../secgloss/s-gly.md), the smart card subsystem provides the following two functions.</span></span> <span data-ttu-id="4415f-114">[**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) 會在資料庫中引進智慧卡，而 [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) 則會將它從資料庫中移除。</span><span class="sxs-lookup"><span data-stu-id="4415f-114">[**SCardIntroduceCardType**](/windows/desktop/api/Winscard/nf-winscard-scardintroducecardtypea) introduces a smart card into the database and [**SCardForgetCardType**](/windows/desktop/api/Winscard/nf-winscard-scardforgetcardtypea) removes it from the database.</span></span>

 

 
