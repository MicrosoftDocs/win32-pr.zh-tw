---
title: 許可權登錄專案
description: 許可權登錄專案
ms.assetid: 01d55d2d-fe29-4006-a34b-9fbc730f9cbc
keywords:
- Windows Media Player、副檔名
- Windows Media Player，許可權
- Windows Media Player，登錄
- 登錄、副檔名
- 登錄，許可權
- 登錄，Windows Media Player 的設定
- 副檔名登錄設定
- 權限
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0aec86b4facec4babed4afed04ca342903670dbb
ms.sourcegitcommit: 48d1c892045445bcbd0f22bafa2fd3861ffaa6e7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/19/2020
ms.locfileid: "104023018"
---
# <a name="permissions-registry-entry"></a>許可權登錄專案

當 Windows Media Player 遇到自訂副檔名時，它會尋找符合擴充功能的登錄子機碼。 此子機碼描述于副檔名登錄 [設定](file-name-extension-registry-settings.md)中。 其中一個可出現在擴充功能子機碼底下的登錄專案是 **許可權** 專案。

**許可權** 專案指定允許在具有自訂延伸模組的檔案上執行 Windows Media Player 的動作。 **許可權** 專案具有下列格式。



| 名稱        | 類型           | 值                                                                  |
|-------------|----------------|------------------------------------------------------------------------|
| 權限 | **REG \_ DWORD** | 一組旗標，每個旗標都授與特定動作的許可權。 |



 

**許可權** 專案的值是下列其中一個或多個旗標的位 **or** 。



|  (decimal 值的旗標)  | 描述                                                                                                                                                                                                                                                                   |
|----------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 1                    | 播放的許可權。 可以播放具有已註冊之副檔名的檔案。                                                                                                                                                                                       |
| 2                    | 放置資料夾的許可權。 當使用者拖曳包含檔案的資料夾，並將它放在播放程式的使用者介面上時，所建立的播放清單中會包含已註冊之副檔名的檔案。                                                      |
| 4                    | 媒體 CD 的許可權。 當包含檔案的 CD 插入 cd-rom 光碟機時，會在建立的播放清單中包含已註冊副檔名的檔案。                                                                                           |
| 8                    | 程式庫的許可權。 具有已註冊之副檔名的檔案可以新增至程式庫。 轉換外掛程式的必要項。                                                                                                                                    |
| 16                   | HTML 串流的許可權。 從 Web 串流傳遞時，具有已註冊之副檔名的檔案將會插入 Internet Explorer 快取中。                                                                                                            |
| 128                  | 轉碼的許可權。 具有已註冊之副檔名的檔案，在特定情況下可以轉碼為 Windows Media 格式。 請參閱 [IWMPTranscodePolicy：： allowTranscode](/previous-versions/windows/desktop/api/wmpservices/nf-wmpservices-iwmptranscodepolicy-allowtranscode)。 需要 Windows Media Player 10 或更新版本。 |



 

當使用者嘗試播放具有自訂副檔名的媒體檔案時，Windows Media Player 會尋找符合延伸模組的登錄子機碼。 如果找不到相符項，播放程式會向使用者呈現警告對話方塊，提示使用者嘗試播放該檔案的許可權。 如果您使用自訂副檔名來建立數位媒體檔案，您可以註冊副檔名並提供 **許可權** 專案，以防止此警告出現在使用者的電腦上。

Windows Media Player 9 系列和更新版本支援旗標值 128) 以外的 **許可權** 專案 (。 Windows Media Player 10 和更新版本支援旗標值128。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**副檔名登錄設定**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




