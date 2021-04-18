---
title: 一般程式設計指導方針
description: 在遠端桌面服務環境中開發應用程式的指導方針。
ms.assetid: 95b49db5-ba3c-4638-9087-6ee3972d8972
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d465c658e64959eb1bfd61cf3c43f6ffd2cc6b1d
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965243"
---
# <a name="general-programming-guidelines"></a><span data-ttu-id="e2cbe-103">一般程式設計指導方針</span><span class="sxs-lookup"><span data-stu-id="e2cbe-103">General programming guidelines</span></span>

<span data-ttu-id="e2cbe-104">下列各節提供在遠端桌面服務環境中開發應用程式的一般方針。</span><span class="sxs-lookup"><span data-stu-id="e2cbe-104">The following sections provide general guidelines for developing applications in a Remote Desktop Services environment.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="e2cbe-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="e2cbe-105">In this section</span></span>

<dl> <dt>

[<span data-ttu-id="e2cbe-106">應用程式相容性層</span><span class="sxs-lookup"><span data-stu-id="e2cbe-106">Application compatibility layer</span></span>](application-compatibility-layer.md)
</dt> <dd>

<span data-ttu-id="e2cbe-107">若要在遠端桌面服務環境中執行繼承應用程式，您可以使用遠端桌面服務應用程式相容性層。</span><span class="sxs-lookup"><span data-stu-id="e2cbe-107">To run legacy applications in a Remote Desktop Services environment you can use the Remote Desktop Services Application Compatibility layer.</span></span>

</dd> <dt>

[<span data-ttu-id="e2cbe-108">用戶端/伺服器應用程式指導方針</span><span class="sxs-lookup"><span data-stu-id="e2cbe-108">Client/Server application guidelines</span></span>](client-server-application-guidelines.md)
</dt> <dd>

<span data-ttu-id="e2cbe-109">用戶端/伺服器應用程式不能假設單一電腦連接相當於單一使用者會話。</span><span class="sxs-lookup"><span data-stu-id="e2cbe-109">Client/server applications must not assume that a single computer connection is equivalent to a single user session.</span></span>

</dd> <dt>

[<span data-ttu-id="e2cbe-110">監視會話連線和中斷連接</span><span class="sxs-lookup"><span data-stu-id="e2cbe-110">Monitoring session connections and disconnections</span></span>](monitoring-session-connections-and-disconnections.md)
</dt> <dd>

<span data-ttu-id="e2cbe-111">若要向遠端桌面服務註冊應用程式，請新增子機碼，以將虛擬通道伺服器應用程式的名稱儲存在登錄中。</span><span class="sxs-lookup"><span data-stu-id="e2cbe-111">To register an application with Remote Desktop Services, store the name of the virtual channel server application in the registry by adding a subkey.</span></span>

</dd> <dt>

[<span data-ttu-id="e2cbe-112">週邊硬體指導方針</span><span class="sxs-lookup"><span data-stu-id="e2cbe-112">Peripheral hardware guidelines</span></span>](peripheral-hardware-guidelines.md)
</dt> <dd>

<span data-ttu-id="e2cbe-113">如果其硬體裝置不是設計來透過遠端會話運作，廠商必須確保設備磁碟機軟體強制使用系統原則或群組原則來停用裝置的重新導向。</span><span class="sxs-lookup"><span data-stu-id="e2cbe-113">If their hardware device is not designed to work over a remote session, vendors must ensure that the device driver software forces disabling the redirection of the device by using a system policy or group policy.</span></span>

</dd> <dt>

[<span data-ttu-id="e2cbe-114">執行時間連結至 Wtsapi32.dll</span><span class="sxs-lookup"><span data-stu-id="e2cbe-114">Run-Time linking to Wtsapi32.dll</span></span>](run-time-linking-to-wtsapi32-dll.md)
</dt> <dd>

<span data-ttu-id="e2cbe-115">您的應用程式可以使用遠端桌面服務 API，在執行時間動態連結到 Wtsapi32.dll。</span><span class="sxs-lookup"><span data-stu-id="e2cbe-115">Your application can use the Remote Desktop Services API to dynamically link to the Wtsapi32.dll at run time.</span></span> <span data-ttu-id="e2cbe-116">若要這樣做，您的應用程式應該呼叫 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函式來載入 Wtsapi32.dll。</span><span class="sxs-lookup"><span data-stu-id="e2cbe-116">To do this, your application should call the [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya) function to load Wtsapi32.dll.</span></span>

</dd> </dl>

 

 