---
title: Run-Time 連結至 Wtsapi32.dll
description: 您的應用程式可以使用遠端桌面服務 API，在執行時間動態連結到 Wtsapi32.dll。 若要這樣做，您的應用程式應該呼叫 LoadLibrary 函式來載入 Wtsapi32.dll。
ms.assetid: b8227e65-be08-4045-a74e-dd3f398a7b9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c53a992955876bf812a87168d2c74b776cf0d4e6
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104376101"
---
# <a name="run-time-linking-to-wtsapi32dll"></a><span data-ttu-id="7acd6-104">Run-Time 連結至 Wtsapi32.dll</span><span class="sxs-lookup"><span data-stu-id="7acd6-104">Run-Time linking to Wtsapi32.dll</span></span>

<span data-ttu-id="7acd6-105">如果您的應用程式是在不是遠端桌面服務環境的環境中執行，但您想要讓應用程式在遠端桌面服務環境中執行時提供額外的功能，應用程式可以使用遠端桌面服務 API 來執行額外的功能，並在執行時間以動態方式連結到 Wtsapi32.dll。</span><span class="sxs-lookup"><span data-stu-id="7acd6-105">If your application runs in an environment that is not a Remote Desktop Services environment, but you want your application to provide additional functionality when it does run in a Remote Desktop Services environment, the application can use the Remote Desktop Services API to implement the additional functionality, and dynamically link to the Wtsapi32.dll at run time.</span></span> <span data-ttu-id="7acd6-106">若要這樣做，您的應用程式應該呼叫 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函式來載入 Wtsapi32.dll。</span><span class="sxs-lookup"><span data-stu-id="7acd6-106">To do this, your application should call the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to load Wtsapi32.dll.</span></span> <span data-ttu-id="7acd6-107">如果 **LoadLibrary** 呼叫失敗，您的應用程式可以使用其基本功能來執行。</span><span class="sxs-lookup"><span data-stu-id="7acd6-107">If the **LoadLibrary** call fails, your application can run using its basic functionality.</span></span> <span data-ttu-id="7acd6-108">如果 **LoadLibrary** 成功，則您的應用程式可以呼叫 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 函式，以取得您想要呼叫之遠端桌面服務函式的指標。</span><span class="sxs-lookup"><span data-stu-id="7acd6-108">If **LoadLibrary** succeeds, your application can call the [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) function to retrieve pointers to the Remote Desktop Services functions that you want to call.</span></span>

<span data-ttu-id="7acd6-109">如果您的應用程式僅適用于遠端桌面服務環境，則不需要動態連結。</span><span class="sxs-lookup"><span data-stu-id="7acd6-109">If your application is intended only for a Remote Desktop Services environment, dynamic linking is not necessary.</span></span> <span data-ttu-id="7acd6-110">在這種情況下，您可以包含 Wtsapi32.dll，並連結 Wtsapi32.dll .lib。</span><span class="sxs-lookup"><span data-stu-id="7acd6-110">In this case, you can include Wtsapi32.h and link with Wtsapi32.lib.</span></span> <span data-ttu-id="7acd6-111">然後，如果您的應用程式在遠端桌面服務以外的環境中啟動，它將會結束，因為 Wtsapi32.dll 並不存在。</span><span class="sxs-lookup"><span data-stu-id="7acd6-111">Then, if your application starts up in an environment other than Remote Desktop Services, it will exit because Wtsapi32.dll is not present.</span></span>

<span data-ttu-id="7acd6-112">如需判斷您的應用程式是否正在遠端桌面服務環境中執行的相關資訊，請參閱偵測 [遠端桌面服務環境](detecting-the-terminal-services-environment.md)。</span><span class="sxs-lookup"><span data-stu-id="7acd6-112">For information about determining whether your application is running in a Remote Desktop Services environment, see [Detecting the Remote Desktop Services Environment](detecting-the-terminal-services-environment.md).</span></span>

## <a name="related-topics"></a><span data-ttu-id="7acd6-113">相關主題</span><span class="sxs-lookup"><span data-stu-id="7acd6-113">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7acd6-114">一般程式設計指導方針</span><span class="sxs-lookup"><span data-stu-id="7acd6-114">General programming guidelines</span></span>](general-programming-guidelines.md)
</dt> </dl>

 

 