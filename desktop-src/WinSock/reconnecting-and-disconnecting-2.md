---
description: 您可以直接呼叫 WSPConnect 來變更預設目的地，即使通訊端已經連接也是一樣。 如果新位址與先前 WSPConnect 中指定的位址不同，則會捨棄任何排入佇列以接收的資料包。
ms.assetid: b5f5ab97-03bd-4f5c-8808-d14ad5a56a5a
title: 重新連線和中斷連接
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7babefe03be44f942ee60a840aa210ee3c0e25da
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848753"
---
# <a name="reconnecting-and-disconnecting"></a><span data-ttu-id="09893-104">重新連線和中斷連接</span><span class="sxs-lookup"><span data-stu-id="09893-104">Reconnecting and Disconnecting</span></span>

<span data-ttu-id="09893-105">您可以直接呼叫 [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) 來變更預設目的地，即使通訊端已經連接也是一樣。</span><span class="sxs-lookup"><span data-stu-id="09893-105">The default destination may be changed by simply calling [**WSPConnect**](/previous-versions/windows/hardware/network/ff566275(v=vs.85)) again, even if the socket is already connected.</span></span> <span data-ttu-id="09893-106">如果新位址與先前 **WSPConnect** 中指定的位址不同，則會捨棄任何排入佇列以接收的資料包。</span><span class="sxs-lookup"><span data-stu-id="09893-106">Any datagrams queued for receipt are discarded if the new address is different from the address specified in a previous **WSPConnect**.</span></span>

<span data-ttu-id="09893-107">如果為通訊端提供的位址全部為零，則通訊端將會中斷連線，因此， [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) 和 [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) 呼叫將會傳回錯誤碼 WSAENOTCONN，不過仍可能使用 [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) 和 [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) 。</span><span class="sxs-lookup"><span data-stu-id="09893-107">If the address supplied for the socket is all zeros, the socket will be disconnected — the default remote address will be indeterminate, so [**WSPSend**](/previous-versions/windows/hardware/network/ff566316(v=vs.85)) and [**WSPRecv**](/previous-versions/windows/hardware/network/ff566309(v=vs.85)) calls will return the error code WSAENOTCONN, although [**WSPSendTo**](/previous-versions/windows/desktop/legacy/ms742291(v=vs.85)) and [**WSPRecvFrom**](/previous-versions/windows/desktop/legacy/ms742287(v=vs.85)) may still be used.</span></span>

 

 
