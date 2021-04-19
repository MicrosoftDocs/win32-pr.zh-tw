---
description: 下列結構是用來建立和維護預留位置檔案和目錄。
ms.assetid: 50CCA8F5-7118-48E8-ADBF-337798FAF549
title: 雲端篩選結構
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: eebe6623ad3d9d348d624f8ab8da3427416d4742
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966652"
---
# <a name="cloud-filter-structures"></a>雲端篩選結構

下列結構是用來建立和維護預留位置檔案和目錄。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                   | 描述                                                                                                                               |
|-----------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------|
| [**CF \_ 回呼 \_ 資訊**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_info)<br/>                          | 包含一般回呼資訊。<br/>                                                                                          |
| [**CF \_ 回呼 \_ 參數**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_parameters)<br/>              | 包含回呼特定的參數，例如檔案位移、長度、旗標等。<br/>                                                 |
| [**CF \_ 回呼 \_ 註冊**](/windows/desktop/api/cfapi/ns-cfapi-cf_callback_registration)<br/>          | 要由同步處理提供者註冊的回呼。<br/>                                                                           |
| [**CF \_ 檔 \_ 範圍**](/windows/desktop/api/cfapi/ns-cfapi-cf_file_range)<br/>                                | 指定預留位置檔案中的資料範圍。<br/>                                                                               |
| [**CF \_ 檔 \_ 範圍 \_ 緩衝區**](/previous-versions/windows/desktop/legacy/mt844616(v=vs.85))<br/>                | 描述檔案中的位置和資料範圍的結構。<br/>                                                              |
| [**CF \_ FS \_ 中繼資料**](/windows/desktop/api/cfapi/ns-cfapi-cf_fs_metadata)<br/>                              | 預留位置檔案或目錄中繼資料。<br/>                                                                                        |
| [**CF \_ 序列化 \_ 原則**](/windows/desktop/api/cfapi/ns-cfapi-cf_hydration_policy)<br/>                    | 指定主要序列化原則與其修飾詞。<br/>                                                                       |
| [**CF \_ 操作 \_ 資訊**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_info)<br/>                        | 預留位置檔案或資料夾上之作業的相關資訊。<br/>                                                                |
| [**CF \_ 操作 \_ 參數**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_parameters)<br/>            | 預留位置檔案或資料夾上之作業的參數。<br/>                                                                    |
| [**CF \_ 預留位置 \_ 基本 \_ 資訊**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_basic_info)<br/>       | 基本預留位置資訊。<br/>                                                                                                 |
| [**CF \_ 預留位置 \_ 建立 \_ 資訊**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_create_info)<br/>     | 包含用來建立新預留位置檔案或目錄的預留位置資訊。 <br/>                                           |
| [**CF \_ 預留位置 \_ 標準 \_ 資訊**](/windows/desktop/api/cfapi/ns-cfapi-cf_placeholder_standard_info)<br/> | 標準預留位置資訊。<br/>                                                                                              |
| [**CF \_ 平臺 \_ 資訊**](/windows/desktop/api/cfapi/ns-cfapi-cf_platform_info)<br/>                          | 傳回雲端檔案平臺的資訊。 這適用于在多個 Windows 版本上執行的同步處理提供者。<br/> |
| [**CF \_ 人口 \_ 原則**](/windows/desktop/api/cfapi/ns-cfapi-cf_population_policy)<br/>                  | 指定主要人口原則和其修飾詞。<br/>                                                                      |
| [**CF \_ 流程 \_ 資訊**](/windows/desktop/api/cfapi/ns-cfapi-cf_process_info)<br/>                            | 包含使用者進程的相關資訊。<br/>                                                                                     |
| [**CF \_ 同步 \_ 原則**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_policies)<br/>                          | 定義同步根所使用的同步處理原則。<br/>                                                                                 |
| [**CF \_ 同步 \_ 註冊**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_registration)<br/>                  | 要註冊之同步處理提供者和同步根的詳細資料。<br/>                                                               |
| [**CF \_ 同步 \_ 根 \_ 基本 \_ 資訊**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_basic_info)<br/>          | 基本同步根資訊。<br/>                                                                                                   |
| [**CF \_ 同步 \_ 根 \_ 提供者 \_ 資訊**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_provider_info)<br/>    | 同步根提供者資訊。<br/>                                                                                                |
| [**CF \_ 同步 \_ 根 \_ 標準 \_ 資訊**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_root_standard_info)<br/>    | 標準同步根資訊。<br/>                                                                                                |
| [**CF \_ 同步 \_ 狀態**](/windows/desktop/api/cfapi/ns-cfapi-cf_sync_status)<br/>                              | 用於 CF 作業 [**\_ \_ 資訊**](/windows/desktop/api/cfapi/ns-cfapi-cf_operation_info) 結構，以描述指定之同步根的狀態。<br/>     |



 

 

