---
title: RTMv2 程式設計問題
description: RTMv2 函式會使用下列假設來撰寫。
ms.assetid: c8c6f553-57cc-4eec-bbc0-b6b50897cc75
keywords:
- 程式設計問題，RTMv2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 584568fc3c4e7a46a2a2114781b81465d893b80978471aa3149d93d38f0c8c5d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120035588"
---
# <a name="rtmv2-programming-issues"></a>RTMv2 程式設計問題

RTMv2 函式會使用下列假設來撰寫。

-   RTMv2 函數不會為用戶端配置記憶體。 用戶端一律必須配置記憶體。
-   當用戶端取消註冊時，它必須執行清除作業本身，例如釋出所有配置的記憶體。
-   用戶端必須正確釋放控制碼;如果用戶端不會察覺到這種做法，可能會發生記憶體流失。

 

 




