---
description: 您可以使用 [元件服務] 系統管理工具，以程式設計的方式設定交易的超時，也可以使用 COM + 系統管理介面以程式設計的方式設定時間。
ms.assetid: f7a35bdf-ea6d-40ea-b3c0-c2a3ae2276c4
title: 設定交易 Time-Out
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b002448ca21e97e2e4996679d87a4b6a7680161f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468477"
---
# <a name="setting-the-transaction-time-out"></a>設定交易 Time-Out

您可以使用 [元件服務] 系統管理工具，以程式設計的方式設定交易的超時，也可以使用 [Com + 系統管理介面](com--administration-interfaces.md)以程式設計的方式設定時間。 您可以在本機電腦層級以及個別元件上設定超時時間。

**若要使用元件服務系統管理工具來設定本機電腦的交易超時**

1.  在主控台樹中，以滑鼠 **按右鍵您** 要設定的本機電腦，然後按一下 [內容]。

2.  在 [電腦屬性] 對話方塊中，按一下 [ **選項** ] 索引標籤。

3.  在 [ **交易超時**] 下，輸入交易超時（以秒為單位）。 預設的超時時間為60秒。

4.  按一下 [確定]  。

**使用元件服務系統管理工具設定元件的交易超時**

1.  在主控台樹中，以滑鼠 **按右鍵您** 要設定的元件，然後按一下 [內容]。

2.  在 [元件屬性] 對話方塊中，按一下 [ **交易** ] 索引標籤。

3.  核取標示為 [覆 **寫全域交易超時值**] 的方塊。

    > [!Note]  
    > 如果 **交易支援** 設定為 [ **已停用**]、[ **不支援**] 或 [ **受支援**]，您就無法選取方塊來覆寫全域交易超時值。

     

4.  在 [ **交易超時**] 下，輸入交易超時（以秒為單位）。 預設的超時時間為0秒，這表示元件永遠不會造成交易超時。

5.  按一下 [確定]  。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[管理 COM + 中的自動交易](managing-automatic-transactions-in-com-.md)
</dt> </dl>

 

 



