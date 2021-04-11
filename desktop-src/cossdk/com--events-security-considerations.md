---
description: 使用 COM + 事件服務時，您可以採取一些步驟，以確保事件中包含的任何機密資訊都不會受到危害。
ms.assetid: 1f8faea0-afc2-4999-a962-d6fd10307d6c
title: COM + 事件安全性考慮
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1e8f5c7dada980046627e9b778fd56e3e2727060
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936537"
---
# <a name="com-events-security-considerations"></a>COM + 事件安全性考慮

使用 COM + 事件服務時，您可以採取一些步驟，以確保事件中包含的任何機密資訊都不會受到危害。

事件發行者應該記住，任何可以寫入至 COM + 類別目錄的合作物件都可以訂閱您的事件。 因此，如果事件類別物件中包含的資訊是機密的，您應該使用 [元件服務管理] 工具來確認與訂閱者的通訊是否已針對包含事件類別元件的應用程式進行加密。  (在 [COM + 應用程式] 屬性工作表的 [ **安全性** ] 索引標籤上，選取 [封 **包隱私權** ] 作為 [ **呼叫的驗證等級** ] 設定 ) 。此外，您也應該使用 [事件篩選器](filtering-events-in-com-.md) ，協助確保只將事件傳遞給適當的訂閱者。

事件訂閱者必須記住，有權存取您的網路並知道事件類別物件的惡意物件，可能會建立錯誤的事件。 因此，您應該使用以 [角色為基礎的安全性](role-based-security-administration.md) ，以協助確保事件類別物件之方法的呼叫端具有適當的認證，以執行您的執行所述的動作。

若要協助保護髮行者和訂閱者，請在受信任主機的私人網路中使用 COM + 事件服務，該服務是由防火牆與網際網路隔離。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[COM + 安全性](com--security.md)
</dt> <dt>

[在 COM + 中篩選事件](filtering-events-in-com-.md)
</dt> <dt>

[COM + 事件類別物件](the-com--event-class-object.md)
</dt> </dl>

 

 



