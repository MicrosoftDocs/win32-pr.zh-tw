---
title: 使用 Windows Media Player SDK 開始使用
description: 使用 Windows Media Player SDK 開始使用
ms.assetid: 47c333dc-dad3-4430-a053-016d2c931f74
keywords:
- Windows Media Player 行動裝置、外掛程式
- Windows Media Player 行動裝置、使用者介面外掛程式
- Windows Media Player Mobile 外掛程式
- 外掛程式，使用者介面
- 外掛程式，Windows Media Player Mobile
- 使用者介面外掛程式，Windows Media Player Mobile
- UI 外掛程式，Windows Media Player Mobile
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2a962c1f815f820a0b2e8125872baf9d02e301dc
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "103685358"
---
# <a name="getting-started-with-the-windows-media-player-sdk"></a>使用 Windows Media Player SDK 開始使用

若要建立外掛程式，您必須先安裝 Microsoft eMbedded Visual C++ 4.0 和 Visual Studio 2003。 您也必須安裝 Pocket PC 2003 SDK 或 Smartphone 2003 SDK （個別下載）。 若要編譯並執行專案，執行 Windows Mobile 2003 第二版作業系統的 Pocket PC 或 Smartphone 裝置必須使用 Microsoft ActiveSync®3.7.1 或更新版本，與開發電腦進行同步處理。

因為 Windows Mobile 裝置上的 UI 外掛程式會使用與桌上出版本相同的外掛程式模型，所以您可以在建立可與 Windows Media Player 10 行動裝置搭配運作的背景 UI 外掛程式時，使用 Windows Media Player 外掛程式嚮導作為起點。

若要建立 UI 外掛程式程式碼，請執行下列動作：

1.  開啟 Visual Studio 2003，並在 Visual C++ 中啟動新專案。
2.  從 [**範本**] 窗格中選取 [ **Windows Media Player 外掛程式]** 。
3.  命名您的專案 NetworkPlugin，然後按一下 **[確定]**。
4.  選取 **UI 外掛程式** ，然後按 **[下一步**]。
5.  選取 **背景** ，然後按一下 **[下一步]**。
6.  按 **[下一步]** 完成精靈。 如果您要使用外掛程式來監視事件，您必須先核取 [ **接聽事件** ] 再完成嚮導，而且您應該閱讀 **IWMPEvents** 介面的檔，以瞭解 Windows Media Player 10 行動裝置支援哪些事件。

現在您已建立 UI 外掛程式程式碼，您必須在 eMbedded Visual C++ 4.0 中建立空的 Windows CE DLL 專案。 然後將您的 wizard 產生的原始程式檔複製到該新專案，以便使用 ARM4 編譯器進行編譯。

若要建立空白專案

1.  在 eMbedded Visual C++ 中啟動新的專案，然後從 [**專案**] 窗格中選取 [ **WCE Dynamic-Link 程式庫**]。
2.  命名您的專案，然後按一下 **[確定]**。
3.  確認已選取 **空白的 WINDOWS CE DLL 專案** ，然後按一下 **[完成]**。
4.  按一下 [ **專案** ] 功能表項目。
5.  選取 [ **加入至專案**]，然後 **按一下 [** 檔案]。
6.  選取您使用外掛程式嚮導建立的 c + + 檔案，然後按一下 **[確定]**。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立 Windows Media Player 10 行動裝置版的消費者介面外掛程式**](creating-a-user-interface-plug-in-for-windows-media-player-10-mobile.md)
</dt> <dt>

[**IWMPEvents 介面**](/previous-versions/windows/desktop/api/wmp/nn-wmp-iwmpevents)
</dt> </dl>

 

 




