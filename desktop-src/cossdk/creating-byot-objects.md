---
description: 建立 BYOT 物件
ms.assetid: 16b68ce2-46b2-4e35-bf92-f132dcb354e3
title: 建立 BYOT 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6544c5085061be5d1100706930a3e1617ec24890
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106998436"
---
# <a name="creating-byot-objects"></a><span data-ttu-id="45434-103">建立 BYOT 物件</span><span class="sxs-lookup"><span data-stu-id="45434-103">Creating BYOT Objects</span></span>

<span data-ttu-id="45434-104">新的 BYOT 物件會建立具有手動交易的物件。</span><span class="sxs-lookup"><span data-stu-id="45434-104">A new BYOT object creates objects with manual transactions.</span></span> <span data-ttu-id="45434-105">[**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex)和 [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex)這兩個介面具有單一方法 **CreateInstance**，分別採用 **ITransaction** 介面指標和提示 URL。</span><span class="sxs-lookup"><span data-stu-id="45434-105">The two interfaces, [**ICreateWithTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtransactionex) and [**ICreateWithTipTransactionEx**](/windows/desktop/api/ComSvcs/nn-comsvcs-icreatewithtiptransactionex), have a single method, **CreateInstance**, which take an **ITransaction** interface pointer and TIP URL, respectively.</span></span> <span data-ttu-id="45434-106">[**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) 會將介面指標傳回至新建立的物件，該物件會在指定的交易中登記。</span><span class="sxs-lookup"><span data-stu-id="45434-106">[**CreateInstance**](/windows/desktop/api/ComSvcs/nf-comsvcs-icreatewithtransactionex-createinstance) returns an interface pointer to the newly created object, which is enlisted within the specified transaction.</span></span>

<span data-ttu-id="45434-107">釋放具有手動交易的物件時，COM + 不會嘗試認可交易。</span><span class="sxs-lookup"><span data-stu-id="45434-107">When an object with a manual transaction is released, COM+ does not attempt to commit the transaction.</span></span> <span data-ttu-id="45434-108">交易是由外部交易管理員明確控制，該管理員會將建立此物件的交易分配給該交易。</span><span class="sxs-lookup"><span data-stu-id="45434-108">The transaction is controlled explicitly by the external transaction manager that dispensed the transaction under which this object had been created.</span></span>

> [!Note]  
> <span data-ttu-id="45434-109">必須將 Byot. ByotServerEx 物件匯入至 COM + 應用程式。</span><span class="sxs-lookup"><span data-stu-id="45434-109">The Byot.ByotServerEx object needs to be imported into a COM+ application.</span></span>

 

 

 



