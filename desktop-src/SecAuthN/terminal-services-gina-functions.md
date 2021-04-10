---
description: 啟用終端機服務時，GINA 必須呼叫 Winlogon 支援函式來完成每個使用者的設定、查詢終端機服務用戶端會話的認證，以及中斷與終端機服務網路會話的連線。注意 GINA 在 Windows Vista 中會忽略 Dll。
ms.assetid: 70b55b99-b350-4638-84ba-e5580d9d992f
title: 終端機服務 GINA 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 19452fb73f00ef4ace0dd85083578334b6fb1038
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847931"
---
# <a name="terminal-services-gina-functions"></a><span data-ttu-id="c3ee9-103">終端機服務 GINA 函式</span><span class="sxs-lookup"><span data-stu-id="c3ee9-103">Terminal Services GINA Functions</span></span>

<span data-ttu-id="c3ee9-104">啟用終端機服務時， [*GINA*](../secgloss/g-gly.md) 必須呼叫 [*Winlogon*](../secgloss/w-gly.md) 支援函式來完成每個使用者的設定、查詢終端機服務用戶端會話的 [*認證*](../secgloss/c-gly.md) ，以及中斷與終端機服務網路會話的連線。</span><span class="sxs-lookup"><span data-stu-id="c3ee9-104">When Terminal Services are enabled, the [*GINA*](../secgloss/g-gly.md) must call [*Winlogon*](../secgloss/w-gly.md) support functions to complete the setup for each user, to query the [*credentials*](../secgloss/c-gly.md) of a Terminal Services client session, and to disconnect from a Terminal Services network session.</span></span>

> [!Note]  
> <span data-ttu-id="c3ee9-105">在 Windows Vista 中會忽略 GINA Dll。</span><span class="sxs-lookup"><span data-stu-id="c3ee9-105">GINA DLLs are ignored in Windows Vista.</span></span>

 

<span data-ttu-id="c3ee9-106">這些支援函數包括下列各項。</span><span class="sxs-lookup"><span data-stu-id="c3ee9-106">These support functions include the following.</span></span>



| <span data-ttu-id="c3ee9-107">函式</span><span class="sxs-lookup"><span data-stu-id="c3ee9-107">Function</span></span>                                                                     | <span data-ttu-id="c3ee9-108">描述</span><span class="sxs-lookup"><span data-stu-id="c3ee9-108">Description</span></span>                                                                                         |
|------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="c3ee9-109">**WlxWin31Migrate**</span><span class="sxs-lookup"><span data-stu-id="c3ee9-109">**WlxWin31Migrate**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_win31_migrate)                                   | <span data-ttu-id="c3ee9-110">完成使用者的設定。</span><span class="sxs-lookup"><span data-stu-id="c3ee9-110">Completes the setup of the user.</span></span>                                                                    |
| [<span data-ttu-id="c3ee9-111">**WlxQueryClientCredentials**</span><span class="sxs-lookup"><span data-stu-id="c3ee9-111">**WlxQueryClientCredentials**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_client_credentials)               | <span data-ttu-id="c3ee9-112">呼叫以查詢未使用網際網路連接器授權之遠端用戶端的認證。</span><span class="sxs-lookup"><span data-stu-id="c3ee9-112">Called to query the credentials of remote clients that are not using an Internet connector license.</span></span> |
| [<span data-ttu-id="c3ee9-113">**WlxQueryInetConnectorCredentials**</span><span class="sxs-lookup"><span data-stu-id="c3ee9-113">**WlxQueryInetConnectorCredentials**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_ic_credentials) | <span data-ttu-id="c3ee9-114">呼叫以查詢使用網際網路連接器授權之遠端用戶端的認證。</span><span class="sxs-lookup"><span data-stu-id="c3ee9-114">Called to query the credentials of remote clients that are using an Internet connector license.</span></span>     |
| [<span data-ttu-id="c3ee9-115">**WlxQueryTerminalServicesData**</span><span class="sxs-lookup"><span data-stu-id="c3ee9-115">**WlxQueryTerminalServicesData**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_query_terminal_services_data)         | <span data-ttu-id="c3ee9-116">呼叫以取得終端機服務使用者設定資訊。</span><span class="sxs-lookup"><span data-stu-id="c3ee9-116">Called to retrieve Terminal Services user configuration information.</span></span>                                |
| [<span data-ttu-id="c3ee9-117">**WlxDisconnect**</span><span class="sxs-lookup"><span data-stu-id="c3ee9-117">**WlxDisconnect**</span></span>](/windows/win32/api/winwlx/nc-winwlx-pwlx_disconnect)                                       | <span data-ttu-id="c3ee9-118">呼叫以中斷與終端機服務網路會話的連線。</span><span class="sxs-lookup"><span data-stu-id="c3ee9-118">Called to disconnect from a Terminal Services network session.</span></span>                                      |



 

<span data-ttu-id="c3ee9-119">為了存取這些 Winlogon 支援函數，GINA DLL 必須使用 [**WLX \_ 分派 \_ \_ 第 1 \_ 版**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3) 的結構。</span><span class="sxs-lookup"><span data-stu-id="c3ee9-119">In order to access these Winlogon support functions, the GINA DLL must use the [**WLX\_DISPATCH\_VERSION\_1\_3**](/windows/desktop/api/Winwlx/ns-winwlx-wlx_dispatch_version_1_3) structure.</span></span> <span data-ttu-id="c3ee9-120">在 GINA 的 [**WlxNegotiate**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate) 函式中，這兩個參數至少必須是 WLX \_ \_ 第1版 \_ 。</span><span class="sxs-lookup"><span data-stu-id="c3ee9-120">In the GINA's [**WlxNegotiate**](/windows/desktop/api/Winwlx/nf-winwlx-wlxnegotiate) function, both parameters must be at least WLX\_VERSION\_1\_3.</span></span>

 

 
