---
title: 引擎介面卡功能
description: 引擎介面卡會從已捕捉的範例產生生物特徵辨識範本、比對現有範本的範例和索引範本。
ms.assetid: d5f4683c-0613-493b-830f-0616ffa0694c
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9046ada411e997c0c6adba7f6c6dcaf6d8b654b6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104301720"
---
# <a name="engine-adapter-functions"></a>引擎介面卡功能

引擎介面卡會從已捕捉的範例產生生物特徵辨識範本、比對現有範本的範例和索引範本。 介面卡開發人員必須執行下列函數。 Windows 生物識別服務會呼叫它們。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                       | 描述                                                                                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**EngineAdapterCreateKey**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn)<br/>                                         | 由 Windows 生物特徵辨識架構呼叫，以將 HMAC 金鑰推送至感應器。 當架構呼叫 [**EngineAdapterIdentifyFeatureSetSecure**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn)時，傳回的金鑰識別碼會傳回給生物特徵辨識單位。 <br/>           |
| [**EngineAdapterAcceptSampleData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn)<br/>                           | 接受原始生物特徵辨識範例，並解壓縮功能集。<br/>                                                                                                                                                                                                                     |
| [**EngineAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_activate_fn)<br/>                                           | 讓引擎介面卡有機會執行任何需要的工作，讓感應器元件退出閒置狀態。<br/>                                                                                                                                                             |
| [**EngineAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_attach_fn)<br/>                                               | 將引擎介面卡新增至生物特徵辨識設備的處理管線。<br/>                                                                                                                                                                                                       |
| [**EngineAdapterCheckForDuplicate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_check_for_duplicate_fn)<br/>                         | 判斷管線中的新範本是否會複製已儲存在資料庫中的任何範本，而不管與範本相關聯的身分識別為何。<br/>                                                                                                              |
| [**EngineAdapterClearCoNtext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn)<br/>                                   | 準備新作業的生物特徵辨識單位處理管線。<br/>                                                                                                                                                                                                    |
| [**EngineAdapterCommitEnrollment**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn)<br/>                           | 完成註冊物件、將它轉換成範本，然後將範本儲存在資料庫中。<br/>                                                                                                                                                                            |
| [**EngineAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_control_unit_fn)<br/>                                     | 執行不需要較高許可權的廠商定義控制項作業。<br/>                                                                                                                                                                                          |
| [**EngineAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_control_unit_privileged_fn)<br/>                 | 執行需要更高許可權的廠商定義控制項作業。<br/>                                                                                                                                                                                                  |
| [**EngineAdapterCreateEnrollment**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_enrollment_fn)<br/>                           | 初始化生物特徵辨識單位管線中的註冊物件。<br/>                                                                                                                                                                                                              |
| [**EngineAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_deactivate_fn)<br/>                                       | 讓引擎介面卡有機會執行任何需要的工作，讓感應器元件進入閒置狀態。<br/>                                                                                                                                                                 |
| [**EngineAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_detach_fn)<br/>                                               | 釋放附加至管線的介面卡特定資源。<br/>                                                                                                                                                                                                                  |
| [**EngineAdapterDiscardEnrollment**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn)<br/>                         | 從管線中刪除中繼註冊狀態資訊。<br/>                                                                                                                                                                                                           |
| [**EngineAdapterExportEngineData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_export_engine_data_fn)<br/>                           | 從標準生物特徵辨識資訊記錄中，抓取引擎最近處理之功能集或範本的複本。<br/>                                                                                                                                            |
| [**EngineAdapterGetEnrollmentHash**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn)<br/>                         | 在管線中抓取已完成註冊範本的雜湊。<br/>                                                                                                                                                                                                       |
| [**EngineAdapterGetEnrollmentStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_status_fn)<br/>                     | 判斷註冊物件是否已準備好認可至管線。<br/>                                                                                                                                                                                             |
| [**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn)<br/>                                     | 決定目前位於相機框架中之任何人的身分識別。<br/>                                                                                                                                                                                                     |
| [**EngineAdapterIdentifyFeatureSet**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_fn)<br/>                       | 從目前的功能集建立範本，並在資料庫中尋找相符的範本。<br/>                                                                                                                                                                                |
| [**EngineAdapterIdentifyFeatureSetSecure**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn)<br/>           | 由 Windows 生物特徵辨識架構呼叫，以從目前的功能集建立範本，並在資料庫中找出相符的範本。 如果找不到相符項，引擎介面卡就必須填滿身分 *識別*、 *SubFactor*、 *授權* 和 *AuthorizationSize* 欄位。<br/> |
| [*EngineAdapterNotifyPowerChange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_notify_power_change_fn)<br/>                           | 接收有關電腦電源狀態變更的通知，並據以準備引擎介面卡。<br/>                                                                                                                                                                  |
| [**EngineAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_pipeline_cleanup_fn)<br/>                             | 讓引擎介面卡有機會執行需要儲存體介面卡協助的任何清除。<br/>                                                                                                                                                                        |
| [**EngineAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_pipeline_init_fn)<br/>                                   | 讓引擎介面卡有機會執行任何未完成的初始化。<br/>                                                                                                                                                                                     |
| [**EngineAdapterQueryCalibrationData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_calibration_data_fn)<br/>                   | 從引擎介面卡取得一組預先捕獲的校正資料。<br/>                                                                                                                                                                                                           |
| [**EngineAdapterQueryExtendedEnrollmentStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_enrollment_status_fn)<br/> | 查詢 **WINBIO \_ 屬性 \_ 延伸 \_ 註冊 \_ 狀態** 屬性。<br/>                                                                                                                                                                                                       |
| [**EngineAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_info_fn)<br/>                         | 決定生物特徵辨識引擎元件的功能和限制。<br/>                                                                                                                                                                                                 |
| [**EngineAdapterQueryHashAlgorithms**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_hash_algorithms_fn)<br/>                     | 抓取物件識別碼的陣列，表示引擎介面卡支援的雜湊演算法。<br/>                                                                                                                                                                   |
| [**EngineAdapterQueryIndexVectorSize**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_index_vector_size_fn)<br/>                   | 抓取引擎介面卡所使用之索引向量的大小。<br/>                                                                                                                                                                                                             |
| [**EngineAdapterQueryPreferredFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_preferred_format_fn)<br/>                   | 決定引擎介面卡慣用的輸入資料格式。<br/>                                                                                                                                                                                                              |
| [**EngineAdapterQuerySampleHint**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_sample_hint_fn)<br/>                             | 抓取引擎介面卡用來建立註冊範本所需的正確樣本數。 <br/>                                                                                                                                                                   |
| [**EngineAdapterRefreshCache**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_refresh_cache_fn)<br/>                                   | 通知引擎介面卡應捨棄任何可能保留在記憶體中的快取範本。<br/>                                                                                                                                                                      |
| [**EngineAdapterSelectCalibrationFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_select_calibration_format_fn)<br/>             | 由 Windows 生物特徵辨識架構呼叫，以判斷引擎介面卡要使用的感應器介面卡校正格式。<br/>                                                                                                                                      |
| [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn)<br/>                           | 設定引擎介面卡所使用的擴充預設和個別使用者 lnk-antispoofing 原則。<br/>                                                                                                                                                                                       |
| [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn)<br/>             | 提供引擎介面卡有關註冊作業的其他資訊。<br/>                                                                                                                                                                                                 |
| [**EngineAdapterSetEnrollmentSelector**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_selector_fn)<br/>                 | 告知引擎介面卡要追蹤目前註冊作業的人員。<br/>                                                                                                                                                                                           |
| [**EngineAdapterSetHashAlgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn)<br/>                           | 選取用於後續作業的雜湊演算法。<br/>                                                                                                                                                                                                                     |
| [**EngineAdapterUpdateEnrollment**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn)<br/>                           | 將目前的功能集加入至註冊物件。<br/>                                                                                                                                                                                                                         |
| [**EngineAdapterVerifyFeatureSet**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_verify_feature_set_fn)<br/>                           | 比較目前功能集中的範本與資料庫中的特定範本。<br/>                                                                                                                                                                                     |
| [**WbioQueryEngineInterface**](/windows/desktop/api/Winbio_adapter/nf-winbio_adapter-wbioqueryengineinterface)<br/>                                     | 抓取引擎介面卡的 [**WINBIO \_ 引擎 \_ 介面**](/windows/desktop/api/Winbio_adapter/ns-winbio_adapter-winbio_engine_interface) 結構指標。<br/>                                                                                                                                                      |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[外掛程式函數](plug-in-functions.md)
</dt> </dl>

 

 





