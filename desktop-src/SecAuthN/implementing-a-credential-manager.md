---
description: 列出必須執行才能建立認證管理員的 DLL 匯出。
ms.assetid: 8b176dd6-0e0b-4330-8889-f87384977ceb
title: 執行認證管理員
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f1a1787fcf72d88ad809f904f9f83179ac86631b83a23314f9d24ee31ce3dec9
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119482658"
---
# <a name="implementing-a-credential-manager"></a>執行認證管理員

若要建立認證管理員，您必須建立可匯出下列函式的 DLL：

-   [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify)
-   [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify)

若要將通知還原至智慧卡登入的 [**NPLogonNotify**](/windows/desktop/api/Npapi/nf-npapi-nplogonnotify) 和 [**NPPasswordChangeNotify**](/windows/desktop/api/Npapi/nf-npapi-nppasswordchangenotify) 功能，請建立名為 **SmartCardLogonNotify** 的登錄專案做為 **DWORD**，然後將它設定為1：

```
HKEY_LOCAL_MACHINE
   Software
   Microsoft
   Windows NT
   CurrentVersion
      Winlogon
         Notify
            SmartCardLogonNotify = 1
```

**Windows Server 2003 和 Windows XP：** 不需要 **SmartCardLogonNotify** 登錄專案。

此外，認證管理員也應該支援 WNNC 開始 (的 [**NPGetCaps**](/windows/desktop/api/Npapi/nf-npapi-npgetcaps) 函式， \_) 的認證管理員不需要支援其他索引。 這會告訴 MPR 何時將啟動認證管理員。 藉由呼叫 **NPGetCaps** ，並將 *nIndex* 參數設定為 WNNC \_ START，MPR 會取得呼叫提供者的認證管理進入點函式之前所等待的時間。 如果 MPR 有此資訊，它可以將它轉寄到認證管理員，設定超時時間。

 

 



