---
title: 介面卡工作流程
description: 本節說明從介面卡外掛程式的角度來看的註冊工作流程。
ms.assetid: 0392124A-78CF-49E3-A52A-1E2E3A100E2E
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 68f93146e1d6cedd42094876547bfe0c945d6a7a
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106966407"
---
# <a name="adapter-workflow"></a><span data-ttu-id="60c1c-103">介面卡工作流程</span><span class="sxs-lookup"><span data-stu-id="60c1c-103">Adapter Workflow</span></span>

<span data-ttu-id="60c1c-104">本節說明從介面卡外掛程式的角度來看的註冊工作流程。</span><span class="sxs-lookup"><span data-stu-id="60c1c-104">This section describes the enrollment workflow from the perspective of the adapter plugins.</span></span>

<span data-ttu-id="60c1c-105">在 Windows 10 中，我們已執行 V4 引擎介面，提供2個新的引擎介面卡函式， [**EngineAdapterCreateKey**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn) 和 [**EngineAdapterIdentifyFeatureSetSecure**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn)。</span><span class="sxs-lookup"><span data-stu-id="60c1c-105">In Windows 10, we ve implemented a V4 engine interface that provides 2 new engine adapter functions, [**EngineAdapterCreateKey**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_key_fn) and [**EngineAdapterIdentifyFeatureSetSecure**](/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_identify_feature_set_secure_fn).</span></span> <span data-ttu-id="60c1c-106">這些新功能可支援使用 TPM 2.0 的安全生物特徵辨識。</span><span class="sxs-lookup"><span data-stu-id="60c1c-106">These new functions allow support for secure biometrics using TPM 2.0.</span></span> <span data-ttu-id="60c1c-107">下表顯示介面卡端註冊工作流程。</span><span class="sxs-lookup"><span data-stu-id="60c1c-107">The following table shows the adapter-side enrollment workflow.</span></span>



<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><span data-ttu-id="60c1c-108">用戶端 API</span><span class="sxs-lookup"><span data-stu-id="60c1c-108">Client API</span></span></td>
<td><span data-ttu-id="60c1c-109">介面卡方法</span><span class="sxs-lookup"><span data-stu-id="60c1c-109">Adapter Methods</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="60c1c-110"><a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>WinBioGetProperty (EXTENDED_ENGINE_INFO) </strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-110"><a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>WinBioGetProperty(EXTENDED_ENGINE_INFO)</strong></a></span></span></td>
<td><span data-ttu-id="60c1c-111"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_info_fn"><strong>EngineAdapterQueryExtendedInfo</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-111"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_info_fn"><strong>EngineAdapterQueryExtendedInfo</strong></a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="60c1c-112"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin"><strong>WinBioEnrollBegin</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-112"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin"><strong>WinBioEnrollBegin</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="60c1c-113"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn"><strong>StorageAdapterQueryBySubject</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-113"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_query_by_subject_fn"><strong>StorageAdapterQueryBySubject</strong></a></span></span></li>
<li><span data-ttu-id="60c1c-114"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn"><strong>SensorAdapterClearCoNtext</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-114"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_clear_context_fn"><strong>SensorAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="60c1c-115"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearCoNtext</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-115"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="60c1c-116"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearCoNtext</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-116"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="60c1c-117"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_enrollment_fn"><strong>EngineAdapterCreateEnrollment</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-117"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_create_enrollment_fn"><strong>EngineAdapterCreateEnrollment</strong></a></span></span></li>
<li><span data-ttu-id="60c1c-118"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn"><strong>EngineAdapterSetEnrollmentParameters</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-118"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_set_enrollment_parameters_fn"><strong>EngineAdapterSetEnrollmentParameters</strong></a></span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="60c1c-119"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture"><strong>WinBioEnrollCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-119"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture"><strong>WinBioEnrollCapture</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="60c1c-120"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn"><strong>SensorAdapterStartCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-120"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_start_capture_fn"><strong>SensorAdapterStartCapture</strong></a></span></span></li>
<li><span data-ttu-id="60c1c-121"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn"><strong>SensorAdapterFinishCapture</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-121"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_finish_capture_fn"><strong>SensorAdapterFinishCapture</strong></a></span></span></li>
<li><span data-ttu-id="60c1c-122"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn"><strong>SensorAdapterPushDataToEngine</strong></a><strong>[-></strong> <a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn"><strong>EngineAdapterAcceptSampleData</strong></a>]</span><span class="sxs-lookup"><span data-stu-id="60c1c-122"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_sensor_push_data_to_engine_fn"><strong>SensorAdapterPushDataToEngine</strong></a><strong>[-></strong><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_accept_sample_data_fn"><strong>EngineAdapterAcceptSampleData</strong></a>]</span></span></li>
<li><span data-ttu-id="60c1c-123">若 S_OK 或 WINBIO_I_MORE_DATA</span><span class="sxs-lookup"><span data-stu-id="60c1c-123">If S_OK or WINBIO_I_MORE_DATA</span></span>
<ol>
<li><span data-ttu-id="60c1c-124"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn"><strong>EngineAdapterUpdateEnrollment</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-124"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_update_enrollment_fn"><strong>EngineAdapterUpdateEnrollment</strong></a></span></span></li>
<li><span data-ttu-id="60c1c-125">[呼叫者繼續註冊]</span><span class="sxs-lookup"><span data-stu-id="60c1c-125">[Caller continues enrollment]</span></span></li>
</ol></li>
<li><span data-ttu-id="60c1c-126">否則如果 WINBIO_E_BAD_CAPTURE [呼叫者顯示拒絕意見反應，則會繼續註冊]</span><span class="sxs-lookup"><span data-stu-id="60c1c-126">Else if WINBIO_E_BAD_CAPTURE [Caller displays reject feedback, continues enrollment]</span></span> <br/></li>
<li><span data-ttu-id="60c1c-127">否則，則為其他錯誤</span><span class="sxs-lookup"><span data-stu-id="60c1c-127">Else if other ERROR</span></span>
<ol>
<li><span data-ttu-id="60c1c-128"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearCoNtext</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-128"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="60c1c-129"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearCoNtext</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-129"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="60c1c-130">[Bio 服務中止註冊]</span><span class="sxs-lookup"><span data-stu-id="60c1c-130">[Bio service aborts enrollment]</span></span></li>
</ol></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="60c1c-131"><a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>WinBioGetProperty (EXTENDED_ENROLLMENT_STATUS) </strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-131"><a href="/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty"><strong>WinBioGetProperty (EXTENDED_ENROLLMENT_STATUS)</strong></a></span></span></td>
<td><span data-ttu-id="60c1c-132"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_enrollment_status_fn"><strong>EngineAdapterQueryExtendedEnrollmentStatus</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-132"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_query_extended_enrollment_status_fn"><strong>EngineAdapterQueryExtendedEnrollmentStatus</strong></a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="60c1c-133"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit"><strong>WinBioEnrollCommit</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-133"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit"><strong>WinBioEnrollCommit</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="60c1c-134"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_check_for_duplicate_fn"><strong>EngineAdapterCheckForDuplicate</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-134"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_check_for_duplicate_fn"><strong>EngineAdapterCheckForDuplicate</strong></a></span></span></li>
<li><span data-ttu-id="60c1c-135">如果可移動資料庫</span><span class="sxs-lookup"><span data-stu-id="60c1c-135">If REMOVABLE DATABASE</span></span>
<ol>
<li><span data-ttu-id="60c1c-136"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn"><strong>EngineAdapterGetEnrollmentHash</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-136"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_get_enrollment_hash_fn"><strong>EngineAdapterGetEnrollmentHash</strong></a></span></span></li>
<li><span data-ttu-id="60c1c-137"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>EngineAdapterCommitEnrollment</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-137"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>EngineAdapterCommitEnrollment</strong></a></span></span></li>
</ol></li>
<li><span data-ttu-id="60c1c-138">否則<a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>EngineAdapterCommitEnrollment</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-138">Else<a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_commit_enrollment_fn"><strong>EngineAdapterCommitEnrollment</strong></a></span></span><br/></li>
</ol></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="60c1c-139"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard"><strong>WinBioEnrollDiscard</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-139"><a href="/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard"><strong>WinBioEnrollDiscard</strong></a></span></span></td>
<td><ol>
<li><span data-ttu-id="60c1c-140"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn"><strong>EngineAdapterDiscardEnrollment</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-140"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_discard_enrollment_fn"><strong>EngineAdapterDiscardEnrollment</strong></a></span></span></li>
<li><span data-ttu-id="60c1c-141"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearCoNtext</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-141"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_engine_clear_context_fn"><strong>EngineAdapterClearContext</strong></a></span></span></li>
<li><span data-ttu-id="60c1c-142"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearCoNtext</strong></a></span><span class="sxs-lookup"><span data-stu-id="60c1c-142"><a href="/windows/desktop/api/Winbio_adapter/nc-winbio_adapter-pibio_storage_clear_context_fn"><strong>StorageAdapterClearContext</strong></a></span></span></li>
</ol></td>
</tr>
</tbody>
</table>



 

 

 





