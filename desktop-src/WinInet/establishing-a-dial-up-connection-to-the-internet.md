---
title: 建立連至網際網路的撥號連線
description: 下列函式是用來處理數據機連接。
ms.assetid: dd33ed4b-eb7c-449c-b309-8f5c290a5a93
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ce03ecc67e27c67bb9807f473aac5210b03f755
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023958"
---
# <a name="establishing-a-dial-up-connection-to-the-internet"></a><span data-ttu-id="1c25b-103">建立連至網際網路的撥號連線</span><span class="sxs-lookup"><span data-stu-id="1c25b-103">Establishing a Dial-Up Connection to the Internet</span></span>

<span data-ttu-id="1c25b-104">下列函式是用來處理數據機連接。</span><span class="sxs-lookup"><span data-stu-id="1c25b-104">The following functions are used to handle modem connections.</span></span>

-   [<span data-ttu-id="1c25b-105">**InternetAutodial**</span><span class="sxs-lookup"><span data-stu-id="1c25b-105">**InternetAutodial**</span></span>](/windows/win32/api/winineti/nf-winineti-internetautodial)
-   [<span data-ttu-id="1c25b-106">**InternetAutodialHangup**</span><span class="sxs-lookup"><span data-stu-id="1c25b-106">**InternetAutodialHangup**</span></span>](/windows/win32/api/winineti/nf-winineti-internetautodialhangup)
-   [<span data-ttu-id="1c25b-107">**InternetDial**</span><span class="sxs-lookup"><span data-stu-id="1c25b-107">**InternetDial**</span></span>](/windows/win32/api/winineti/nf-winineti-internetdial)
-   [<span data-ttu-id="1c25b-108">**InternetGetConnectedState**</span><span class="sxs-lookup"><span data-stu-id="1c25b-108">**InternetGetConnectedState**</span></span>](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstate)
-   [<span data-ttu-id="1c25b-109">**InternetGetConnectedStateEx**</span><span class="sxs-lookup"><span data-stu-id="1c25b-109">**InternetGetConnectedStateEx**</span></span>](/windows/win32/api/winineti/nf-winineti-internetgetconnectedstateex)
-   [<span data-ttu-id="1c25b-110">**InternetHangUp**</span><span class="sxs-lookup"><span data-stu-id="1c25b-110">**InternetHangUp**</span></span>](/windows/win32/api/winineti/nf-winineti-internethangup)
-   [<span data-ttu-id="1c25b-111">**InternetGoOnline**</span><span class="sxs-lookup"><span data-stu-id="1c25b-111">**InternetGoOnline**</span></span>](/windows/win32/api/winineti/nf-winineti-internetgoonline)

> [!Note]  
> <span data-ttu-id="1c25b-112">WinINet 撥號函式不支援雙撥號連線、智慧卡驗證，或需要以登錄為基礎之認證的連線。</span><span class="sxs-lookup"><span data-stu-id="1c25b-112">WinINet dial-up functions do not support double-dial connections, SmartCard authentication, or connections that require registry-based certification.</span></span>

 

> [!Note]  
> <span data-ttu-id="1c25b-113">從 Windows Vista 和 Windows Server 2008 開始，WinINet 撥號函式會使用 [RAS 函數](/windows/desktop/RRAS/remote-access-service-functions) 來建立撥號連線。</span><span class="sxs-lookup"><span data-stu-id="1c25b-113">Starting on Windows Vista and Windows Server 2008, the WinINet dial-up functions use the [RAS functions](/windows/desktop/RRAS/remote-access-service-functions) to establish a dial-up connection.</span></span> <span data-ttu-id="1c25b-114">WinINet 支援 [**RasDialDlg**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga) 函式中記載的功能。</span><span class="sxs-lookup"><span data-stu-id="1c25b-114">WinINet supports the functionality documented in the [**RasDialDlg**](/windows/desktop/api/rasdlg/nf-rasdlg-rasdialdlga) function.</span></span>

 

> [!Note]  
> <span data-ttu-id="1c25b-115">WinINet 不支援伺服器實施。</span><span class="sxs-lookup"><span data-stu-id="1c25b-115">WinINet does not support server implementations.</span></span> <span data-ttu-id="1c25b-116">此外，它不應該從服務使用。</span><span class="sxs-lookup"><span data-stu-id="1c25b-116">In addition, it should not be used from a service.</span></span> <span data-ttu-id="1c25b-117">針對伺服器執行或服務，請使用 [Microsoft WINDOWS HTTP services (WinHTTP) ](/windows/desktop/WinHttp/winhttp-start-page)。</span><span class="sxs-lookup"><span data-stu-id="1c25b-117">For server implementations or services use [Microsoft Windows HTTP Services (WinHTTP)](/windows/desktop/WinHttp/winhttp-start-page).</span></span>

 

 

 