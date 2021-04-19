---
title: 適用于桌面應用程式的高 DPI Windows 8。1
description: 適用于桌面應用程式的高 DPI Windows 8。1
ms.assetid: 1E92D3C8-C117-463A-AF31-12D3CAA31E2A
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6c223e9dc39cda9a109280926a5eb47a8fffcc
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106966871"
---
# <a name="high-dpi-for-desktop-apps-in-windows-81"></a>適用于桌面應用程式的高 DPI Windows 8。1

## <a name="platforms"></a>平台

<dl> 用戶端-Windows 8。1  
伺服器-Windows Server 2012 R2  
</dl>

## <a name="description"></a>Description

在 Windows 8.1 的桌面應用程式中，除了100%、125% 和150% 調整（Windows 8 支援）之外，還會在顯示時執行200% 的縮放。 此外，桌面應用程式會以個別監視器為基礎進行調整，而不是針對套用至所有顯示器的單一縮放比例進行縮放。 開發人員也可以在 Windows 8.1 中呼叫新的 Api，以取得個別監視器規模的因素。

## <a name="manifestations"></a>表現

使用者可以使用新的高密度顯示器搭配 Windows 8.1，取得利用較高圖元資料的絕佳視覺體驗。 如果應用程式不會處理高 DPI，Windows 會將其調整為使用者。 此外，使用者也可以在同一部電腦上混用高與低密度的組合，而 Windows 會適當地為每個顯示器調整內容規模。 這是 Windows 8 的改進，其中的內容在某些顯示器上可能太大。

## <a name="mitigation"></a>降低

由於 Windows 會調整不會自行擴充的應用程式，因此開發人員通常不需要執行額外的工作，但投資撰寫支援高 DPI 應用程式的開發人員會有競爭優勢，因為這些應用程式在新的高 DPI 膝上型電腦和桌上型電腦上看起來會更好。

## <a name="solution"></a>解決方法

製作可利用高 DPI 的應用程式，是一項複雜的設計和執行工作。 請參閱下列連結以取得教學課程資訊、建立簡報內容和類似的支援。

## <a name="tests"></a>測試

即使開發人員未選擇讓應用程式使用高 DPI，也應在100%、125%、150% 和200% 的調整中測試其應用程式，以確保使用者體驗能獲得滿意且具競爭力。

## <a name="resources"></a>資源

-   [Windows 8.1 中的高 DPI 白皮書和教學課程](../hidpi/high-dpi-desktop-application-development-on-windows.md)
-   [Windows 桌面範例程式](https://www.microsoft.com/?ref=go)
-   [Windows 8.1 中的高 DPI 組建2013細分會話](https://channel9.msdn.com/Events/Build/2013/4-184)

 

 