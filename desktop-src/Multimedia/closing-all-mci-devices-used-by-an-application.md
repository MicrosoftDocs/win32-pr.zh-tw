---
title: 關閉應用程式所使用的所有 MCI 裝置
description: 關閉應用程式所使用的所有 MCI 裝置
ms.assetid: 1d7d3800-b38f-4187-ba57-9849fef4d707
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b84db0bc6a6160098a3714f9cc7dbf455427bc28
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103842123"
---
# <a name="closing-all-mci-devices-used-by-an-application"></a><span data-ttu-id="dd03d-103">關閉應用程式所使用的所有 MCI 裝置</span><span class="sxs-lookup"><span data-stu-id="dd03d-103">Closing All MCI Devices Used by an Application</span></span>

<span data-ttu-id="dd03d-104">下列範例會關閉應用程式使用 [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) 函式所開啟的所有 MCI 裝置。</span><span class="sxs-lookup"><span data-stu-id="dd03d-104">The following example closes all of the MCI devices that are opened by an application using the [**mciSendCommand**](/previous-versions//dd757160(v=vs.85)) function.</span></span>


```C++
UINT wDeviceID;
DWORD dwReturn;
 
// Closes all MCI devices opened by this application.
// Waits until devices are closed before returning.

if(dwReturn = mciSendCommand(MCI_ALL_DEVICE_ID, MCI_CLOSE, MCI_WAIT, 
    NULL))
    
    // Error, unable to close all devices.
    
```



 

 