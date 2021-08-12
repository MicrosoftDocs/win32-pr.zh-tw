---
title: 通用控制項的 Unicode 支援
description: 本主題說明如何支援一般控制項通知的 Unicode。
ms.assetid: 5020F638-261D-4D32-ACC4-F9572EDBE875
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01ab987516f1a91b47f8e5fd5f031631956d8c7bf59cd164edd83d414d5e72d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118668890"
---
# <a name="unicode-support-for-common-controls"></a>通用控制項的 Unicode 支援

本主題說明如何支援一般控制項通知的 Unicode。


針對 comctl32.dll 的5.80 版和更新版本，通用控制項通知支援 Windows 95 系統或更新版本上的 ANSI 和 Unicode 格式。 系統會將您的視窗傳送至 [**WM \_ NOTIFYFORMAT**](wm-notifyformat.md) 訊息，以決定要使用的格式。 若要指定格式，請傳回 \_ ansi 通知的 NFR ansi，或 \_ unicode 通知的 NFR unicode。 如果您未處理此訊息，系統會呼叫 [**IsWindowUnicode**](/windows/desktop/api/winuser/nf-winuser-iswindowunicode) 來判斷格式。 由於 Windows 95 和 Windows 98 一律會將 **FALSE** 傳回給此函式呼叫，因此預設會使用 ANSI 通知。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於通用控制項](common-controls-intro.md)
</dt> </dl>

 

 