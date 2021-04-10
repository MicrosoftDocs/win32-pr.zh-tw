---
title: 錯誤
description: 錯誤
ms.assetid: d3a087e4-7b57-4070-aa82-3673bc18a54f
keywords:
- AVICap 回呼函式，錯誤通知訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6f418f16ae2af15902e96927990d79a4ecac08b1
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021867"
---
# <a name="error"></a><span data-ttu-id="d5bdd-104">錯誤</span><span class="sxs-lookup"><span data-stu-id="d5bdd-104">Error</span></span>

<span data-ttu-id="d5bdd-105">「捕獲視窗」會使用錯誤通知訊息，通知您應用程式的 AVICap 錯誤，例如磁碟空間不足、嘗試寫入唯讀檔案、無法存取硬體或卸載過多的畫面格。</span><span class="sxs-lookup"><span data-stu-id="d5bdd-105">A capture window uses error notification messages to notify your application of AVICap errors, such as running out of disk space, attempting to write to a read-only file, failing to access hardware, or dropping too many frames.</span></span> <span data-ttu-id="d5bdd-106">錯誤通知的內容包含可供顯示的訊息識別碼和格式化的文字字串。</span><span class="sxs-lookup"><span data-stu-id="d5bdd-106">The content of an error notification includes a message identifier and a formatted text string ready for display.</span></span> <span data-ttu-id="d5bdd-107">您的應用程式可以使用訊息識別碼來篩選通知，以及限制要向使用者顯示的訊息。</span><span class="sxs-lookup"><span data-stu-id="d5bdd-107">Your application can use the message identifier to filter the notifications and limit the messages to present to the user.</span></span> <span data-ttu-id="d5bdd-108">訊息識別碼為零表示正在啟動新的作業，而且回呼函式應清除任何顯示的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="d5bdd-108">A message identifier of zero indicates a new operation is starting and the callback function should clear any displayed error message.</span></span>

 

 




