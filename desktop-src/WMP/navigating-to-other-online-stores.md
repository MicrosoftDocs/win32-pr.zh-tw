---
title: 流覽至其他線上商店
description: 流覽至其他線上商店
ms.assetid: e88164ef-0f8e-4c54-be34-422662796c63
keywords:
- Windows Media Player 線上商店，導覽
- 線上商店，導覽
- 輸入2個線上商店，導覽
- 流覽類型2線上商店
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff1b2cb120ac161fd92bf8d35826b9dc096c95c37d916f19eb2aeb7362aabe7e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118574431"
---
# <a name="navigating-to-other-online-stores"></a>流覽至其他線上商店

您可以建立您所擁有之其他線上商店的連結，或與其他人所提供的線上商店連結。 若要這樣做，您需要知道您想要流覽的線上商店的金鑰名稱。

下列範例程式碼顯示的 HTML 會建立一個連結，以從 Proseware online store 切換至 Southridge Video online store 的 "ServiceTask2" 功能：


```C++
<A HREF = 
"javascript:window.external.NavigateTaskPaneURL('SouthridgeVideo', 'ServiceTask2', 'From=Proseware&To=2')"
>Switch to Southridge Video</A>

```



當使用者按一下連結時，Windows Media Player 會提示使用者切換至 Southridge 影片存放區。 如果使用者允許，則玩家會切換儲存並流覽至指定的工作窗格，並附加查詢字串參數。 上述範例中所示的查詢字串參數是自訂參數。 這表示您切換的線上商店必須預期這些值並加以處理。 無論您選擇哪一種方式，您的線上商店 (以及切換至) 的任何存放區都可以使用查詢字串參數。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**在服務工作窗格之間流覽**](navigating-between-service-task-panes.md)
</dt> <dt>

[**類型2線上商店的流覽**](navigation-for-type-2-online-stores.md)
</dt> </dl>

 

 




