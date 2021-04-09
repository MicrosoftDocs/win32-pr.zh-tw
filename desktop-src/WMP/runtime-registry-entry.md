---
title: 執行時間登錄專案
description: 執行時間登錄專案
ms.assetid: 3b2880f9-acb9-4a13-8364-67fbe76f8d29
keywords:
- Windows Media Player，執行時間登錄專案
- Windows Media Player、副檔名
- Windows Media Player，登錄
- 登錄、副檔名
- 登錄，執行時間專案
- 登錄，Windows Media Player 的設定
- 副檔名登錄設定
- 執行時間登錄專案
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b01a83c3642f49a9fdbe7f8c51f157a154a9843b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021693"
---
# <a name="runtime-registry-entry"></a>執行時間登錄專案

當 Windows Media Player 遇到自訂副檔名時，它會尋找符合擴充功能的登錄子機碼。 此子機碼描述于副檔名登錄 [設定](file-name-extension-registry-settings.md)中。 其中一個可出現在擴充功能子機碼底下的登錄專案是 **運行** 時間專案。

**運行** 時間專案會指定 Windows Media Player 可用來播放或轉換具有自訂延伸模組之數位媒體檔案的基礎技術。 **運行** 時間專案具有下列格式。



|          |                |                                                               |
|----------|----------------|---------------------------------------------------------------|
| **名稱** | **型別**       | **ReplTest1**                                                     |
| 執行階段  | **REG \_ DWORD** | 識別基礎技術的正整數。 |



 

**運行** 時間專案的值必須是下列其中一項。



| **值 (decimal)** | **說明**                                                                            |
|---------------------|--------------------------------------------------------------------------------------------|
| 6                   | 使用 Windows Media Format SDK 轉譯。                                                 |
| 7                   | 使用 Microsoft DirectShow 轉譯。                                                         |
| 13                  | 使用指定的轉換外掛程式來轉換檔案。 需要 Windows Media Player 11。 |



 

Windows Media Player 9 系列和更新版本支援 **運行** 時間登錄專案值6和7。 Windows Media Player 11 支援值13。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ConvertPluginCLSID 子機碼**](convertpluginclsid-subkey.md)
</dt> <dt>

[**副檔名登錄設定**](file-name-extension-registry-settings.md)
</dt> </dl>

 

 




