---
title: 顯示對話方塊
description: 顯示對話方塊
ms.assetid: 637555af-0a36-4aee-908f-496b52f7bd78
keywords:
- Windows Media Player 線上商店，顯示對話方塊
- 線上商店，顯示對話方塊
- 輸入1個線上商店，顯示對話方塊
- Windows Media Player 線上商店，對話方塊
- 線上商店、對話方塊
- 輸入1個線上商店、對話方塊
- 顯示對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 00e71d177e7675822b1f2704bf62776e598c2e817d583020b0df962347dac4f7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118997268"
---
# <a name="displaying-dialog-boxes"></a>顯示對話方塊

線上商店可以透過 Windows Media Player 叫用對話方塊。 若要這樣做，請從探索頁面腳本程式碼呼叫 [External. showPopup](external-showpopup.md) ，提供代表要顯示之對話方塊的自訂索引值。 此索引值只對線上商店程式碼具有意義;Windows Media Player 不會解讀此值。 Windows Media Player 接著會呼叫 [IWMPContentPartner：： GetItemInfo](/previous-versions/windows/desktop/api/contentpartner/nf-contentpartner-iwmpcontentpartner-getiteminfo)，並傳遞 g \_ szItemInfo \_ PopupURL 作為 *bstrInfoName* 參數和 *pCoNtext* 參數的索引編號。 外掛程式接著會傳回包含要在對話方塊中顯示之網頁 URL 的 **BSTR** ，而播放程式會顯示對話方塊。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**類型1線上商店的程式設計指南**](programming-guide-for-type-1-online-stores.md)
</dt> </dl>

 

 




