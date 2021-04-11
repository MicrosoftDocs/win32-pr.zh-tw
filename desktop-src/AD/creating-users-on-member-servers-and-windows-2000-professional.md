---
title: 在成員伺服器與 Windows 2000 Professional 上建立使用者
description: 本主題說明在成員伺服器或執行 Windows 2000 Professional 的電腦上建立使用者時所使用的步驟。
ms.assetid: 714a36d4-3407-426f-b4e9-27ec399f742a
ms.tgt_platform: multiple
keywords:
- 在成員伺服器與 Windows 2000 Professional AD 上建立使用者
- 使用者廣告，在成員伺服器和 Windows 2000 Professional 上建立使用者
- Active Directory、使用、使用者、在成員伺服器與 Windows 2000 Professional 上建立使用者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3050c9e8ecf68465097f2c185d2d31e0195c25a6
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "104023264"
---
# <a name="creating-users-on-member-servers-and-windows-2000-professional"></a>在成員伺服器與 Windows 2000 Professional 上建立使用者

**建立使用者**

1.  使用下列規則系結至電腦：
    1.  使用具有足夠許可權的帳戶來存取該電腦。
    2.  使用 WinNT 提供者、電腦名稱稱和額外的參數，來使用下列系結字串格式，以告訴 ADSI 系結至電腦： "WinNT://" <computer name> <computer> 。 「 &lt; 電腦名稱稱」 &gt; 電腦是您想要存取其群組的電腦名稱稱。 此參數會指示 ADSI 系結至電腦，並允許 WinNT 提供者的剖析器略過一些不明確的解析查詢，以判斷您要系結到的物件類型。
    3.  系結至 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 介面。
2.  使用 [**IADsContainer**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) 來指定 "user" 作為類別，以新增使用者。
3.  使用 IADs 將使用者寫入電腦的安全性資料庫 [**。 SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo)。

 

 