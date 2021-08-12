---
description: 在分割區中註冊和啟用元件
ms.assetid: 2cca71da-c7f7-4997-b63a-74ba266e9e95
title: 在分割區中註冊和啟用元件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cf17787c953e3fe615432a8100fa71390e8aa3b8c90453a310813207ba5df7fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118547060"
---
# <a name="registering-and-activating-components-in-partitions"></a>在分割區中註冊和啟用元件

建立分割區之後，下一個步驟是在該分割區內註冊您的 COM + 元件。 當建立新的 COM + 應用程式，或將現有的 COM + 應用程式安裝到磁碟分割時，就會在分割區內註冊元件。 為了在多個資料分割包含相同的 COM + 元件時簡化註冊管理，分割區服務可讓系統管理員將應用程式或元件從某個分割區複製到另一個分割區。 當系統複製 COM + 應用程式或元件時，除了應用程式的身分識別或角色的任何成員以外，所有相關聯的資料分割屬性都會連同該屬性一起複製。

當用戶端程式呼叫 [**CoCreateInstance**](/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance) 或 [**CoGetObject**](/windows/desktop/api/objbase/nf-objbase-cogetobject) 函式來具現化物件時，com + 會執行兩個不同的步驟，如下所示：

1.  尋找元件所在的磁碟分割
2.  在該分割區內找出正確的元件

本節中的下列主題將詳細說明這些步驟：

-   [在啟用期間尋找磁碟分割](locating-partitions-during-activation.md)
-   [找出要啟用的元件](locating-a-component-for-activation.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[應用程式設計限制](application-design-restrictions.md)
</dt> <dt>

[COM + 佇列元件和分割區](com--queued-components-and-partitions.md)
</dt> <dt>

[分割區執行](partition-implementation.md)
</dt> <dt>

[什麼是 COM + 磁碟分割？](what-are-com--partitions-.md)
</dt> </dl>

 

 
