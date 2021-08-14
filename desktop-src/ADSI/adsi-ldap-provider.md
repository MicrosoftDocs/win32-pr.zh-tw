---
title: ADSI LDAP 提供者
description: ADSI LDAP 提供者會執行一組支援各種 ADSI 介面的 ADSI 物件。 若要存取 LDAP 提供者，請使用 LDAP ADsPath 系結至任何 ADSI LDAP 物件。
ms.assetid: 3c13ea2f-fe40-4fd4-8540-422f277e07c1
ms.tgt_platform: multiple
keywords:
- ADSI LDAP 提供者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2d9632f352bdfab9653de5c443d750be027c3dd74140c2a017e5d12a6dc0f673
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118180592"
---
# <a name="adsi-ldap-provider"></a>ADSI LDAP 提供者

ADSI LDAP 提供者會執行一組支援各種 ADSI 介面的 ADSI 物件。 若要存取 LDAP 提供者，請使用 LDAP ADsPath 系結至任何 ADSI LDAP 物件。

您必須在用戶端電腦上安裝 Adsldp.dll、Adsldpc.dll、Adsmsext.dll 和 Activeds.dll，才能與提供者搭配使用。

> [!Note]  
> 預設的 ADSI LDAP 提供者無法假設為完全安全線程。 多執行緒應用程式的寫入器應該透過適當的同步處理物件（例如，信號、mutex、重要區段等等）來適當地協調執行緒之間的存取。

 

 

 




