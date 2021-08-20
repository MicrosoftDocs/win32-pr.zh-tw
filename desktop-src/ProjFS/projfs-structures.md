---
title: ProjFS 結構
description: 下列結構是在 projectedfslib 中宣告。
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 9524b1244406c1de129ed0056fa6e2f3f7b0cb10552087e2d06639d168bb1d13
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117792419"
---
# <a name="projfs-structures"></a>ProjFS 結構

下列結構是在 projectedfslib 中宣告。

## <a name="in-this-section"></a>本節內容

| 主題 | 描述 |
|-|-|
| [**PRJ_CALLBACK_DATA**](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_callback_data) | 針對每個作業回呼，定義傳遞給提供者的標準資訊。 |
| [**PRJ_CALLBACKS**](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_callbacks) | 一組指標，可讓提供者儲存其回呼常式的實作為位置。 |
| [**PRJ_COMPLETE_COMMAND_EXTENDED_PARAMETERS**](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_complete_command_extended_parameters) | 指定完成某些回呼所需的參數。 |
| [**PRJ_FILE_BASIC_INFO**](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_file_basic_info) | 專案的基本資訊。 |
| [**PRJ_NOTIFICATION_MAPPING**](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_notification_mapping) | 描述通知對應，也就是目錄 (稱為「通知根目錄」 ) 和一組通知（以位遮罩表示）之間的配對。 |
| [**PRJ_NOTIFICATION_PARAMETERS**](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_notification_parameters) | 通知的額外參數。 |
| [**PRJ_PLACEHOLDER_INFO**](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_info) | 預留位置檔案或目錄的元資料緩衝區。 |
| [**PRJ_PLACEHOLDER_VERSION_INFO**](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_placeholder_version_info) | 可唯一識別預留位置檔案內容的資訊。 |
| [**PRJ_STARTVIRTUALIZING_OPTIONS**](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_startvirtualizing_options) | 啟動虛擬化實例時要提供的選項。 |
| [**PRJ_VIRTUALIZATION_INSTANCE_INFO**](/windows/win32/api/projectedfslib/ns-projectedfslib-prj_virtualization_instance_info) | 虛擬化實例的相關資訊。 |
