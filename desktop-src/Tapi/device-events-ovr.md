---
description: TAPI 會回應裝置變更，例如已開始響鈴的電話，或藉由引發裝置事件而移除的數據機。
ms.assetid: afa504ca-6e70-4076-a179-31002d3b38e2
title: '裝置事件 (電話語音 API) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 47f5508e74424a13117facc1c4c370144ecd46de
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103690491"
---
# <a name="device-events-telephony-api"></a><span data-ttu-id="3e3dd-103">裝置事件 (電話語音 API) </span><span class="sxs-lookup"><span data-stu-id="3e3dd-103">Device Events (Telephony API)</span></span>

<span data-ttu-id="3e3dd-104">TAPI 會回應裝置變更，例如已開始響鈴的電話，或藉由引發裝置事件而移除的數據機。</span><span class="sxs-lookup"><span data-stu-id="3e3dd-104">TAPI responds to device changes such as a phone that has started ringing or a modem that has been removed by firing device events.</span></span> <span data-ttu-id="3e3dd-105">TAPI 應用程式應該藉由查詢發生的特定變更，然後採取適當的動作來回應裝置事件。</span><span class="sxs-lookup"><span data-stu-id="3e3dd-105">A TAPI application should respond to a device event by querying for the specific change that has occurred and then taking appropriate action.</span></span> <span data-ttu-id="3e3dd-106">應用程式可能會對其使用 [事件通知](event-notification.md)接收的事件顯示幕幕。</span><span class="sxs-lookup"><span data-stu-id="3e3dd-106">An application may screen for events it will receive using [event notification](event-notification.md).</span></span>

<span data-ttu-id="3e3dd-107">**TAPI 2.x：** 應用程式會使用 [**LINE \_ LINEDEVSTATE**](./line-linedevstate.md) 訊息接收裝置事件的通知。</span><span class="sxs-lookup"><span data-stu-id="3e3dd-107">**TAPI 2.x:** Applications receive notification of device events using the [**LINE\_LINEDEVSTATE**](./line-linedevstate.md) message.</span></span> <span data-ttu-id="3e3dd-108">位址的目前狀態是藉由呼叫 [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus)來決定，這會在 [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) 結構中傳回其資訊。</span><span class="sxs-lookup"><span data-stu-id="3e3dd-108">The current status of an address is determined by calling [**lineGetAddressStatus**](/windows/win32/api/tapi/nf-tapi-linegetaddressstatus), which returns its information in a [**LINEADDRESSSTATUS**](/windows/win32/api/tapi/ns-tapi-lineaddressstatus) structure.</span></span> <span data-ttu-id="3e3dd-109">藉由呼叫 [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus)來取得指定之開放線路裝置的狀態，該裝置會在 [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) 結構中傳回其資訊。</span><span class="sxs-lookup"><span data-stu-id="3e3dd-109">The status of a specified open line device is obtained by calling [**lineGetLineDevStatus**](/windows/win32/api/tapi/nf-tapi-linegetlinedevstatus), which returns its information in a [**LINEDEVSTATUS**](/windows/win32/api/tapi/ns-tapi-linedevstatus) structure.</span></span>

<span data-ttu-id="3e3dd-110">**TAPI 3.x：** 應用程式會接收 [**位址 \_ 事件**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_event) 通知，此通知會使用 [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent) 介面來處理。</span><span class="sxs-lookup"><span data-stu-id="3e3dd-110">**TAPI 3.x:** Applications receive an [**ADDRESS\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-address_event) notification, which is processed using the [**ITAddressEvent**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddressevent) interface.</span></span> <span data-ttu-id="3e3dd-111">然後，您可以使用 [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) 來取得更多詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="3e3dd-111">The [**ITAddressCapabilities**](/windows/desktop/api/tapi3if/nn-tapi3if-itaddresscapabilities) can then be used to acquire more detail information.</span></span>

 

 
