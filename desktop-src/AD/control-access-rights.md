---
title: 控制 (AD DS) 的存取權限
description: Active Directory Domain Services 中的所有物件都支援 ADS \_ 許可權列舉列舉中所定義的一組標準存取權限 \_ 。
ms.assetid: 27ad74bd-ad87-422e-a4a2-02c0d51c4dd4
ms.tgt_platform: multiple
keywords:
- 控制存取權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c975ac20cac683e754f1b703bd272356c9b8df8f
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122881615"
---
# <a name="control-access-rights-ad-ds"></a>控制 (AD DS) 的存取權限

Active Directory Domain Services 中的所有物件都支援 [**ADS \_ 許可權 \_ 列舉**](/windows/win32/api/iads/ne-iads-ads_rights_enum) 列舉中所定義的一組標準存取權限。 這些存取權限可以在物件的安全描述項 (Ace) 的存取控制專案中使用，以控制物件的存取權;也就是說，您可以控制誰可以執行標準作業，例如建立和刪除子物件，或讀取和寫入物件屬性。 不過，對於某些物件類別，可能需要以標準存取權限不支援的方式來控制存取權。 為了達成此目的，Active Directory Domain Services 允許透過 **controlAccessRight** 物件延伸標準存取控制機制。

使用控制存取權限的方式有三種：

-   針對擴充許可權，這是標準存取權限集未涵蓋的特殊作業。 例如，使用者類別可以被授與可供 Exchange、Outlook 或任何其他郵件應用程式使用的「傳送為」許可權，以判斷特定使用者是否可以讓其他使用者代表他們傳送郵件。 在 **controlAccessRight** 物件上建立延伸許可權的方式，是將 **validAccesses** 屬性設定為等於 (256) 存取權限的 **ADS \_ 正確 \_ DS \_ 控制 \_ 存取權** 。
-   若要定義屬性集，可讓您控制對物件屬性子集的存取，而不只是個別的屬性。 使用標準存取權限時，單一 ACE 可以授與或拒絕存取所有物件的屬性或單一屬性。 控制存取權限提供單一 ACE 的方法，以控制一組屬性的存取權。 例如，使用者類別支援包含如街道位址和電話號碼等屬性的 **個人資訊** 屬性集。 在 **controlAccessRight** 物件上建立屬性集許可權的方法是設定 **validAccesses** 屬性，以同時包含 **ACTR \_ ds \_ 讀取 \_** 屬性 (16) 和 **ACTRL \_ DS \_ 寫入 \_** 屬性 (32) 存取權限。
-   針對已驗證的寫入，要求系統在將值寫入 DS 物件的屬性之前，先執行值檢查或驗證（除了架構所需的值）。 這樣可確保針對屬性輸入的值符合所需的語法、位於值的合法範圍內，或進行一些其他特殊檢查，而不會對屬性進行簡單的低層級寫入。 驗證的寫入會與「寫入屬性」許可權不同的特殊許可權相關聯 &lt; ， &gt; 該許可權會允許將任何值寫入屬性，且不會執行任何值檢查。 驗證的寫入是這三種存取權限的唯一一種，無法建立為應用程式的新控制項存取權限。 這是因為無法以程式設計方式修改現有的系統來強制執行驗證。 如果控制項存取權是在系統中設定為經過驗證的寫入，則 **controlAccessRight** 物件上的 **validAccesses** 屬性將會包含 **ADS \_ right \_ \_ SELF** (8) 存取權限。

    在 Windows 2000 Active Directory 架構中，只會定義三個已驗證的寫入：

    -   群組物件的 Self-Membership 許可權，允許從群組的成員資格新增或移除呼叫者的帳戶，而不是其他帳戶。
    -   電腦物件上已驗證的 DNS 主機名稱許可權，允許符合要設定之電腦名稱稱和功能變數名稱的 DNS 主機名稱屬性。
    -   已驗證-電腦物件的 SPN 許可權，允許符合要設定之電腦的 DNS 主機名稱的 SPN 屬性。

為了方便起見，每個存取權限都是由設定磁碟分割之 Extended-Rights 容器中的 **controlAccessRight** 物件代表，即使屬性集和驗證的寫入不會被視為擴充許可權也一樣。 由於設定容器會複寫到整個樹系中，因此控制權會傳播到樹系中的所有網域。 有許多預先定義的控制存取權限，當然也可以定義自訂存取權限。

您可以在 ACL 編輯器中，將所有控制存取權限視為許可權。

如需詳細資訊以及設定 ace 來控制屬性集之讀取/寫入存取的 c + + 和 Visual Basic 程式碼範例，請參閱[在目錄物件上設定 ace 的範例程式碼](example-code-for-setting-an-ace-on-a-directory-object.md)。

如需使用控制存取權限來控制特殊作業存取權的詳細資訊，請參閱：

-   [建立控制項存取權](creating-a-control-access-right.md)
-   [在物件的 ACL 中設定 Control 存取權限 ACE](setting-a-control-access-right-ace-in-an-objectampaposs-acl.md)
-   [在物件的 ACL 中檢查控制項存取權](checking-a-control-access-right-in-an-objectampaposs-acl.md)
-   [讀取物件 ACL 中的 Control 存取權限集合](reading-a-control-access-right-set-in-an-objectampaposs-acl.md)

 

 
