---
description: 您可以使用 EscapeCommFunction 函式，針對裝置呼叫某些通訊功能。
ms.assetid: 12b92d4b-04b5-4509-9fad-af23fcfd8857
title: 擴充函數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1d0e57c316b521cbc246e5f31dcfb683238e216e
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025972"
---
# <a name="extended-functions"></a><span data-ttu-id="b0ba9-103">擴充函數</span><span class="sxs-lookup"><span data-stu-id="b0ba9-103">Extended Functions</span></span>

<span data-ttu-id="b0ba9-104">您可以使用 [**EscapeCommFunction**](/windows/desktop/api/Winbase/nf-winbase-escapecommfunction) 函式，針對裝置呼叫某些通訊功能。</span><span class="sxs-lookup"><span data-stu-id="b0ba9-104">Some communications functions can be called for a device by using the [**EscapeCommFunction**](/windows/desktop/api/Winbase/nf-winbase-escapecommfunction) function.</span></span> <span data-ttu-id="b0ba9-105">此函式會傳送程式碼，以指示裝置執行擴充功能。</span><span class="sxs-lookup"><span data-stu-id="b0ba9-105">This function sends a code to direct the device to perform an extended function.</span></span> <span data-ttu-id="b0ba9-106">例如，應用程式可以使用 SETBREAK 碼暫停字元傳輸，並使用 CLRBREAK 程式碼繼續傳輸。</span><span class="sxs-lookup"><span data-stu-id="b0ba9-106">For example, an application can suspend character transmission with the SETBREAK code and resume transmission with the CLRBREAK code.</span></span> <span data-ttu-id="b0ba9-107">您也可以藉由呼叫 [**SetCommBreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak) 和 [**ClearCommBreak**](/windows/desktop/api/Winbase/nf-winbase-clearcommbreak) 函數來啟動這些特定作業。</span><span class="sxs-lookup"><span data-stu-id="b0ba9-107">These particular operations can also be started by calling the [**SetCommBreak**](/windows/desktop/api/Winbase/nf-winbase-setcommbreak) and [**ClearCommBreak**](/windows/desktop/api/Winbase/nf-winbase-clearcommbreak) functions.</span></span> <span data-ttu-id="b0ba9-108">**EscapeCommFunction** 也可以用來執行手動數據機控制。</span><span class="sxs-lookup"><span data-stu-id="b0ba9-108">**EscapeCommFunction** can also be used to implement manual modem control.</span></span> <span data-ttu-id="b0ba9-109">例如，CLRDTR 和 SETDTR 碼可以用來實 (資料終端機) 流量控制的手動 DTR。</span><span class="sxs-lookup"><span data-stu-id="b0ba9-109">For example, the CLRDTR and SETDTR codes can be used to implement manual DTR (data-terminal-ready) flow control.</span></span> <span data-ttu-id="b0ba9-110">不過，請注意，如果在裝置設定為啟用 DTR 握手時，進程使用 **EscapeCommFunction** 來操作 dtr 行，或如果啟用了 rts 握手，)  (則會發生錯誤。</span><span class="sxs-lookup"><span data-stu-id="b0ba9-110">Note, however, that an error occurs if a process uses **EscapeCommFunction** to manipulate the DTR line when the device has been configured to enable DTR handshaking, or the RTS (request-to-send) line if RTS handshaking is enabled.</span></span>

<span data-ttu-id="b0ba9-111">[**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol)函式可讓程式將擴充的函式程式碼直接傳送到指定的設備磁碟機，使裝置執行指定的作業。</span><span class="sxs-lookup"><span data-stu-id="b0ba9-111">The [**DeviceIoControl**](/windows/win32/api/ioapiset/nf-ioapiset-deviceiocontrol) function enables a process to send an extended function code directly to a specified device driver, causing the device to perform a given operation.</span></span> <span data-ttu-id="b0ba9-112">**DeviceIoControl** 會提供與標準串列通訊功能不支援的通訊資源功能相關聯的裝置。</span><span class="sxs-lookup"><span data-stu-id="b0ba9-112">**DeviceIoControl** gives a device associated with a communications resource capabilities not supported by the standard serial communications functions.</span></span> <span data-ttu-id="b0ba9-113">它可讓應用程式使用該裝置特有的參數來設定裝置，以及呼叫任何裝置特定的函式。</span><span class="sxs-lookup"><span data-stu-id="b0ba9-113">It enables an application to configure a device using parameters unique to that device as well as to call any device-specific functions.</span></span>

 

 
