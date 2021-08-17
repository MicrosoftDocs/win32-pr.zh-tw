---
description: 啟用內容函式和結構會搭配並存元件使用。
ms.assetid: b53b30e0-948e-406c-9fb4-9681dc3c5670
title: 啟用內容參考
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 72eb4bc136a95766a62bb96e67ac198f88fca905c60ba98e6bf922ce65a36389
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119142581"
---
# <a name="activation-context-reference"></a>啟用內容參考

啟用內容函式和結構會搭配並存元件使用。

下表列出啟用內容函數。



| 函式                                                   | 描述                                                                                                                                             |
|------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ActivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-activateactctx)                   | 啟用指定的啟用內容。                                                                                                             |
| [**AddRefActCtx**](/windows/desktop/api/Winbase/nf-winbase-addrefactctx)                       | 遞增指定之啟用內容的參考計數。                                                                                     |
| [**CreateActCtx**](/windows/desktop/api/Winbase/nf-winbase-createactctxa)                       | 建立啟用內容。                                                                                                                          |
| [**DeactivateActCtx**](/windows/desktop/api/Winbase/nf-winbase-deactivateactctx)               | 停用指定的啟用內容。                                                                                                           |
| [**FindActCtxSectionGuid**](/windows/desktop/api/Winbase/nf-winbase-findactctxsectionguid)     | 傳回 [**ACTCTX 區段中所包含 \_ \_ \_**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data) 的資料，此資料結構與指定的 GUID 對應。   |
| [**FindActCtxSectionString**](/windows/desktop/api/Winbase/nf-winbase-findactctxsectionstringa) | 傳回 [**ACTCTX 區段中所包含 \_ \_ \_**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data) 的資料，此資料結構與指定的字串對應。 |
| [**GetCurrentActCtx**](/windows/desktop/api/Winbase/nf-winbase-getcurrentactctx)               | 傳回目前的啟用內容。                                                                                                                 |
| [**IsolationAwareCleanup**](/previous-versions/windows/desktop/legacy/aa375204(v=vs.85))     | 確保在載入、卸載和重載資訊清單時，會釋放記憶體。                                                                         |
| [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw)                       | 查詢啟用內容以取得元件或檔案的相關資訊。                                                                               |
| [**QueryActCtxSettingsW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxsettingsw)       | 指定要查詢之屬性的命名空間和屬性名稱。                                                                      |
| [**ReleaseActCtx**](/windows/desktop/api/Winbase/nf-winbase-releaseactctx)                     | 遞減指定之啟用內容的參考計數。                                                                                     |
| [**ZombifyActCtx**](/windows/desktop/api/Winbase/nf-winbase-zombifyactctx)                     | 停用指定的啟用內容，但不將它解除配置。                                                                               |



 

下表列出啟用內容結構。



| 結構                                                                                                        | 描述                                                                                                                                                                                                                                                                                                                                                                                  |
|------------------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**啟用 \_ 內容 \_ 元件 \_ 詳細 \_ 資訊**](/windows/desktop/api/Winnt/ns-winnt-activation_context_assembly_detailed_information) | 包含啟用內容的詳細資訊。                                                                                                                                                                                                                                                                                                                                  |
| [**啟用 \_ 內容 \_ 詳細 \_ 資訊**](/windows/desktop/api/Winnt/ns-winnt-activation_context_detailed_information)                    | 包含啟用內容中元件的相關資訊。                                                                                                                                                                                                                                                                                                                           |
| [**啟用 \_ 內容 \_ 查詢 \_ 索引**](/windows/desktop/api/Winnt/ns-winnt-activation_context_query_index)                                      | 包含啟用內容中的元件，以及元件內檔案的索引。                                                                                                                                                                                                                                                                                           |
| [**ACTCTX**](/windows/win32/api/winbase/ns-winbase-actctxa)                                                                                     | 包含描述特定啟用內容的資訊。                                                                                                                                                                                                                                                                                                                           |
| [**ACTCTX \_ 區段 \_ 索引 \_ 資料**](/windows/win32/api/winbase/ns-winbase-actctx_section_keyed_data)                                            | 傳回啟用內容資訊以及 GUID 或32位整數標記的啟用內容區段。                                                                                                                                                                                                                                                                   |
| [**元件 \_ 檔 \_ 詳細 \_ 資訊**](/windows/desktop/api/Winnt/ns-winnt-assembly_file_detailed_information)                              | 包含啟用內容中元件檔案的相關資訊。                                                                                                                                                                                                                                                                                                                 |
| [**啟用 \_ 內容 \_ 執行 \_ 層級 \_ 資訊**](/windows/desktop/api/Winnt/ns-winnt-activation_context_run_level_information)                 | 由 [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) 函式使用。<br/> **Windows Server 2003 和 Windows XP：** 無法使用此結構。<br/>                                                                                                                                                                                                                                    |
| [**相容性 \_ 內容 \_ 元素**](/windows/desktop/api/Winnt/ns-winnt-compatibility_context_element)                                         | 供 [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) 函式使用，作為 [**啟用 \_ 內容 \_ 相容性 \_ 資訊**](/windows/desktop/api/Winnt/ns-winnt-activation_context_compatibility_information) 結構的一部分。 <br/> **Windows Server 2008 及更早版本，以及 Windows Vista 及更早版本：** 無法使用此結構。 從 Windows Server 2008 R2 和 Windows 7 開始提供。<br/> |
| [**啟用 \_ 內容 \_ 相容性 \_ 資訊**](/windows/desktop/api/Winnt/ns-winnt-activation_context_compatibility_information)          | 由 [**QueryActCtxW**](/windows/desktop/api/Winbase/nf-winbase-queryactctxw) 函式使用。<br/> **Windows Server 2008 及更早版本，以及 Windows Vista 及更早版本：** 無法使用此結構。 從 Windows Server 2008 R2 和 Windows 7 開始提供。<br/>                                                                                                                                   |



 

下表列出啟用內容列舉。

| 列舉型別                                                                       | 描述                                                                                                                                                                                                                                            |
|-----------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**ACTCTX \_ 要求的 \_ 執行 \_ 層級**](/windows/desktop/api/Winnt/ne-winnt-actctx_requested_run_level)               | 描述啟用內容所要求的執行層級。**Windows Server 2003 和 Windows XP：** 無法使用這個列舉。<br/>                                                                                                      |
| [**ACTCTX \_ 相容性 \_ 元素 \_ 類型**](/windows/desktop/api/Winnt/ne-winnt-actctx_compatibility_element_type) | 描述應用程式資訊清單中的相容性元素。**Windows Server 2008 及更早版本，以及 Windows Vista 及更早版本：** 無法使用這個列舉。 從 Windows Server 2008 R2 和 Windows 7 開始提供。<br/> |



 

 

