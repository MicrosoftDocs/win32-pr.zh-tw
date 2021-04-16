---
description: PhoneClose 函式會關閉指定的電話裝置。
ms.assetid: 7607d779-0715-48a3-a4f2-bcf07026d7c5
title: 關閉電話裝置
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f137004e63b4b377e9ee88266d11f9c2b21d0af7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512149"
---
# <a name="closing-the-phone-device"></a><span data-ttu-id="7be2c-103">關閉電話裝置</span><span class="sxs-lookup"><span data-stu-id="7be2c-103">Closing the Phone Device</span></span>

<span data-ttu-id="7be2c-104">[**PhoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose)函式會關閉指定的電話裝置。</span><span class="sxs-lookup"><span data-stu-id="7be2c-104">The [**phoneClose**](/windows/desktop/api/Tapi/nf-tapi-phoneclose) function closes the specified phone device.</span></span> <span data-ttu-id="7be2c-105">在使用者修改該電話的設定或其驅動程式之後，也可以強制關閉電話裝置。</span><span class="sxs-lookup"><span data-stu-id="7be2c-105">The phone device can also be forcibly closed after the user has modified the configuration of that phone or its driver.</span></span> <span data-ttu-id="7be2c-106">如果使用者想要讓設定變更立即生效 (而不是在下一次系統重新開機) 後，它們會影響應用程式目前的裝置視圖 (例如裝置功能) 的變更，則服務提供者可以強制關閉電話裝置。</span><span class="sxs-lookup"><span data-stu-id="7be2c-106">If the user wants the configuration changes to be effective immediately (as opposed to after the next system restart), and they affect the application's current view of the device (such as a change in device capabilities), then a service provider can forcibly close the phone device.</span></span>

<span data-ttu-id="7be2c-107">這些訊息也可以透過其他方式來回收電話裝置的結果來傳送。</span><span class="sxs-lookup"><span data-stu-id="7be2c-107">These messages can also be sent unsolicited as a result of the phone device being reclaimed in some other manner.</span></span> <span data-ttu-id="7be2c-108">因此，應用程式必須準備好處理未經要求的 [**電話 \_ 關閉**](phone-close.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="7be2c-108">An application should therefore be prepared to handle unsolicited [**PHONE\_CLOSE**](phone-close.md) messages.</span></span> <span data-ttu-id="7be2c-109">當手機裝置關閉時，就會隱藏與該裝置相關的任何未完成非同步回復。</span><span class="sxs-lookup"><span data-stu-id="7be2c-109">At the time the phone device is closed, any outstanding asynchronous replies pertaining to that device are suppressed.</span></span>

 

 



