---
description: RealTimeStylus、GestureRecognizer 和 DynamicRenderer 類別會實作為 COM 包裝函式，而且只能在 managed 程式碼中使用。
ms.assetid: db8f0f25-3650-4843-92e4-af5460841e7e
title: StylusInput Api 的執行注意事項
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47150d6a9aff5495e89f30d29929fd7d604f9eed
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943261"
---
# <a name="implementation-notes-for-the-stylusinput-apis"></a><span data-ttu-id="7fcb0-103">StylusInput Api 的執行注意事項</span><span class="sxs-lookup"><span data-stu-id="7fcb0-103">Implementation Notes for the StylusInput APIs</span></span>

<span data-ttu-id="7fcb0-104">[**RealTimeStylus**](realtimestylus-class.md)、 [GestureRecognizer](/previous-versions/ms575185(v=vs.100))和 [DYNAMICRENDERER](/previous-versions/ms575176(v=vs.100))類別會實作為 COM 包裝函式，而且只能在 managed 程式碼中使用。</span><span class="sxs-lookup"><span data-stu-id="7fcb0-104">The [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100)), and [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) classes are implemented as COM wrappers and are available only in managed code.</span></span>

<span data-ttu-id="7fcb0-105">當 [**realtimestylus**](realtimestylus-class.md)、 [GestureRecognizer](/previous-versions/ms575185(v=vs.100))或 [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) 物件以外掛程式的形式加入至 **realtimestylus** 物件時，基礎 com 物件就會在 COM 層級上互動。</span><span class="sxs-lookup"><span data-stu-id="7fcb0-105">When the [**RealTimeStylus**](realtimestylus-class.md), [GestureRecognizer](/previous-versions/ms575185(v=vs.100)), or [DynamicRenderer](/previous-versions/ms575176(v=vs.100)) object is added as a plug-in to a **RealTimeStylus** object, the underlying COM objects interact on the COM level.</span></span> <span data-ttu-id="7fcb0-106">因此，不支援直接呼叫 [IStylusSyncPlugin](/previous-versions/ms575201(v=vs.100)) 或 [IStylusAsyncPlugin](/previous-versions/ms575194(v=vs.100)) 介面的方法。</span><span class="sxs-lookup"><span data-stu-id="7fcb0-106">Therefore, directly calling the methods of the [IStylusSyncPlugin](/previous-versions/ms575201(v=vs.100)) or [IStylusAsyncPlugin](/previous-versions/ms575194(v=vs.100)) interfaces are not supported.</span></span> <span data-ttu-id="7fcb0-107">將 **realtimestylus**、GestureRecognizer 或 DynamicRenderer 物件新增至 **realtimestylus** 物件是存取這些功能的唯一方法。</span><span class="sxs-lookup"><span data-stu-id="7fcb0-107">Adding the **RealTimeStylus**, GestureRecognizer, or DynamicRenderer object to the **RealTimeStylus** object is the only way to access these features.</span></span>

 

 
