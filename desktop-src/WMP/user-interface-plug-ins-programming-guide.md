---
title: 消費者介面外掛程式程式設計指南
description: 消費者介面外掛程式程式設計指南
ms.assetid: 7bc0805a-306d-4b48-bc24-41077c8c7b3d
keywords:
- Windows Media Player、外掛程式
- Windows Media Player，使用者介面外掛程式
- Windows Media Player 外掛程式、使用者介面
- 外掛程式，使用者介面
- 使用者介面外掛程式，程式設計指南
- UI 外掛程式，程式設計指南
- 程式設計指南，使用者介面外掛程式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fcba6c3c7218e504a2e8752a4d1680e4887ec5aa7bfa69744fab00b27cbee797
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118831478"
---
# <a name="user-interface-plug-ins-programming-guide"></a>消費者介面外掛程式程式設計指南

本節所述的兩個程式碼範例會示範如何從 Windows Media Player 外掛程式 Wizard 產生的程式碼開始， (UI) 外掛程式來執行自訂使用者介面的流程。

搜尋 UI 外掛程式是提供 **搜尋** 按鈕的中繼資料區域外掛程式。 按一下這個按鈕時，會在預設網頁瀏覽器中啟動搜尋頁面，其中包含目前媒體專案之演出者的相關資訊。

建立此外掛程式的第一個步驟是在 [**專案**] 索引標籤中選取 [ **Windows Media Player 外掛程式嚮導**]，以在 Microsoft Visual C++ 中啟動新專案。將專案命名為「搜尋」，然後按一下 **[確定]**。 選擇 **UI 外掛程式** ，然後按 **[下一步**]。 然後從選項清單中選擇元資料類型，然後按 **[下一步]**。 最後，按一下 [自動執行支援] 的核取方塊，如此即會自動載入外掛程式，然後按一下 **[完成]**。 Wizard 會產生必要的專案檔，包括 CSearch 類別的基本執行和它所支援的 **IWMPPluginUI** 介面，以及提供 UI 的 CPluginWindow 類別。 這是將修改以提供本節所述外掛程式功能的程式碼。

本節中的最後一個主題說明如何建立 Windows Media Player 10 Mobile 的背景 UI 外掛程式。 此外掛程式會使用 Windows Media Player 外掛程式 Wizard 產生的修改程式碼，來建立 Windows Media Player 10 行動裝置版的外掛程式。

此章節包含下列主題。



| 主題                                                                                                                                            | 描述                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------|
| [執行 CSearch](implementing-csearch.md)                                                                                                 | 描述 CSearch 類別所需的變更。                                |
| [執行 CPluginWindow](implementing-cpluginwindow.md)                                                                                     | 描述 CPluginWindow 類別所需的變更。                          |
| [建立 Windows Media Player 10 行動裝置版的消費者介面外掛程式](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md) | 說明如何建立 Windows Media Player 10 行動裝置版的背景 UI 外掛程式。 |



 

 

 




