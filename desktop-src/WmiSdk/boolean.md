---
title: WMI)  (布林值
description: 這是一種 VT \_ BOOL 參數，會採用 variant \_ TRUE (&\# 8211; 1) 或 variant \_ FALSE (0) 的值。
ms.assetid: 3928ff39-ed17-4a61-bb72-a3c9be16ae45
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 569f7ce633bfb70fdba5e7055a80ad73ebd0fb6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978310"
---
# <a name="boolean-wmi"></a>WMI)  (布林值

布林資料類型是一種 VT \_ BOOL 參數，會採用 variant \_ TRUE ( – 1) 或 variant \_ FALSE (0) 的值。 下表列出 C/c + + 中邏輯 **TRUE** 的程式設計標記法與 Automation 型別之間的差異。

| 語言   | 值         | 數值 |
|------------|---------------|-----------------|
| C/C++      | **TRUE**      | 1               |
| 自動化 | VARIANT \_ TRUE | –1              |

這兩種類型都是非零，因此不是 **FALSE**，但是有不同的標記法表示為 **TRUE**。
