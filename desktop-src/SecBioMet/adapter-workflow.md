---
title: 介面卡工作流程
description: 本節說明從介面卡外掛程式的角度來看的註冊工作流程。
ms.assetid: 0392124A-78CF-49E3-A52A-1E2E3A100E2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e79d018cfc853e8b92c1e9bd5400526fe0d425c7
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122466015"
---
# <a name="adapter-workflow"></a>介面卡工作流程

本節說明從介面卡外掛程式的角度來看的註冊工作流程。

在 Windows 10 中，我們已執行 V4 引擎介面，提供2個新的引擎介面卡函式， [**EngineAdapterCreateKey**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn)和 [**EngineAdapterIdentifyFeatureSetSecure**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn)。 這些新功能可支援使用 TPM 2.0 的安全生物特徵辨識。 下表顯示介面卡端註冊工作流程。




| | |用戶端 API |介面卡方法 | |<a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>WinBioGetProperty (EXTENDED_ENGINE_INFO) </strong></a>  | <a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_info_fn"><strong>EngineAdapterQueryExtendedInfo</strong></a> | |<a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin"><strong>WinBioEnrollBegin</strong></a> | <ol><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn"><strong>StorageAdapterQueryBySubject</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn"><strong>SensorAdapterClearCoNtext</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearCoNtext</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearCoNtext</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_enrollment_fn"><strong>EngineAdapterCreateEnrollment</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn"><strong>EngineAdapterSetEnrollmentParameters</strong></a></li></ol> | |<a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture"> <strong>WinBioEnrollCapture</strong></a> | <ol><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn"><strong>SensorAdapterStartCapture</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn"><strong>SensorAdapterFinishCapture</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn"><strong>SensorAdapterPushDataToEngine</strong></a><strong>[- &gt; </strong> <a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn"><strong>EngineAdapterAcceptSampleData</strong></a>]</li><li>若 S_OK 或 WINBIO_I_MORE_DATA<ol><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn"><strong>EngineAdapterUpdateEnrollment</strong></a></li><li>[呼叫者繼續註冊]</li></ol></li><li>否則如果 WINBIO_E_BAD_CAPTURE [呼叫者顯示拒絕意見反應，則會繼續註冊] <br /></li><li>否則，則為其他錯誤<ol><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearCoNtext</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearCoNtext</strong></a></li><li>[Bio 服務中止註冊]</li></ol></li></ol> | |<a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>WinBioGetProperty (EXTENDED_ENROLLMENT_STATUS) </strong></a>  | <a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_enrollment_status_fn"><strong>EngineAdapterQueryExtendedEnrollmentStatus</strong></a> | |<a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit"><strong>WinBioEnrollCommit</strong></a> | <ol><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_check_for_duplicate_fn"><strong>EngineAdapterCheckForDuplicate</strong></a></li><li>如果可移動資料庫<ol><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn"><strong>EngineAdapterGetEnrollmentHash</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>EngineAdapterCommitEnrollment</strong></a></li></ol></li><li>否則<a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>EngineAdapterCommitEnrollment</strong></a><br /></li></ol> | |<a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard"> <strong>WinBioEnrollDiscard</strong></a> | <ol><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn"><strong>EngineAdapterDiscardEnrollment</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearCoNtext</strong></a></li><li><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearCoNtext</strong></a></li></ol> | 




 

 

 





