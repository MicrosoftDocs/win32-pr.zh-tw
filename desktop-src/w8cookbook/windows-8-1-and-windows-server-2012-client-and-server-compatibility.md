---
title: Windows 8.1 和 Windows Server 2012 R2 用戶端和伺服器相容性
description: Windows 8.1 和 Windows Server 2012 R2 用戶端和伺服器相容性
ms.assetid: 45C37E2D-3513-4708-A562-1426D2B832F0
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c46647dd9ad0f0baeae1ffb98905740a37f9530
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507128"
---
# <a name="windows-81-and-windows-server-2012-r2-client-and-server-compatibility"></a><span data-ttu-id="1b21a-103">Windows 8.1 和 Windows Server 2012 R2 用戶端和伺服器相容性</span><span class="sxs-lookup"><span data-stu-id="1b21a-103">Windows 8.1 and Windows Server 2012 R2 client and server compatibility</span></span>

<span data-ttu-id="1b21a-104">本節描述作業系統中的變更，您應該特別注意，因為現有的應用程式可能會受到影響，以及如何在用戶端、伺服器或用戶端和伺服器上設計新的應用程式。</span><span class="sxs-lookup"><span data-stu-id="1b21a-104">This section describes changes in the operating system that you should pay special attention to due to the potential impacts on existing apps and how new apps should be designed on clients, on servers, or on both clients and servers.</span></span> <span data-ttu-id="1b21a-105">以下是本節所涵蓋的主題清單：</span><span class="sxs-lookup"><span data-stu-id="1b21a-105">Following is the list of topics covered in this section:</span></span>

## <a name="in-this-section"></a><span data-ttu-id="1b21a-106">本節內容</span><span class="sxs-lookup"><span data-stu-id="1b21a-106">In this section</span></span>



| <span data-ttu-id="1b21a-107">主題</span><span class="sxs-lookup"><span data-stu-id="1b21a-107">Topic</span></span>                                                                                                                                                                                                                         | <span data-ttu-id="1b21a-108">描述</span><span class="sxs-lookup"><span data-stu-id="1b21a-108">Description</span></span> |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------|
| [<span data-ttu-id="1b21a-109">Windows 8.1 中的作業系統版本變更</span><span class="sxs-lookup"><span data-stu-id="1b21a-109">Operating system version changes in Windows 8.1</span></span>](operating-system-version-changes-in-windows-8-1.md)<br/>                                                                                                             |             |
| [<span data-ttu-id="1b21a-110">隨選安裝的 Windows 元件</span><span class="sxs-lookup"><span data-stu-id="1b21a-110">Windows components installed on demand</span></span>](windows-components-installed-on-demand.md)<br/>                                                                                                                               |             |
| [<span data-ttu-id="1b21a-111">HTML 字型回溯行為</span><span class="sxs-lookup"><span data-stu-id="1b21a-111">HTML font fallback behavior</span></span>](html-font-fallback-behavior.md)<br/>                                                                                                                                                     |             |
| [<span data-ttu-id="1b21a-112">Windows 8.1 只允許 HTTPs Uri，而非 HTTP Uri</span><span class="sxs-lookup"><span data-stu-id="1b21a-112">Windows 8.1 allows only https URIs, not http URIs</span></span>](windows-8-1-allows-only-https-uris--not-http-uris.md)<br/>                                                                                                         |             |
| [<span data-ttu-id="1b21a-113">Windows 8.1 的滑鼠滾輪輸入</span><span class="sxs-lookup"><span data-stu-id="1b21a-113">Mousewheel input for Windows 8.1</span></span>](mousewheel-input-for-windows-8-1.md)<br/>                                                                                                                                           |             |
| [<span data-ttu-id="1b21a-114">Windows 精確的觸控板裝置</span><span class="sxs-lookup"><span data-stu-id="1b21a-114">Windows precision touchpad devices</span></span>](windows-precision-touchpad-devices.md)<br/>                                                                                                                                       |             |
| [<span data-ttu-id="1b21a-115">適用于桌面應用程式的高 DPI Windows 8。1</span><span class="sxs-lookup"><span data-stu-id="1b21a-115">High DPI for desktop apps in Windows 8.1</span></span>](high-dpi-for-desktop-apps-in-windows-8-1.md)<br/>                                                                                                                           |             |
| [<span data-ttu-id="1b21a-116">在內建和慣性案例中隱藏邊緣 UI</span><span class="sxs-lookup"><span data-stu-id="1b21a-116">Edge UI is suppressed in  in-out-in  and  inertia  scenarios</span></span>](edge-ui-is-suppressed-in--in-out-in--and--inertia--scenarios.md)<br/>                                                                                   |             |
| [<span data-ttu-id="1b21a-117">不支援從 Windows Store 應用程式呼叫 ImmSetConversionStatus () 或 ImmGetConversionStatus () </span><span class="sxs-lookup"><span data-stu-id="1b21a-117">Calling ImmSetConversionStatus() or ImmGetConversionStatus() from Windows Store apps is not supported</span></span>](calling-immsetconversionstatus---or-immgetconversionstatus---from-windows-store-apps-is-not-supported.md)<br/> |             |
| [<span data-ttu-id="1b21a-118">輸入法模式模型從每位使用者變更為每個執行緒</span><span class="sxs-lookup"><span data-stu-id="1b21a-118">IME mode model changed from per-user to per-thread</span></span>](ime-mode-model-changed-from-per-user-to-per-thread.md)<br/>                                                                                                       |             |
| [<span data-ttu-id="1b21a-119">簡體中文 IME 不支援輸入方法管理員 Api</span><span class="sxs-lookup"><span data-stu-id="1b21a-119">Input Method manager APIs are not supported by Simplified Chinese IME</span></span>](input-method-manager-apis-are-not-supported-by-simplified-chinese-ime.md)<br/>                                                                 |             |
| [<span data-ttu-id="1b21a-120">某些東亞 IME 軟體輸入面板現在會傳送 vKey</span><span class="sxs-lookup"><span data-stu-id="1b21a-120">Some East Asian IME software input panels now send vKey</span></span>](some-east-asian-ime-software-input-panels-now-send-vkey.md)<br/>                                                                                             |             |



 

 

 





