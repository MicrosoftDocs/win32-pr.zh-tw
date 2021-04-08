---
title: 連接到 Active Directory
description: 有數種方法可用來存取 Active Directory。
ms.assetid: ef5720ff-6c66-466c-967e-f9c72a7bc0fa
ms.tgt_platform: multiple
keywords:
- 連接至 Active Directory ADSI
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7626f01b644a0bb1a3acb39c5ef5ead70434e21e
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103931851"
---
# <a name="connecting-to-active-directory"></a>連接到 Active Directory

有數種方法可用來存取 Active Directory。 建議您使用 ADSI API 來存取 Active Directory。 ADSI 會執行 LDAP 通訊協定，以與 Active Directory 進行通訊。 下列程式碼範例示範如何存取 Active Directory。


```VB
Set ns = GetObject("LDAP:")
```



這會開啟 LDAP 提供者，並將它準備好取出資料。 在要求資料之前，不會建立連接。 當要求資料時，ADSI 在定位器服務的協助下，會嘗試找出最適合的網域控制站 (DC) 來進行連線，並建立與伺服器的連接。 此進程稱為無伺服器系結。

ADSI 也可讓您指定要用於連接的伺服器名稱。


```VB
Set obj = GetObject("LDAP://mysrv01")
```



在另一個案例中，您可能只知道功能變數名稱，但不知道特定的伺服器名稱。 同樣地，ADSI 還可讓您指定功能變數名稱。 在 Windows 2000 中，功能變數名稱會以 DNS 名稱表示。 例如，如果 Joe Worden （網路系統管理員）選擇使用功能變數名稱進行連線，他就可以使用下列程式碼範例。


```VB
Set obj = GetObject("LDAP://fabrikam.com")
```



ADSI 會連接到 fabrikam.com 網域中的其中一個網域控制站。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[系結至 Active Directory 物件](binding-to-active-directory-objects.md)
</dt> </dl>

 

 




