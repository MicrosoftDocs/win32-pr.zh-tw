---
description: 當您使用 CreateProcess 函數建立處理常式時，可以指定進程使用安全性屬性結構，繼承 mutex、事件、信號或計時器物件的控制碼 \_ 。
ms.assetid: 36491a5c-7599-4f69-ab76-d3a62261a151
title: 物件繼承
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6087ae3699e7628ab97871ede41cc2e406e40157
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106987240"
---
# <a name="object-inheritance"></a><span data-ttu-id="47508-103">物件繼承</span><span class="sxs-lookup"><span data-stu-id="47508-103">Object Inheritance</span></span>

<span data-ttu-id="47508-104">當您使用 [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) 函數建立處理常式時，可以指定進程使用 [**安全性 \_ 屬性**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) 結構，繼承 mutex、事件、信號或計時器物件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="47508-104">When you create a process with the [**CreateProcess**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa) function, you can specify that the process inherit handles to mutex, event, semaphore, or timer objects using the [**SECURITY\_ATTRIBUTES**](/previous-versions/windows/desktop/legacy/aa379560(v=vs.85)) structure.</span></span> <span data-ttu-id="47508-105">進程繼承的控制碼具有與原始控制碼相同的物件存取權。</span><span class="sxs-lookup"><span data-stu-id="47508-105">The handle inherited by the process has the same access to the object as the original handle.</span></span> <span data-ttu-id="47508-106">繼承的控制碼會出現在所建立之進程的控制碼資料表中，但是您必須將控制碼值傳達給已建立的進程。</span><span class="sxs-lookup"><span data-stu-id="47508-106">The inherited handle appears in the handle table of the created process, but you must communicate the handle value to the created process.</span></span> <span data-ttu-id="47508-107">若要這麼做，您可以在呼叫 **CreateProcess** 時將值指定為命令列引數。</span><span class="sxs-lookup"><span data-stu-id="47508-107">You can do this by specifying the value as a command-line argument when you call **CreateProcess**.</span></span> <span data-ttu-id="47508-108">然後，建立的進程會使用 [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) 函式來抓取命令列字串，並將控制碼引數轉換成可用的控制碼。</span><span class="sxs-lookup"><span data-stu-id="47508-108">The created process then uses the [**GetCommandLine**](/windows/win32/api/processenv/nf-processenv-getcommandlinea) function to retrieve the command-line string and convert the handle argument into a usable handle.</span></span> <span data-ttu-id="47508-109">如需詳細資訊，請參閱[繼承](../procthread/inheritance.md)。</span><span class="sxs-lookup"><span data-stu-id="47508-109">For more information, see [Inheritance](../procthread/inheritance.md).</span></span>

 

 
