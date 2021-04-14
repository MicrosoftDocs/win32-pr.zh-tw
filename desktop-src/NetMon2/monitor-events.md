---
description: 監視的設計目的是要使用 Windows Management Instrumentation (WMI) 來將事件引發至本機或遠端電腦。
ms.assetid: b20746dd-d8d9-49b6-95b7-5151ee02901d
title: 監視事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d98241081d8a59c33ab173447eaedd903e72eb09
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469160"
---
# <a name="monitor-events"></a>監視事件

監視的設計目的是要使用 [Windows Management Instrumentation](/windows/desktop/WmiSdk/wmi-start-page) (WMI) 來將事件引發至本機或遠端電腦。

> [!Note]  
> 因為監視器會使用即時捕獲，所以只能在本機電腦上捕獲資料。 這是網路封包提供者之 **IRTC** 介面的限制。 不過，藉由使用 WMI 事件，可以在本機檢查捕捉的資料，而將事件傳送到本機或遠端電腦。

 

監視器不會直接與 WMI 通訊。 [*監視器控制服務*](m.md) (MCSVC) 會提供一個稱為 [IMonitorEventer](imonitoreventer.md)) 的介面，此 (介面可讓監視用來取得事件資料結構，並將相關資訊填入其中。 然後，MCSVC 會將事件資料結構傳送至 WMI，進而引發事件。

 

 
