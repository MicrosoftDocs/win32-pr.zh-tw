---
description: COM + 事件服務會使用事件類別物件來管理「發行者」與「訂閱者」之間的連接。
ms.assetid: 877c5890-588d-4978-8fb2-b4ecf4134068
title: COM + 事件類別物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aae397f647354ac24395fa073365160829a687a2
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936260"
---
# <a name="the-com-event-class-object"></a>COM + 事件類別物件

COM + 事件服務會使用 *事件類別物件* 來管理「發行者」與「訂閱者」之間的連接。 事件類別物件是由 COM + 事件系統管理和儲存的 COM + 元件，其中包含發行者用來引發事件的介面和方法。 它是一個持續性物件，指出可能發生的事件，並選擇性地識別發行者。 您可以藉由提供類型程式庫，指定要讓事件類別包含的介面和方法。

為了引發事件，發行者會藉由呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 或 Microsoft Visual Basic **CreateObject** 方法來具現化事件類別物件，並要求傳回事件介面。 具現化事件類別物件包含事件系統執行所要求介面的程式。 有興趣的訂閱者也必須執行事件類別介面，以便從指定的發行者接收事件。 當事件類別物件具現化時，事件系統會將它與適當的訂閱者產生關聯。 訂閱者的清單會在事件類別物件的存留期內進行維護。 事件可以依照順序或平行方式傳遞給多個訂閱者。

當您執行事件類別物件時，您應該提供可匯出 [**DllRegisterServer**](/windows/desktop/api/olectl/nf-olectl-dllregisterserver) 和 [**DllUnregisterServer**](/windows/desktop/api/olectl/nf-olectl-dllunregisterserver) 函數的自我註冊 DLL。 **DllRegisterServer** 函式會註冊 COM 類別，而 **DllUnregisterServer** 函式會取消註冊元件。 事件類別物件是以「元件服務」管理工具或使用 [**ICOMAdminCatalog：： InstallEventClass**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installeventclass) 或 [**ICOMAdminCatalog：： InstallMultipleEventClasses**](/windows/desktop/api/ComAdmin/nf-comadmin-icomadmincatalog-installmultipleeventclasses) 介面的方法，以程式設計方式儲存在 com + 目錄中。 如需註冊事件類別物件的詳細資訊，請參閱 [註冊事件類別](registering-an-event-class.md)。

由於事件類別物件是設定的元件，因此可以使用元件服務管理工具或 COM + 系統管理 SDK 函式來設定其他屬性，例如佇列、交易、安全性等等。

> [!Note]  
> COM + 事件服務會使用類型程式庫封送處理。 這會對事件類別介面施加一些限制。 例如，類型程式庫封送處理器不支援 MIDL 屬性 [**大小， \_**](/windows/desktop/Midl/size-is) 且 [**長度 \_ 為**](/windows/desktop/Midl/length-is)。

 

事件類別物件擁有決定事件發佈方式的發行集屬性，以及下列屬性：

-   **EventCLSID**。 指定元件 CLSID 的唯一識別碼。
-   **EventClassName**。 指定元件 PROGID 的唯一識別碼。
-   **類型程式庫**。 提供事件類別物件所提供的介面清單。 不需要執行類型程式庫中指定的引發介面。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 事件安全性考慮](com--events-security-considerations.md)
</dt> <dt>

[在 COM + 中篩選事件](filtering-events-in-com-.md)
</dt> <dt>

[在 COM + 中發行和傳遞事件](publishing-and-delivering-events-in-com-.md)
</dt> <dt>

[訂用帳戶](subscriptions.md)
</dt> <dt>

[使用 com + 事件與 COM + 佇列元件](using-com--events-with-com--queued-components.md)
</dt> </dl>

 

 
