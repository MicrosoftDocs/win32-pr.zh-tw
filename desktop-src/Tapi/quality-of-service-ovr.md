---
description: 非同步傳輸模式 (ATM) 網路功能逐漸進入運算的主要部分，而對 ATM 的支援已新增至作業系統的許多部分。
ms.assetid: 0ca0ecf3-2b67-4925-a6fc-3edfaad2c0e2
title: '服務品質 (電話語音 API) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6525ced0b29d35482244c3c37f8382edbfcb9fd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851252"
---
# <a name="quality-of-service-telephony-api"></a><span data-ttu-id="c4bd2-103">服務品質 (電話語音 API) </span><span class="sxs-lookup"><span data-stu-id="c4bd2-103">Quality of Service (Telephony API)</span></span>

<span data-ttu-id="c4bd2-104">非同步傳輸模式 (ATM) 網路功能逐漸進入運算的主要部分，而對 ATM 的支援已新增至作業系統的許多部分。</span><span class="sxs-lookup"><span data-stu-id="c4bd2-104">Asynchronous Transfer Mode (ATM) networking is emerging into the mainstream of computing, and support for ATM has been added to many parts of the operating system.</span></span> <span data-ttu-id="c4bd2-105">TAPI 也支援在 ATM 設施上建立呼叫的重要屬性。</span><span class="sxs-lookup"><span data-stu-id="c4bd2-105">TAPI also supports key attributes of establishing calls on ATM facilities.</span></span> <span data-ttu-id="c4bd2-106">從應用程式的觀點來看，最重要的就是能夠要求、協調、重新協商和接收服務品質的徵兆， (QOS) 參數的傳入和撥出電話。</span><span class="sxs-lookup"><span data-stu-id="c4bd2-106">The most important of these from an application perspective is the ability to request, negotiate, renegotiate, and receive indications of Quality of Service (QOS) parameters on incoming and outgoing calls.</span></span>

<span data-ttu-id="c4bd2-107">TAPI 中的 QOS 資訊是在 Windows 通訊端2.0 所定義 [**FLOWSPEC**](/windows/desktop/api/qos/ns-qos-flowspec) 結構中的應用程式與服務提供者之間進行交換。</span><span class="sxs-lookup"><span data-stu-id="c4bd2-107">QOS information in TAPI is exchanged between applications and service providers in [**FLOWSPEC**](/windows/desktop/api/qos/ns-qos-flowspec) structures that are defined in Windows Sockets 2.0.</span></span>

<span data-ttu-id="c4bd2-108">應用程式會在啟動通訊會話之前，藉由設定會話資訊值來要求撥出電話的 QOS。</span><span class="sxs-lookup"><span data-stu-id="c4bd2-108">Applications request QOS on outgoing calls by setting session information values prior to starting a communications session.</span></span> <span data-ttu-id="c4bd2-109">服務提供者將嘗試提供指定的 QOS，如果無法，則會使呼叫失敗。</span><span class="sxs-lookup"><span data-stu-id="c4bd2-109">The service provider will try to provide the specified QOS, and fail the call if it cannot.</span></span> <span data-ttu-id="c4bd2-110">然後，應用程式可以調整其參數，然後再次嘗試呼叫。</span><span class="sxs-lookup"><span data-stu-id="c4bd2-110">The application can then adjust its parameters and try the call again.</span></span> <span data-ttu-id="c4bd2-111">建立呼叫之後，應用程式可以要求 QOS 中的變更。</span><span class="sxs-lookup"><span data-stu-id="c4bd2-111">After a call is established, an application can request a change in the QOS.</span></span>

<span data-ttu-id="c4bd2-112">如果 QOS 層級有任何變更，TAPI 會提供事件通知給擁有者或監視應用程式。</span><span class="sxs-lookup"><span data-stu-id="c4bd2-112">TAPI provides event notifications to owner or monitor applications if there is any change in QOS levels.</span></span>

<span data-ttu-id="c4bd2-113">對 QOS 的支援不限於 ATM 傳輸;任何服務提供者都可以執行 QOS 功能。</span><span class="sxs-lookup"><span data-stu-id="c4bd2-113">Support for QOS is not restricted to ATM transports; any service provider can implement QOS features.</span></span>

<span data-ttu-id="c4bd2-114">並非所有服務提供者都支援使用這項資訊。</span><span class="sxs-lookup"><span data-stu-id="c4bd2-114">Not all service providers support use of this information.</span></span>

<span data-ttu-id="c4bd2-115">\* \* TAPI 2.x： \* \*[**lineSetCallQualityOfService**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice)、 [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo)、 **dwSendingFlowspecSize**、 **dwSendingFlowspecOffset**、 **dwReceivingFlowspecSize** 和 **dwReceivingFlowspecOffset** 成員 [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams)</span><span class="sxs-lookup"><span data-stu-id="c4bd2-115">\*\*TAPI 2.x:  \*\*[**lineSetCallQualityOfService**](/windows/win32/api/tapi/nf-tapi-linesetcallqualityofservice), [**lineGetCallInfo**](/windows/win32/api/tapi/nf-tapi-linegetcallinfo), **dwSendingFlowspecSize**, **dwSendingFlowspecOffset**, **dwReceivingFlowspecSize**, and **dwReceivingFlowspecOffset** members of [**LINECALLPARAMS**](/windows/win32/api/tapi/ns-tapi-linecallparams)</span></span>

<span data-ttu-id="c4bd2-116">\* \* TAPI 3.x： \* \*[**ITBasicCallControl：： SetQOS**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos)， [**ITQOSEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)</span><span class="sxs-lookup"><span data-stu-id="c4bd2-116">\*\*TAPI 3.x:  \*\*[**ITBasicCallControl::SetQOS**](/windows/desktop/api/tapi3if/nf-tapi3if-itbasiccallcontrol-setqos), [**ITQOSEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itqosevent)</span></span>

 

 
