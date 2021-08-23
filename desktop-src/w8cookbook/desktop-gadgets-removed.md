---
title: 已移除桌面小工具
description: 已移除桌面小工具
ms.assetid: 0074204B-F568-4F9B-A0F7-3E330B91E4CD
keywords:
- 小工具
- 桌面小工具
- Windows 資訊看板
- 資訊看板
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f254c4794c93c6afeeec9374e7c1c73f7d538c82b343ffaea984369a72231deb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119707008"
---
# <a name="desktop-gadgets-removed"></a>已移除桌面小工具

## <a name="platforms"></a>平台

 **客戶** 端-Windows 8  
**伺服器**-Windows Server 2012  



## <a name="description"></a>描述

從功能的觀點來看，小工具已被取代，並由新的動態磚和應用程式 outclassed。 小工具也會對使用者帶來安全性風險。 作為平臺，有弱點存在，甚至可能會惡意探索無害的小工具。 因此，為了將 Windows 8 保持在最新且安全的作業系統，我們選擇完全移除作業系統中的小工具。 Windows 7 使用者桌面上具有小工具的使用者，將會收到通知，並將會卸載小工具。

## <a name="manifestation"></a>表現

桌面小工具將無法在 Windows desktop 中使用。

## <a name="mitigation"></a>降低

桌面小工具 API 和資料夾結構將保留 Windows 8 的位置。 使用此 API 以程式設計方式安裝和執行小工具的應用程式將會繼續執行，而不會 (失敗，但小工具本身將不會) 。

## <a name="solution"></a>解決方案

桌面應用程式開發人員不應該在其安裝程式中封裝小工具。 這些小工具會佔用空間給使用者，而且將無法在系統中執行。

## <a name="tests"></a>測試

開發人員可以在 Windows 7 中停用桌面小工具的選用元件，以測試這項變更的相容性。 若要停用 Windows 7 電腦上的小工具，請依照下列步驟執行：

1.  流覽以從主控台開啟或關閉 Windows 功能。
2.  取消核取 [Windows 小工具平台] 旁的方塊。
3.  按一下 [確定]，並遵循任何其他螢幕上的指示。

## <a name="resources"></a>資源

[小工具中的弱點可能會允許遠端執行程式碼](https://support.microsoft.com/kb/2719662)

 

 




