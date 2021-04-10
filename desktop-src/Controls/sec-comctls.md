---
title: Microsoft Windows 控制項安全性考慮
description: 本主題提供與 Windows 控制項相關之安全性考慮的資訊。
ms.assetid: d5396fa1-452e-40e1-beaf-ae04690048f1
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e29ba986ddd1db980134f428c8abf152321617ef
ms.sourcegitcommit: 773fa6257ead6c74154ad3cf46d21e49adc900aa
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/09/2020
ms.locfileid: "104093459"
---
# <a name="security-considerations-microsoft-windows-controls"></a>安全性考慮： Microsoft Windows 控制項

本主題提供與 Windows 控制項相關之安全性考慮的資訊。 本主題中的資訊並不提供您需要瞭解的安全性問題，請使用它作為此技術領域的起點和參考。

電腦之間的互連能力很常見;開發人員的主要考慮必須是應用程式安全性。 下列各節將討論在撰寫 Windows 控制項的程式設計時應考慮的一些潛在安全性問題。

-   [以 Null 終止的控制訊息](#null-terminated-control-messages)
-   [字串使用](#string-use)
-   [輸入驗證](#input-validation)
-   [密碼使用](#password-use)
-   [安全性警示](#security-alerts)
-   [相關主題](#related-topics)

## <a name="null-terminated-control-messages"></a>以 Null 終止的控制訊息

許多控制訊息和宏都有字串參數。 這些訊息通常不會驗證輸入字串，尤其是它們不會檢查是否有終止 `'\0'` 。 當您呼叫使用字串作為參數的訊息時，請明確指定字串為以 null 結束。

## <a name="string-use"></a>字串使用

當您編寫 Windows 控制項的程式時，必須操作字串。 幾乎每個控制項都需要插入文字。 例如，若要填入清單方塊，您必須將字串載入控制項。 因為使用字串不正確通常會造成緩衝區溢位，請採取預防措施以避免此安全性風險。

For more information about buffer overruns, see *Writing Secure Code* by Michael Howard and David LeBlanc, Microsoft Press, 2002 and [Best Practices for the Security APIs](/windows/desktop/SecBP/best-practices-for-the-security-apis).

## <a name="input-validation"></a>輸入驗證

下列控制訊息可能會出現安全性問題。

-   [**CB \_ GETLBTEXT**](cb-getlbtext.md)
-   [**LVM \_ GETISEARCHSTRING**](lvm-getisearchstring.md)
-   [**SB \_ GETTEXT**](sb-gettext.md)
-   [**SB \_ GETTIPTEXT**](sb-gettiptext.md)
-   [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)
-   [**TTM \_ GETTEXT**](ttm-gettext.md)
-   [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md)

如果文字在呼叫之間變更，以取得文字長度以及文字顯示或使用的時間，則可能會發生緩衝區溢位。 若要避免這種情況，您必須在使用之前先驗證字串。 此外，抓取文字、 [**CB \_ GETLBTEXT**](cb-getlbtext.md)、 [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)和 [**TTM \_ GETTEXT**](ttm-gettext.md)的訊息沒有任何緩衝區大小參數，可呈現緩衝區溢位的可能性。

當您使用 [**cb \_ GETLBTEXT**](cb-getlbtext.md) 或 [**sb \_ GETTEXT**](sb-gettext.md)時，您應該先呼叫 [**CB \_ GETLBTEXTLEN**](cb-getlbtextlen.md) 或 [**sb \_ GETTEXTLENGTH**](sb-gettextlength.md) 來取得緩衝區大小。 其中有些訊息、 [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)、 [**LVM \_ GETISEARCHSTRING**](lvm-getisearchstring.md)和 [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md)可以使用 **Null** 參數值來呼叫，以取得字串的長度，然後再叫用訊息來取得字串。

您應該特別注意的訊息是狀態列 [**SB \_ GETTIPTEXT**](sb-gettiptext.md) 訊息。 此訊息不會提供任何方法來查詢要抓取之字串的長度。

## <a name="password-use"></a>密碼使用

如果您使用密碼保護的編輯控制項 ([**ES \_ 密碼**](edit-control-styles.md) 樣式) ，包含所抓取文字的緩衝區必須儘快設定為零，以避免在記憶體中公開使用者的密碼。

## <a name="security-alerts"></a>安全性警示

下表列出如果使用不當，可能會危及應用程式安全性的功能。 此處所列的訊息不會提供指定緩衝區大小的參數。



| 功能                                               | 降低                                                                                                                                              |
|-------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**DlgDirListComboBox**](/windows/desktop/api/Winuser/nf-winuser-dlgdirlistcomboboxa)      | 請確定函式所使用的緩衝區可以寫入，而且是以 null 結束。                                                                     |
| [**CB \_ GETLBTEXT**](cb-getlbtext.md)                 | 呼叫 [**cb \_ GETLBTEXTLEN**](cb-getlbtextlen.md) 以取得緩衝區大小，然後呼叫 [**cb \_ GETLBTEXT**](cb-getlbtext.md) 來取出字串。 |
| [**LVM \_ GETISEARCHSTRING**](lvm-getisearchstring.md) | 呼叫具有 **Null** 參數值的訊息，以取得緩衝區大小，然後再次呼叫訊息以取得字串。             |
| [**SB \_ GETTEXT**](sb-gettext.md)                     | 呼叫 [**sb \_ GETTEXTLENGTH**](sb-gettextlength.md) 來取得緩衝區大小，然後呼叫 [**sb \_ GETTEXT**](sb-gettext.md) 來取出字串。   |
| [**TB \_ GETBUTTONTEXT**](tb-getbuttontext.md)         | 呼叫具有 **Null** 參數值的訊息，以取得緩衝區大小，然後再次呼叫訊息以取得字串。             |
| [**TTM \_ GETTEXT**](ttm-gettext.md)                   | 此訊息不會提供您知道或指定緩衝區大小的方法。                                                                  |
| [**TVM \_ GETISEARCHSTRING**](tvm-getisearchstring.md) | 傳遞 **Null** 參數值以取得緩衝區大小，然後再次呼叫訊息以取得字串，藉以呼叫訊息。       |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

**其他資源**
</dt> <dt>

[Microsoft 安全性](https://www.microsoft.com/security/default.aspx)
</dt> <dt>

[安全性](/windows/desktop/security)
</dt> <dt>

[TechNet 安全性資源](https://www.microsoft.com/technet/security/Bulletin/MS10-059.mspx)
</dt> <dt>

[安全性 Api 的最佳作法](/windows/desktop/SecBP/best-practices-for-the-security-apis)
</dt> </dl>

 

 