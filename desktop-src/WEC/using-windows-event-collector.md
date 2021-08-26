---
title: 使用 Windows 事件收集器
description: 本節列出的主題說明可使用 Windows 事件收集器 SDK 完成的工作。 所有工作的程式碼範例和說明都包含在下列每個主題中。
ms.assetid: 3396454a-4f43-45d0-951e-3096b9a4a077
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cb8b928dddcd3e70848d510a8986962d478bedbe6f2f8bffcbec19c276983328
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120006008"
---
# <a name="using-windows-event-collector"></a>使用 Windows 事件收集器

本節列出的主題說明可使用 Windows 事件收集器 SDK 完成的工作。 所有工作的程式碼範例和說明都包含在下列每個主題中。

## <a name="in-this-section"></a>本節內容

-   [建立收集器起始的訂用帳戶](creating-an-event-collector-subscription.md)

    提供用來建立收集器起始訂用帳戶的資訊和 c + + 程式碼範例。 收集器起始的訂用帳戶可讓您在本機電腦上接收事件， (從遠端電腦轉送的事件收集器)  (事件來源) 。

-   [設定來源起始的訂用帳戶](setting-up-a-source-initiated-subscription.md)

    提供用來建立來源起始訂用帳戶的資訊和 c + + 程式碼範例。 來源起始的訂用帳戶可讓您在本機電腦上接收事件 (事件收集器) 從遠端電腦轉送 (事件來源) 而不指定訂用帳戶中的事件來源。

-   [將事件來源新增至收集器起始的訂用帳戶](adding-an-event-source-to-an-event-collector-subscription.md)

    提供資訊和 c + + 程式碼範例，以將事件來源 (本機電腦或遠端電腦) 新增至收集器起始的訂用帳戶。 收集器起始的訂用帳戶無法開始收集事件，直到將事件來源新增至訂用帳戶為止。

-   [建立硬體事件訂閱](creating-hardware-event-subscriptions.md)

    提供有關如何建立事件訂閱，以便從已安裝基礎板管理控制器 (BMC) 的電腦接收硬體事件的資訊。

-   [刪除事件收集器訂用帳戶](deleting-an-event-collector-subscription.md)

    提供從本機電腦刪除事件收集器訂用帳戶的資訊和 c + + 程式碼範例。

-   [顯示事件收集器訂用帳戶的屬性](displaying-the-properties-of-an-event-collector-subscription.md)

    提供資訊和 c + + 程式碼範例，以顯示事件收集器訂用帳戶的屬性值。 屬性值可提供有用的資訊，例如事件來源的位址、訂用帳戶和事件來源的狀態，以及事件傳遞方式的相關資訊。

-   [顯示事件收集器訂用帳戶的狀態](displaying-the-status-of-an-event-collector-subscription.md)

    提供資訊和 c + + 程式碼範例，以顯示與事件收集器訂用帳戶相關聯之事件來源的執行時間狀態。 這可讓您查看有助於解決問題的錯誤訊息，以防止事件來源轉送事件。

-   [列出事件收集器訂閱](listing-event-collector-subscriptions.md)

    提供資訊和 c + + 程式碼範例，以列出存在於本機電腦上的訂閱。 您可以使用以此範例取得的訂用帳戶名稱來刪除訂用帳戶、將事件來源新增至訂用帳戶、取出訂用帳戶的屬性，或查看訂用帳戶的狀態。

-   [從收集器起始的訂用帳戶中移除事件來源](removing-an-event-source-from-an-event-collector-subscription.md)

    提供資訊和 c + + 程式碼範例，以從收集器起始的訂用帳戶中移除事件來源。 您可以從收集器起始的訂用帳戶中移除事件來源，而不需要停用訂用帳戶。

-   [重試事件收集器訂用帳戶](retrying-an-event-collector-subscription.md)

    提供資訊和 c + + 程式碼範例，以在一或多個事件來源失敗時重試事件收集器訂用帳戶。 您可以重試單一事件來源，也可以重試整個訂用帳戶。

 

 




