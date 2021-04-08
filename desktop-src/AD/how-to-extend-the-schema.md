---
title: 如何延伸架構
description: 當現有的類別及/或屬性不符合您想要儲存的資料類型時，您可能會想要擴充架構。
ms.assetid: 9a80ce29-8ff0-4324-8a2f-afd6c5d2272e
ms.tgt_platform: multiple
keywords:
- 架構 AD，如何擴充
- Active Directory，使用架構
- Active Directory，使用、架構、延伸架構、如何擴充
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 437b23229182e6ec6f94b500feb764b4bbcf06e7
ms.sourcegitcommit: 803f3ccd65bdefe36bd851b9c6e7280be9489016
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/17/2020
ms.locfileid: "103681656"
---
# <a name="how-to-extend-the-schema"></a>如何延伸架構

當現有的類別及/或屬性不符合您想要儲存的資料類型時，您可能會想要擴充架構。 如需有關如何決定何時延伸架構的詳細資訊，請參閱 [擴充架構](extending-the-schema.md)。 當您決定需要架構延伸時，請使用下列程式來擴充架構。

## <a name="verify-active-directory-functionality-before-you-apply-any-schema-extensions"></a>套用任何架構延伸之前，請先確認 Active Directory 功能

請先確認 Active Directory 功能，然後再更新架構，以協助確保架構延伸模組不會發生錯誤。 至少要確定樹系的所有網域控制站都在線上，並且執行輸入複寫。

**若要在套用架構延伸之前確認 Active Directory 功能**

1.  登入已安裝 Windows 支援工具 Repadmin.exe 的系統管理工作站。
    > [!Note]  
    > 支援工具位於作業系統安裝媒體的 [支援 \\ 工具] 資料夾中。

     

2.  開啟命令提示字元，然後將目錄變更為安裝 Windows 支援工具的資料夾。
3.  在命令提示字元輸入以下命令，然後按下 ENTER：

    ``` syntax
    repadmin /replsum /bysrc /bydest /sort:delta
    ```

    所有網域控制站都應該在 [失敗] 資料行中顯示0，而最大的差異 (表示自上次) 成功複寫之後，對 Active Directory 資料庫所做的變更數目，應該小於或等於網域控制站用於複寫的站台連結的複寫頻率。 預設複寫頻率為180分鐘。

    如需在套用架構延伸之前，您可以採取以確認 Active Directory 功能之其他步驟的詳細資訊，請參閱 [Microsoft 知識庫中的文章 325379](https://support.microsoft.com/kb/325379/en-us)。

**延伸架構**

1.  決定擴充方法。 當您仔細設計架構變更之後，下一步是決定要使用哪一種方法來擴充架構。 您可以使用下列其中一種方法：
    -   使用匯入檔案手動進行。 請參閱 [使用 LDIFDE 工具](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))的檔。
        > [!Note]  
        > 請勿使用 LDIFDE 匯入 Windows .Sch \* .ldf 檔案。 需要這些檔案才能延伸 Active Directory 的架構，以便安裝執行比目前架構主機上所執行之新版 Windows Server 的網域控制站。 當您需要擴充架構以便安裝新的網域控制站時，請使用 Adprep.exe。

         

    -   以程式設計方式使用安裝程式。 如需詳細資訊，請參閱程式 [設計延伸](programmatic-extension.md)
2.  啟用架構變更。 如需詳細資訊，請參閱 [安裝架構延伸的必要條件](prerequisites-for-installing-a-schema-extension.md) ，以及 [在架構主機上啟用架構變更](enabling-schema-changes-at-the-schema-master.md)。
3.  取得新屬性和/或類別 (OID) 的物件識別碼，如 [取得物件識別碼](obtaining-an-object-identifier.md)中所述。
4.  建立新的屬性和類別。
5.  如有必要，請使用顯示規範，將新的屬性和類別與使用者介面整合。
6.  更新架構快取，如 [更新架構](updating-the-schema-cache.md)快取中所述。
7.  使用 LDP.exe 來確認架構延伸。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[取得物件識別碼](obtaining-an-object-identifier.md)
</dt> <dt>

[Windows Server 2003 中 Active Directory 的新命令列工具](https://support.microsoft.com/kb/298882)
</dt> <dt>

[使用 LDIFDE 工具](/previous-versions/office/developer/exchange-server-2003/ms870068(v=exchg.65))
</dt> <dt>

[擴充 Active Directory 架構](/previous-versions/ms806972(v=msdn.10))
</dt> <dt>

[架構延伸的限制](restrictions-on-schema-extension.md)
</dt> </dl>

 

 