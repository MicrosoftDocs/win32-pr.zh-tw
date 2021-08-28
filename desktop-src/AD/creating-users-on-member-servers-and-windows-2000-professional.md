---
title: 在成員伺服器和 Windows 2000 Professional 上建立使用者
description: 本主題說明用來在成員伺服器上建立使用者的步驟，或執行 Windows 2000 Professional 的電腦。
ms.assetid: 714a36d4-3407-426f-b4e9-27ec399f742a
ms.tgt_platform: multiple
keywords:
- 在成員伺服器和 Windows 2000 Professional AD 上建立使用者
- 使用者 AD、在成員伺服器上建立使用者，以及 Windows 2000 Professional
- Active Directory、使用、使用者、在成員伺服器上建立使用者，以及 Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 21490302b025e20f836cbbc957d0f86824b3456d
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881579"
---
# <a name="creating-users-on-member-servers-and-windows-2000-professional"></a>在成員伺服器和 Windows 2000 Professional 上建立使用者

**建立使用者**

1.  使用下列規則系結至電腦：
    1.  使用具有足夠許可權的帳戶來存取該電腦。
    2.  使用 WinNT 提供者、電腦名稱稱和額外的參數，來使用下列系結字串格式，以告訴 ADSI 系結至電腦： "WinNT:// <computer name> ， &lt; computer &gt; "。 「 &lt; 電腦名稱稱」 &gt; 電腦是您想要存取其群組的電腦名稱稱。 此參數會指示 ADSI 系結至電腦，並允許 WinNT 提供者的剖析器略過一些不明確的解析查詢，以判斷您要系結到的物件類型。
    3.  系結至 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 介面。
2.  使用 [**IADsContainer**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) 來指定 "user" 作為類別，以新增使用者。
3.  使用 IADs 將使用者寫入電腦的安全性資料庫 [**。 SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo)。

 

 
