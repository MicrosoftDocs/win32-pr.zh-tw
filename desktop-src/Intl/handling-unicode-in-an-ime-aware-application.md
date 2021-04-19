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
# <a name="handling-unicode-in-an-ime-aware-application"></a><span data-ttu-id="d3996-103">在 IME-Aware 應用程式中處理 Unicode</span><span class="sxs-lookup"><span data-stu-id="d3996-103">Handling Unicode in an IME-Aware Application</span></span>

<span data-ttu-id="d3996-104">有兩個問題與 IMM 和其 Unicode 處理有關。</span><span class="sxs-lookup"><span data-stu-id="d3996-104">Two issues are involved with the IMM and its handling of Unicode.</span></span> <span data-ttu-id="d3996-105">第一個問題是，Unicode 版本的 IMM 函式會以位元組為單位來取得緩衝區大小，而不是使用16位 Unicode 字元。</span><span class="sxs-lookup"><span data-stu-id="d3996-105">The first issue is that the Unicode versions of IMM functions retrieve the size of a buffer in bytes instead of 16-bit Unicode characters.</span></span> <span data-ttu-id="d3996-106">第二個問題是，IMM 通常會在 [**WM \_ CHAR**](../inputdev/wm-char.md) 和 [**wm \_ IME \_ 字元**](wm-ime-char.md) 訊息中， (抓取 Unicode 字元，而不是 DBCS 字元) 。</span><span class="sxs-lookup"><span data-stu-id="d3996-106">The second issue is that the IMM normally retrieves Unicode characters (instead of DBCS characters) in the [**WM\_CHAR**](../inputdev/wm-char.md) and [**WM\_IME\_CHAR**](wm-ime-char.md) messages.</span></span>

<span data-ttu-id="d3996-107">除了原本支援的 ANSI 介面，Windows 還支援適用于 IMM 的 Unicode 介面。</span><span class="sxs-lookup"><span data-stu-id="d3996-107">Windows supports a Unicode interface for the IMM, in addition to the ANSI interface originally supported.</span></span>

<span data-ttu-id="d3996-108">您的應用程式應該使用 [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) ，讓 [**Wm \_ char**](../inputdev/wm-char.md) 和 [**WM \_ IME \_ 字元**](wm-ime-char.md) 訊息在 *WPARAM* 參數中取出 Unicode 字元，而不是 DBCS 字元。</span><span class="sxs-lookup"><span data-stu-id="d3996-108">Your applications should use [**RegisterClassW**](/windows/win32/api/winuser/nf-winuser-registerclassa) to cause the [**WM\_CHAR**](../inputdev/wm-char.md) and [**WM\_IME\_CHAR**](wm-ime-char.md) messages to retrieve Unicode characters instead of DBCS characters in the *wParam* parameter.</span></span>

## <a name="related-topics"></a><span data-ttu-id="d3996-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="d3996-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="d3996-110">使用輸入方法管理員</span><span class="sxs-lookup"><span data-stu-id="d3996-110">Using Input Method Manager</span></span>](using-input-method-manager.md)
</dt> </dl>

 

 
