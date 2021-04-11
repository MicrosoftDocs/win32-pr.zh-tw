---
description: 轉送是指連至不同目的地位址的連入會話的偏離。
ms.assetid: c70bf596-b2a4-46ec-9b1a-c9d948768b51
title: 轉寄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4154e2bb6f8c688feffe2e33d3c5988b0b7da27b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848041"
---
# <a name="forward"></a><span data-ttu-id="1143f-103">轉寄</span><span class="sxs-lookup"><span data-stu-id="1143f-103">Forward</span></span>

<span data-ttu-id="1143f-104">轉送是指連至不同目的地位址的連入會話的偏離。</span><span class="sxs-lookup"><span data-stu-id="1143f-104">Forwarding is the deflection of an incoming session to a different destination address.</span></span> <span data-ttu-id="1143f-105">TAPI 可讓應用程式指定位址的轉送條件清單。</span><span class="sxs-lookup"><span data-stu-id="1143f-105">TAPI allows an application to specify a list of forwarding conditions for an address.</span></span> <span data-ttu-id="1143f-106">轉送條件可以精確為每個呼叫端位址的不同目的地和 [**轉送模式**](./lineforwardmode--constants.md) 。</span><span class="sxs-lookup"><span data-stu-id="1143f-106">Forwarding conditions can be as finely grained as a different destination and [**forwarding mode**](./lineforwardmode--constants.md) for each caller address.</span></span>

<span data-ttu-id="1143f-107">轉送作業也可以用來執行選擇性的不幹擾功能，方法是將一些來電者轉寄給語音信箱，讓其他人嘗試完成。</span><span class="sxs-lookup"><span data-stu-id="1143f-107">The forwarding operation can also be used to implement a selective do-not-disturb feature, by forwarding some callers to voice mail and allowing others to attempt completion.</span></span>

<span data-ttu-id="1143f-108">轉送作業也可以取消目前作用中的任何轉送。</span><span class="sxs-lookup"><span data-stu-id="1143f-108">The forwarding operation can also cancel any forwarding currently in effect.</span></span>

<span data-ttu-id="1143f-109">某些服務提供者要求應用程式在轉送作業之前建立諮詢通話。</span><span class="sxs-lookup"><span data-stu-id="1143f-109">Some service providers require that an application create a consultation call prior to a forwarding operation.</span></span> <span data-ttu-id="1143f-110">轉送作業接著會傳遞給諮詢通話的指標。</span><span class="sxs-lookup"><span data-stu-id="1143f-110">The forwarding operation is then passed a pointer to the consultation call.</span></span>

<span data-ttu-id="1143f-111">並非所有服務提供者都支援使用這項作業。</span><span class="sxs-lookup"><span data-stu-id="1143f-111">Not all service providers support use of this operation.</span></span>

<span data-ttu-id="1143f-112">**TAPI 2.x：** 若要將 [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward) 設定為取得 [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus)，請使用 LINEADDRESSSTATE 轉寄來變更 [**行 \_ ADDRESSSTATE**](./line-addressstate.md) 通知訊息 \_ 。</span><span class="sxs-lookup"><span data-stu-id="1143f-112">**TAPI 2.x:** To set [**lineForward**](/windows/win32/api/tapi/nf-tapi-lineforward) to get [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), change the [**LINE\_ADDRESSSTATE**](./line-addressstate.md) notification message with LINEADDRESSSTATE\_FORWARD.</span></span>

<span data-ttu-id="1143f-113">**TAPI 3.x：** 請參閱 [**ITAddress：： Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward)、 [**ITAddress：： get \_ CurrentForwardInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo)、change notification： [**ITADDRESSEVENT：： get \_ Event**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event) with AE \_ Forward。</span><span class="sxs-lookup"><span data-stu-id="1143f-113">**TAPI 3.x:** See [**ITAddress::Forward**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-forward), [**ITAddress::get\_CurrentForwardInfo**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddress-get_currentforwardinfo), change notification: [**ITAddressEvent::get\_Event**](/windows/desktop/api/tapi3if/nf-tapi3if-itaddressevent-get_event) with AE\_FORWARD.</span></span>

> [!Note]  
> <span data-ttu-id="1143f-114">服務提供者可能無法隨時知道轉送對位址有何作用。</span><span class="sxs-lookup"><span data-stu-id="1143f-114">It may be impossible for a service provider to know at all times what forwarding is in effect for an address.</span></span> <span data-ttu-id="1143f-115">轉送可以取消或變更，而不會產生通知給服務提供者。</span><span class="sxs-lookup"><span data-stu-id="1143f-115">Forwarding can be canceled or changed in ways that do not result in notification to the service provider.</span></span>

 

 

 
