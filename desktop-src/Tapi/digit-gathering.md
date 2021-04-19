---
description: 除了啟用數位監視，以及一次有一個數位的通知，應用程式也可以要求在緩衝區中收集多個數位。
ms.assetid: db83c48a-5178-40ed-90a9-e7c8e1886fe0
title: 數位收集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d5eab4185882b86a5a8e5dcb1444f39c9db2b3ba
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106987457"
---
# <a name="digit-gathering"></a>數位收集

除了啟用數位監視，以及一次有一個數位的通知，應用程式也可以要求在緩衝區中收集多個數位。 只有當緩衝區已滿或符合某些其他終止條件時，應用程式才會收到通知。 數位收集適用于信用卡號碼集合之類的功能。 它會在應用程式呼叫 [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)時執行，並指定緩衝區以數位填滿。 當下列其中一個條件成立時，就會終止數位收集：

-   已收集要求的數位數目。
-   偵測到多個終止數位的其中一個。 終止數位會指定為 [**lineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)，而且終止數位也會放在緩衝區中。
-   兩個超時的其中一個過期。 Timeout 是第一個位數的 timeout，指定必須收集第一個數位之前的最大持續時間，以及指定連續位數之間的最大持續時間長度（以位數為限）的時間長度。
-   [**LineGatherDigits**](/windows/desktop/api/Tapi/nf-tapi-linegatherdigits)會以另一組參數再次取消數位收集，以啟動新的收集要求或使用 **Null** 位數的緩衝區參數來取消。

當數位收集因任何原因而終止時，會將 [**行 \_ GATHERDIGITS**](line-gatherdigits.md) 訊息傳送至要求數位收集的應用程式。 在呼叫擁有者的所有應用程式中，只有單一數位收集要求可以在任何指定時間的時間內完成。

您可以同時在相同的呼叫上啟用數位收集和數位監視。 在這種情況下，應用程式將會收到每個偵測到之數位的 [**行 \_ MONITORDIGITS**](line-monitordigits.md) 訊息，以及 \_ 傳送回緩衝區時的個別行 GATHERDIGITS 訊息。

 

 



