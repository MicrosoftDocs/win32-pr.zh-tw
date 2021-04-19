---
description: 當 ITTAPIEventNotification：： Event 方法傳回的 TAPI \_ 事件等於 TE 終端機時 \_ ，ITTerminalEvent 介面所公開的方法可以用來取得發生的終端機事件相關資訊（如果有 MSP 存在的話）。
ms.assetid: 5277776e-0471-41b6-b662-4346a9d237ec
title: 'ITTerminalEvent (MSPI) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 593b9a7d048db9843825ccde8b22d0585a0c07fb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990347"
---
# <a name="itterminalevent-mspi"></a><span data-ttu-id="11cde-103">ITTerminalEvent (MSPI) </span><span class="sxs-lookup"><span data-stu-id="11cde-103">ITTerminalEvent (MSPI)</span></span>

<span data-ttu-id="11cde-104">當 [**ITTAPIEventNotification：： Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) 方法傳回的 [**TAPI \_ 事件**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) 等於 **TE \_ 終端** 機時， **ITTerminalEvent** 介面所公開的方法可以用來取得發生的終端機事件相關資訊（如果有 MSP 存在的話）。</span><span class="sxs-lookup"><span data-stu-id="11cde-104">When the [**ITTAPIEventNotification::Event**](/windows/desktop/api/Tapi3if/nf-tapi3if-ittapieventnotification-event) method returns [**TAPI\_EVENT**](/windows/desktop/api/Tapi3if/ne-tapi3if-tapi_event) equal to **TE\_TERMINAL**, the methods exposed by the **ITTerminalEvent** interface can be used to retrieve information concerning the terminal event that has occurred, if an MSP exists.</span></span>

<span data-ttu-id="11cde-105">**ITTerminalEvent** 介面是由 MSP 所執行，而且如果沒有與該位址相關聯的媒體服務提供者，就無法使用。</span><span class="sxs-lookup"><span data-stu-id="11cde-105">The **ITTerminalEvent** interface is implemented by an MSP and is not available if there is no media service provider associated with the address.</span></span> <span data-ttu-id="11cde-106">如需此介面的詳細資訊，請參閱 MSP 介面一節中的 **ITTerminalEvent** 。</span><span class="sxs-lookup"><span data-stu-id="11cde-106">Please see **ITTerminalEvent** in the MSP Interface section for details on this interface.</span></span>

 

 



