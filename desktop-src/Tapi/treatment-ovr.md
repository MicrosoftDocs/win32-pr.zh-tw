---
description: 處理是指處理尚未接聽或已暫停的傳入會話（例如音樂）。 請參閱 LINECALLTREATMENT 的 \_ 常數，以取得 TAPI 所定義的一組治療。
ms.assetid: 0b8d1023-374a-4937-b39c-04043423eb47
title: 處理方式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4bbde0e602836b543e849afb3d56c33fd6df0a60
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469377"
---
# <a name="treatment"></a><span data-ttu-id="988e9-104">處理方式</span><span class="sxs-lookup"><span data-stu-id="988e9-104">Treatment</span></span>

<span data-ttu-id="988e9-105">處理是指處理尚未接聽或已暫停的傳入會話（例如音樂）。</span><span class="sxs-lookup"><span data-stu-id="988e9-105">Treatment refers to the handling of an incoming session that has not yet been answered or has been put on hold, such as music.</span></span> <span data-ttu-id="988e9-106">請參閱 [LINECALLTREATMENT 的 \_ 常數](./linecalltreatment--constants.md) ，以取得 TAPI 所定義的一組治療。</span><span class="sxs-lookup"><span data-stu-id="988e9-106">Please see [LINECALLTREATMENT\_ Constants](./linecalltreatment--constants.md) for a list of treatments defined by TAPI.</span></span>

<span data-ttu-id="988e9-107">並非所有服務提供者都支援使用這項資訊。</span><span class="sxs-lookup"><span data-stu-id="988e9-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="988e9-108">**TAPI 2.x： **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** dwCallTreatment** 成員的 *lpCallInfo*) </span><span class="sxs-lookup"><span data-stu-id="988e9-108">**TAPI 2.x:  **[**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (** dwCallTreatment** member of *lpCallInfo*)</span></span>

<span data-ttu-id="988e9-109">**TAPI 3.x： **[**ITCallInfo：： get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** \_** [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)) 的 CIL CALLTREATMENT 成員</span><span class="sxs-lookup"><span data-stu-id="988e9-109">**TAPI 3.x:  **[**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (** CIL\_CALLTREATMENT** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long))</span></span>

 

 
