---
title: 建立本機群組
description: 只有本機群組可以針對成員伺服器和 Windows 2000 Professional 建立。
ms.assetid: 76cbac51-d8ba-4114-9951-060273be52f3
ms.tgt_platform: multiple
keywords:
- 建立本機群組 AD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 06410572e6e5897280b2a03c99b387dbf81b3cca
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881582"
---
# <a name="creating-local-groups"></a>建立本機群組

只有本機群組可以針對成員伺服器和 Windows 2000 Professional 建立。

**若要建立成員伺服器的本機群組，或執行 Windows 2000 Professional 的電腦**

1.  使用下列規則系結至電腦：
    1.  使用具有足夠許可權的帳戶來存取該電腦。
    2.  使用 WinNT 提供者、電腦名稱稱和額外的參數來使用下列系結字串格式，以指示 ADSI 系結至電腦： "WinNT:// <computer name> ， &lt; computer &gt; "。

        「 &lt; 電腦名稱稱」 &gt; 參數是要存取的電腦群組名。

        在系結字串中，" &lt; computer &gt; " 參數會指示 ADSI 系結至電腦。 ADSI 會將此資料提供給 WinNT 提供者的剖析器，讓它可以略過一些明確的解析查詢，以判斷您要系結到的物件類型。

    3.  系結至 [**IADsContainer**](/windows/desktop/api/iads/nn-iads-iadscontainer) 介面。

2.  使用 [**IADsContainer**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) 指定 "localGroup" 作為類別，以新增群組。
    > [!Note]  
    > 如果您指定 "group" 作為類別，ADSI 會使用 "localGroup"。 請勿將類別指定為 "globalGroup"。 無法在成員伺服器或執行 Windows NT 工作站/Windows 2000 Professional 的電腦上建立類別 "globalGroup" 的群組。 如果您指定 "globalGroup"， [**IADsContainer**](/windows/desktop/api/iads/nf-iads-iadscontainer-create) 就會在屬性快取中建立群組，但是 [**IADs. SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo) 不會將群組寫入安全性資料庫，而且不會傳回錯誤。

     

3.  使用 [**IADs SetInfo**](/windows/desktop/api/iads/nf-iads-iads-setinfo)將群組寫入電腦安全性性資料庫。

 

 
