---
title: 通用控制項的 Unicode 支援
description: 本主題說明如何支援一般控制項通知的 Unicode。
ms.assetid: 5020F638-261D-4D32-ACC4-F9572EDBE875
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdb029d6e1c018f1793c749aefb2f88104559cae
ms.sourcegitcommit: a716ca2a6a22a400f02c6b31699cf4da83ee3619
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/04/2020
ms.locfileid: "103933736"
---
# <a name="unicode-support-for-common-controls"></a>通用控制項的 Unicode 支援

本主題說明如何支援一般控制項通知的 Unicode。


針對 comctl32.dll 5.80 版和更新版本，通用控制項通知支援 Windows 95 系統或更新版本上的 ANSI 和 Unicode 格式。 系統會將您的視窗傳送至 [**WM \_ NOTIFYFORMAT**](wm-notifyformat.md) 訊息，以決定要使用的格式。 若要指定格式，請傳回 \_ ansi 通知的 NFR ansi，或 \_ unicode 通知的 NFR unicode。 如果您未處理此訊息，系統會呼叫 [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) 來判斷格式。 由於 Windows 95 和 Windows 98 一律會傳回 **FALSE** 給此函式呼叫，因此預設會使用 ANSI 通知。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於通用控制項](common-controls-intro.md)
</dt> </dl>

 

 