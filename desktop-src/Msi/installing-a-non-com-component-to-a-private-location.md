---
description: 若要強制用戶端應用程式一律使用相同的非 COM 伺服器複本，請撰寫應用程式的安裝封裝，以指定伺服器與用戶端之間的隔離元件關聯性。
ms.assetid: 3ca9cad7-6848-4483-b5e3-2b7bbdefe605
title: 將非 COM 元件安裝至私用位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 52ea4e10e7a08fd008352a36feca537685ee4390
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852763"
---
# <a name="installing-a-non-com-component-to-a-private-location"></a><span data-ttu-id="4fd04-103">將非 COM 元件安裝至私用位置</span><span class="sxs-lookup"><span data-stu-id="4fd04-103">Installing a non-COM Component to a Private Location</span></span>

<span data-ttu-id="4fd04-104">若要強制用戶端應用程式一律使用相同的非 COM 伺服器複本，請撰寫應用程式的安裝封裝，以指定伺服器與用戶端之間的 [隔離元件](isolated-components.md) 關聯性。</span><span class="sxs-lookup"><span data-stu-id="4fd04-104">To force a client application to always use the same copy of a non-COM server, author the application's installation package to specify an [isolated components](isolated-components.md) relationship between the server and client.</span></span> <span data-ttu-id="4fd04-105">這會將伺服器元件的私用複本安裝至用戶端應用程式專用的位置。</span><span class="sxs-lookup"><span data-stu-id="4fd04-105">This installs a private copy of the server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="4fd04-106">撰寫套件時，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="4fd04-106">Do the following when authoring the package:</span></span>

-   <span data-ttu-id="4fd04-107">將伺服器 DLL 和 .exe 用戶端放在不同的元件中。</span><span class="sxs-lookup"><span data-stu-id="4fd04-107">Put the server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="4fd04-108">在 [元件共用] [](isolatedcomponent-table.md)資料行中的用戶端元件和 [ \_ 元件應用程式] 資料行中的用戶端應用程式中，輸入 IsolatedComponent 資料表中的記錄 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4fd04-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="4fd04-109">在順序資料表中包含 [IsolateComponents 動作](isolatecomponents-action.md) 。</span><span class="sxs-lookup"><span data-stu-id="4fd04-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="4fd04-110">在元件 [資料表](component-table.md) 記錄中，為共用的元件設定 msidbComponentAttributesSharedDllRefCount 位 \_ 。</span><span class="sxs-lookup"><span data-stu-id="4fd04-110">Set the msidbComponentAttributesSharedDllRefCount bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="4fd04-111">在與其他安裝技術共用的情況下，安裝程式需要在共用位置上使用此全域 refcount 來保護共用檔案和註冊。</span><span class="sxs-lookup"><span data-stu-id="4fd04-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>
-   <span data-ttu-id="4fd04-112">避免在元件之間撰寫共用的已註冊路徑。</span><span class="sxs-lookup"><span data-stu-id="4fd04-112">Avoid authoring a shared registered path across components.</span></span>

 

 



