---
title: 元件感知
description: 您的應用程式必須回應 WM \_ PALETTECHANGED、wm \_ QUERYNEWPALETTE 和 wm \_ 啟動訊息，才能察覺並使用調色板。 將您的應用程式設計為選取並實現調色板以回應這些訊息。
ms.assetid: 0670e929-dfdb-44d2-bda2-c532d1739d8e
keywords:
- Windows 上的 OpenGL、元件感知
- 調色板感知 OpenGL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5172d3b0a353141900bd873d8f97d6a25ce570e54d180ce1c8b1ca949e51d8ed
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118936294"
---
# <a name="palette-awareness"></a>元件感知

您的應用程式必須回應 [wm \_ PALETTECHANGED](/windows/desktop/gdi/wm-palettechanged)、 [wm \_ QUERYNEWPALETTE](/windows/desktop/gdi/wm-querynewpalette)和 [wm \_ 啟動](../inputdev/wm-activate.md) 訊息，才能察覺並使用調色板。 將您的應用程式設計為選取並實現調色板以回應這些訊息。

如需調色板和調色板感知的詳細資訊，請參閱 Microsoft 開發人員網路開發程式庫 compact 光碟上的「調色板感知」和「元件管理員：如何與原因」文章。

 

 