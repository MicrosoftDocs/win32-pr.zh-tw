---
description: 連接的識別會識別實際連接的合作物件。 如果呼叫轉向，這可能與被呼叫的識別碼不同。
ms.assetid: 3f9ba728-8e78-4f1f-a0c1-76799fd62c9d
title: 連接的識別
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 59fdb2f11b27bf9281b381170aa0d5b5ab027088
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321203"
---
# <a name="connected-identification"></a><span data-ttu-id="54013-104">連接的識別</span><span class="sxs-lookup"><span data-stu-id="54013-104">Connected Identification</span></span>

<span data-ttu-id="54013-105">連接的識別會識別實際連接的合作物件。</span><span class="sxs-lookup"><span data-stu-id="54013-105">The connected identification identifies the party that was actually connected to.</span></span> <span data-ttu-id="54013-106">如果呼叫轉向，這可能與被呼叫的識別碼不同。</span><span class="sxs-lookup"><span data-stu-id="54013-106">This may be different from the called identification if the call was diverted.</span></span>

<span data-ttu-id="54013-107">並非所有服務提供者都支援使用這項資訊。</span><span class="sxs-lookup"><span data-stu-id="54013-107">Not all service providers support use of this information.</span></span>

<span data-ttu-id="54013-108">**TAPI 2.x：** 請參閱 *dwConnectedIDNameSize*) 的 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwConnectedIDFlags**、 **dwConnectedIDSize**、 **dwConnectedIDOffset**、 **dwConnectedIDNameOffset** 和 **lpCallInfo** 成員。</span><span class="sxs-lookup"><span data-stu-id="54013-108">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo) (**dwConnectedIDFlags**, **dwConnectedIDSize**, **dwConnectedIDOffset**, **dwConnectedIDNameSize**, and **dwConnectedIDNameOffset** members of *lpCallInfo*).</span></span>

<span data-ttu-id="54013-109">**TAPI 3.x：** 請參閱 [**ITCallInfo：： get \_ CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) ([**CALLINFO \_ STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)) 的 **CIL \_ CONNECTEDIDNAME** 成員。</span><span class="sxs-lookup"><span data-stu-id="54013-109">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoString**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfostring) (**CIL\_CONNECTEDIDNAME** member of [**CALLINFO\_STRING**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_string)).</span></span>

 

 
