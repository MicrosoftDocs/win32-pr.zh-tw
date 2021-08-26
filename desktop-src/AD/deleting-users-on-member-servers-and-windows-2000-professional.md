---
title: 刪除成員伺服器上的使用者和 Windows 2000 Professional
description: 本主題說明如何從成員伺服器或 Windows 2000 Professional 上執行的電腦刪除使用者。
ms.assetid: 0c94c08b-46cb-494e-89f8-a21bfb20e34c
ms.tgt_platform: multiple
keywords:
- 使用者 AD、刪除成員伺服器上的使用者，以及 Windows 2000 Professional
- Active Directory、使用、使用者、刪除成員伺服器上的使用者和 Windows 2000 Professional
- 刪除使用者
- 伺服器，刪除使用者
- 刪除成員伺服器與 windows 2000 professional AD 上的使用者
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e366356696c1e8b11a53b45aae3860600fc6555
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881443"
---
# <a name="deleting-users-on-member-servers-and-windows-2000-professional"></a>刪除成員伺服器上的使用者和 Windows 2000 Professional

本主題說明如何從成員伺服器或 Windows 2000 Professional 上執行的電腦刪除使用者。

**刪除使用者**

1.  使用下列規則系結至電腦：
    1.  使用具有足夠許可權的帳戶來存取該電腦。
    2.  使用 WinNT 提供者、電腦名稱稱和額外的參數，來使用下列系結字串格式，以告訴 ADSI 系結至電腦： "WinNT:// <computer name> ， &lt; computer &gt; "。 「 &lt; 電腦名稱稱」 &gt; 參數是您想要存取其群組的電腦名稱稱。 此參數會通知 ADSI 它正在系結至電腦，並允許 WinNT 提供者剖析器略過一些不明確的解析查詢，以判斷您要系結到的物件類型。
    3.  系結至 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 介面。
2.  使用 [**IADsContainer**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete) 來指定 "user" 作為類別，以刪除使用者。

    請注意，您不需要呼叫 [**IADs SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) 來認可容器的變更。 [**IADsContainer**](/windows/desktop/api/iads/nf-iads-iadscontainer-delete)呼叫會認可將使用者直接刪除到目錄的動作。

 

 
