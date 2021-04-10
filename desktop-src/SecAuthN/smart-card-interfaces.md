---
description: 智慧卡介面是由一組智慧卡內可用的預先定義的服務、叫用服務所需的通訊協定，以及有關服務內容的任何假設所組成。
ms.assetid: 4f9c13da-8fe3-43e7-875f-04850495edf3
title: 智慧卡介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4d5f11f619e69cafa484e209c3346357aa5a031d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694235"
---
# <a name="smart-card-interfaces"></a><span data-ttu-id="23676-103">智慧卡介面</span><span class="sxs-lookup"><span data-stu-id="23676-103">Smart Card Interfaces</span></span>

<span data-ttu-id="23676-104">[*智慧卡*](../secgloss/s-gly.md)介面是由一組 *智慧卡* 內可用的預先定義的服務、叫用服務所需的通訊協定，以及有關服務內容的任何假設所組成。</span><span class="sxs-lookup"><span data-stu-id="23676-104">A [*smart card*](../secgloss/s-gly.md) interface consists of a predefined set of services available within a *smart card*, the protocols necessary to invoke the services, and any assumptions regarding the context of the services.</span></span>

<span data-ttu-id="23676-105">就智慧卡而言，「介面」一詞類似于 COM 中使用它的方式，後者在概念上類似于 ISO 7816/5 應用程式識別碼，但具有不同的範圍。</span><span class="sxs-lookup"><span data-stu-id="23676-105">With respect to smart cards, the term "interface" is similar to how it is used in COM, which in turn is similar in concept to the ISO 7816/5 application identifier but with a different scope.</span></span>

<span data-ttu-id="23676-106">每個智慧卡介面都是由 GUID 識別。</span><span class="sxs-lookup"><span data-stu-id="23676-106">Each smart card interface is identified by a GUID.</span></span> <span data-ttu-id="23676-107">例如，可能定義了可提供 biorhythm 資訊給其持有者的介面。</span><span class="sxs-lookup"><span data-stu-id="23676-107">For example, an interface might be defined that provides biorhythm information to its holder.</span></span> <span data-ttu-id="23676-108">如果指定的智慧卡支援這種服務，則可能會宣稱支援該介面 GUID。</span><span class="sxs-lookup"><span data-stu-id="23676-108">If a given smart card supports this service, then it may claim to support that interface GUID.</span></span> <span data-ttu-id="23676-109">使用介面 Guid，應用程式可能會搜尋一組特定的介面，找出支援該集合的任何卡片來完成工作。</span><span class="sxs-lookup"><span data-stu-id="23676-109">Using the interface GUIDs, an application may search for a particular set of interfaces, locating any card that supports that set, to complete a task.</span></span>

<span data-ttu-id="23676-110">雖然介面具有一個 GUID，但在不同的卡片上可能會有不同的執行方式。</span><span class="sxs-lookup"><span data-stu-id="23676-110">Although an interface has one GUID, it might be implemented differently on different cards.</span></span> <span data-ttu-id="23676-111">例如，上述 biorhythm 介面可以有數個不同的實作為，但全部都是使用相同的 GUID 來參考。</span><span class="sxs-lookup"><span data-stu-id="23676-111">For example, the biorhythm interface mentioned above can have several different implementations, yet all are referenced using the same GUID.</span></span> <span data-ttu-id="23676-112">不同的執行不會變更應用程式與智慧卡之間的互動;不過， [*服務提供者*](../secgloss/c-gly.md) 和智慧卡之間的互動可能會因介面的執行而有所不同。</span><span class="sxs-lookup"><span data-stu-id="23676-112">The different implementations would not change the interaction between the application and the smart card; however, the interaction between the [*service provider*](../secgloss/c-gly.md) and the smart cards may differ depending on the interface's implementation.</span></span>

<span data-ttu-id="23676-113">智慧卡支援的一組介面是在智慧卡簡介中定義 (請參閱 [將智慧卡引入系統](introducing-smart-cards-to-the-system.md)) 。</span><span class="sxs-lookup"><span data-stu-id="23676-113">The set of interfaces supported by a smart card is defined during smart card introduction (see [Introducing Smart Cards to the System](introducing-smart-cards-to-the-system.md)).</span></span>

 

 
