---
description: 概念和邏輯模型完成之後，您就可以在應用程式的實體實作為決策。
ms.assetid: 18c440f0-88c8-4738-9f29-c82772439b51
title: 實體模型：應用程式架構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2f0fab87d76e445a365958ab330f572f657d1505
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104111425"
---
# <a name="the-physical-model-application-architecture"></a><span data-ttu-id="81027-103">實體模型：應用程式架構</span><span class="sxs-lookup"><span data-stu-id="81027-103">The Physical Model: Application Architecture</span></span>

<span data-ttu-id="81027-104">概念和邏輯模型完成之後，您就可以在應用程式的實體實作為決策。</span><span class="sxs-lookup"><span data-stu-id="81027-104">After the conceptual and logical models are complete, you can make decisions on the physical implementation of the application.</span></span> <span data-ttu-id="81027-105">若要建立實體模型，您必須瞭解應用程式的各種服務的所在位置，以及應該如何執行這些服務。</span><span class="sxs-lookup"><span data-stu-id="81027-105">To create the physical model, you must understand where the various services of the application should be located and how they should be implemented.</span></span> <span data-ttu-id="81027-106">判斷各服務的所在位置應該在服務的執行之前。</span><span class="sxs-lookup"><span data-stu-id="81027-106">Determining where various services reside should come before how the services will be implemented.</span></span>

<span data-ttu-id="81027-107">判斷各種服務所在位置的其中一個基本規則：將元件放在使用的位置。</span><span class="sxs-lookup"><span data-stu-id="81027-107">One basic rule for determining where various services reside is this: Put the component where it is being used.</span></span> <span data-ttu-id="81027-108">例如，如果元件顯示基礎用戶端的資訊，則應該在使用者的電腦上。</span><span class="sxs-lookup"><span data-stu-id="81027-108">If, for example, a component displays information for the base client, it should go on the user's computer.</span></span> <span data-ttu-id="81027-109">如果元件會驗證來自基底用戶端的資訊，它也應該位於基礎用戶端的電腦上。</span><span class="sxs-lookup"><span data-stu-id="81027-109">If a component validates information from the base client, it should also reside on the base client's computer.</span></span> <span data-ttu-id="81027-110">如果元件更新資料庫中的資訊，它應該位於資料庫伺服器上。</span><span class="sxs-lookup"><span data-stu-id="81027-110">If a component updates information in a database, it should reside on the database server.</span></span>

<span data-ttu-id="81027-111">當然，還有其他考慮會造成此規則的例外狀況。</span><span class="sxs-lookup"><span data-stu-id="81027-111">There are, of course, additional considerations that make exceptions to this rule.</span></span> <span data-ttu-id="81027-112">效能和安全性問題也可以規定元件的所在位置。</span><span class="sxs-lookup"><span data-stu-id="81027-112">Performance and security issues can also dictate where a component is located.</span></span> <span data-ttu-id="81027-113">請考慮下列事項：</span><span class="sxs-lookup"><span data-stu-id="81027-113">Consider the following:</span></span>

-   <span data-ttu-id="81027-114">元件是否會經常變更，使散發更新變得很困難？</span><span class="sxs-lookup"><span data-stu-id="81027-114">Is a component going to change frequently, making distributing updates difficult?</span></span>
-   <span data-ttu-id="81027-115">元件是否會由其他應用程式使用，例如一般安全性驗證元件？</span><span class="sxs-lookup"><span data-stu-id="81027-115">Will the component be used by other applications, such as a common security verification component?</span></span>
-   <span data-ttu-id="81027-116">元件是否會進行冗長的計算，或執行可卸載至伺服器的功能（例如列印）？</span><span class="sxs-lookup"><span data-stu-id="81027-116">Does the component make lengthy calculations or performs functions, such as printing, that can be offloaded to a server?</span></span>
-   <span data-ttu-id="81027-117">將元件放在伺服器上可以增強元件的安全性嗎？</span><span class="sxs-lookup"><span data-stu-id="81027-117">Can the security of a component be enhanced by placing it on a server?</span></span>

<span data-ttu-id="81027-118">如果資料的系統或位置有所變更，適當地找出應用程式的元件也可以將開發小組與昂貴的編碼進行隔離。</span><span class="sxs-lookup"><span data-stu-id="81027-118">Properly locating components of an application can also insulate the development team from costly recoding if the system or the location of the data changes.</span></span> <span data-ttu-id="81027-119">例如，將資料存取規則放在資料層，而不是在預存程式中，則應用程式更容易與特定 DBMS 的相依性隔離。</span><span class="sxs-lookup"><span data-stu-id="81027-119">For example, by putting the data access rules in a data layer rather than in stored procedures, the application is more easily insulated from dependence on a specific DBMS.</span></span> <span data-ttu-id="81027-120">不只是變更的限制和測試劃分，還可以改變數據源，而且可以散發資料，而不需要以根本上變更應用程式。</span><span class="sxs-lookup"><span data-stu-id="81027-120">Not only are changes confined and testing compartmentalized, but data sources can be changed and data can be distributed without fundamentally changing the application.</span></span>

<span data-ttu-id="81027-121">最後，找出元件應該利用系統效率。</span><span class="sxs-lookup"><span data-stu-id="81027-121">Finally, locating components should take advantage of system efficiencies.</span></span> <span data-ttu-id="81027-122">將商務物件放在網路上的集中位置是時間且符合成本效益的。</span><span class="sxs-lookup"><span data-stu-id="81027-122">It is time and cost-effective to place business objects in centralized locations on the network.</span></span> <span data-ttu-id="81027-123">物件可以在應用程式之間共用，而且可以在部署任何元件之前完成單元測試。</span><span class="sxs-lookup"><span data-stu-id="81027-123">Objects can be shared among applications, and unit testing can be done before any components are deployed.</span></span> <span data-ttu-id="81027-124">您也可以減少維護成本，因為規則變更只會在單一點發生。</span><span class="sxs-lookup"><span data-stu-id="81027-124">Maintenance costs can also be decreased because rule changes occur only at a single point.</span></span>

## <a name="related-topics"></a><span data-ttu-id="81027-125">相關主題</span><span class="sxs-lookup"><span data-stu-id="81027-125">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="81027-126">概念模型：應用程式需求</span><span class="sxs-lookup"><span data-stu-id="81027-126">The Conceptual Model: Application Requirements</span></span>](the-conceptual-model--application-requirements.md)
</dt> <dt>

[<span data-ttu-id="81027-127">邏輯模型：應用程式定義和規劃</span><span class="sxs-lookup"><span data-stu-id="81027-127">The Logical Model: Application Definition and Planning</span></span>](the-logical-model--application-definition-and-planning.md)
</dt> </dl>

 

 



