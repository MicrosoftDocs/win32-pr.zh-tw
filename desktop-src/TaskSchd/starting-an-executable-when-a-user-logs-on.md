---
title: 當使用者登入時啟動可執行檔
description: 藉由定義登入觸發程式和可執行檔動作，寫入在使用者登入時啟動可執行檔的工作。
ms.assetid: 0c5912aa-913d-42ce-a01b-b1359b49bb2f
keywords:
- 工作排程器範例工作排程器，登入觸發程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6ffa758546dbd08b6ccf27412f38891589cb9643
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371833"
---
# <a name="starting-an-executable-when-a-user-logs-on"></a>當使用者登入時啟動可執行檔

藉由定義登入觸發程式和可執行檔動作，寫入在使用者登入時啟動可執行檔的工作。

## <a name="logon-trigger"></a>登入觸發程式

登入觸發程式是由其開始界限啟動，但在指定的使用者登入之前，不會啟動可執行檔。 您可以指定在特定使用者登入時啟動登入觸發程式，方法是在 [**ILogonTrigger**](/windows/desktop/api/taskschd/nn-taskschd-ilogontrigger)介面的 [**UserId**](/windows/desktop/api/taskschd/nf-taskschd-ilogontrigger-get_userid)屬性中指定使用者， ([**LogonTrigger**](logontrigger.md)腳本) 。

## <a name="logontrigger-examples"></a>LogonTrigger 範例

下列範例會在使用者登入之後啟動 [記事本]。

-   [登入觸發程式範例 (腳本) ](logon-trigger-example--scripting-.md)
-   [ (c + +) 的登入觸發程式範例 ](logon-trigger-example--c---.md)
-   [ (XML) 的登入觸發程式範例 ](logon-trigger-example--xml-.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工作排程器](using-the-task-scheduler.md)
</dt> </dl>

 

 




