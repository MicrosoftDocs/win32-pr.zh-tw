---
description: 呼叫端識別會在接收傳入的會話時，提供呼叫方的相關資訊。 應用程式通常會使用此資料做為使用者的狀態訊息的一部分。
ms.assetid: aaaa5eae-e917-44a7-b9c5-97ca2d9a4eec
title: 呼叫端識別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93513e3d94fac9c550b23651b3987bc794905beb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850476"
---
# <a name="caller-identification"></a><span data-ttu-id="1ed8d-104">呼叫端識別</span><span class="sxs-lookup"><span data-stu-id="1ed8d-104">Caller Identification</span></span>

<span data-ttu-id="1ed8d-105">呼叫端識別會在接收傳入的會話時，提供呼叫方的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="1ed8d-105">Caller identification provides information on the calling party when receiving an incoming session.</span></span> <span data-ttu-id="1ed8d-106">應用程式通常會使用此資料做為使用者的狀態訊息的一部分。</span><span class="sxs-lookup"><span data-stu-id="1ed8d-106">An application typically uses this data as part of a status message to a user.</span></span>

<span data-ttu-id="1ed8d-107">這項資訊不一定會立即可用。</span><span class="sxs-lookup"><span data-stu-id="1ed8d-107">This information is not always available immediately.</span></span> <span data-ttu-id="1ed8d-108">如果應用程式想要使用這項資訊，並已驗證服務提供者支援它，則應該先檢查數次，再假設資訊無法使用。</span><span class="sxs-lookup"><span data-stu-id="1ed8d-108">An application that wants to use this information and has verified that the service provider supports it should check several times before assuming that the information is not available.</span></span>

<span data-ttu-id="1ed8d-109">並非所有服務提供者都支援使用這項資訊。</span><span class="sxs-lookup"><span data-stu-id="1ed8d-109">Not all service providers support use of this information.</span></span>

<span data-ttu-id="1ed8d-110">**TAPI 2.x：** 請參閱 *dwCallerIDNameSize*) 的 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallerIDFlags**、 **dwCallerIDSize**、 **dwCallerIDOffset**、 **dwCallerIDNameOffset**、 **dwCallerIDAddressType** 和 **lpCallInfo** 成員。</span><span class="sxs-lookup"><span data-stu-id="1ed8d-110">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwCallerIDFlags**, **dwCallerIDSize**, **dwCallerIDOffset**, **dwCallerIDNameSize**, **dwCallerIDNameOffset**, and **dwCallerIDAddressType** members of *lpCallInfo*).</span></span>

<span data-ttu-id="1ed8d-111">**TAPI 3.x：** 請參閱 [**ITCallInfo：： \_ get CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) () [**\_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)的 **\_ CALLERIDADDRESSTYPE** 成員、 [**ITCallInfo：： Get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS \_ CALLERIDNAME** 和 [**CALLERIDNAME \_ STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)) 的 **cis \_ CALLINFO** 成員。</span><span class="sxs-lookup"><span data-stu-id="1ed8d-111">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong) (**CIL\_CALLERIDADDRESSTYPE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)), [**ITCallInfo::get\_CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIS\_CALLERIDNAME** and **CIS\_CALLERIDNAME** members of [**CALLINFO\_STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span></span>

 

 
