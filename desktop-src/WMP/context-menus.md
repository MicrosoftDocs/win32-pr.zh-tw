---
title: 操作功能表
description: 操作功能表
ms.assetid: d1ea899a-9087-4502-8825-5cef1a87ef03
keywords:
- Windows Media Player 線上商店，內容功能表
- 線上商店、內容功能表
- 輸入1個線上商店、內容功能表
- Windows Media Player 線上商店、自訂內容功能表
- 線上商店、自訂內容功能表
- 輸入1個線上商店、自訂內容功能表
- 內容功能表
- 自訂內容功能表
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c6ad3bba5863f83b5f324821ec0904e7ef4c5881c7f10b9214eebde1081b217d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118119347"
---
# <a name="context-menus"></a>操作功能表

線上商店可以提供自訂的內容功能表。 若要這樣做，線上商店外掛程式會執行 [IWMPContentPartner：： GetCommands](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getcommands) 方法。 Windows Media Player 會呼叫這個方法，以提供使用者介面中顯示內容功能表之位置的相關資訊， (使用者以滑鼠右鍵按一下) 。 外掛程式會傳回一組描述每個內容功能表項目的 [WMPCoNtextMenuInfo](/previous-versions/windows/desktop/api/contentpartner/ns-contentpartner-wmpcontextmenuinfo) 結構，包括每個內容功能表項目的命令識別碼。

在 Windows Media Player 取出陣列之後，播放程式會使用陣列來建立使用者所看到的內容功能表。 當使用者按一下內容功能表中的專案時，播放程式會呼叫 [IWMPContentPartner：： InvokeCommand](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-invokecommand)，並透過 *dwCommandID* 參數傳遞與功能表項目相關聯的命令識別碼。 播放程式也會傳遞程式庫位置值和識別碼陣列，代表功能表叫用的專案，例如追蹤識別碼的陣列。 藉由使用這項資訊，外掛程式可以啟動任何適當的進程，以回應使用者的滑鼠點擊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於類型1線上商店**](about-type-1-online-stores.md)
</dt> </dl>

 

 




