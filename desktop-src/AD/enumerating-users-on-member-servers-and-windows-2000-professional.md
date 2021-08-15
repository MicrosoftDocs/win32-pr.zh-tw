---
title: 列舉成員伺服器上的使用者和 Windows 2000 Professional
description: 本主題說明如何列舉本機安全性資料庫中，在 Windows 2000 Professional 上執行的成員伺服器和電腦上的所有使用者。
ms.assetid: 56c20e8a-2861-4cd9-8058-271c89db7ec9
ms.tgt_platform: multiple
keywords:
- 列舉成員伺服器和 Windows 2000 Professional AD 的使用者
- 使用者廣告，列舉成員伺服器上的使用者和 Windows 2000 Professional
- Active Directory、使用、使用者、列舉成員伺服器上的使用者和 Windows 2000 Professional
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a7f72e38a00e0fcc4310f7b8498b0dda28d71231df7e65fcf2de9945f5feef2d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118694875"
---
# <a name="enumerating-users-on-member-servers-and-windows-2000-professional"></a>列舉成員伺服器上的使用者和 Windows 2000 Professional

本主題說明如何列舉本機安全性資料庫中，在 Windows 2000 Professional 上執行的成員伺服器和電腦上的所有使用者。

**列舉使用者**

1.  使用下列規則系結至電腦：
    1.  使用具有足夠許可權的帳戶來存取該電腦。
    2.  使用 WinNT 提供者、電腦名稱稱和額外的參數來使用下列系結字串格式，以指示 ADSI 系結至電腦： "WinNT://" <computer name> <computer> 。 「 &lt; 電腦名稱稱」 &gt; 參數是要存取其群組的電腦名稱稱。 此參數會指示 ADSI 系結至電腦，並讓 WinNT 提供者剖析器略過一些不明確的解析查詢，以判斷您要系結到的物件類型。
    3.  系結至 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 介面。
2.  將 "user" 新增至 [**IADsContainer. Filter**](/windows/desktop/ADSI/iadscontainer-property-methods) 屬性。 這會使列舉只包含具有 "user" 物件類別的物件。
3.  列舉物件。 針對每個使用者物件，使用 [**IADs**](/windows/desktop/api/iads/nn-iads-iads) 或 [**IADsUser**](/windows/desktop/api/iads/nn-iads-iadsuser) 介面方法來讀取使用者屬性。

 

 