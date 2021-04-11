---
description: 若要強制 COM 用戶端應用程式一律使用相同的 COM 伺服器複本，請撰寫應用程式的安裝封裝，以指定 COM 伺服器和用戶端之間的隔離元件關聯性。
ms.assetid: 387c1c4d-16f5-4f46-b868-c2be7cb3f942
title: 將 COM 元件安裝至私用位置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 838b3f40c513fd0998402893543e88526e4a6d07
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848373"
---
# <a name="installing-a-com-component-to-a-private-location"></a><span data-ttu-id="f250f-103">將 COM 元件安裝至私用位置</span><span class="sxs-lookup"><span data-stu-id="f250f-103">Installing a COM Component to a Private Location</span></span>

<span data-ttu-id="f250f-104">若要強制 COM 用戶端應用程式一律使用相同的 COM 伺服器複本，請撰寫應用程式的安裝封裝，以指定 COM 伺服器和用戶端之間的 [隔離元件](isolated-components.md) 關聯性。</span><span class="sxs-lookup"><span data-stu-id="f250f-104">To force a COM-client application to always use the same copy of a COM-server, author the application's installation package to specify an [isolated components](isolated-components.md) relationship between the COM server and client.</span></span> <span data-ttu-id="f250f-105">這會將 COM 伺服器元件的私用複本安裝至用戶端應用程式專用的位置。</span><span class="sxs-lookup"><span data-stu-id="f250f-105">This installs a private copy of the COM-server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="f250f-106">撰寫套件時，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="f250f-106">Do the following when authoring the package:</span></span>

-   <span data-ttu-id="f250f-107">將 COM 伺服器 DLL 和 .exe 用戶端放在不同的元件中。</span><span class="sxs-lookup"><span data-stu-id="f250f-107">Put the COM server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="f250f-108">在 [元件共用] 資料行中，以 COM-用戶端元件的 [IsolatedComponent 資料表](isolatedcomponent-table.md) 輸入記錄 \_ ，並在 [元件應用程式] 資料行中輸入用戶端應用程式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f250f-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the COM-client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="f250f-109">在順序資料表中包含 [IsolateComponents 動作](isolatecomponents-action.md) 。</span><span class="sxs-lookup"><span data-stu-id="f250f-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="f250f-110">在元件 [資料表](component-table.md) 記錄中，為共用的元件設定 msidbComponentAttributesSharedDllRefCount 位 \_ 。</span><span class="sxs-lookup"><span data-stu-id="f250f-110">Set the msidbComponentAttributesSharedDllRefCount bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="f250f-111">在與其他安裝技術共用的情況下，安裝程式需要在共用位置上使用此全域 refcount 來保護共用檔案和註冊。</span><span class="sxs-lookup"><span data-stu-id="f250f-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>

 

 



