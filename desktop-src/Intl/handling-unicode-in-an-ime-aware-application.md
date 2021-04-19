---
description: 在 IME-Aware 應用程式中處理 Unicode
ms.assetid: fa202c1e-d0af-441f-b878-ed98205a880c
title: 在 IME-Aware 應用程式中處理 Unicode
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d78174776eb608c3e494fd5967acba41609e436a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998000"
---
# <a name="handling-unicode-in-an-ime-aware-application"></a>在 IME-Aware 應用程式中處理 Unicode

有兩個問題與 IMM 和其 Unicode 處理有關。 第一個問題是，Unicode 版本的 IMM 函式會以位元組為單位來取得緩衝區大小，而不是使用16位 Unicode 字元。 第二個問題是，IMM 通常會在 [**WM \_ CHAR**](../inputdev/wm-char.md) 和 [**wm \_ IME \_ 字元**](wm-ime-char.md) 訊息中， (抓取 Unicode 字元，而不是 DBCS 字元) 。

除了原本支援的 ANSI 介面，Windows 還支援適用于 IMM 的 Unicode 介面。

您的應用程式應該使用 [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) ，讓 [**Wm \_ char**](../inputdev/wm-char.md) 和 [**WM \_ IME \_ 字元**](wm-ime-char.md) 訊息在 *WPARAM* 參數中取出 Unicode 字元，而不是 DBCS 字元。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用輸入方法管理員](using-input-method-manager.md)
</dt> </dl>

 

 
