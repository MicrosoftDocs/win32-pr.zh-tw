---
title: 在特定時間啟動可執行檔
description: 撰寫可在特定時間啟動可執行檔的工作，是藉由定義時間觸發程式和可執行檔動作來完成。
ms.assetid: a45a403d-5a54-4648-b517-41e01a0745c9
keywords:
- 工作排程器範例工作排程器、時間觸發程式
- 工作排程器範例工作排程器，啟動可執行檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c0ce5a1be1586e12399f1dd5d6969170bffa92f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103840384"
---
# <a name="starting-an-executable-at-a-specific-time"></a>在特定時間啟動可執行檔

撰寫可在特定時間啟動可執行檔的工作，是藉由定義時間觸發程式和可執行檔動作來完成。

## <a name="start-boundary"></a>開始界限

請務必注意，時間觸發程式與其他以時間為基礎的觸發程式不同，因為觸發程式是由其開始界限啟動時所引發。 其他以時間為基礎的觸發程式是由其開始界限啟動，但是它們不會開始執行其動作 (在此案例中，啟動可執行檔) ，直到達到排程的日期為止。

## <a name="time-trigger-examples"></a>時間觸發程式範例

下列範例會在工作啟動後的30秒內啟動「記事本」：

-   [時間觸發程式範例 (c + +) ](time-trigger-example--c---.md)
-   [腳本)  (時間觸發程式範例 ](time-trigger-example--scripting-.md)
-   [ (XML) 的時間觸發程式範例 ](time-trigger-example--xml-.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工作排程器](using-the-task-scheduler.md)
</dt> </dl>

 

 




