---
title: WinNT 使用者物件
description: WinNT user 物件代表 Windows NT 4.0 網域中的使用者帳戶。
ms.assetid: c57016e2-538b-4f37-a1bb-699fcf3c080d
ms.tgt_platform: multiple
keywords:
- WinNT 使用者物件 ADSI
- WinNT 提供者 ADSI、user 物件
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 50a89c2c4daf0d02e1cb9a150e35702ab4f8775f6bcc993db2b0348768bb1603
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119022996"
---
# <a name="winnt-user-object"></a>WinNT 使用者物件

WinNT user 物件代表 Windows NT 4.0 網域中的使用者帳戶。 物件展示了特殊功能。 在一個實例中，它不支援 [**IADsUser**](/windows/desktop/api/Iads/nn-iads-iadsuser) 介面的所有屬性方法。 在第二個實例中，它支援一些只能使用 [**IADs**](/windows/desktop/api/Iads/nf-iads-iads-get) 或 [**IADs. Put**](/windows/desktop/api/Iads/nf-iads-iads-put) 方法存取的自訂屬性。

如需 WinNT 使用者物件的詳細資訊，請參閱：

-   [不支援的 IADsUser 屬性](unsupported-iadsuser-properties.md)
-   [WinNT 自訂使用者屬性](winnt-custom-user-properties.md)
-   [WinNT 使用者帳戶管理範例](winnt-user-account-management-examples.md)

 

 




