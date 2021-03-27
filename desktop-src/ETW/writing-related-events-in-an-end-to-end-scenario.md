---
description: ETW 提供從多個元件群組相關事件的方法。
ms.assetid: 2a85e4af-a1fe-4c28-8ce2-14d15deaa820
title: 在端對端案例中撰寫相關事件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 67d27b3455ffe71c6d657e935e6f93dc2dc39392
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972256"
---
# <a name="writing-related-events-in-an-end-to-end-scenario"></a>在端對端案例中撰寫相關事件

ETW 提供從多個元件群組相關事件的方法。 例如，如果有數個元件 (在同一部電腦或不同的電腦上) 牽涉到處理相同的資料，而且每個元件都會記錄活動部分的事件，您可以將所有相關事件群組在一起。 這可讓取用者從進程開始到進程結束時取用所有的事件。

若要在以 [資訊清單為基礎](about-event-tracing.md) 的提供者中寫入相關事件，請參閱 [在以資訊清單為基礎的提供者中撰寫相關事件](writing-related-events-in-a-manifest-base-provider.md)。

若要在 [傳統](about-event-tracing.md) 提供者中寫入相關的事件，請參閱 [在傳統提供者中撰寫相關的事件](tracing-event-instances.md)。

 

 



