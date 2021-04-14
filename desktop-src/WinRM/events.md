---
title: '事件 (Windows 遠端管理) '
description: 事件收集器服務會使用 WS-Management 的通訊協定，從遠端電腦收集事件。
ms.assetid: 5c8e0559-c576-4ac6-b636-c4a6fc399c9f
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 06f96877904a5e76ea61a6b2f636e962e4dbd9b9
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104383562"
---
# <a name="events-windows-remote-management"></a>事件 (Windows 遠端管理) 

事件收集器服務會使用 WS-Management 的通訊協定，從遠端電腦收集事件。 使用事件收集器服務時，您可以在遠端電腦上建立 Windows 事件的訂用帳戶，以及在基礎板管理控制器 (Bmc) 產生的硬體事件上建立訂閱。 Bmc 必須支援 WS-Management 的通訊協定。

當您建立訂用帳戶時，系統會將這些事件轉送至已建立訂用帳戶的電腦。 它們會出現在事件檢視器中。

智慧型平臺管理介面所產生的硬體事件 (IPMI) 在 Windows 電腦上是使用 IPMI 驅動程式在本機收集，並儲存在硬體事件記錄檔中，之後就可以像其他 Windows 作業系統事件一樣地轉送它們。

您可以使用 Wecutil.exe 命令列工具來建立訂閱。 如需如何使用此工具的詳細資訊，請在命令提示字元中輸入 **>wecutil/？**。 如需事件收集器服務的詳細資訊，請參閱 [Windows 事件收集器](/windows/desktop/WEC/windows-event-collector)。

> [!Note]  
> Windows 遠端管理 Api 要求所有 IPv6 位址都以方括弧括住。

 

> [!Caution]
>
> 使用收集器起始的訂用帳戶時，請將遠端電腦的數目限制為500，並將 [Windows 事件收集器](/windows/desktop/WEC/windows-event-collector) 服務 (wecsvc) 隔離在個別的主機進程中。
>
> 連接錯誤會保留執行緒，直到超時為止。大量的同時連線錯誤可能會導致執行緒集區耗盡，而導致伺服器沒有回應。

 

 

 
