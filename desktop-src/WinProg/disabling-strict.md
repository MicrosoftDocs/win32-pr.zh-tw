---
title: 停用 STRICT
description: 若要停用嚴格類型檢查，請定義符號名稱 NO \_ strict。 在 Visual C/c + + 中，您也可以指定/DNO \_ STRICT 作為編譯器選項，在命令列或 makefile 中指定這個定義。
ms.assetid: 57b01d2e-1f64-4ac0-b4f0-624c241899d7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62bfdfef2aa7988576aa4c1e17f002639de98121
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103674184"
---
# <a name="disabling-strict"></a>停用 STRICT

若要停用 **嚴格** 類型檢查，請定義符號名稱 **NO \_ strict**。 在 Visual C/c + + 中，您也可以指定 **/DNO \_ STRICT** 作為編譯器選項，在命令列或 makefile 中指定這個定義。

若要針對逐檔案定義 **不 \_ 嚴格** 的，請在包含 Windows .h 之前插入 **\# 定義** 語句：


```C++
#define NO_STRICT
#include <windows.h>
```



為了獲得最佳結果，您也應該將錯誤訊息的警告層級設定為至少 **/W3**。 這對 Windows 的應用程式一律是建議的作法，因為會造成警告的編碼做法 (例如，傳遞錯誤的參數數目) 通常會在執行時間造成嚴重錯誤（如果未修正）。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[啟用 STRICT](enabling-strict.md)
</dt> <dt>

[嚴格合規性](strict-compliance.md)
</dt> </dl>

 

 




