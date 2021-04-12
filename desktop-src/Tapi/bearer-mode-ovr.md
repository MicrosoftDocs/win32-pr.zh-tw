---
description: 持有人模式對應于從網路要求以建立呼叫的傳輸品質。
ms.assetid: 5276e1e7-7a91-4b74-b8c2-c0c7cebb203f
title: 持有者模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1780bee44254e6da754584f838785452ee728f18
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192101"
---
# <a name="bearer-mode"></a><span data-ttu-id="5cbea-103">持有者模式</span><span class="sxs-lookup"><span data-stu-id="5cbea-103">Bearer Mode</span></span>

<span data-ttu-id="5cbea-104">[**持有人模式**](./linebearermode--constants.md)對應于從網路要求以建立呼叫的傳輸品質。</span><span class="sxs-lookup"><span data-stu-id="5cbea-104">The [**bearer mode**](./linebearermode--constants.md) corresponds to the quality of transmission requested from the network for establishing a call.</span></span> <span data-ttu-id="5cbea-105">請務必將持有人模式的概念與 [**媒體類型**](tapimediatype--constants.md)分開。</span><span class="sxs-lookup"><span data-stu-id="5cbea-105">It is important to keep the concept of bearer mode separate from that of [**media type**](tapimediatype--constants.md).</span></span> <span data-ttu-id="5cbea-106">例如，類比電話網絡 (PSTN) 只提供 3.1 kHz 語音等級的持有者模式，但使用它的呼叫可以支援語音、傳真或資料數據機等媒體類型。</span><span class="sxs-lookup"><span data-stu-id="5cbea-106">As an example, the analog telephone network (PSTN) provides only a 3.1 kHz voice-grade bearer mode but calls using it can support media types such as voice, fax, or data modem.</span></span>

<span data-ttu-id="5cbea-107">呼叫的持有人模式是在呼叫設定時指定，或在提供呼叫時提供。</span><span class="sxs-lookup"><span data-stu-id="5cbea-107">The bearer mode of a call is specified when the call is set up, or is provided when the call is offered.</span></span> <span data-ttu-id="5cbea-108">使用可代表通道集區的線路裝置，服務提供者可以允許以較大的頻寬建立呼叫。</span><span class="sxs-lookup"><span data-stu-id="5cbea-108">With line devices able to represent channel pools, it is possible for a service provider to allow calls to be established with wider bandwidth.</span></span>

<span data-ttu-id="5cbea-109">並非所有服務提供者都支援使用這項資訊。</span><span class="sxs-lookup"><span data-stu-id="5cbea-109">Not all service providers support use of this information.</span></span>

<span data-ttu-id="5cbea-110">**TAPI 2.x：** 請參閱 [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo)的 [**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams)、 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo)、 **dwBearerMode** 成員。</span><span class="sxs-lookup"><span data-stu-id="5cbea-110">**TAPI 2.x:** See [**lineSetCallParams**](/windows/win32/api/tapi/nf-tapi-linesetcallparams), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwBearerMode** member of [**LINECALLINFO**](/windows/win32/api/tapi/ns-tapi-linecallinfo).</span></span>

<span data-ttu-id="5cbea-111">**TAPI 3.x：** 請 [**參閱 ITCallInfo：： get \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong)、 [**ITCallInfo：:P BEARERMODE \_ CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong)、 [**CALLINFO \_ LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long)的 **CIL \_** 成員。</span><span class="sxs-lookup"><span data-stu-id="5cbea-111">**TAPI 3.x:** See [**ITCallInfo::get\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-get_callinfolong), [**ITCallInfo::put\_CallInfoLong**](/windows/desktop/api/tapi3if/nf-tapi3if-itcallinfo-put_callinfolong), **CIL\_BEARERMODE** member of [**CALLINFO\_LONG**](/windows/desktop/api/Tapi3if/ne-tapi3if-callinfo_long).</span></span>

<span data-ttu-id="5cbea-112">**TSPI：** 請參閱程式 [**行 \_ CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) 訊息，並將 *dwParam1* 設定為 LINECALLINFOSTATE \_ BEARERMODE。</span><span class="sxs-lookup"><span data-stu-id="5cbea-112">**TSPI:** See [**LINE\_CALLINFO**](/previous-versions/windows/desktop/legacy/ms725218(v=vs.85)) message, with *dwParam1* set to LINECALLINFOSTATE\_BEARERMODE.</span></span>

 

 
