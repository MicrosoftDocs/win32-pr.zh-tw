---
description: 服務提供者可以將 PBX 上的每個資源公開為線路裝置，以及可能的關聯電話裝置。
ms.assetid: 25394b19-bf75-4adc-b07d-41bc781931b6
title: 撥打電話中心的模型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2763a1baafa41cf2d9b3b9b3c9d13be675a02d83
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386064"
---
# <a name="modeling-of-a-call-center"></a><span data-ttu-id="67a6b-103">撥打電話中心的模型</span><span class="sxs-lookup"><span data-stu-id="67a6b-103">Modeling of a Call Center</span></span>

<span data-ttu-id="67a6b-104">服務提供者可以將 PBX 上的每個資源公開為線路裝置，以及可能的關聯電話裝置。</span><span class="sxs-lookup"><span data-stu-id="67a6b-104">Service providers can expose each resource on the PBX as a line device and possibly an associated phone device.</span></span> <span data-ttu-id="67a6b-105">支援多個呼叫外觀的終端機會透過多個位址來執行，就像第一方的呼叫控制一樣。</span><span class="sxs-lookup"><span data-stu-id="67a6b-105">Terminals that support multiple call appearances would do so through multiple addresses, just as in first-party call control.</span></span> <span data-ttu-id="67a6b-106">事實上，裝置的協力廠商觀點等同于第一方的觀點;伺服器上的應用程式可以查看及控制所有第一方的裝置，而連接到伺服器的個別用戶端電腦只能透過伺服器上的 TAPISRV 所管理的存取控制，來查看可看見的裝置。</span><span class="sxs-lookup"><span data-stu-id="67a6b-106">In fact, the third-party view of a device is identical to the first-party view; applications on the server can see and control all of the first-party devices, whereas an individual client PC connected to the server can only see those devices that are made visible to it through access controls administered by TAPISRV on the server.</span></span> <span data-ttu-id="67a6b-107">終端機以外的資源也可以模型化為線路裝置。</span><span class="sxs-lookup"><span data-stu-id="67a6b-107">Resources other than terminals can also be modeled as line devices.</span></span> <span data-ttu-id="67a6b-108">例如，ACD 佇列或路由點會模型化為可能具有許多使用中呼叫的線路裝置;IVR 伺服器、語音郵件伺服器或一組預測撥號埠也可以模型化為支援多個呼叫的線路裝置。</span><span class="sxs-lookup"><span data-stu-id="67a6b-108">For example, an ACD queue or route point would be modeled as a line device that could have many active calls; an IVR server, voice mail server, or set of predictive dialing ports could also be modeled as a line device that supports multiple calls.</span></span>

<span data-ttu-id="67a6b-109">在此模型中，您可以透過現有的 TAPI 訊息（例如 [**行 \_ LINEDEVSTATE**](line-linedevstate.md)、 [**行 \_ ADDRESSSTATE**](line-addressstate.md)、 [**行 \_ CALLSTATE**](line-callstate.md)和 [**行 \_ CALLINFO**](line-callinfo.md)），以及透過 [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus)、 [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus)、 [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus)和 [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo)等函式取得的詳細資料，來監視定址裝置的狀態和與其相關聯的呼叫。</span><span class="sxs-lookup"><span data-stu-id="67a6b-109">Within this model, the status of the addressed device and calls associated with it can be monitored though existing TAPI messages such as [**LINE\_LINEDEVSTATE**](line-linedevstate.md), [**LINE\_ADDRESSSTATE**](line-addressstate.md), [**LINE\_CALLSTATE**](line-callstate.md), and [**LINE\_CALLINFO**](line-callinfo.md), and details obtained through functions such as [**lineGetLineDevStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetlinedevstatus), [**lineGetAddressStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetaddressstatus), [**lineGetCallStatus**](/windows/desktop/api/Tapi/nf-tapi-linegetcallstatus), and [**lineGetCallInfo**](/windows/desktop/api/Tapi/nf-tapi-linegetcallinfo).</span></span> <span data-ttu-id="67a6b-110">只要透過伺服器上執行的協力廠商應用程式來操作 TAPI 物件，結果就會與該裝置相關聯的用戶端電腦上執行的第一方應用程式同樣操作時，所發生的結果相同。</span><span class="sxs-lookup"><span data-stu-id="67a6b-110">Whenever a TAPI object is operated upon through a third-party application running on the server, the result is identical to what would have occurred if the same object had been similarly operated on by a first-party application running on a client PC associated with that device.</span></span> <span data-ttu-id="67a6b-111">由伺服器服務提供者所傳送的狀態指標，可控制切換網狀架構 (或切換) 會傳遞給在伺服器上執行的應用程式，以及在相關聯的授權用戶端上執行的應用程式。</span><span class="sxs-lookup"><span data-stu-id="67a6b-111">Status indications sent by the server service provider controlling the switching fabric (or switch) are delivered both to applications running on the server and to those running on associated, authorized clients.</span></span>

 

 



