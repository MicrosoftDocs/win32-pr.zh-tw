---
description: 網址類別型會識別位址所需的格式。 例如，如果類型是 LINEADDRESSTYPE \_ PHONENUMBER，則用來撥入會話的位址必須是電話號碼。
ms.assetid: bea48bde-927a-400a-9a7e-a77e30ba35eb
title: 會話的網址類別型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 42499c19a08d67ce2e6e7ea5741053686c32aa6d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977343"
---
# <a name="address-type-for-a-session"></a><span data-ttu-id="e0d91-104">會話的網址類別型</span><span class="sxs-lookup"><span data-stu-id="e0d91-104">Address Type for a Session</span></span>

<span data-ttu-id="e0d91-105">[**網址類別型**](lineaddresstype--constants.md)會識別位址所需的格式。</span><span class="sxs-lookup"><span data-stu-id="e0d91-105">The [**address type**](lineaddresstype--constants.md) identifies the format required for an address.</span></span> <span data-ttu-id="e0d91-106">例如，如果類型是 LINEADDRESSTYPE \_ PHONENUMBER，則用來撥入會話的位址必須是電話號碼。</span><span class="sxs-lookup"><span data-stu-id="e0d91-106">For example, if the type is LINEADDRESSTYPE\_PHONENUMBER, the address used to dial on the session must be a phone number.</span></span>

<span data-ttu-id="e0d91-107">指定的裝置和服務提供者支援一或多個網址類別型。</span><span class="sxs-lookup"><span data-stu-id="e0d91-107">A given device and service provider supports one or more address types.</span></span> <span data-ttu-id="e0d91-108">如需如何輪詢裝置以取得其所支援之位址格式的資訊，請參閱 [裝置的網址類別型](address-type-ovr.md) 。</span><span class="sxs-lookup"><span data-stu-id="e0d91-108">See the [address types for a device](address-type-ovr.md) for information on how to poll a device for the address formats it supports.</span></span>

<span data-ttu-id="e0d91-109">**TAPI 2.x：** 請參閱 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo)、 **DwAddressType** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)。</span><span class="sxs-lookup"><span data-stu-id="e0d91-109">**TAPI 2.x:** See [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwAddressType** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).</span></span>

<span data-ttu-id="e0d91-110">**TAPI 3.x：** 請參閱 [**CONNECTEDIDADDRESSTYPE \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)的 cil **\_ CALLERIDADDRESSTYPE**、 **Cil \_ CALLEDIDADDRESSTYPE** 或 **cil \_ CALLINFO** 成員呼叫 [**ITCallInfo：： get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)。</span><span class="sxs-lookup"><span data-stu-id="e0d91-110">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), called with the **CIL\_CALLERIDADDRESSTYPE**, **CIL\_CALLEDIDADDRESSTYPE**, or **CIL\_CONNECTEDIDADDRESSTYPE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span></span>

 

 
