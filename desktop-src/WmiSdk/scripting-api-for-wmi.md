---
description: WMI 腳本參考包含 WMI 腳本 API 的定義。
ms.assetid: 83fc78fc-929d-4d32-940e-9147543a6324
ms.tgt_platform: multiple
title: 適用于 WMI 的腳本 API
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d6c43587fd8f40c2524bcabd79fe80e3d00d74b1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848631"
---
# <a name="scripting-api-for-wmi"></a><span data-ttu-id="cc86c-103">適用于 WMI 的腳本 API</span><span class="sxs-lookup"><span data-stu-id="cc86c-103">Scripting API for WMI</span></span>

<span data-ttu-id="cc86c-104">WMI 腳本參考包含 WMI 腳本 API 的定義。</span><span class="sxs-lookup"><span data-stu-id="cc86c-104">The WMI scripting reference contains definitions for the WMI Scripting API.</span></span> <span data-ttu-id="cc86c-105">如果使用 Microsoft Visual Basic、Visual Basic for Applications Visual Basic Scripting Edition (VBScript) ，或任何其他支援動態指令碼技術的指令碼語言來撰寫應用程式，請使用此 API。</span><span class="sxs-lookup"><span data-stu-id="cc86c-105">Use this API if writing applications with Microsoft Visual Basic, Visual Basic for Applications, Visual Basic Scripting Edition (VBScript), or any other scripting language that supports active scripting technologies.</span></span>

> [!Note]  
> <span data-ttu-id="cc86c-106">PowerShell 也可用於使用 WMI 編寫腳本。</span><span class="sxs-lookup"><span data-stu-id="cc86c-106">PowerShell is also available for scripting with WMI.</span></span> <span data-ttu-id="cc86c-107">Get-WMI Cmdlet 和三種類型加速器 (\[ wmi \] 、 \[ wmiclass \] 和 \[ wmisearcher \]) 啟用 wmi 的基本系統管理存取權。</span><span class="sxs-lookup"><span data-stu-id="cc86c-107">The Get-WMI cmdlet and the three type accelerators (\[wmi\], \[wmiclass\], and \[wmisearcher\]) enable basic administrative access to WMI.</span></span> <span data-ttu-id="cc86c-108">如需詳細資訊，請參閱 [使用 Windows PowerShell 編寫腳本](https://TechNet.Microsoft.Com/library/bb978526.aspx)。</span><span class="sxs-lookup"><span data-stu-id="cc86c-108">For more information, see [Scripting with Windows PowerShell](https://TechNet.Microsoft.Com/library/bb978526.aspx).</span></span>

 

<span data-ttu-id="cc86c-109">除了 [**SWbemDateTime**](swbemdatetime.md) 以外，WMI 腳本物件也不會標示為安全，以在 INTERNET EXPLORER 的 HTML 網頁上執行腳本。</span><span class="sxs-lookup"><span data-stu-id="cc86c-109">WMI scripting objects, except for [**SWbemDateTime**](swbemdatetime.md) are not marked safe for scripting for scripts running on HTML pages in Internet Explorer.</span></span> <span data-ttu-id="cc86c-110">因此，除非 Internet Explorer 中的安全性層級減少，否則腳本將會失敗。</span><span class="sxs-lookup"><span data-stu-id="cc86c-110">Therefore, unless the security level within Internet Explorer is lowered, the script will fail.</span></span> <span data-ttu-id="cc86c-111">**SWbemDateTime** 標示為 safe 以進行初始化和腳本處理。</span><span class="sxs-lookup"><span data-stu-id="cc86c-111">**SWbemDateTime** is marked safe for initialization and scripting.</span></span> <span data-ttu-id="cc86c-112">不過，在 Active Server Pages (ASP) 的伺服器端程式碼上，使用 **GetObject** 和 **CreateObject** 呼叫中的所有 WMI 腳本物件。</span><span class="sxs-lookup"><span data-stu-id="cc86c-112">However, use all WMI scripting objects in **GetObject** and **CreateObject** calls on server-side code in Active Server Pages (ASP).</span></span>

-   [<span data-ttu-id="cc86c-113">腳本 API 物件模型</span><span class="sxs-lookup"><span data-stu-id="cc86c-113">Scripting API Object Model</span></span>](scripting-api-object-model.md)
-   [<span data-ttu-id="cc86c-114">腳本 API 的檔慣例</span><span class="sxs-lookup"><span data-stu-id="cc86c-114">Document Conventions for the Scripting API</span></span>](document-conventions-for-the-scripting-api.md)
-   [<span data-ttu-id="cc86c-115">腳本 API 物件</span><span class="sxs-lookup"><span data-stu-id="cc86c-115">Scripting API Objects</span></span>](scripting-api-objects.md)
-   [<span data-ttu-id="cc86c-116">腳本 API 常數</span><span class="sxs-lookup"><span data-stu-id="cc86c-116">Scripting API Constants</span></span>](scripting-api-constants.md)

## <a name="related-topics"></a><span data-ttu-id="cc86c-117">相關主題</span><span class="sxs-lookup"><span data-stu-id="cc86c-117">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="cc86c-118">WMI 參考</span><span class="sxs-lookup"><span data-stu-id="cc86c-118">WMI Reference</span></span>](wmi-reference.md)
</dt> <dt>

[<span data-ttu-id="cc86c-119">WMI 傳回碼</span><span class="sxs-lookup"><span data-stu-id="cc86c-119">WMI Return Codes</span></span>](wmi-return-codes.md)
</dt> </dl>

 

 



