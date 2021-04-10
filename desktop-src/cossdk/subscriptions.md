---
description: 訂用帳戶資料位於訂用帳戶 COM + 目錄中。 您可以使用 [元件服務] 系統管理工具或使用 ICOMAdminCatalog：： InstallComponent 介面以程式設計方式建立訂用帳戶。
ms.assetid: 190e88f3-1d87-4c27-9451-0a633cbae829
title: 訂用帳戶
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9973eb76fc22354f1a2fc8e381c90cf5be1efee3
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187707"
---
# <a name="subscriptions"></a>訂用帳戶

訂用帳戶資料位於訂用帳戶 COM + 目錄中。 您可以使用 [元件服務] 系統管理工具或使用 [**ICOMAdminCatalog：： InstallComponent**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installcomponent) 介面以程式設計方式建立訂用帳戶。

[**SubscriptionsForComponent**](subscriptionsforcomponent.md)集合是用來新增、刪除或變更訂閱的相關資訊。 **SubscriptionsForComponent** 集合是元件的子集合。 若要加入訂用帳戶，請取得元件的 **SubscriptionsForComponent** 集合，並使用 [**add**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-add) 方法將專案加入至集合。 若要設定訂用帳戶物件的各種屬性，請使用 [**Value**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogobject-get_value) 屬性。 若要儲存變更，請使用 **SubscriptionsForComponent** 集合物件上的 [**SaveChanges**](/windows/desktop/api/ComAdmin/nf-comadmin-icatalogcollection-savechanges) 。

您也可以使用「元件服務」系統管理工具來修改部分（但不是全部）的訂用帳戶屬性。 訂閱會指定下列資訊：

-   訂閱者的身分識別和位置
-   傳遞方法
-   要傳遞的事件方法
-   訂閱者想要從中接收事件之事件類別元件的事件類別物件和 PublisherID 屬性

訂閱與事件類別物件分開存在。 您可以將 [已啟用] 屬性設定為 [False]，以停用訂用帳戶。 COM + 事件不會呼叫已停用的訂用帳戶。

這三種訂用帳戶類型如下：

<dl> <dt>

<span id="Persistent"></span><span id="persistent"></span><span id="PERSISTENT"></span>持續
</dt> <dd>

持續性訂用帳戶位於 COM + 目錄中，而且與訂閱者的存留期無關。 持續性訂閱會在系統重新開機後存活。 一般而言，當應用程式安裝在訂閱者的電腦上，並在移除應用程式時移除時，就會建立持續性訂閱。 建立持續性訂閱之後，COM + 事件會在每次傳遞事件時啟動訂閱者。

當發行者具現化並在 [事件類別](the-com--event-class-object.md) 物件上進行呼叫時，物件會在 com + 目錄中尋找所有持續性的訂閱，並為每個物件建立新的實例。 建立程式可以是直接或透過已排入佇列之元件的標記。 依訂用帳戶的 [**SubscriberMoniker**](subscriptionsforcomponent.md) 屬性來指定訂閱者物件。 持續性訂用帳戶所建立的訂閱者物件一律會在每次事件呼叫之後釋放。

</dd> <dt>

<span id="Transient"></span><span id="transient"></span><span id="TRANSIENT"></span>瞬 態
</dt> <dd>

對於暫時性訂閱，您可以使用 [**TransientSubscriptions**](transientsubscriptions.md) 集合，其父物件是根目錄物件。 暫時性訂閱會要求已存在之特定訂閱者物件的事件。 暫時性訂閱會儲存在 COM + 目錄中，但如果事件系統或作業系統停止，就會刪除訂閱。 與持續性訂閱不同的是，暫時性訂閱會系結至特定的物件，而且只會儲存在事件系統中。 暫時性訂用帳戶可比持續性訂閱更有效率，但您必須管理其物件生命週期。 如需註冊暫時性訂閱的詳細資訊，請參閱 [註冊暫時性訂用](registering-a-transient-subscription.md)帳戶。

</dd> <dt>

<span id="Per_user"></span><span id="per_user"></span><span id="PER_USER"></span>每位使用者
</dt> <dd>

只有當訂閱者登入事件系統的電腦時，每個使用者訂閱才可以提供事件。 當訂閱者登入時，事件系統會啟用 *PerUser* 旗標設為 **TRUE** 的所有訂用帳戶，並將 *UserName* 設定為登入之使用者的名稱。 當訂閱者登出時，就會停用訂閱。

只有當「發行者」和「訂閱者」位於同一部電腦時，每個使用者訂閱才會生效。 只有在發行者電腦上才會偵測到登入和登出，而不是在訂閱者物件所在的電腦上偵測到。

</dd> </dl>

事件系統會在建立、修改或移除事件類別物件或訂用帳戶時，使用中繼事件來通知有興趣的訂閱者。 若要從事件系統接收中繼事件，應用程式必須建立位於事件系統電腦上的訂用帳戶，並指定引發介面識別碼 (IID \_ IEventObjectChange) 。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[在 COM + 中篩選事件](filtering-events-in-com-.md)
</dt> <dt>

[在 COM + 中發行和傳遞事件](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[COM + 事件類別物件](the-com--event-class-object.md)
</dt> <dt>

[使用 com + 事件與 COM + 佇列元件](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 



