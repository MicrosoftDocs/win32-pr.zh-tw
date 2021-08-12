---
title: 用於追蹤安裝進度的登錄專案
description: 用於追蹤安裝進度的登錄專案
ms.assetid: 898f9117-94fd-4230-9378-b8c6a4401a96
keywords:
- Windows Media Player，追蹤安裝進度
- Windows Media Player，安裝進度追蹤
- Windows Media Player，安裝進度追蹤
- Windows Media Player，登錄
- 登錄，追蹤安裝進度
- 登錄，安裝進度追蹤
- 登錄，安裝進度追蹤
- 登錄，Windows Media Player 的設定
- 追蹤安裝進度
- 正在安裝進度追蹤
- 安裝進度追蹤
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7febb9f25a04c5e4358e891f963ab6a8569cfd6facef7e4f2072807bd09e2605
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118570299"
---
# <a name="registry-entries-for-tracking-installation-progress"></a>用於追蹤安裝進度的登錄專案

安裝程式wm.exe Windows Media Player 11 安裝程式 \_ 會在登錄中寫入下列專案，讓安裝程式可以在執行 Windows Media Player 安裝程式時追蹤其進度。


```C++
[HKEY_LOCAL_MACHINE\Software\Microsoft\MediaPlayer\Setup]
"Progress_CurrentDialog" = dword:value
"Progress_MaxDialog" = dword:value
"Progress_CurrentInstall" = dword:value
"Progress_MaxInstall" = dword:value
```



在上述的登錄語法中， *value* 是整數值的預留位置。

進度 \_ CurrentDialog 指出目前顯示 Windows Media Player 安裝程式的對話方塊。 進度 \_ MaxDialog 指出 Windows 媒體將顯示的對話方塊總數。 例如，如果進度 \_ CurrentDialog = 2 和進度 \_ MaxDialog = 5，Windows Media Player 目前會以五的序列顯示第二個對話方塊。

進度 \_ CurrentInstall 和進度 \_ MaxInstall 會合在一起，指出目前對話方塊完成的百分比。 例如，如果進度 \_ CurrentInstall = 6 且進度 \_ MaxInstall = 25，則目前的對話是 6/25 (也就是 24% ) 完成。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**登錄設定**](registry-settings.md)
</dt> </dl>

 

 




