---
title: 'RootDSE (ADSI) '
description: 每部目錄伺服器都有一個稱為 RootDSE 的唯一專案。 它會提供伺服器的相關資料，例如其功能、支援的 LDAP 版本，以及它所使用的命名內容。
ms.assetid: bb6b7676-7042-453f-83f9-b0dd2e377a13
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f241f2b8bb08248c0579c5c23d461b8c0acf1e01
ms.sourcegitcommit: b0ebdefc3dcd5c04bede94091833aa1015a2f95c
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/21/2020
ms.locfileid: "103683093"
---
# <a name="rootdse-adsi"></a>RootDSE (ADSI) 

每部目錄伺服器都有一個稱為 **RootDSE** 的唯一專案。 它會提供伺服器的相關資料，例如其功能、支援的 LDAP 版本，以及它所使用的命名內容。

例如，建立可在任何 Windows 網域環境執行的腳本或應用程式。 您可以在連接到 Active Directory 時指定辨別名稱、伺服器名稱或功能變數名稱。 如果您沒有此資訊，您可以接著使用 **RootDSE** 物件來建立連接。 下列程式碼範例會變更任何網域中的網域描述。


```VB
Set rootDSE = GetObject("LDAP://RootDSE")
Set dom = GetObject( "LDAP://" & rootDSE.Get("defaultNamingContext"))
dom.Put "description", "My domain"
dom.SetInfo
```



藉由從 **RootDSE** 取得 **defaultNamingCoNtext** 屬性，您可以系結至目前的網域，例如 fabrikam **defaultNamingCoNtext** 是 DC = Fabrikam，DC = COM。

若要列舉 **RootDSE** 的屬性，請使用 [**IADsPropertyList**](/windows/desktop/api/Iads/nn-iads-iadspropertylist) 介面。 [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject) 不能用於這項工作。

如需詳細資訊，請參閱 [無伺服器系結和 RootDSE](/windows/desktop/AD/serverless-binding-and-rootdse)。

 

 