---
description: 如果每一電腦的系統原則設定為大於0的值，Windows Installer 將修補程式套用至應用程式時，會將舊版本的檔案儲存在快取中。
ms.assetid: 986cd521-6907-420d-a2e9-5e0da0069834
title: MaxPatchCacheSize
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b8d9930f4a52d3ea0126a19d4dfadae359321f56
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104469217"
---
# <a name="maxpatchcachesize"></a>MaxPatchCacheSize

如果每一電腦的 [系統原則](system-policy.md) 設定為大於0的值，Windows Installer 將修補程式套用至應用程式時，會將舊版本的檔案儲存在快取中。 快取可能會增加未來安裝的效能，否則需要從原始應用程式來源取得舊的檔案。

MaxPatchCacheSize 原則的值是安裝程式可用於快取舊檔案的磁碟空間的最大百分比。 例如，值20表示不超過20% 的使用。 如果快取的總大小達到指定的磁碟空間百分比，則不會將其他檔案儲存至快取。 原則不會影響已儲存的檔案。

如果 MaxPatchCacheSize 原則的值設定為0，則不會儲存其他檔案。

如果未設定 MaxPatchCacheSize 原則，預設值為10，且最多可以使用10% 的磁碟空間來儲存舊檔案。

## <a name="registry-key"></a>登錄金鑰

**HKEY \_本機 \_ 電腦** \\ **軟體** \\ **原則** \\ **Microsoft** \\ **Windows** \\ **Installer**

## <a name="data-type"></a>資料類型

**REG \_ DWORD**

## <a name="related-topics"></a>相關主題

<dl> <dt>

[Windows Installer 2.0 及更早版本不支援](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 



