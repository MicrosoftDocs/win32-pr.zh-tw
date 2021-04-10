---
title: 設定 Windows 3.x 或 MS-DOS 的名稱服務
description: 遠端程序呼叫 (RPC) 和設定 Windows 3.x 或 MS-DOS 的名稱服務。
ms.assetid: 7b22a12e-43d0-4e32-a191-d63a56559143
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 533a0d8556f9cc51d0842768d0df1bdd0d553b5d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021604"
---
# <a name="configuring-the-name-service-for-windows-3x-or-ms-dos"></a><span data-ttu-id="f3f47-103">設定 Windows 3.x 或 MS-DOS 的名稱服務</span><span class="sxs-lookup"><span data-stu-id="f3f47-103">Configuring the Name Service for Windows 3.x or MS-DOS</span></span>

<span data-ttu-id="f3f47-104">當您執行 Setup.exe 安裝16位的 RPC 執行時間程式庫時，它會提示您選取名稱服務提供者：</span><span class="sxs-lookup"><span data-stu-id="f3f47-104">When you run Setup.exe to install the 16-bit RPC run-time library, it prompts you to select a name service provider:</span></span>

-   <span data-ttu-id="f3f47-105">如果您選擇 [ **安裝預設名稱服務提供者**]，則會安裝預設的 NSP （Microsoft 定位器）。</span><span class="sxs-lookup"><span data-stu-id="f3f47-105">If you choose **Install Default Name Service Provider**, the default NSP, Microsoft Locator, is installed.</span></span>
-   <span data-ttu-id="f3f47-106">如果您選擇 [ **安裝自訂名稱服務提供者**]，請完成 [ **定義網路位址** ] 對話方塊，將 [DCE Cell Directory 服務安裝為您的 NSP。</span><span class="sxs-lookup"><span data-stu-id="f3f47-106">If you choose **Install Custom Name Service Provider**, complete the **Define Network Address** dialog box to install the DCE Cell Directory Service as your NSP.</span></span> <span data-ttu-id="f3f47-107">DCE Cell Directory 服務是與 DCE 伺服器搭配使用的 NSP。</span><span class="sxs-lookup"><span data-stu-id="f3f47-107">The DCE Cell Directory Service is the NSP used with DCE servers.</span></span>

<span data-ttu-id="f3f47-108">網路位址是執行 NSI daemon (nsid) 的主電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="f3f47-108">The network address is the name of the host computer that runs the NSI daemon (nsid).</span></span> <span data-ttu-id="f3f47-109">此電腦可作為 DCE Cell Directory 服務的閘道，並在執行 Microsoft 作業系統和 DCE 電腦的電腦之間傳遞 NSI 函數呼叫。</span><span class="sxs-lookup"><span data-stu-id="f3f47-109">This computer acts as a gateway to the DCE Cell Directory Service, passing NSI function calls between computers that run Microsoft operating systems and DCE computers.</span></span> <span data-ttu-id="f3f47-110">網路位址可以是80個字元或更少，例如，11.1.9.169 是有效的位址。</span><span class="sxs-lookup"><span data-stu-id="f3f47-110">The network address can be 80 characters or less—for example, 11.1.9.169 is a valid address.</span></span>

 

 




