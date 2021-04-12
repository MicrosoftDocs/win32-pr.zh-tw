---
description: 應用程式可以在其應用程式資訊清單中宣告印表機驅動程式隔離，以隔離應用程式與印表機驅動程式，並改善應用程式的可靠性。
ms.assetid: 80650C46-AC96-46FD-894A-4F34B056AB79
ms.topic: article
title: 如何：使用應用程式隔離
ms.date: 05/31/2018
ms.openlocfilehash: 28c2a143406e9501662e0ddf7294abfb25e362b0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192709"
---
# <a name="how-to-use-application-isolation"></a><span data-ttu-id="ef5e5-103">如何：使用應用程式隔離</span><span class="sxs-lookup"><span data-stu-id="ef5e5-103">How To: Use Application Isolation</span></span>

<span data-ttu-id="ef5e5-104">應用程式可以在其應用程式資訊清單中宣告印表機驅動程式隔離，以隔離應用程式與印表機驅動程式，並改善應用程式的可靠性。</span><span class="sxs-lookup"><span data-stu-id="ef5e5-104">Apps can declare printer-driver isolation in their app manifest to isolate the app from the printer driver and improve the app's reliability.</span></span> <span data-ttu-id="ef5e5-105">Windows 列印服務可讓印表機驅動程式在與執行列印多工緩衝處理器不同的進程中執行。</span><span class="sxs-lookup"><span data-stu-id="ef5e5-105">The Windows print service allows printer drivers to run in processes that are separate from the process in which the print spooler runs.</span></span> <span data-ttu-id="ef5e5-106">使用這項功能時，您的應用程式會在印表機驅動程式發生錯誤時，防止應用程式損毀。</span><span class="sxs-lookup"><span data-stu-id="ef5e5-106">Using this feature your app prevents it from crashing in the event the printer driver has an error.</span></span>

<span data-ttu-id="ef5e5-107">印表機驅動程式隔離是在 Windows 7 和 Windows Server 2008 R2 中執行。</span><span class="sxs-lookup"><span data-stu-id="ef5e5-107">Printer-driver isolation is implemented in Windows 7 and Windows Server 2008 R2.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="ef5e5-108">必要條件</span><span class="sxs-lookup"><span data-stu-id="ef5e5-108">Prerequisites</span></span>

-   <span data-ttu-id="ef5e5-109">使用 Windows 列印的 managed 程式碼或 Windows Store 應用程式。</span><span class="sxs-lookup"><span data-stu-id="ef5e5-109">A managed-code or Windows Store app that uses Windows printing.</span></span>

## <a name="instructions"></a><span data-ttu-id="ef5e5-110">指示</span><span class="sxs-lookup"><span data-stu-id="ef5e5-110">Instructions</span></span>

### <a name="update-the-app-manifest"></a><span data-ttu-id="ef5e5-111">更新應用程式資訊清單</span><span class="sxs-lookup"><span data-stu-id="ef5e5-111">Update the app manifest</span></span>

<span data-ttu-id="ef5e5-112">啟用印表機驅動程式隔離需要您將 **printerDriverIsolation** 專案新增至應用程式的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="ef5e5-112">Enabling printer-driver isolation requires you to add the **printerDriverIsolation** element to the app's manifest.</span></span> <span data-ttu-id="ef5e5-113">方法如下：</span><span class="sxs-lookup"><span data-stu-id="ef5e5-113">Here's how:</span></span>

1.  <span data-ttu-id="ef5e5-114">編輯應用程式資訊清單，並將值為 **true** 的 **printerDriverIsolation** 專案加入至 **應用程式** 專案的 **windowsSettings** 專案，如這個範例所示。</span><span class="sxs-lookup"><span data-stu-id="ef5e5-114">Edit the app manifest, adding the **printerDriverIsolation** element with a value of **true** to the **windowsSettings** element of the **application** element, as shown in this example.</span></span>
    ```XML
    <application xmlns="urn:schemas-microsoft-com:asm.v3">
        <windowsSettings>
            <printerDriverIsolation xmlns="http://schemas.microsoft.com/SMI/2011/WindowsSettings">true</printerDriverIsolation>
        </windowsSettings>
    </application>
    ```

    

2.  <span data-ttu-id="ef5e5-115">重建您的應用程式。</span><span class="sxs-lookup"><span data-stu-id="ef5e5-115">Rebuild your app.</span></span>

 

 



