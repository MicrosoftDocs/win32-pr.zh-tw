---
title: 與其他應用程式共用 i/o 程式
description: 與其他應用程式共用 i/o 程式
ms.assetid: 56e4804b-fe88-4b3b-93f6-f8e41048780d
keywords:
- 多媒體檔案 i/o，共用程式
- 檔案 i/o，共用程式
- 輸入和輸出 (i/o) ，共用程式
- I/o (輸入和輸出) ，共用程式
- 與其他應用程式共用 i/o 程式
- mmioInstallIOProc 函式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd7931bde28338cc625c828128e05047d8ec3370
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "104375076"
---
# <a name="sharing-an-io-procedure-with-other-applications"></a>與其他應用程式共用 i/o 程式

如果您想要與其他應用程式共用 i/o 程式，您需要為應用程式撰寫 (DLL) 的動態連結程式庫。 您可以藉由執行下列其中一項動作來共用 i/o 程式：

-   將 i/o 程式的程式碼包含在 DLL 中。
-   在 DLL 中建立函式，此函式會呼叫 [**mmioInstallIOProc**](/windows/win32/api/mmiscapi/nf-mmiscapi-mmioinstallioproc) 函數來安裝 i/o 程式。
-   在 DLL 的模組定義檔中匯出此函數。

若要使用共用的 i/o 程式，應用程式必須先呼叫 DLL 中的函式，以安裝 i/o 程式。

 

 