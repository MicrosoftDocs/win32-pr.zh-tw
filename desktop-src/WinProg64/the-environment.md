---
title: 環境
description: 使用64位 Windows 應用程式的開發人員，會發現開發環境與32位 Windows 的開發環境幾乎完全相同。
ms.assetid: 49b2b952-f771-4721-a9b0-01eb67a98007
keywords:
- 開發環境 64-位 Windows 程式設計
- 環境 64-位 Windows 程式設計
- 64位 Windows 程式設計指南64位 Windows 程式設計、開發環境
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 69580d6537c832abaf51b20a553c4e4e788a6013bdfc14a8002f60de9872da62
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119734128"
---
# <a name="the-environment"></a>環境

使用64位 Windows 應用程式的開發人員，會發現開發環境與32位 Windows 的開發環境幾乎完全相同。 在必要時已修改現有的 Api，以允許它們反映其執行所在平臺的精確度。 結果是簡單的，而且是開發人員的簡短學習曲線，撰寫64位 Windows 程式碼就像撰寫32位 Windows 的程式碼一樣。

Windows 標頭檔支援新的資料類型，可讓指標和指標相關聯的變數反映平臺的精確度。 這表示開發人員可以編譯單一來源基底，以原生方式在 32 Windows 或64位 Windows 上執行。 這項策略可降低開發應用程式的成本，這些應用程式會利用64位硬體，例如 AMD 皓龍或 Athlon64 處理器或 Intel Itanium 處理器。

如果您盡速採用新的資料類型慣例，您將有更多時間讓應用程式64位就緒。 如果您要變更程式碼，您應該同時變更資料定義。 在32位 Windows 上測試應用程式、透過64位編譯器執行， ([[工具](the-tools.md)) ] 中所述，而且當您有適當的64位硬體時，應用程式就可以開始測試。

 

 




