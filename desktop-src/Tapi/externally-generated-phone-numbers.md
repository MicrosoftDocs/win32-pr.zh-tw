---
description: 服務提供者可以在處理 TSPI lineGetCallInfo 函式時，藉由設定 LINECALLINFO 結構的成員，來指出外部產生的電話號碼 \_ 。
ms.assetid: 10c83199-de7d-4a9b-84c4-ef8f5ea5055a
title: 外部產生的電話號碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b53e7039023ecec987a16c39367a569925c20ef8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690484"
---
# <a name="externally-generated-phone-numbers"></a><span data-ttu-id="50ee1-103">外部產生的電話號碼</span><span class="sxs-lookup"><span data-stu-id="50ee1-103">Externally Generated Phone Numbers</span></span>

<span data-ttu-id="50ee1-104">服務提供者可以表示外部產生的電話號碼 (也就是在外部對電腦產生的輸出呼叫數目) ，方法是在處理 [**TSPI \_ lineGetCallInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo)函式時，設定 [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)結構中的 **DisplayableAddress**、 **CalledParty** 或 [Comment](./comment-ovr.md)成員。</span><span class="sxs-lookup"><span data-stu-id="50ee1-104">A service provider can indicate externally generated phone numbers (that is, numbers for outbound calls generated externally to the computer) by setting the **DisplayableAddress**, **CalledParty**, or [Comment](./comment-ovr.md) members in the [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo) structure when processing the [**TSPI\_lineGetCallInfo**](/windows/win32/api/tspi/nf-tspi-tspi_linegetcallinfo) function.</span></span> <span data-ttu-id="50ee1-105">如果 TAPI 尚未為這些成員儲存自己的資料，則服務提供者所設定的資料會保持不變。</span><span class="sxs-lookup"><span data-stu-id="50ee1-105">If TAPI has not saved its own data for these members, it leaves the data set by the service provider unchanged.</span></span> <span data-ttu-id="50ee1-106">如果 TAPI 已快取這些成員的資料，TAPI 會將其文字新增至 **LINECALLINFO** 結構之變數部分的結尾，並覆寫服務提供者放入固定部分的大小和位移。</span><span class="sxs-lookup"><span data-stu-id="50ee1-106">If TAPI does have cached data for these members, TAPI adds its text to the end of the variable portion of the **LINECALLINFO** structure and overwrites the size and offset the service provider has put into the fixed portion.</span></span>

<span data-ttu-id="50ee1-107">服務提供者也可以將輸出號碼複製到 **CalledID** 成員。</span><span class="sxs-lookup"><span data-stu-id="50ee1-107">A service provider can also copy an outbound number into the **CalledID** member.</span></span> <span data-ttu-id="50ee1-108">因此，如果 **DisplayableAddress** 和 **CalledParty** 成員是空的，則記錄應用程式應該檢查輸出呼叫的 **CalledID** 成員。</span><span class="sxs-lookup"><span data-stu-id="50ee1-108">Therefore, logging applications should check the **CalledID** member on outbound calls if the **DisplayableAddress** and **CalledParty** members are empty.</span></span>

 

 
