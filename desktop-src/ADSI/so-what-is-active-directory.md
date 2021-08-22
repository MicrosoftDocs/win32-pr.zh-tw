---
title: 教學課程總覽與 Visual Basic 的 ADSI
description: Active Directory 是特殊用途的資料庫 \ 8212;它不是登錄取代。
ms.assetid: 899799e3-5ab9-4d19-883a-5bc9f20d2bad
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 44cd6afe11b8991b6ced53367582ddf11d8eba0ea428105d3e9ba39c625d54fd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119082245"
---
# <a name="tutorial-overview-adsi-with-visual-basic"></a>教學課程總覽： ADSI 與 Visual Basic

> [!Note]  
> 下列檔是 Visual Basic 開發人員擴充案例描述的一部分。 如果您要尋找 Active Directory 的一般總覽，請參閱[Technet 上的 IT Pro 檔](/previous-versions/windows/it-pro/windows-2000-server/cc977985(v=technet.10))。 若要深入瞭解 Active Directory 的開發端，請參閱 [Active Directory Domain Services](/windows/desktop/AD/active-directory-domain-services)。 如需 Active Directory 服務介面的更大介紹，請參閱本主題的父主題： [Active Directory 服務介面](active-directory-service-interfaces-adsi.md)，以及同級主題： [關於 Active Directory 服務介面](about-adsi.md)。

 

Active Directory 是特殊用途的資料庫，而不是登錄取代。 目錄的設計目的是要處理大量的讀取和搜尋作業，並大幅減少變更和更新的數目。 Active Directory 資料是階層式、複寫和可擴充的。 因為它已複寫，所以您不想要儲存動態資料，例如公司股票價格或 CPU 效能。 如果您的資料是電腦特有的，請將資料儲存在登錄中。 目錄中儲存的一般資料範例包括印表機佇列資料、使用者連絡人資料和網路/電腦設定資料。 Active Directory 資料庫是由物件和屬性所組成。 物件和屬性定義會儲存在 Active Directory 架構中。

您可能想知道哪些物件目前儲存在 Active Directory 中。 Active Directory 有三個磁碟分割。 這些也稱為命名內容：網域、架構和設定。 網域分割區包含使用者、群組、連絡人、電腦、組織單位以及許多其他物件類型。 因為 Active Directory 可延伸，所以您也可以新增自己的類別及/或屬性。 架構分割區包含類別和屬性定義。 設定磁碟分割包含服務、磁碟分割和網站的設定資料。

下列螢幕擷取畫面顯示 Active Directory 的網域分割區。

![active directory 網域分割](images/adadsi1.png)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Visual Basic 存取 Active Directory](accessing-active-directory-using-visual-basic.md)
</dt> <dt>

[案例： Fabrikam Corporation](scenario--the-fabrikam-corporation.md)
</dt> <dt>

[Advanced 主題](advanced-topics.md)
</dt> </dl>

 

 