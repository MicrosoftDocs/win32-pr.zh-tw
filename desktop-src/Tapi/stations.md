---
description: 透過協力廠商連結監視的工作站集會被模型化為線路裝置，也可能是關聯的電話裝置。
ms.assetid: 1d116734-cd8f-40f1-9069-2dad351a24bf
title: 站
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff497eb70d1a1fd8441eeb8ad24bae6e5d1cd03e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983917"
---
# <a name="stations"></a><span data-ttu-id="fa098-103">站</span><span class="sxs-lookup"><span data-stu-id="fa098-103">Stations</span></span>

<span data-ttu-id="fa098-104">透過協力廠商連結監視的工作站集會被模型化為線路裝置，也可能是關聯的電話裝置。</span><span class="sxs-lookup"><span data-stu-id="fa098-104">Station sets being monitored through a third-party link are modeled as a line device and possibly an associated phone device.</span></span> <span data-ttu-id="fa098-105">如果模型化終端 (DN) 支援一個以上的目錄編號，線路裝置可以有多個位址。</span><span class="sxs-lookup"><span data-stu-id="fa098-105">The line device can have multiple addresses, if the modeled terminal supports more than one directory number (DN).</span></span> <span data-ttu-id="fa098-106">相同 DN 上的多個呼叫外觀可以模型化為支援多個呼叫的單一位址。</span><span class="sxs-lookup"><span data-stu-id="fa098-106">Multiple call appearances on the same DN can be modeled as a single address that supports multiple calls.</span></span>

<span data-ttu-id="fa098-107">交換器上兩個電臺之間的呼叫會有兩個呼叫控制碼，一種是提供第一個站 (在其線路裝置上的呼叫視圖) ，另一個則是從第二站裝置上的第二站 () 。</span><span class="sxs-lookup"><span data-stu-id="fa098-107">Calls between two stations on the switch have two call handles, one giving the call view from the first station (on its line device), and the other giving the call view from the second station (on its line device).</span></span> <span data-ttu-id="fa098-108">例如，應用程式在伺服器上的協力廠商 [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) 會被導向至與撥打電話的來源裝置相關聯的線路裝置;在 ([**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) 中指定的位址上，會針對該行建立呼叫控制碼，以控制在支援多個 DNs) 的電話上使用的 DN。</span><span class="sxs-lookup"><span data-stu-id="fa098-108">For example, a third-party [**lineMakeCall**](/windows/desktop/api/Tapi/nf-tapi-linemakecall) placed by an application on the server would be directed to the line device associated with the station from which the call is to be dialed; a call handle would be created on that line, on the address specified in [**LINECALLPARAMS**](/windows/desktop/api/Tapi/ns-tapi-linecallparams) (thereby giving control over which DN is used on a phone that supports multiple DNs).</span></span> <span data-ttu-id="fa098-109">當將呼叫提供給目的地位址時，會建立新的呼叫控制碼，顯示 *提供* 狀態的呼叫;應用程式會知道它是相同呼叫的另一個觀點，而 [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo)中的 **dwCallID** 成員對兩個呼叫都相等。</span><span class="sxs-lookup"><span data-stu-id="fa098-109">When the call is offered to the destination address, a new call handle showing a call in *offering* state is created; applications would know that it was another view of the same call by the **dwCallID** member in [**LINECALLINFO**](/windows/desktop/api/Tapi/ns-tapi-linecallinfo) being equal for both calls.</span></span> <span data-ttu-id="fa098-110">當呼叫中斷時，這兩個呼叫都會 *閒置* ;您可以透過在其中一個呼叫控制碼上執行 [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) ，從協力廠商應用程式中卸載呼叫。</span><span class="sxs-lookup"><span data-stu-id="fa098-110">Both calls would go *idle* when the call was dropped; a call could be dropped from the third-party application by doing a [**lineDrop**](/windows/desktop/api/Tapi/nf-tapi-linedrop) on either of the call handles.</span></span>

 

 



