---
description: 下列各節包含依區域分組的函式字母清單。 每個函式的資訊都包含函式專案上的有效撥號狀態清單，以及要求完成時的一般撥號狀態轉換清單。
ms.assetid: 555d6af2-b440-4636-b90e-da297a369753
title: TAPI 功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 38532fa1c0b978e3e59e54b08fbc43152fa0bd64
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104513469"
---
# <a name="tapi-functions"></a><span data-ttu-id="07a51-104">TAPI 功能</span><span class="sxs-lookup"><span data-stu-id="07a51-104">TAPI Functions</span></span>

<span data-ttu-id="07a51-105">下列各節包含依區域分組的函式字母清單。</span><span class="sxs-lookup"><span data-stu-id="07a51-105">The following sections contain an alphabetic list of functions grouped by area.</span></span> <span data-ttu-id="07a51-106">每個函式的資訊都包含函式專案上的有效撥號狀態清單，以及要求完成時的一般撥號狀態轉換清單。</span><span class="sxs-lookup"><span data-stu-id="07a51-106">The information for each function includes a list of the valid call states on entry of the function and typical call state transitions when the request is complete.</span></span>

-   [<span data-ttu-id="07a51-107">輔助電話語音功能</span><span class="sxs-lookup"><span data-stu-id="07a51-107">Assisted Telephony Functions</span></span>](assisted-telephony-functions.md)
-   [<span data-ttu-id="07a51-108">撥置中心函數</span><span class="sxs-lookup"><span data-stu-id="07a51-108">Call Center Functions</span></span>](call-center-functions.md)
-   [<span data-ttu-id="07a51-109">線路裝置功能</span><span class="sxs-lookup"><span data-stu-id="07a51-109">Line Device Functions</span></span>](line-device-functions.md)
-   [<span data-ttu-id="07a51-110">電話裝置功能</span><span class="sxs-lookup"><span data-stu-id="07a51-110">Phone Device Functions</span></span>](phone-device-functions.md)

<span data-ttu-id="07a51-111">針對依服務層級和工作分類的 TAPI 函式，請參閱 [Tapi 快速](tapi-quick-function-reference.md)函式參考。</span><span class="sxs-lookup"><span data-stu-id="07a51-111">For TAPI functions categorized by service level and task, see [TAPI Quick Function Reference](tapi-quick-function-reference.md).</span></span>

<span data-ttu-id="07a51-112">請注意，服務提供者的限制可能會與可執行函數的實際狀態有關。</span><span class="sxs-lookup"><span data-stu-id="07a51-112">Please note that service provider limitations may exist concerning the actual states in which a function can be performed.</span></span> <span data-ttu-id="07a51-113">應用程式必須檢查 [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus)結構中的 **DwCallFeatures** 成員、 [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus)結構中的 **dwAddressFeatures** 成員，以及 [**dwLineFeatures**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus)結構中的 **LINEDEVSTATUS** 成員，以判斷目前的撥號狀態中是否允許函數。</span><span class="sxs-lookup"><span data-stu-id="07a51-113">Applications must check the **dwCallFeatures** member in the [**LINECALLSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linecallstatus) structure, the **dwAddressFeatures** member in the [**LINEADDRESSSTATUS**](/windows/desktop/api/Tapi/ns-tapi-lineaddressstatus) structure, and the **dwLineFeatures** member in the [**LINEDEVSTATUS**](/windows/desktop/api/Tapi/ns-tapi-linedevstatus) structure to determine whether or not a function is permitted within the current call state.</span></span>

 

 



