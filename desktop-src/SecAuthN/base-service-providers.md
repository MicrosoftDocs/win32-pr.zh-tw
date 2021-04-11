---
description: 這些服務提供者提供基本的智慧卡功能。
ms.assetid: 1d887c4c-095c-4e1e-8b9a-7761acda2cbf
title: 基底服務提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 25dfa6c190e7a09ed4dfceafb983878906e8e3b2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944463"
---
# <a name="base-service-providers"></a><span data-ttu-id="923c7-103">基底服務提供者</span><span class="sxs-lookup"><span data-stu-id="923c7-103">Base Service Providers</span></span>

<span data-ttu-id="923c7-104">這些 [*服務提供者*](/windows/desktop/SecGloss/c-gly) 提供基本的 [*智慧卡*](/windows/desktop/SecGloss/s-gly) 功能。</span><span class="sxs-lookup"><span data-stu-id="923c7-104">These [*service providers*](/windows/desktop/SecGloss/c-gly) provide the basic [*smart card*](/windows/desktop/SecGloss/s-gly) capabilities.</span></span> <span data-ttu-id="923c7-105">它們可用來存取單一智慧卡功能，或可結合其 COM 介面，在單一服務提供者內提供數個功能。</span><span class="sxs-lookup"><span data-stu-id="923c7-105">They can be used to access a single smart card capability, or their COM interfaces can be combined to provide several capabilities within a single service provider.</span></span> <span data-ttu-id="923c7-106">這些服務提供者是用於開發其他服務提供者其他功能的組建區塊。</span><span class="sxs-lookup"><span data-stu-id="923c7-106">These service providers are the building blocks for developing additional functionality to other service providers.</span></span>

<span data-ttu-id="923c7-107">下列工作可由智慧卡 SDK 提供的基底服務提供者介面執行。</span><span class="sxs-lookup"><span data-stu-id="923c7-107">The following tasks can be performed by base service provider interfaces supplied by the Smart Card SDK.</span></span>



| <span data-ttu-id="923c7-108">Task</span><span class="sxs-lookup"><span data-stu-id="923c7-108">Task</span></span>                                                                                                                   | <span data-ttu-id="923c7-109">基底服務提供者介面</span><span class="sxs-lookup"><span data-stu-id="923c7-109">Base service provider interfaces</span></span>         | <span data-ttu-id="923c7-110">DLL</span><span class="sxs-lookup"><span data-stu-id="923c7-110">DLL</span></span>      |
|------------------------------------------------------------------------------------------------------------------------|------------------------------------------|----------|
| <span data-ttu-id="923c7-111">連接到智慧卡、執行交易、關閉連接等。</span><span class="sxs-lookup"><span data-stu-id="923c7-111">Connect to a smart card, implement transactions, close connections, and so on.</span></span>                                         | [<span data-ttu-id="923c7-112">**ISCard**</span><span class="sxs-lookup"><span data-stu-id="923c7-112">**ISCard**</span></span>](iscard.md)                 | <span data-ttu-id="923c7-113">SCardSSP</span><span class="sxs-lookup"><span data-stu-id="923c7-113">SCardSSP</span></span> |
| <span data-ttu-id="923c7-114">維護命令 APDU 和 [*回復 apdu*](/windows/desktop/SecGloss/r-gly)。</span><span class="sxs-lookup"><span data-stu-id="923c7-114">Maintain a command APDU and [*reply APDU*](/windows/desktop/SecGloss/r-gly).</span></span>          | [<span data-ttu-id="923c7-115">**ISCardCmd**</span><span class="sxs-lookup"><span data-stu-id="923c7-115">**ISCardCmd**</span></span>](iscardcmd.md)           | <span data-ttu-id="923c7-116">SCardSSP</span><span class="sxs-lookup"><span data-stu-id="923c7-116">SCardSSP</span></span> |
| <span data-ttu-id="923c7-117">查詢 [*智慧卡資料庫*](/windows/desktop/SecGloss/s-gly)。</span><span class="sxs-lookup"><span data-stu-id="923c7-117">Query the [*smart card database*](/windows/desktop/SecGloss/s-gly).</span></span> | [<span data-ttu-id="923c7-118">**ISCardDatabase**</span><span class="sxs-lookup"><span data-stu-id="923c7-118">**ISCardDatabase**</span></span>](iscarddatabase.md) | <span data-ttu-id="923c7-119">SCardSSP</span><span class="sxs-lookup"><span data-stu-id="923c7-119">SCardSSP</span></span> |
| <span data-ttu-id="923c7-120">找出智慧卡或讀卡機。</span><span class="sxs-lookup"><span data-stu-id="923c7-120">Locate a smart card or reader.</span></span>                                                                                         | [<span data-ttu-id="923c7-121">**ISCardLocate**</span><span class="sxs-lookup"><span data-stu-id="923c7-121">**ISCardLocate**</span></span>](iscardlocate.md)     | <span data-ttu-id="923c7-122">SCardSSP</span><span class="sxs-lookup"><span data-stu-id="923c7-122">SCardSSP</span></span> |
| <span data-ttu-id="923c7-123">建立 ISO7816-4 命令 APDU。</span><span class="sxs-lookup"><span data-stu-id="923c7-123">Build an ISO7816-4 command APDU.</span></span>                                                                                       | [<span data-ttu-id="923c7-124">**ISCardISO7816**</span><span class="sxs-lookup"><span data-stu-id="923c7-124">**ISCardISO7816**</span></span>](iscardiso7816.md)   | <span data-ttu-id="923c7-125">SCardSSP</span><span class="sxs-lookup"><span data-stu-id="923c7-125">SCardSSP</span></span> |
| <span data-ttu-id="923c7-126">使用 Visual Basic 相容的類型包裝 Istream 緩衝區。</span><span class="sxs-lookup"><span data-stu-id="923c7-126">Wrap an Istream buffer by using Visual Basic–compatible types.</span></span>                                                         | [<span data-ttu-id="923c7-127">**IByteBuffer**</span><span class="sxs-lookup"><span data-stu-id="923c7-127">**IByteBuffer**</span></span>](ibytebuffer.md)       | <span data-ttu-id="923c7-128">SCardSSP</span><span class="sxs-lookup"><span data-stu-id="923c7-128">SCardSSP</span></span> |



 

<span data-ttu-id="923c7-129">下列程式顯示這些基底服務提供者介面的一般使用方法。</span><span class="sxs-lookup"><span data-stu-id="923c7-129">The following procedure shows a typical use of these base service provider interfaces.</span></span> <span data-ttu-id="923c7-130">在此範例中，會使用 [**ISCard**](iscard.md)、 [**ISCardISO7816**](iscardiso7816.md)和 [**ISCardCmd**](iscardcmd.md) 介面來執行交易。</span><span class="sxs-lookup"><span data-stu-id="923c7-130">In this example, the [**ISCard**](iscard.md), [**ISCardISO7816**](iscardiso7816.md), and [**ISCardCmd**](iscardcmd.md) interfaces are used to perform a transaction.</span></span>

<span data-ttu-id="923c7-131">**執行交易**</span><span class="sxs-lookup"><span data-stu-id="923c7-131">**To perform a transaction**</span></span>

1.  <span data-ttu-id="923c7-132">針對所需的所有基底服務提供者介面建立實例 (例如， [**ISCard**](iscard.md)、 [**ISCardISO7816**](iscardiso7816.md)和 [**ISCardCmd**](iscardcmd.md)) 。</span><span class="sxs-lookup"><span data-stu-id="923c7-132">Create an instance for all base service provider interfaces needed (for example, [**ISCard**](iscard.md), [**ISCardISO7816**](iscardiso7816.md), and [**ISCardCmd**](iscardcmd.md)).</span></span>
2.  <span data-ttu-id="923c7-133">使用 [**ISCard**](iscard.md) 介面中的方法連接到特定的智慧卡。</span><span class="sxs-lookup"><span data-stu-id="923c7-133">Connect to a particular smart card by using the methods in the [**ISCard**](iscard.md) interface.</span></span>
3.  <span data-ttu-id="923c7-134">使用 [**ISCardISO7816**](iscardiso7816.md) 和 [**ISCardCmd**](iscardcmd.md) 物件，藉由呼叫 **ISCardISO7816** 方法來建立 ISO 7816-4 命令。</span><span class="sxs-lookup"><span data-stu-id="923c7-134">Using [**ISCardISO7816**](iscardiso7816.md) and an [**ISCardCmd**](iscardcmd.md) object, build an ISO 7816-4 command by calling the **ISCardISO7816** method.</span></span> <span data-ttu-id="923c7-135">此命令會包含在 **ISCardCmd** 中做為命令 APDU。</span><span class="sxs-lookup"><span data-stu-id="923c7-135">The command is contained in **ISCardCmd** as the command APDU.</span></span>
4.  <span data-ttu-id="923c7-136">藉由呼叫 [**ISCard**](iscard.md) transaction 方法並傳遞所建立的 [**ISCardCmd**](iscardcmd.md) 物件，以使用卡片進行交易。</span><span class="sxs-lookup"><span data-stu-id="923c7-136">Do a transaction with the card by calling the [**ISCard**](iscard.md) transaction method and passing the created [**ISCardCmd**](iscardcmd.md) object.</span></span> <span data-ttu-id="923c7-137">當交易完成時，結果會儲存在 **ISCardCmd** 回復 APDU 中。</span><span class="sxs-lookup"><span data-stu-id="923c7-137">When the transaction is complete, the results are stored in the **ISCardCmd** reply APDU.</span></span>
5.  <span data-ttu-id="923c7-138">解讀 [**ISCardCmd**](iscardcmd.md) 回復 APDU 並重複。</span><span class="sxs-lookup"><span data-stu-id="923c7-138">Interpret the [**ISCardCmd**](iscardcmd.md) reply APDU and repeat.</span></span>
6.  <span data-ttu-id="923c7-139">在作業完成時釋放所有介面。</span><span class="sxs-lookup"><span data-stu-id="923c7-139">Release all interfaces when operations are complete.</span></span>

<span data-ttu-id="923c7-140">如需在 Dll 內建立的 APDU 命令的詳細資訊，請參閱 [建立 ISO7816-4 APDU 命令](building-an-iso7816-4-apdu-command.md)。</span><span class="sxs-lookup"><span data-stu-id="923c7-140">For information about the APDU command built within the DLLs, see [Building an ISO7816-4 APDU Command](building-an-iso7816-4-apdu-command.md).</span></span>

 

 
