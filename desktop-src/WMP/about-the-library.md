---
title: 關於程式庫
description: 關於程式庫
ms.assetid: a43c57ac-deb4-4c86-a8a2-bcfd214b9d0a
keywords:
- Windows Media Player，程式庫
- Windows Media Player 物件模型，程式庫
- 物件模型，程式庫
- Windows Media Player ActiveX 控制項、物件模型的程式庫
- ActiveX 控制項，物件模型的程式庫
- Windows Media PlayerMobile ActiveX 控制項，物件模型的程式庫
- Windows Media Player適用于物件模型的 Mobile、library
- Windows Media Player 程式庫，關於
- 程式庫，關於
- 中繼資料，Windows Media Player 程式庫
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 63fdaa19fc8be11de1886074a21b0cc1fb6d4be7dde73faa05c67e1f496ac17c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119470348"
---
# <a name="about-the-library"></a>關於程式庫

程式庫是有關可 Windows Media Player 之數位媒體內容的資訊或 *中繼資料* 的資料庫。 部分資訊會顯示在播放程式的 [連結 **庫** ] 窗格中;它有更多可透過程式碼來使用。

 (在 Windows Media Player 9 系列及更早版本中，這項功能稱為 **Media Library**。 ) 

程式庫可讓使用者輕鬆地組織及存取數位媒體內容。 例如，使用者可以依專輯、演出者、內容類型或單純的所有音樂清單，來查看所組織的音樂。 您可以使用 Windows Media Player SDK 物件模型來存取程式庫，以播放內容、取出播放清單、新增內容、移除內容，以及變更相關聯的中繼資料。 Windows Media Player 在某些情況下，限制從程式碼存取程式庫的能力，以保護使用者的隱私權。 如需存取權限的詳細資訊，請參閱連結 [庫存取](library-access.md)。

程式庫會儲存兩種基本數位媒體內容類型的相關中繼資料。 第一種類型的數位媒體專案是個別的內容檔案，例如音樂軌或相片。 第二種類型（播放清單）是代表數位媒體專案群組的檔案，通常是以指定的順序播放。 與數位媒體內容相關聯的中繼資料會儲存為名稱/值配對。 例如，描述執行歌曲之人員的中繼資料名稱為「演出者」，而與其相關聯的值通常是包含執行者名稱的文字字串。 每個唯一的中繼資料名稱稱為 *屬性*。 如需支援的屬性清單，請參閱 [屬性參考](attribute-reference.md)。 如需在程式碼中使用屬性的詳細資訊，請參閱 [媒體專案屬性](media-item-attributes.md)。

下列各節提供使用程式庫的詳細資訊：

-   [以程式設計方式存取程式庫](accessing-the-library-programmatically.md)
-   [關於程式庫服務](about-library-services.md)

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**關於 Player 物件模型**](about-the-player-object-model.md)
</dt> </dl>

 

 




