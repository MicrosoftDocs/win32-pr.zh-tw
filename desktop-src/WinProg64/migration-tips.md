---
title: 移轉提示
description: 將您的程式碼移植到64位 Windows 時，請務必考慮定址計算和指標算術。
ms.assetid: ae562a85-d6ea-4595-b54c-0a28e6532cf5
keywords:
- 64位 Windows 程式設計指南64位 Windows 程式設計，遷移秘訣
- 遷移秘訣 64-位 Windows 程式設計
- 相容性 64-位 Windows 程式設計
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3ee1480bec99bdc3b620d5d349343330aa3c34121ff697d5e8b15497c72baedc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117743593"
---
# <a name="migration-tips"></a>移轉提示

檢查程式碼是否有64位相容時，有兩個主要的考慮區域如下：

-   位址計算
-   指標算術

基於許多原因，開發人員會以 **ULONG** 值的形式儲存位址。 畢竟，在32位 Windows 上，位址、指標和 **ULONG** 值全都是32位長。 不過，在64位 Windows 上，位址和 **ULONG** 的長度不相同。 雖然 **ULONG** 保持為32位值，但所有指標現在都是64位值。

## <a name="in-this-section"></a>本章節內容

-   [一般移植指導方針](general-porting-guidelines.md)
-   [儲存64位值](storing-a-64-bit-value.md)
-   [常見的編譯器錯誤](common-compiler-errors.md)
-   [其他考慮](additional-considerations.md)

 

 




