---
title: ConvertPluginCLSID 子機碼
description: ConvertPluginCLSID 子機碼
ms.assetid: 2bf5b6ad-31e9-40c2-a682-c7ad813e8f7a
keywords:
- Windows Media Player，ConvertPluginCLSID 子機碼
- Windows Media Player、副檔名
- Windows Media Player，登錄
- 登錄、副檔名
- registry，ConvertPluginCLSID 子機碼
- 登錄，Windows Media Player 的設定
- 副檔名登錄設定
- ConvertPluginCLSID 子機碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4229617c3999708d89fac976e94b2747b5a69145
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021541"
---
# <a name="convertpluginclsid-subkey"></a>ConvertPluginCLSID 子機碼

當 Windows Media Player 11 遇到自訂副檔名時，它會尋找符合擴充功能的登錄子機碼。 此子機碼描述于副檔名登錄 [設定](file-name-extension-registry-settings.md)中。 在某些情況下，延伸的子機碼具有名為 **ConvertPluginCLSID** 的子機碼。

例如，假設您已建立副檔名為 (的自訂檔案格式。 xyz) 和轉換外掛程式，可將檔案轉換成 Windows Media Player 所支援的格式，然後您可以在下列其中一或兩個子機碼中儲存外掛程式的類別識別碼。

**HKEY \_ 本機 \_ 電腦 \\ 軟體 \\ Microsoft \\ 多媒體 \\ WMPlayer \\ 擴充功能 \\ 。 xyz \\ ConvertPluginCLSID**

**HKEY \_ 目前的 \_ 使用者 \\ 軟體 \\ Microsoft \\ MediaPlayer \\ Player 擴充功能 \\ \\ 。 xyz \\ ConvertPluginCLSID**

**ConvertPluginCLSID** 子機碼會指定外掛程式的類別識別碼，Windows Media Player 可以用來將媒體檔案從其自訂格式轉換為播放程式所支援的格式。

**ConvertPluginCLSID** 子機碼具有下列專案。

-   代表預設轉換外掛程式的預設專案。
-   代表預設轉換外掛程式的已命名專案。
-   代表替代轉換外掛程式的其他已命名專案。

例如，假設自訂檔案格式具有預設轉換外掛程式和兩個替代的轉換外掛程式。 **ConvertPluginCLSID** 子機碼底下的登錄專案會有下列格式。



| 名稱                                                                          | 類型        | 值                                                                |
|-------------------------------------------------------------------------------|-------------|----------------------------------------------------------------------|
| 預設                                                                       | **REG \_ SZ** | 預設轉換外掛程式的類別識別碼（登錄格式）。 |
| 預設轉換外掛程式的類別識別碼（登錄格式）。          | **REG \_ SZ** | 預設轉換外掛程式的易記名稱。                 |
| 第一個替代轉換外掛程式的類別識別碼（登錄格式）。  | **REG \_ SZ** | 第一個替代轉換外掛程式的易記名稱。         |
| 第二個替代轉換外掛程式的類別識別碼（登錄格式）。 | **REG \_ SZ** | 第二個替代轉換外掛程式的易記名稱。        |



 

請注意，預設的轉換外掛程式會以兩個登錄專案表示：預設專案和已命名的專案。 Windows Media Player 使用預設專案來判斷哪個外掛程式是主要) 轉換外掛程式的預設 (。 Windows Media Player 會使用已命名的專案來取得所有轉換外掛程式的易記名稱，包括預設外掛程式。

轉換外掛程式的易記名稱是由建立外掛程式的公司所決定。 Windows Media Player 可能會在其使用者介面中顯示易記名稱。

當 Windows Media Player 嘗試將檔案從自訂格式轉換成標準格式時，會先載入預設外掛程式。 如果預設外掛程式無法轉換檔案，並傳回 NS \_ E \_ WMP \_ convert \_ 外掛程式 \_ 未知的檔案擁有者 \_ \_ ，則 Player 會載入每個替代外掛程式，直到成功轉換或沒有其他外掛程式可供嘗試為止。 如果找不到副檔名的轉換外掛程式，播放程式就不會顯示警告訊息。

Windows Media Player 11 支援 **ConvertPluginCLSID** 登錄專案。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**副檔名登錄設定**](file-name-extension-registry-settings.md)
</dt> <dt>

[**Windows Media Player 轉換外掛程式**](windows-media-player-conversion-plug-ins.md)
</dt> </dl>

 

 




