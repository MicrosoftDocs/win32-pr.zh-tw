---
title: 便攜音訊播放程式需要出現在 Windows 檔案總管中的需求
description: 便攜音訊播放程式需要出現在 Windows 檔案總管中的需求
ms.assetid: 94227ed8-56e7-4366-9c38-9b5dbf907e16
keywords:
- Windows Media 裝置管理員、便攜音訊播放機
- 裝置管理員、便攜音訊播放機
- 程式設計指南，便攜音訊播放機
- 服務提供者，便攜音訊播放機
- 建立服務提供者，便攜音訊播放機
- 便攜音訊播放機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4a163bf04f4185bc1325aa12ea6acddd43191529
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106969460"
---
# <a name="requirements-for-portable-audio-players-to-appear-in-windows-explorer"></a>便攜音訊播放程式需要出現在 Windows 檔案總管中的需求

便攜音訊播放機 shell 命名空間延伸模組可讓 Windows 使用者以一致的方式管理由 Windows Media 裝置管理員管理的音訊裝置。 如果您根據下列指導方針來撰寫服務提供者和驅動程式元件，則您的裝置會顯示在 shell 命名空間中。 使用者將能夠在 Windows 檔案總管中以一致的方式與裝置內容互動，以執行複製、刪除和重新命名等基本作業。

下列服務提供者和驅動程式元件的 shell 需求，旨在補充一般 Windows Media 裝置管理員指導方針。

裝置功能

Windows Media 裝置管理員服務提供者的支援功能應該是明確的。 如果不支援呼叫，就必須傳回錯誤碼。 您必須設定適當的欄位，以便在從下列函式傳回時存在或缺少功能：

-   [**IMDSPStorageGlobals::GetCapabilities**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getcapabilities)
-   [**IMDSPStorage：： GetAttributes**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorage-getattributes)
-   [**IMDSPDevice::GetFormatSupport**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getformatsupport)

服務提供者必須支援下列功能，才能與 shell 相容：

-   複製到裝置 (支援取消和進度回呼) 
-   刪除裝置 (的檔案，並支援取消和進度回呼) 
-   重新命名裝置上的檔案
-   空間報告 (空間總計、可用空間、無法使用的空間) 
-   隨插即用 (請參閱 [為裝置啟用 PnP](enabling-pnp-for-devices.md)) 
-   格式化 (最好支援取消和進度回呼) 

如果支援中繼資料，則必須針對個別檔案支援下欄欄位。 如果沒有可用的資料，應該將欄位初始化為空字串：



| 欄位        | WMDM 中定義的常數 ()  | 元資料標記    |
|--------------|--------------------------------|-----------------|
| 歌曲標題   | g \_ wszWMDMTitle                | WMDM/標題      |
| 追蹤編號 | g \_ wszWMDMTrack                | WMDM/追蹤      |
| 演出者       | g \_ wszWMDMAuthor               | WMDM/作者     |
| 專輯        | g \_ wszWMDMAlbumTitle           | WMDM/AlbumTitle |
| Year         | g \_ wszWMDMYear                 | WMDM/Year       |
| Genre        | g \_ wszWMDMGenre                | WMDM/內容類型      |



 

並行

Windows Media 裝置管理員的核心模式驅動程式必須健全，才能處理平行存取。 例如，使用者可以同時透過 shell 和 media player 存取裝置，或直接透過 shell 中的多個視窗存取裝置。 在處理並行處理的過程中，驅動程式應該不會假設是因為已載入服務提供者，而是裝置正在使用中。 相反地，它們應該會執行鎖定機制，視個別作業的需要將裝置存取序列化。

UI

Windows Media 裝置管理員的服務提供者不應顯示任何使用者介面。 任何錯誤都應該盡可能地從方法呼叫傳回，做為特定的 Windows Media 裝置管理員錯誤碼。

在 Shell 中啟用

如果您的套件符合所有 shell 需求，您可以在裝置參數下將 *ShowInShell* 值設定為1，讓您的裝置顯示在 shell 中。 如需詳細資訊，請參閱 [裝置參數](device-parameters.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**建立服務提供者**](creating-a-service-provider.md)
</dt> </dl>

 

 




