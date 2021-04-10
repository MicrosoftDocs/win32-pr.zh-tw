---
title: 在工作註冊時啟動可執行檔
description: 在註冊工作時，撰寫啟動可執行檔的工作是藉由定義註冊觸發程式和可執行檔動作來完成。
ms.assetid: 426fa79d-7f0d-42fb-a8c4-15981d13be71
keywords:
- 工作排程器範例工作排程器、註冊觸發程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a8036b8bdff807ded582279e0ba7675bc2160811
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932327"
---
# <a name="starting-an-executable-when-a-task-is-registered"></a>在工作註冊時啟動可執行檔

在註冊工作時，撰寫啟動可執行檔的工作是藉由定義註冊觸發程式和可執行檔動作來完成。

## <a name="registration-trigger"></a>註冊觸發程式

註冊觸發程式會在註冊後立即啟動工作。 您也可以指定註冊觸發程式的延遲，這會在一段特定時間之後啟動工作， (在註冊工作之後的延遲) 。 延遲是在 [**IRegistrationTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iregistrationtrigger)介面的 [**delay**](/windows/desktop/api/taskschd/nf-taskschd-iregistrationtrigger-get_delay)屬性中指定， ([**RegistrationTrigger**](registrationtrigger.md)腳本) 。

> [!Note]  
> 更新註冊觸發程式的工作時，工作會在更新發生之後執行。

 

## <a name="registration-trigger-examples"></a>註冊觸發程式範例

下列範例會在工作註冊時啟動「記事本」：

-   [ (腳本) 的註冊觸發程式範例 ](registration-trigger-example--scripting-.md)
-   [ (c + +) 的註冊觸發程式範例 ](registration-trigger-example--c---.md)
-   [ (XML) 的註冊觸發程式範例 ](registration-trigger-example--xml-.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工作排程器](using-the-task-scheduler.md)
</dt> </dl>

 

 




