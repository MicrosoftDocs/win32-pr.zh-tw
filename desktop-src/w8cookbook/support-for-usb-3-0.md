---
title: USB 3.0 的支援
description: USB 3.0 的支援
ms.assetid: AACE4B57-A03F-40C7-AFDD-514D29F24521
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c2f6fa342efa5e7b4fd95287a2061482fa0cbb9
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "103683222"
---
# <a name="support-for-usb-30"></a>USB 3.0 的支援

## <a name="platforms"></a>平台

**用戶端** – Windows 8  
**伺服器** – Windows Server 2012  


## <a name="description"></a>Description

在 Windows 8 和 Windows Server 2012 中，我們新增了 USB 3.0 的支援。 做法是新增軟體堆疊，以增強 USB 3.0 主機控制器的電源，稱為可延伸的主機控制器 (XHC) 。 我們維護了介面同位、IRQL 層級、呼叫端內容、錯誤狀態、重試頻率等等。 當您與透過 USB 2.0 或 USB 3.0 連接的裝置進行互動時，不會有任何差異。

但是，如果您要為新的 USB 3.0 裝置撰寫驅動程式，絕對可以選擇新的 USB 3.0 功能。

## <a name="manifestation"></a>表現

整體 USB 裝置從電腦取用裝置傳輸的速度較快，且耗電量較低。 連線到 USB 3.0 埠時，現有的 USB 裝置可能無法正常運作。 這應該不會發生，而且不是預期的，但因為支援 USB 3.0 的軟體是新的，所以這是一項風險。

 

 




