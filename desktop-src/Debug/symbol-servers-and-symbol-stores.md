---
description: 正確設定要進行偵錯工具的符號可能是一項具挑戰性的工作，尤其是針對內核偵錯工具。
ms.assetid: 96b2c9db-58fb-4c28-b17c-3b1cc06ed96b
title: "  符號伺服器和符號存放區"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 644410fcb929308a259c5fc752f55742bfb23bae
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104187672"
---
# <a name="symbol-server-and-symbol-stores"></a>  符號伺服器和符號存放區

正確設定要進行偵錯工具的符號可能是一項具挑戰性的工作，尤其是針對內核偵錯工具。 它通常會要求您知道電腦上所有產品的名稱和版本。 偵錯工具必須能夠找出對應于每個產品版本和 service pack 的符號檔。 這可能會產生非常長的符號路徑，其中包含長清單的目錄。

若要簡化協調符號檔的這些問題，請使用 *符號伺服器*。 符號伺服器可讓偵錯工具自動取得正確的符號檔，而不包含產品名稱、版本或組建編號。 適用于 Windows 的偵錯工具包含 SymSrv 符號伺服器。

符號伺服器的啟用方式是在符號路徑中包含特定文字字串。 每次偵錯工具需要載入新載入模組的符號時，就會呼叫符號伺服器以找出適當的符號檔。 符號伺服器會在 *符號存放區* 中尋找檔案。 這是符號檔、索引和工具的集合，可供系統管理員用來新增及刪除檔案。 這些檔案會根據唯一的參數（例如時間戳記和影像大小）進行索引。 適用于 Windows 的偵錯工具包含名為 SymStore 的符號存放區工具。

如需詳細資訊，請參閱

-   [使用 SymSrv](using-symsrv.md)
-   [使用 SymStore](using-symstore.md)
-   [使用其他符號存放區](using-other-symbol-stores.md)
-   [SymStore Command-Line 選項](symstore-command-line-options.md)
-   [符號伺服器和網際網路防火牆](symbol-servers-and-internet-firewalls.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[符號檔](symbol-files.md)
</dt> </dl>

 

 



