---
description: 某些物件一次只支援一個控制碼。
ms.assetid: 3eafd0e0-3923-4489-8a0a-63007dd3183a
title: 控制碼限制
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 99caa991b1ffa0a4e0c02ff32225c3260eb4a016
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194727"
---
# <a name="handle-limitations"></a><span data-ttu-id="ca4a9-103">控制碼限制</span><span class="sxs-lookup"><span data-stu-id="ca4a9-103">Handle Limitations</span></span>

<span data-ttu-id="ca4a9-104">某些物件一次只支援一個控制碼。</span><span class="sxs-lookup"><span data-stu-id="ca4a9-104">Some objects support only one handle at a time.</span></span> <span data-ttu-id="ca4a9-105">當應用程式建立物件時，系統會提供控制碼，並在應用程式終結物件時使控制碼失效。</span><span class="sxs-lookup"><span data-stu-id="ca4a9-105">The system provides the handle when an application creates the object and invalidates the handle when the application destroys the object.</span></span> <span data-ttu-id="ca4a9-106">其他物件支援單一物件的多個控制碼。</span><span class="sxs-lookup"><span data-stu-id="ca4a9-106">Other objects support multiple handles to a single object.</span></span> <span data-ttu-id="ca4a9-107">當物件的最後控制碼關閉之後，作業系統會自動從記憶體中移除該物件。</span><span class="sxs-lookup"><span data-stu-id="ca4a9-107">The operating system automatically removes the object from memory after the last handle to the object is closed.</span></span>

<span data-ttu-id="ca4a9-108">系統中開啟的控制碼總數只受限於可用的記憶體數量。</span><span class="sxs-lookup"><span data-stu-id="ca4a9-108">The total number of open handles in the system is limited only by the amount of memory available.</span></span> <span data-ttu-id="ca4a9-109">某些物件類型支援每個會話或每個進程的控制碼數目有限。</span><span class="sxs-lookup"><span data-stu-id="ca4a9-109">Some object types support a limited number of handles per session or per process.</span></span>

 

 



