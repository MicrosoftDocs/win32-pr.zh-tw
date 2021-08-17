---
description: 硬體設定函式會取出處理器、硬體設定檔和鍵盤資訊等資訊。
ms.assetid: c6245571-428a-4965-b58c-24645ddca70d
title: 硬體組態
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e396b2d08b489e92c7a407ca892250135fdd3d174d16de50d0c2d75428a88dce
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117764416"
---
# <a name="hardware-configuration"></a>硬體組態

硬體設定函式會取出處理器、硬體設定檔和鍵盤資訊等資訊。

[**GetSystemInfo**](/windows/win32/api/sysinfoapi/nf-sysinfoapi-getsysteminfo)函式會取出處理器和記憶體資訊，例如頁面大小、原始設備製造商 (OEM) 識別碼、處理器數目和類型、應用程式位址範圍等等。 [**IsProcessorFeaturePresent**](/windows/win32/api/processthreadsapi/nf-processthreadsapi-isprocessorfeaturepresent)函式會抓取處理器所支援的浮點運算和指令集的相關資訊。

[**GetCurrentHwProfile**](/windows/desktop/api/Winbase/nf-winbase-getcurrenthwprofilea)函式會捕獲硬體設定檔的相關資訊。 硬體設定檔包含設定檔的銜接狀態、全域唯一識別碼 (GUID) 和顯示名稱等資訊。 [**GetKeyboardType**](/windows/desktop/api/winuser/nf-winuser-getkeyboardtype)函式會以鍵盤的類型和目前鍵盤上的函式索引鍵數目來抓取這類資訊。

 

 
