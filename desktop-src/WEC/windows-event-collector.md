---
title: Windows 事件收集器
description: 您可以在本機電腦上訂閱接收和儲存事件 (事件收集器) 從遠端電腦轉送 (事件來源) 。
ms.assetid: 7725e06d-4df1-4b3e-9f2f-2b8bdd805cb6
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c4ef9e0cb647236daa55771222f25b7e0e370ef
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106999588"
---
# <a name="windows-event-collector"></a>Windows 事件收集器

您可以在本機電腦上訂閱接收和儲存事件 (事件收集器) 從遠端電腦轉送 (事件來源) 。 [Windows 事件收集器函數](windows-event-collector-functions.md)支援使用 WS-Management 通訊協定來訂閱事件。 如需 WS-MANAGEMENT 的詳細資訊，請參閱 [關於 Windows 遠端管理](/windows/desktop/WinRM/about-windows-remote-management)。

## <a name="event-forwarding-and-event-collection-architecture"></a>事件轉送和事件集合架構

事件收集可讓系統管理員從遠端電腦取得事件，並將它們儲存在收集器電腦上的本機事件記錄檔中。 事件的目的地記錄檔路徑是訂用帳戶的屬性。 轉寄事件中的所有資料都會儲存在收集器電腦事件記錄檔中， (不會遺失任何資訊) 。 事件轉送的其他相關資訊也會新增至事件。 如需如何讓電腦接收收集到的事件或轉寄事件的詳細資訊，請參閱 [設定電腦以轉送和收集](/previous-versions/windows/it-pro/windows-server-2008-R2-and-2008/cc748890(v=ws.11))事件。

## <a name="subscriptions"></a>訂用帳戶

下列清單描述事件訂閱的類型：

-   來源起始的訂用帳戶：可讓您在事件收集器電腦上定義事件訂閱，而不需要定義事件來源電腦。 然後，您可以使用群組原則設定) 將事件轉寄至事件收集器電腦，來設定多個遠端事件來源電腦 (。 如需詳細資訊，請參閱 [設定來源起始的訂用](setting-up-a-source-initiated-subscription.md)帳戶。 當您不知道或不想要指定將轉寄事件的所有事件來源電腦時，此訂閱類型會很有用。
-   收集器起始的訂閱：如果您知道將轉寄事件的所有事件來源電腦，可讓您建立事件訂閱。 您可以在建立訂閱時指定所有事件來源。 如需詳細資訊，請參閱 [建立收集器起始的訂用](creating-an-event-collector-subscription.md)帳戶。

## <a name="windows-event-collector-functions"></a>Windows 事件收集器函式

如需使用事件收集器函式的詳細資訊和程式碼範例，請參閱 [使用 Windows 事件收集器](using-windows-event-collector.md)。

如需用來收集和轉送事件之函式的詳細資訊，請參閱 [Windows 事件收集器](windows-event-collector-functions.md)函式。

 

 