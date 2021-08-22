---
description: 您可以使用 [元件服務] 系統管理工具手動設定交易屬性，也可以在撰寫元件時加入程式設計的交易支援。
ms.assetid: b0d701c7-47ef-4034-873f-dd4428efb4c7
title: 設定交易屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: de6310d2544090d4b551a93782b4756b3d89f2d6d365dfc09aec4658d5d3e1b4
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118546215"
---
# <a name="setting-the-transaction-attribute"></a>設定交易屬性

您可以使用 [元件服務] 系統管理工具手動設定交易屬性，也可以在撰寫元件時加入程式設計的交易支援。

如需交易屬性值的詳細資訊，請參閱設定 [交易](configuring-transactions.md)。

**使用元件服務系統管理工具來設定屬性值**

1.  在主控台樹中，以滑鼠 **按右鍵您** 要設定的元件，然後按一下 [內容]。

2.  在 [元件屬性] 對話方塊中，按一下 [ **交易** ] 索引標籤。

3.  在 [ **交易支援**] 下，選取您要的值選項。 **不支援** 所有元件的預設值。

4.  按一下 [確定]。

您必須為每個元件重複此程式。

## <a name="to-set-the-attribute-value-programmatically"></a>以程式設計方式設定屬性值

使用 Microsoft Visual Basic 的程式設計人員可以使用 **MTSTransactionMode**（ActiveX DLL 專案的類別模組屬性）來設定 transaction 屬性。 Visual Basic 將您的選取專案對應至相等的 com + 交易屬性值，並在元件的類型程式庫中發佈此值。

下表會將每個 **MTSTransactionMode** 常數值對應至其相等的 com + 交易值。



| MTSTransactionMode 常數         | COM + 交易值             |
|-------------------------------------|------------------------------------|
| NotAnMTSObject (預設) <br/> | 停用<br/>                |
| NoTransactions<br/>           |  (預設) 不支援<br/> |
| RequiresTransaction <br/>     | 必要<br/>                |
| UsesTransaction <br/>         | 支援<br/>               |
| RequiresNewTransaction <br/>  | 必須是新交易<br/>            |



 

您也可以使用 COM + 系統管理程式庫 API，以程式設計方式存取 **MTSTransactionMode** 屬性。

 

 




