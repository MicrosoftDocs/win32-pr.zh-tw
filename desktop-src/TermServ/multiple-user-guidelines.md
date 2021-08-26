---
title: 多使用者指導方針
description: 在遠端桌面服務環境中為多個使用者開發應用程式的指導方針。
ms.assetid: c7acbedb-3bf2-4519-ab11-a50bf071e757
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5bc598042530ab59c0c8932522185ce5a9d0d3dce04cabce44239c3c81b79d59
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119988848"
---
# <a name="multiple-user-guidelines"></a>多使用者指導方針

下列各節提供在遠端桌面服務環境中為多個使用者開發應用程式的指導方針。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[應用程式設定](application-setup-in-a-terminal-services-environment.md)
</dt> <dd>

針對單一使用者安裝應用程式，可能會在多使用者遠端桌面服務環境中產生問題。

</dd> <dt>

[儲存使用者特定資訊](storing-user-specific-information.md)
</dt> <dd>

應用程式應在使用者特定位置中 儲存使用者專屬資訊 ，藉此與套用到所有使用者的全域資訊區隔。

</dd> <dt>

[核心物件命名空間](kernel-object-namespaces.md)
</dt> <dd>

遠端桌面服務針對核心物件使用多個命名空間;全域命名空間主要是由用戶端/伺服器應用程式中的服務所使用。

</dd> <dt>

[IP 位址和電腦名稱稱](ip-addresses-and-computer-names.md)
</dt> <dd>

假設指派給電腦的電腦名稱或 IP 位址 與單一使用者相關聯並不安全，因為多個使用者可以同時登入遠端桌面工作階段主機 (RD 工作階段主機) 伺服器。

</dd> </dl>

像往常一樣，在進行變更時鎖定檔案和資料庫，以防止意外遺失資料。

您的應用程式不能鎖定不是每個使用者檔案的任何執行時間應用程式檔。 鎖定的執行時間檔案可以保留應用程式的多個實例，或應用程式（例如，嚮導）下的進程執行。 測試哪些檔案是執行時間應用程式檔的好方法，就是追蹤應用程式安裝程式所安裝的檔案。 安裝程式很少會安裝每個使用者的檔案;因此，安裝程式安裝的大部分檔案都是執行時間的應用程式檔。

 

 




