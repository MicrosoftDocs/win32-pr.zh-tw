---
title: 無伺服器系結和 RootDSE
description: 可能的話，請勿將伺服器名稱硬式編碼。
ms.assetid: 24cfd8ce-18e6-42f1-8bc5-2c6dee82d133
ms.tgt_platform: multiple
keywords:
- 無伺服器系結和 RootDSE AD
- 無伺服器系結廣告
- RootDSE AD
- Active Directory、Using、Binding、無伺服器系結
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 96a2b567ebfae52a316dce59c3bc6ab442780e61
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881223"
---
# <a name="serverless-binding-and-rootdse"></a>無伺服器系結和 RootDSE

可能的話，請勿將伺服器名稱硬式編碼。 此外，在大部分情況下，系結不應與單一伺服器不必要地系結。 Active Directory Domain Services 支援無伺服器系結，這表示 Active Directory 可以在預設網域上系結，而不需要指定網域控制站的名稱。 若為一般應用程式，這通常是已登入使用者的網域。 針對服務應用程式，這是服務登入帳戶的網域，或是服務所模擬之用戶端的網域。

在 LDAP 3.0 中，會將 rootDSE 定義為目錄伺服器上目錄資料樹狀結構的根目錄。 RootDSE 不是任何命名空間的一部分。 RootDSE 的目的是要提供目錄伺服器的相關資料。 以下是用來系結至 rootDSE 的系結字串。


```C++
LDAP://<servername>/rootDSE
```



&lt;Servername &gt; 是伺服器的 DNS 名稱。 &lt;Servername &gt; 是選擇性的，如下列格式所示。


```C++
LDAP://rootDSE
```



在此情況下，將會使用來自網域的預設網域控制站，而呼叫執行緒的安全性內容將會使用。 如果無法在網站記憶體取網域控制站，則會使用可找到的第一個網域控制站。

RootDSE 是每個目錄伺服器上已知且可靠的位置，可取得網域、架構和設定容器的辨別名稱，以及伺服器的其他相關資料以及其目錄資料樹狀結構的內容。 這些屬性在特定伺服器上很少變更。 應用程式可以在啟動時讀取這些屬性，並在整個會話中使用它們。

總而言之，應用程式應該使用無伺服器系結來系結至目前網域上的目錄、使用 rootDSE 取得命名空間的辨別名稱，以及使用該辨別名稱系結至命名空間中的物件。

如需 rootDSE 所支援之屬性的詳細資訊，請參閱 Active Directory 架構檔中的 [rootdse](/windows/desktop/ADSchema/rootdse) 。

如需詳細資訊和示範如何使用無伺服器系結和 rootDSE 的程式碼範例，請參閱 [取得網域辨別名稱的範例程式碼](example-code-for-getting-the-distinguished-name-of-the-domain.md)。

 

 
