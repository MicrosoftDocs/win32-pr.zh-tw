---
description: 您可以使用智慧卡子系統，與可能不符合 ISO 7816 規格的卡片進行通訊。
ms.assetid: ea6cfa5a-2abf-4b7f-b3f4-99655266f030
title: 直接存取卡的功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ad360974210114a1069db3226ee814d08008cc98
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847724"
---
# <a name="direct-card-access-functions"></a><span data-ttu-id="83aae-103">直接存取卡的功能</span><span class="sxs-lookup"><span data-stu-id="83aae-103">Direct Card Access Functions</span></span>

<span data-ttu-id="83aae-104">您可以使用 [*智慧卡*](/windows/desktop/SecGloss/s-gly) 子系統，與可能不符合 ISO 7816 規格的卡片進行通訊。</span><span class="sxs-lookup"><span data-stu-id="83aae-104">By using the [*smart card*](/windows/desktop/SecGloss/s-gly) subsystem, you can communicate with cards that may not conform to the ISO 7816 specifications.</span></span> <span data-ttu-id="83aae-105">若要這樣做，下列函式可讓您藉由提供 [*讀取器*](/windows/desktop/SecGloss/r-gly)的直接、低層級操作，來控制應用程式與卡片之間通訊的屬性。</span><span class="sxs-lookup"><span data-stu-id="83aae-105">To do this, the following functions let you control the attributes of the communications between the application and the card by giving you direct, low-level manipulation of the [*reader*](/windows/desktop/SecGloss/r-gly).</span></span>

<span data-ttu-id="83aae-106">若要使用這些函式，您必須提供有問題的屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="83aae-106">To use these functions, you have to supply an identifier for the attribute in question.</span></span> <span data-ttu-id="83aae-107">如需有效的屬性識別碼和值，請參閱表格3-1 中 *PC-Connected 介面裝置的需求*。</span><span class="sxs-lookup"><span data-stu-id="83aae-107">For valid attribute identifiers and values, refer to Table 3-1 in *Requirements for PC-Connected Interface Devices*.</span></span>



| <span data-ttu-id="83aae-108">主題</span><span class="sxs-lookup"><span data-stu-id="83aae-108">Topic</span></span>                                    | <span data-ttu-id="83aae-109">描述</span><span class="sxs-lookup"><span data-stu-id="83aae-109">Description</span></span>                           |
|------------------------------------------|---------------------------------------|
| [<span data-ttu-id="83aae-110">**SCardControl**</span><span class="sxs-lookup"><span data-stu-id="83aae-110">**SCardControl**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardcontrol)     | <span data-ttu-id="83aae-111">提供讀取器的直接控制權。</span><span class="sxs-lookup"><span data-stu-id="83aae-111">Provide direct control of the reader.</span></span> |
| [<span data-ttu-id="83aae-112">**SCardGetAttrib**</span><span class="sxs-lookup"><span data-stu-id="83aae-112">**SCardGetAttrib**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardgetattrib) | <span data-ttu-id="83aae-113">取得讀取器屬性。</span><span class="sxs-lookup"><span data-stu-id="83aae-113">Get reader attributes.</span></span>                |
| [<span data-ttu-id="83aae-114">**SCardSetAttrib**</span><span class="sxs-lookup"><span data-stu-id="83aae-114">**SCardSetAttrib**</span></span>](/windows/desktop/api/Winscard/nf-winscard-scardsetattrib) | <span data-ttu-id="83aae-115">設定讀取器屬性。</span><span class="sxs-lookup"><span data-stu-id="83aae-115">Set reader attribute.</span></span>                 |



 

 

 
