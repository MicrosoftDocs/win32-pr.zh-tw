---
title: 在系統開機時啟動可執行檔
description: 藉由定義開機觸發程式和可執行檔動作，來撰寫在系統啟動時啟動可執行檔的工作。
ms.assetid: 9e2359df-a223-4a0c-9051-01b73a83c1f7
keywords:
- 工作排程器範例工作排程器、開機觸發程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b7d41c39e9c80d3fc8f14c0bc9b9d9305de38e16
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674584"
---
# <a name="starting-an-executable-on-system-boot"></a>在系統開機時啟動可執行檔

藉由定義開機觸發程式和可執行檔動作，來撰寫在系統啟動時啟動可執行檔的工作。

## <a name="boot-trigger"></a>開機觸發程式

開機觸發程式是由其開始界限啟動，但是在系統開機之前，它們不會啟動可執行檔。 您也可以在開機觸發程式中指定延遲時間，以指定系統開機和啟動工作之間的時間長度。 這是由 [**IBootTrigger**](/windows/desktop/api/taskschd/nn-taskschd-iboottrigger)介面中的 [**Delay**](/windows/desktop/api/taskschd/nf-taskschd-iboottrigger-get_delay)屬性所定義， ([**BootTrigger**](boottrigger.md)物件來撰寫腳本) 。

## <a name="boot-trigger-examples"></a>開機觸發程式範例

下列範例會在系統開機之後啟動「記事本」：

-   [ (腳本) 的開機觸發程式範例 ](boot-trigger-example--scripting-.md)
-   [ (c + +) 的開機觸發程式範例 ](boot-trigger-example--c---.md)
-   [ (XML) 的開機觸發程式範例 ](boot-trigger-example--xml-.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工作排程器](using-the-task-scheduler.md)
</dt> </dl>

 

 




