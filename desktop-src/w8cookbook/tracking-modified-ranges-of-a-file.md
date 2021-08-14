---
title: 追蹤檔案的修改範圍
description: 追蹤檔案的修改範圍
ms.assetid: 756881E9-EFD0-42FE-9B1C-4A2EF1998D71
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 6998d2706cd4d8bdb4e94b95fd0e617dbbf4e3a1b288d33dbcebe5528d544c07
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117852025"
---
# <a name="tracking-modified-ranges-of-a-file"></a>追蹤檔案的修改範圍

## <a name="platforms"></a>平台

**用戶端-** Windows 8.1 (所有 sku)   
**伺服器-** Windows Server 2012 R2  

## <a name="description"></a>Description

NT 檔案系統 (NTFS) 小組已將新功能新增至 Windows。 USN 日誌會將更新序號輸出 (USN) 記錄，其中包含關閉時檔案的修改範圍。 引進了新的記錄類型，已 \_ 引進 USN 記錄 \_ V4 來記錄這些變更的檔案範圍。

預設不會啟用此功能;使用者必須叫用檔案系統控制項 (FSCTL) 命令才能啟用它。 不過，因為其他 Windows 元件可能會開啟範圍追蹤，所以使用者和開發人員可能會察覺到功能一律為啟用狀態。 Windows 可讓開發人員查詢 USN 日誌，以找出是否已啟用範圍追蹤。

MSDN 檔將于稍後提供，以指示開發人員如何存取 USN \_ 記錄 \_ V4 記錄。

## <a name="manifestation"></a>表現

所有使用 USN 日誌的現有應用程式將繼續正常運作，而不會有任何相容性問題。

 

 




