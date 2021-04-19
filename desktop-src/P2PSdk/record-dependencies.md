---
description: 對等基礎結構不保證接收和處理記錄的順序。
ms.assetid: 840aa931-c54c-463d-b37b-7d01c8a44409
title: 記錄相依性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 75a7cce0803ad25f4a67908256ad78c7abe4b4af
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969365"
---
# <a name="record-dependencies"></a><span data-ttu-id="d2265-103">記錄相依性</span><span class="sxs-lookup"><span data-stu-id="d2265-103">Record Dependencies</span></span>

<span data-ttu-id="d2265-104">對等基礎結構不保證接收和處理記錄的順序。</span><span class="sxs-lookup"><span data-stu-id="d2265-104">The Peer Infrastructure does not guarantee the order for receiving and processing records.</span></span> <span data-ttu-id="d2265-105">如果您的應用程式具有記錄相依性，這表示某一筆記錄的處理或驗證相依于另一筆記錄，則您的應用程式必須能夠處理以任意且無法預測的順序接收記錄的情況。</span><span class="sxs-lookup"><span data-stu-id="d2265-105">If your application has record dependencies, which means that the processing or validation of one record relies on another record, then your application must be able to handle situations when records might be received in an arbitrary and unpredictable order.</span></span> <span data-ttu-id="d2265-106">例如，聊天應用程式可能會有兩種類型的記錄：包含特定使用者相關資訊的記錄，以及包含參考使用者記錄之交談訊息的記錄。</span><span class="sxs-lookup"><span data-stu-id="d2265-106">For example, a chat application may have two types of records: a record that contains information about a specific user, and a record that contains a chat message that refers to the user record.</span></span>

<span data-ttu-id="d2265-107">應用程式必須能夠在使用者記錄聊天訊息之前收到聊天訊息記錄時，處理這種情況。</span><span class="sxs-lookup"><span data-stu-id="d2265-107">An application must be able to handle the situation when a chat message record is received before the user record for the chat message.</span></span> <span data-ttu-id="d2265-108">處理這種情況的其中一種方式是使用 [待命] **清單** 或快取和計時器來等候使用者記錄。</span><span class="sxs-lookup"><span data-stu-id="d2265-108">One way to handle the situation is to wait for the user record by using a **stand-by list**, or a cache and timer.</span></span> <span data-ttu-id="d2265-109">應用程式可以定期檢查清單或快取中的每一筆記錄，然後在收到必要的使用者記錄時處理此情況。</span><span class="sxs-lookup"><span data-stu-id="d2265-109">The application can periodically examine each record in the list or cache, and then handle the situation when the required user record is received.</span></span>

<span data-ttu-id="d2265-110">若要處理記錄相依性，設計完善的應用程式包含下列各項：</span><span class="sxs-lookup"><span data-stu-id="d2265-110">To handle record dependencies, a well-designed application consists of the following:</span></span>

-   <span data-ttu-id="d2265-111">執行動作之前，一律會檢查記錄相依性。</span><span class="sxs-lookup"><span data-stu-id="d2265-111">Always checks for record dependencies before performing an action.</span></span>
-   <span data-ttu-id="d2265-112">預期當以非預期的順序接收記錄時可能會發生的狀況，然後處理此情況。</span><span class="sxs-lookup"><span data-stu-id="d2265-112">Anticipates conditions that might occur when records are received in an unexpected order, and then handles the situation.</span></span>

 

 



