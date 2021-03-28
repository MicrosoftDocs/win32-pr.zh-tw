---
description: 下列函式可用於筆刷。
ms.assetid: 617eb778-876c-4bbb-90da-c5f13359becb
title: " (Windows GDI) 的筆刷函數"
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c2170ff5c4b743e19da669bd76b340ca95ac2ef9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512924"
---
# <a name="brush-functions-windows-gdi"></a> (Windows GDI) 的筆刷函數

下列函式可用於筆刷。



| 函式                                                   | 描述                                                |
|------------------------------------------------------------|------------------------------------------------------------|
| [**CreateBrushIndirect**](/windows/desktop/api/Wingdi/nf-wingdi-createbrushindirect)         | 使用指定的樣式、色彩和模式建立筆刷 |
| [**CreateDIBPatternBrushPt**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrushpt) | 使用 DIB 的模式建立筆刷                |
| [**CreateHatchBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createhatchbrush)               | 使用影線圖樣和色彩建立筆刷             |
| [**CreatePatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createpatternbrush)           | 使用點陣圖模式建立筆刷                      |
| [**CreateSolidBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createsolidbrush)               | 以純色建立筆刷                         |
| [**GetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-getbrushorgex)                     | 取得裝置內容的筆刷來源                 |
| [**GetSysColorBrush**](/windows/desktop/api/Winuser/nf-winuser-getsyscolorbrush)               | 取得對應至色彩索引之筆刷的控制碼 |
| [**PatBlt**](/windows/desktop/api/Wingdi/nf-wingdi-patblt)                                   | 繪製矩形                                         |
| [**SetBrushOrgEx**](/windows/desktop/api/Wingdi/nf-wingdi-setbrushorgex)                     | 設定裝置內容的筆刷來源                 |
| [**SetDCBrushColor**](/windows/desktop/api/Wingdi/nf-wingdi-setdcbrushcolor)                 | 設定目前的裝置內容筆刷色彩。               |



 

## <a name="obsolete-functions"></a>過時的函式

下列函式僅提供給 Windows 的16位版本相容。

[**CreateDIBPatternBrush**](/windows/desktop/api/Wingdi/nf-wingdi-createdibpatternbrush)

 

 



