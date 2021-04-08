---
title: 列舉本機群組
description: 在執行 Windows 2000 Professional 的成員伺服器和電腦上，您可以列舉所有本機群組。
ms.assetid: edbabbe5-13e1-42f6-8e73-f8e18ba4866b
ms.tgt_platform: multiple
keywords:
- 列舉本機群組 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a6e106fc2517cfedd8fb5fa40e4b99798ee32de8
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681671"
---
# <a name="enumerating-local-groups"></a>列舉本機群組

在執行 Windows 2000 Professional 的成員伺服器和電腦上，您可以列舉所有本機群組。

只有本機群組可以在成員伺服器和 Windows 2000 Professional 上建立。 不過，這些本機群組可以包含：

-   樹系中的通用和全域群組，其中包含電腦所屬的網域。
-   來自該電腦網域的網域本機群組。
-   樹系中任何網域的使用者。

**在成員伺服器或執行 Windows 2000 Professional 的電腦上列舉本機群組**

1.  使用下列規則系結至電腦：
    1.  使用具有足夠許可權的帳戶來存取該電腦。
    2.  使用 WinNT 提供者、電腦名稱稱和額外的參數來使用下列系結字串格式，以指示 ADSI 系結至電腦： "WinNT://" <computer name> <computer> 。

        " <computer name> 參數是要存取的電腦群組名。 此參數會指示 ADSI 系結至電腦，並允許 WinNT 提供者的剖析器略過一些不明確的解析查詢，以判斷您要系結到的物件類型。

    3.  系結至 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 介面。

2.  使用 [**IADsContainer. filter**](/windows/desktop/api/iads/nn-iads-iadscontainer) 屬性設定包含 "groups" 的篩選準則。 這可讓您列舉容器，並只取得群組。
3.  使用 [**IADsContainer：： get \_ \_ NewEnum**](/windows/desktop/api/iads/nf-iads-iadscontainer-get__newenum)方法來列舉群組物件。
4.  針對每個群組物件，使用 [**IADsGroup**](/windows/desktop/api/iads/nn-iads-iadsgroup) 介面讀取群組的名稱和成員。

 

 