---
title: 關於轉換外掛程式
description: 關於轉換外掛程式
ms.assetid: bd6d1020-e8e1-492e-9c76-9f3cf04190de
keywords:
- Windows Media Player，轉換外掛程式
- Windows Media Player 外掛程式，轉換
- 外掛程式，轉換
- 轉換外掛程式，關於
- 進階系統格式 (ASF)
- 'ASF (Advanced Systems 格式) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ada6e2a8fa41b657a593dc03082f871503b53eba
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103671568"
---
# <a name="about-conversion-plug-ins"></a>關於轉換外掛程式

您可以建立 Windows Media Player 外掛程式，將使用 Microsoft 未提供的技術所建立的數位媒體檔案轉換成 Advanced Systems 格式 (ASF) 。

轉換外掛程式是元件物件模型 (COM) 物件，這些物件會封裝並散發為可執行檔 ( .exe) 檔。 在下列案例中，Windows Media Player 具現化轉換外掛程式以轉換協力廠商數位媒體格式：

-   數位媒體內容會從可攜式裝置複製到電腦上。
-   使用 **IWMPMediaCollection：： add**，將數位媒體內容新增至程式庫。
-   數位媒體內容會使用 Windows Media Player 的搜尋功能新增至程式庫。
-   數位媒體內容會依 Windows Media Player 的資料夾監控功能新增至程式庫。
-   當使用者拖放檔案時，數位媒體內容會新增至同步處理清單。

在 Windows Media Player 建立轉換外掛程式的實例之後，外掛程式必須將提供的檔案轉換成 ASF 或 WMA，並新增相關的中繼資料。  (不使用轉換外掛程式轉碼檔案。 ) 外掛程式必須將已轉換的檔案複製到指定的資料夾，並將新檔案的路徑傳回給 Windows Media Player。

轉換外掛程式必須執行 **IWMPConvert** 介面。 請參閱 [轉換外掛程式程式設計參考](conversion-plug-ins-programming-reference.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於轉換流程**](about-the-conversion-process.md)
</dt> <dt>

[**將中繼資料新增至轉換的檔案**](adding-metadata-to-converted-files.md)
</dt> <dt>

[**Windows Media Player 轉換外掛程式**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




