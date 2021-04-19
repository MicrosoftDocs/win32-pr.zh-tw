---
title: 程式庫分類登錄專案
description: 程式庫分類登錄專案
ms.assetid: 3ef7d384-503f-4b8f-9f4b-e0ef3c56616b
keywords:
- Windows Media Player，程式庫
- Windows Media Player，分類登錄專案
- Windows Media Player、副檔名
- Windows Media Player，登錄
- 登錄、副檔名
- 登錄，程式庫分類專案
- 登錄，Windows Media Player 的設定
- 副檔名登錄設定
- 程式庫，分類登錄專案
- 程式庫，登錄
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e48ea1aacdd1e4c553a7e83bfdd711ff331c0878
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106965180"
---
# <a name="library-classification-registry-entries"></a>程式庫分類登錄專案

當 Windows Media Player 遇到具有自訂副檔名的媒體檔案時，它並不知道檔案是否應分類為音訊、影片或其他類型。 根據預設，Windows Media Player 會將這些檔案放在程式庫的其他媒體部分。

如果您的數位媒體檔案有自訂格式，您可以在使用者電腦上的登錄中放入兩個專案，以提供 Windows Media Player 的資訊，告訴您檔案在播放程式媒體櫃中的顯示位置。

其中一個專案會進入下列子機碼。

**HKEY \_ LOCAL \_ MACHINE \\ Software \\ Microsoft \\ MediaPlayer \\ MLS \\ Extensions**

登錄專案具有下列格式。



| Name                                                  | 資料類型   | 值                                      |
|-------------------------------------------------------|-------------|--------------------------------------------|
| 沒有句點 ( 的副檔名 ) 分隔符號 | **REG \_ SZ** | 指定程式庫位置的字串 |



 

另一個登錄專案會進入您所建立的下列子機碼。

**HKEY \_類別 \_ 根 \\** *customExtension*

其中 *customExtension* 是副檔名，包括點 (. ) 分隔符號。

登錄專案具有下列格式。



| Name          | 資料類型   | 值                                      |
|---------------|-------------|--------------------------------------------|
| PerceivedType | **REG \_ SZ** | 指定程式庫位置的字串 |



 

這兩個登錄專案都必須具有相同的值。 下表提供可能的值。



| 值 | 描述                                                                      |
|-------|----------------------------------------------------------------------------------|
| 音訊 | 具有自訂延伸模組的檔案會出現在文件庫的音樂部分。 |
| 影片 | 具有自訂延伸模組的檔案會出現在文件庫的影片部分。 |



 

例如，下列登錄專案會指定副檔名為的檔案。 xyz 將會出現在文件庫的音樂部分：


```C++

HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\MLS\Extensions
    xyz     REG_SZ     audio

HKEY_CLASSES_ROOT\.xyz
    PerceivedType     REG_SZ     audio

```



請注意，嘗試寫入使用者電腦上登錄的任何程式碼， \_ \_ 只有在目前的使用者具有系統管理許可權時，才可以寫入至 HKEY 本機電腦子樹。

下列 Windows Media Player 版本支援程式庫分類登錄專案。

-   Windows Media Player 9 系列（含修正程式823275）
-   Windows Media Player 10 和更新版本

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**副檔名登錄設定**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




