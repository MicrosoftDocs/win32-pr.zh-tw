---
title: 引擎介面卡包裝函式
description: 您可以用來在引擎介面卡上呼叫函式的函式。 這些函式定義于 Winbio \_ adapter. h 中。
ms.assetid: b3d6d617-e423-4ed5-9d29-be72c5dd8b49
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9c5ec0fcc3b6ea358e8238061bc74e2933d8bf87
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968445"
---
# <a name="engine-adapter-wrappers"></a>引擎介面卡包裝函式

下列包裝函式是在 Winbio \_ adapter. h 中定義。 您可以使用它們來呼叫引擎介面卡上的函式。



| 函式                                           | 描述                                                                                                                                                                                           |
|----------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| WbioEngineAcceptSampleData<br/>              | 呼叫 [**EngineAdapterAcceptSampleData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn) 函數。<br/>                                                                                                 |
| WbioEngineActivate<br/>                      | 呼叫 [**EngineAdapterActivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_activate_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/>                                           |
| WbioEngineAttach<br/>                        | 呼叫 [**EngineAdapterAttach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_attach_fn) 函數。<br/>                                                                                                                     |
| WbioEngineCheckForDuplicate<br/>             | 呼叫 [**EngineAdapterCheckForDuplicate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_check_for_duplicate_fn) 函數。<br/>                                                                                               |
| WbioEngineClearCoNtext<br/>                  | 呼叫 [**EngineAdapterClearCoNtext**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn) 函數。<br/>                                                                                                         |
| WbioEngineCommitEnrollment<br/>              | 呼叫 [**EngineAdapterCommitEnrollment**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn) 函數。<br/>                                                                                                 |
| WbioEngineControlUnit<br/>                   | 呼叫 [**EngineAdapterControlUnit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_control_unit_fn) 函數。<br/>                                                                                                           |
| WbioEngineControlUnitPrivileged<br/>         | 呼叫 [**EngineAdapterControlUnitPrivileged**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_control_unit_privileged_fn) 函數。<br/>                                                                                       |
| WbioEngineCreateEnrollment<br/>              | 呼叫 [**EngineAdapterCreateEnrollment**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_enrollment_fn) 函數。<br/>                                                                                                 |
| WbioEngineDeactivate<br/>                    | 呼叫 [**EngineAdapterDeactivate**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_deactivate_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/>                                       |
| WbioEngineDetach<br/>                        | 呼叫 [**EngineAdapterDetach**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_detach_fn) 函數。<br/>                                                                                                                     |
| WbioEngineDiscardEnrollment<br/>             | 呼叫 [**EngineAdapterDiscardEnrollment**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn) 函數。<br/>                                                                                               |
| WbioEngineExportEngineData<br/>              | 呼叫 [**EngineAdapterExportEngineData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_export_engine_data_fn) 函數。<br/>                                                                                                 |
| WbioEngineGetEnrollmentHash<br/>             | 呼叫 [**EngineAdapterGetEnrollmentHash**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn) 函數。<br/>                                                                                               |
| WbioEngineGetEnrollmentStatus<br/>           | 呼叫 [**EngineAdapterGetEnrollmentStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_status_fn) 函數。<br/>                                                                                           |
| WbioEngineIdentifyAll<br/>                   | 呼叫 [**EngineAdapterIdentifyAll**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_all_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/>                                     |
| WbioEngineIdentifyFeatureSet<br/>            | 呼叫 [**EngineAdapterIdentifyFeatureSet**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_fn) 函數。<br/>                                                                                             |
| WbioEngineNotifyPowerChange<br/>             | 呼叫 [*EngineAdapterNotifyPowerChange*](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_notify_power_change_fn) 函數。<br/> 從 Windows 8 開始，支援這個包裝函式函數。<br/>                            |
| WbioEnginePipelineCleanup<br/>               | 呼叫 [**EngineAdapterPipelineCleanup**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_pipeline_cleanup_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/>                             |
| WbioEnginePipelineInit<br/>                  | 呼叫 [**EngineAdapterPipelineInit**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_pipeline_init_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/>                                   |
| WbioEngineQueryCalibrationData<br/>          | 呼叫 [**EngineAdapterQueryCalibrationData**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_calibration_data_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/>                   |
| WbioEngineQueryExtendedEnrollmentStatus<br/> | 呼叫 [**EngineAdapterQueryExtendedEnrollmentStatus**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_enrollment_status_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/> |
| WbioEngineQueryExtendedInfo<br/>             | 呼叫 [**EngineAdapterQueryExtendedInfo**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_info_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/>                         |
| WbioEngineQueryHashAlgorithms<br/>           | 呼叫 [**EngineAdapterQueryHashAlgorithms**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_hash_algorithms_fn) 函數。<br/>                                                                                           |
| WbioEngineQueryIndexVectorSize<br/>          | 呼叫 [**EngineAdapterQueryIndexVectorSize**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_index_vector_size_fn) 函數。<br/>                                                                                         |
| WbioEngineQueryPreferredFormat<br/>          | 呼叫 [**EngineAdapterQueryPreferredFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_preferred_format_fn) 函數。<br/>                                                                                         |
| WbioEngineQuerySampleHint<br/>               | 呼叫 [**EngineAdapterQuerySampleHint**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_sample_hint_fn) 函數。<br/>                                                                                                   |
| WbioEngineRefreshCache<br/>                  | 呼叫 [**EngineAdapterRefreshCache**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_refresh_cache_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/>                                   |
| WbioEngineSelectCalibrationFormat<br/>       | 呼叫 [**EngineAdapterSelectCalibrationFormat**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_select_calibration_format_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/>             |
| WbioEngineSetAccountPolicy<br/>              | 呼叫 [**EngineAdapterSetAccountPolicy**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_account_policy_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/>                           |
| WbioEngineSetEnrollmentParameters<br/>       | 呼叫 [**EngineAdapterSetEnrollmentParameters**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/>             |
| WbioEngineSetEnrollmentSelector<br/>         | 呼叫 [**EngineAdapterSetEnrollmentSelector**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_selector_fn) 函數。<br/> 從 Windows 10 開始，支援這個包裝函式函數。<br/>                 |
| WbioEngineSetHashAlgorithm<br/>              | 呼叫 [**EngineAdapterSetHashAlgorithm**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_hash_algorithm_fn) 函數。<br/>                                                                                                 |
| WbioEngineUpdateEnrollment<br/>              | 呼叫 [**EngineAdapterUpdateEnrollment**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn) 函數。<br/>                                                                                                 |
| WbioEngineVerifyFeatureSet<br/>              | 呼叫 [**EngineAdapterVerifyFeatureSet**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_verify_feature_set_fn) 函數。<br/>                                                                                                 |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[引擎介面卡功能](engine-adapter-functions.md)
</dt> <dt>

[外掛程式函數](plug-in-functions.md)
</dt> </dl>

 

 





