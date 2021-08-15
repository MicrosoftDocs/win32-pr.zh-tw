---
title: 在特定時間啟動可執行檔
description: 撰寫可在特定時間啟動可執行檔的工作，是藉由定義時間觸發程式和可執行檔動作來完成。
ms.assetid: a45a403d-5a54-4648-b517-41e01a0745c9
keywords:
- 工作排程器範例工作排程器、時間觸發程式
- 工作排程器範例工作排程器，啟動可執行檔
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62276568f7c626935d8c5c518d51f58ad0a58b5c313e780ec5651067af625068
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119059956"
---
# <a name="starting-an-executable-at-a-specific-time"></a>在特定時間啟動可執行檔

撰寫可在特定時間啟動可執行檔的工作，是藉由定義時間觸發程式和可執行檔動作來完成。

## <a name="start-boundary"></a>開始界限

請務必注意，時間觸發程式與其他以時間為基礎的觸發程式不同，因為觸發程式是由其開始界限啟動時所引發。 其他以時間為基礎的觸發程式是由其開始界限啟動，但是它們不會開始執行其動作 (在此案例中，啟動可執行檔) ，直到達到排程的日期為止。

## <a name="time-trigger-examples"></a>時間觸發程式範例

下列範例會在啟動工作記事本30秒後開始：

-   [時間觸發程式範例 (c + +) ](time-trigger-example--c---.md)
-   [腳本)  (時間觸發程式範例 ](time-trigger-example--scripting-.md)
-   [ (XML) 的時間觸發程式範例 ](time-trigger-example--xml-.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用工作排程器](using-the-task-scheduler.md)
</dt> </dl>

 

 




