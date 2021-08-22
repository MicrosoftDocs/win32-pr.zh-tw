---
description: Microsoft Message Queuing (MSMQ) 移除 Windows 2000 用戶端支援服務
ms.assetid: e29b477e-f7e9-413c-8eb9-2e764b7dd910
title: Microsoft Message Queuing (MSMQ) 移除 Windows 2000 用戶端支援服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8bdcba684faa0a25994f66cc9cd205ba22b5ed949d8dcdd3e67497484f2784ff
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119053046"
---
# <a name="microsoft-message-queuing-msmq---removal-of-windows-2000-client-support-service"></a>Microsoft Message Queuing (MSMQ) 移除 Windows 2000 用戶端支援服務

## <a name="affected-platforms"></a>受影響的平臺

**伺服器**-Windows Server 2008 R2  



## <a name="feature-impact"></a>功能影響

 **嚴重性** -高  
**頻率** -低  

## <a name="description"></a>描述

Windows 2000 用戶端支援服務是訊息佇列伺服器的選用元件，您可以在 Windows 2003 或 Windows 2008 網域控制站電腦上安裝此元件。 這項服務可讓 Windows 2000 用戶端以網域整合模式運作，並在 Windows 2003/2008 電腦上安裝任何訊息佇列伺服器。 在 Windows XP 上運作的 MSMQ 用戶端不需要此服務。

### <a name="manifestation-of-impact"></a>影響的表現

這項變更會影響 2000 Windows 7 網域（所有網域控制站都 Windows Server 2008 R2）之間的互通性 Windows。 如果客戶升級至 Windows 7 網域，除非這些用戶端升級為較高的 Windows 版本，否則網域中任何 Windows 2000 電腦上的現有 MSMQ 應用程式將無法以網域整合模式運作。

### <a name="mitigation"></a>降低

在 Windows 7 網域上具有 Windows 2000 用戶端電腦的使用者，可以在網域中設定 Windows 2003/2008 網域控制站，並在這個網域控制站上安裝 MSMQ Windows 2000 用戶端支援服務。

### <a name="leveraging-feature-capabilities"></a>運用功能功能

具有執行 msmq Windows 2000 用戶端電腦的使用者應該升級至較高的 Windows 版本，才能利用 MSMQ 伺服器的 Active Directory 型執行。

### <a name="compatibility-performance-reliability-and-usability-testing"></a>相容性、效能、可靠性和可用性測試

Windows 2000 用戶端電腦在具有一或多個下層網域控制站的 Windows 7 網域上執行 MSMQ 的使用者，應該確認其應用程式在此混合網域上是否正常運作。

 

 



