---
description: 系統管理員可以強制 COM 用戶端應用程式一律使用現有封裝中的相同 COM 伺服器複本&\# 郵件，而不會影響其他應用程式&\# 郵件; 方法是指定 COM 伺服器和用戶端之間的隔離元件關聯性。
ms.assetid: 814eca94-2bb5-4aff-8de3-473da71d4400
title: 使現有封裝中的 COM 元件成為私用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4935d20c5034af81a52c18d35454553b04cfb97
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987720"
---
# <a name="make-a-com-component-in-an-existing-package-private"></a><span data-ttu-id="a71bf-103">使現有封裝中的 COM 元件成為私用</span><span class="sxs-lookup"><span data-stu-id="a71bf-103">Make a COM Component in an Existing Package Private</span></span>

<span data-ttu-id="a71bf-104">系統管理員可以藉由指定 COM 伺服器和用戶端之間的 [隔離元件](isolated-components.md) 關聯性，強制 com 用戶端應用程式一律使用現有封裝中的相同 com 伺服器複本，而不會影響其他應用程式。</span><span class="sxs-lookup"><span data-stu-id="a71bf-104">An administrator can force a COM-client application to always use the same copy of a COM-server in an existing package—without affecting other applications—by specifying an [isolated components](isolated-components.md) relationship between the COM server and client.</span></span> <span data-ttu-id="a71bf-105">這會將 COM 伺服器元件的私用複本安裝至用戶端應用程式專用的位置。</span><span class="sxs-lookup"><span data-stu-id="a71bf-105">This installs a private copy of the COM-server component to a location used exclusively by the client application.</span></span> <span data-ttu-id="a71bf-106">系統管理員必須使用轉換或封裝撰寫工具來執行下列作業：</span><span class="sxs-lookup"><span data-stu-id="a71bf-106">The administrator needs to use transforms or a package authoring tool to do the following:</span></span>

-   <span data-ttu-id="a71bf-107">將 COM 伺服器 DLL 和 .exe 用戶端放在不同的元件中。</span><span class="sxs-lookup"><span data-stu-id="a71bf-107">Put the COM server DLL and the .exe client in separate components.</span></span>
-   <span data-ttu-id="a71bf-108">在 [元件共用] 資料行中，以 COM-用戶端元件的 [IsolatedComponent 資料表](isolatedcomponent-table.md) 輸入記錄 \_ ，並在 [元件應用程式] 資料行中輸入用戶端應用程式 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a71bf-108">Enter a record in the [IsolatedComponent table](isolatedcomponent-table.md) with the COM-client component in the Component\_Shared column and the client application in the Component\_Application column.</span></span> <span data-ttu-id="a71bf-109">在順序資料表中包含 [IsolateComponents 動作](isolatecomponents-action.md) 。</span><span class="sxs-lookup"><span data-stu-id="a71bf-109">Include the [IsolateComponents action](isolatecomponents-action.md) in the sequence tables.</span></span>
-   <span data-ttu-id="a71bf-110">在元件 [資料表](component-table.md)記錄中，為共用的元件設定 **msidbComponentAttributesSharedDllRefCount** 位 \_ 。</span><span class="sxs-lookup"><span data-stu-id="a71bf-110">Set the **msidbComponentAttributesSharedDllRefCount** bit in the [Component table](component-table.md) record for Component\_Shared.</span></span> <span data-ttu-id="a71bf-111">在與其他安裝技術共用的情況下，安裝程式需要在共用位置上使用此全域 refcount 來保護共用檔案和註冊。</span><span class="sxs-lookup"><span data-stu-id="a71bf-111">The installer requires this global refcount on the shared location to protect the shared files and registration in cases where there is sharing with other installation technologies.</span></span>

 

 



