---
title: RTMv2 程式設計問題
description: RTMv2 函式會使用下列假設來撰寫。
ms.assetid: c8c6f553-57cc-4eec-bbc0-b6b50897cc75
keywords:
- 程式設計問題，RTMv2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2b607adc939ff72a4d9fee99c15f6aa5192fa4c6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300800"
---
# <a name="rtmv2-programming-issues"></a>RTMv2 程式設計問題

RTMv2 函式會使用下列假設來撰寫。

-   RTMv2 函數不會為用戶端配置記憶體。 用戶端一律必須配置記憶體。
-   當用戶端取消註冊時，它必須執行清除作業本身，例如釋出所有配置的記憶體。
-   用戶端必須正確釋放控制碼;如果用戶端不會察覺到這種做法，可能會發生記憶體流失。

 

 




