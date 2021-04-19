---
description: 類似于命令列參數。 不過，您不需要在 \# 每次編譯 MOF 檔案時重新輸入 pragma 命令。
ms.assetid: 3cf22686-dd56-43a3-9584-3d707a20a3a0
ms.tgt_platform: multiple
title: '#pragma'
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 62ae13d5f960e0b415f34dce97a40cff6cba8056
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106991915"
---
# <a name="pragma"></a>\#pragma

**\# Pragma** 預處理器命令類似于命令列參數。 不過，您不需要在每次編譯 MOF 檔案時重新輸入 **\# pragma** 命令。 下列範例說明 **\# pragma** 命令語法：


```mof
#pragma [command]
```



您通常會在 MOF 檔案的開頭放置 **\# pragma** 命令。 不過，您可以將一些命令（例如 **\# pragma** 命令）放在您的 MOF 程式碼主體中。 下列範例會顯示 **\# pragma** 命令，指出 MOF 編譯器必須將類別和實例放在根 \\ cimv2 命名空間中，並且編譯儲存機制復原期間包含命令的檔案：


```mof
#pragma autorecover
#pragma namespace ("\\\\.\\root\\cimv2")
```



以下列出可用的 **\# pragma** 命令。



| 命令                                         | 描述                                                                                           |
|-------------------------------------------------|-------------------------------------------------------------------------------------------------------|
| [**修訂**](pragma-amendment.md)           | 指示 MOF 編譯器將 MOF 檔案分隔成非語言相關和語言特定版本。 |
| [**自動**](pragma-autorecover.md)       | 將 MOF 檔案新增至儲存機制復原期間所編譯的檔案清單。                             |
| [**classflags**](pragma-classflags.md)         | 根據指定的旗標，控制建立或更新類別的方式。                     |
| [**deleteclass**](pragma-deleteclass.md)       | 從存放庫中刪除現有的類別及其實例。                                      |
| [**路經**](pragma-deleteinstance.md) | 從存放庫中刪除類別的現有實例。                                          |
| [**instanceflags**](pragma-instanceflags.md)   | 根據指定的旗標，控制建立或更新實例的方式。                   |
| [**命名 空間**](pragma-namespace.md)           | 要求編譯器將 MOF 檔案載入至指定為 *namespacepath* 的命名空間。         |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[預處理器命令](preprocessor-commands.md)
</dt> </dl>

 

 



