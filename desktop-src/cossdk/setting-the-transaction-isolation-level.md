---
description: 您可以使用 [元件服務] 系統管理工具手動設定元件的交易隔離等級，也可以使用 COM + 系統管理介面，以程式設計的方式設定元件的交易隔離等級。
ms.assetid: 3ef5b805-334d-4803-be67-00c9e35cdcc6
title: 設定交易隔離等級
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 08b0447af2591c4f4b3e8e76c017157c02908367
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103689099"
---
# <a name="setting-the-transaction-isolation-level"></a>設定交易隔離等級

您可以使用 [元件服務] 系統管理工具手動設定元件的交易隔離等級，也可以使用 [Com + 系統管理介面](com--administration-interfaces.md)，以程式設計的方式設定元件的交易隔離等級。

如需交易隔離等級的詳細資訊，請參閱設定 [交易隔離等級](configuring-transaction-isolation-levels.md)。

**使用元件服務系統管理工具設定交易隔離等級**

1.  在主控台樹中，以滑鼠 **按右鍵您** 要設定的元件，然後按一下 [內容]。

2.  在 [元件屬性] 對話方塊中，按一下 [ **交易** ] 索引標籤。

3.  在 [ **交易隔離等級**] 下，從下拉式方塊中選取您想要的值。 所有元件的預設值都已 **序列化**。

    > [!Note]  
    > 如果選取 [**交易支援**] 下的 [**停用**] 或 [**不支援**]，您就無法設定交易隔離等級。

     

4.  按一下 [確定]  。

您必須為每個元件重複此程式。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[設定交易隔離等級](configuring-transaction-isolation-levels.md)
</dt> </dl>

 

 



