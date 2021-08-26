---
description: Windows GDI+ 是 Windows XP 作業系統或 Windows Server 2003 的子系統，負責顯示畫面和印表機的資訊。 GDI+ 是透過一組 c + + 類別公開的 API。
ms.assetid: 8797e7c4-44d8-49f7-aec8-37ee48c24747
title: GDI+ 總覽
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 15ca4eadf9eaf27cbe35103753a49c4bc25d2974ee1051481b0b52787a6602e2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830758"
---
# <a name="overview-of-gdi"></a>GDI+ 總覽

Windows GDI+ 是 Windows XP 作業系統或 Windows Server 2003 的子系統，負責顯示畫面和印表機的資訊。 GDI+ 是透過一組 c + + 類別公開的 API。

如其名所示，GDI+ 是 Windows 圖形裝置介面 (GDI) （舊版 Windows 隨附的圖形裝置介面）的後續版本。 WindowsXP 或 Windows Server 2003 支援 gdi，以與現有的應用程式相容，但新應用程式的程式設計人員應該針對其所有圖形需求使用 GDI+，因為 GDI+ 會優化許多 GDI 的功能，同時也提供額外的功能。

圖形裝置介面，例如 GDI+，可讓應用程式設計人員在螢幕或印表機上顯示資訊，而不需要擔心特定顯示裝置的詳細資料。 應用程式程式設計師會呼叫 GDI+ 類別所提供的方法，而這些方法接著會對特定設備磁碟機進行適當的呼叫。 GDI+ 將應用程式與圖形硬體隔離，而這是一種可讓開發人員建立裝置獨立應用程式的保溫。

 

 



