---
title: 'WINBIO_OPERATION_TYPE 常數 (Winbio \_ 類型 .h) '
description: 指定要執行的非同步操作類型。
ms.assetid: D4ECEF91-BEC7-4A42-8808-F09F5C141180
topic_type:
- apiref
api_name:
- WINBIO_OPERATION_NONE
- WINBIO_OPERATION_OPEN
- WINBIO_OPERATION_CLOSE
- WINBIO_OPERATION_VERIFY
- WINBIO_OPERATION_IDENTIFY
- WINBIO_OPERATION_LOCATE_SENSOR
- WINBIO_OPERATION_ENROLL_BEGIN
- WINBIO_OPERATION_ENROLL_CAPTURE
- WINBIO_OPERATION_ENROLL_COMMIT
- WINBIO_OPERATION_ENROLL_DISCARD
- WINBIO_OPERATION_ENUM_ENROLLMENTS
- WINBIO_OPERATION_DELETE_TEMPLATE
- WINBIO_OPERATION_CAPTURE_SAMPLE
- WINBIO_OPERATION_GET_PROPERTY
- WINBIO_OPERATION_SET_PROPERTY
- WINBIO_OPERATION_GET_EVENT
- WINBIO_OPERATION_LOCK_UNIT
- WINBIO_OPERATION_UNLOCK_UNIT
- WINBIO_OPERATION_CONTROL_UNIT
- WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED
- WINBIO_OPERATION_OPEN_FRAMEWORK
- WINBIO_OPERATION_CLOSE_FRAMEWORK
- WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS
- WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS
- WINBIO_OPERATION_ENUM_DATABASES
- WINBIO_OPERATION_UNIT_ARRIVAL
- WINBIO_OPERATION_UNIT_REMOVAL
- WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET
- WINBIO_OPERATION_MONITOR_PRESENCE
- WINBIO_OPERATION_ENROLL_SELECT
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b83f32b9f98a24d0ed4d9995bf5fcb7eaa3a2b6c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104106494"
---
# <a name="winbio_operation_type-constants"></a><span data-ttu-id="3a48d-103">WINBIO \_ 運算 \_ 類型常數</span><span class="sxs-lookup"><span data-stu-id="3a48d-103">WINBIO\_OPERATION\_TYPE Constants</span></span>

<span data-ttu-id="3a48d-104">[**WINBIO \_ 非同步 \_ 結果**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result)中的 Windows 生物特徵辨識架構可以傳回下列常數，以指定要執行的非同步操作類型。</span><span class="sxs-lookup"><span data-stu-id="3a48d-104">The following constants can be returned by the Windows Biometric Framework in a [**WINBIO\_ASYNC\_RESULT**](/windows/desktop/api/Winbio/ns-winbio-winbio_async_result) to specify the type of asynchronous operation being performed.</span></span>

<dl> <dt>

<span data-ttu-id="3a48d-105"><span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**WINBIO \_ 操作 \_ 無**</span><span class="sxs-lookup"><span data-stu-id="3a48d-105"><span id="WINBIO_OPERATION_NONE"></span><span id="winbio_operation_none"></span>**WINBIO\_OPERATION\_NONE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-106">0</span><span class="sxs-lookup"><span data-stu-id="3a48d-106">0</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-107">未識別任何作業。</span><span class="sxs-lookup"><span data-stu-id="3a48d-107">No operation has been identified.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-108"><span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**WINBIO \_ 操作 \_ 開啟**</span><span class="sxs-lookup"><span data-stu-id="3a48d-108"><span id="WINBIO_OPERATION_OPEN"></span><span id="winbio_operation_open"></span>**WINBIO\_OPERATION\_OPEN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-109">1</span><span class="sxs-lookup"><span data-stu-id="3a48d-109">1</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-110">生物識別會話已開啟。</span><span class="sxs-lookup"><span data-stu-id="3a48d-110">A biometric session was opened.</span></span> <span data-ttu-id="3a48d-111">如需詳細資訊，請參閱 [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-111">For more information see [**WinBioAsyncOpenSession**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncopensession).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-112"><span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**WINBIO \_ 作業 \_ 關閉**</span><span class="sxs-lookup"><span data-stu-id="3a48d-112"><span id="WINBIO_OPERATION_CLOSE"></span><span id="winbio_operation_close"></span>**WINBIO\_OPERATION\_CLOSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-113">2</span><span class="sxs-lookup"><span data-stu-id="3a48d-113">2</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-114">生物識別會話已關閉。</span><span class="sxs-lookup"><span data-stu-id="3a48d-114">A biometric session was closed.</span></span> <span data-ttu-id="3a48d-115">如需詳細資訊，請參閱 [**WinBioCloseSession**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-115">For more information, see [**WinBioCloseSession**](/windows/desktop/api/Winbio/nf-winbio-winbioclosesession).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-116"><span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**WINBIO \_ 操作 \_ 驗證**</span><span class="sxs-lookup"><span data-stu-id="3a48d-116"><span id="WINBIO_OPERATION_VERIFY"></span><span id="winbio_operation_verify"></span>**WINBIO\_OPERATION\_VERIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-117">3</span><span class="sxs-lookup"><span data-stu-id="3a48d-117">3</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-118">已根據使用者身分識別來驗證生物識別範例。</span><span class="sxs-lookup"><span data-stu-id="3a48d-118">A biometric sample was verified against a user identity.</span></span> <span data-ttu-id="3a48d-119">如需詳細資訊，請參閱 [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-119">For more information, see [**WinBioVerify**](/windows/desktop/api/Winbio/nf-winbio-winbioverify).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-120"><span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**WINBIO \_ 操作 \_ 識別**</span><span class="sxs-lookup"><span data-stu-id="3a48d-120"><span id="WINBIO_OPERATION_IDENTIFY"></span><span id="winbio_operation_identify"></span>**WINBIO\_OPERATION\_IDENTIFY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-121">4</span><span class="sxs-lookup"><span data-stu-id="3a48d-121">4</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-122">已捕獲並與現有範本比較的生物識別範例。</span><span class="sxs-lookup"><span data-stu-id="3a48d-122">A biometric sample was captured and compared to an existing template.</span></span> <span data-ttu-id="3a48d-123">如需詳細資訊，請參閱 [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-123">For more information, see [**WinBioIdentify**](/windows/desktop/api/Winbio/nf-winbio-winbioidentify).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-124"><span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**WINBIO \_ 操作 \_ 找出 \_ 感應器**</span><span class="sxs-lookup"><span data-stu-id="3a48d-124"><span id="WINBIO_OPERATION_LOCATE_SENSOR"></span><span id="winbio_operation_locate_sensor"></span>**WINBIO\_OPERATION\_LOCATE\_SENSOR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-125">5</span><span class="sxs-lookup"><span data-stu-id="3a48d-125">5</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-126">已抓取生物特徵辨識單位的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3a48d-126">The ID number of a biometric unit was retrieved.</span></span> <span data-ttu-id="3a48d-127">如需詳細資訊，請參閱 [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-127">For more information, see [**WinBioLocateSensor**](/windows/desktop/api/Winbio/nf-winbio-winbiolocatesensor).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-128"><span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**WINBIO \_ 操作 \_ 註冊 \_ 開始**</span><span class="sxs-lookup"><span data-stu-id="3a48d-128"><span id="WINBIO_OPERATION_ENROLL_BEGIN"></span><span id="winbio_operation_enroll_begin"></span>**WINBIO\_OPERATION\_ENROLL\_BEGIN**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-129">6</span><span class="sxs-lookup"><span data-stu-id="3a48d-129">6</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-130">已起始生物識別註冊順序。</span><span class="sxs-lookup"><span data-stu-id="3a48d-130">A biometric enrollment sequence was initiated.</span></span> <span data-ttu-id="3a48d-131">如需詳細資訊，請參閱 [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-131">For more information, see [**WinBioEnrollBegin**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollbegin).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-132"><span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**WINBIO \_ OPERATION \_ 註冊 \_ 捕獲**</span><span class="sxs-lookup"><span data-stu-id="3a48d-132"><span id="WINBIO_OPERATION_ENROLL_CAPTURE"></span><span id="winbio_operation_enroll_capture"></span>**WINBIO\_OPERATION\_ENROLL\_CAPTURE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-133">7</span><span class="sxs-lookup"><span data-stu-id="3a48d-133">7</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-134">已捕捉並將生物識別範例新增至範本。</span><span class="sxs-lookup"><span data-stu-id="3a48d-134">A biometric sample was captured and added to the template.</span></span> <span data-ttu-id="3a48d-135">如需詳細資訊，請參閱 [**WinBioEnrollCapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-135">For more information, see [**WinBioEnrollCapture**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcapture).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-136"><span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**WINBIO \_ 作業 \_ 註冊 \_ 認可**</span><span class="sxs-lookup"><span data-stu-id="3a48d-136"><span id="WINBIO_OPERATION_ENROLL_COMMIT"></span><span id="winbio_operation_enroll_commit"></span>**WINBIO\_OPERATION\_ENROLL\_COMMIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-137">8</span><span class="sxs-lookup"><span data-stu-id="3a48d-137">8</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-138">擱置的生物特徵辨識範本已完成。</span><span class="sxs-lookup"><span data-stu-id="3a48d-138">A pending biometric template was finalized.</span></span> <span data-ttu-id="3a48d-139">如需詳細資訊，請參閱 [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-139">For more information, see [**WinBioEnrollCommit**](/windows/desktop/api/Winbio/nf-winbio-winbioenrollcommit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-140"><span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**WINBIO \_ OPERATION \_ 註冊 \_ 捨棄**</span><span class="sxs-lookup"><span data-stu-id="3a48d-140"><span id="WINBIO_OPERATION_ENROLL_DISCARD"></span><span id="winbio_operation_enroll_discard"></span>**WINBIO\_OPERATION\_ENROLL\_DISCARD**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-141">9</span><span class="sxs-lookup"><span data-stu-id="3a48d-141">9</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-142">擱置的生物特徵辨識範本已捨棄。</span><span class="sxs-lookup"><span data-stu-id="3a48d-142">A pending biometric template was discarded.</span></span> <span data-ttu-id="3a48d-143">如需詳細資訊，請參閱 [**WinBioEnrollDiscard**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-143">For more information, see [**WinBioEnrollDiscard**](/windows/desktop/api/Winbio/nf-winbio-winbioenrolldiscard).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-144"><span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**WINBIO \_ 作業 \_ 列舉 \_ 註冊**</span><span class="sxs-lookup"><span data-stu-id="3a48d-144"><span id="WINBIO_OPERATION_ENUM_ENROLLMENTS"></span><span id="winbio_operation_enum_enrollments"></span>**WINBIO\_OPERATION\_ENUM\_ENROLLMENTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-145">10</span><span class="sxs-lookup"><span data-stu-id="3a48d-145">10</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-146">指定之範本的子因數已列舉。</span><span class="sxs-lookup"><span data-stu-id="3a48d-146">The sub-factors for a given template were enumerated.</span></span> <span data-ttu-id="3a48d-147">如需詳細資訊，請參閱 [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-147">For more information, see [**WinBioEnumEnrollments**](/windows/desktop/api/Winbio/nf-winbio-winbioenumenrollments).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-148"><span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**WINBIO \_ 操作 \_ 刪除 \_ 範本**</span><span class="sxs-lookup"><span data-stu-id="3a48d-148"><span id="WINBIO_OPERATION_DELETE_TEMPLATE"></span><span id="winbio_operation_delete_template"></span>**WINBIO\_OPERATION\_DELETE\_TEMPLATE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-149">11</span><span class="sxs-lookup"><span data-stu-id="3a48d-149">11</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-150">已從存放區刪除生物識別範本。</span><span class="sxs-lookup"><span data-stu-id="3a48d-150">A biometric template was deleted from the store.</span></span> <span data-ttu-id="3a48d-151">如需詳細資訊，請參閱 [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-151">For more information, see [**WinBioDeleteTemplate**](/windows/desktop/api/Winbio/nf-winbio-winbiodeletetemplate).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-152"><span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**WINBIO \_ OPERATION \_ CAPTURE \_ 範例**</span><span class="sxs-lookup"><span data-stu-id="3a48d-152"><span id="WINBIO_OPERATION_CAPTURE_SAMPLE"></span><span id="winbio_operation_capture_sample"></span>**WINBIO\_OPERATION\_CAPTURE\_SAMPLE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-153">12</span><span class="sxs-lookup"><span data-stu-id="3a48d-153">12</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-154">已捕捉到生物識別範例。</span><span class="sxs-lookup"><span data-stu-id="3a48d-154">A biometric sample was captured.</span></span> <span data-ttu-id="3a48d-155">如需詳細資訊，請參閱 [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-155">For more information, see [**WinBioCaptureSample**](/windows/desktop/api/Winbio/nf-winbio-winbiocapturesample).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-156"><span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**WINBIO \_ 操作 \_ 取得 \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="3a48d-156"><span id="WINBIO_OPERATION_GET_PROPERTY"></span><span id="winbio_operation_get_property"></span>**WINBIO\_OPERATION\_GET\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-157">13</span><span class="sxs-lookup"><span data-stu-id="3a48d-157">13</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-158">已抓取生物識別會話、單位或範本屬性。</span><span class="sxs-lookup"><span data-stu-id="3a48d-158">A biometric session, unit, or template property was retrieved.</span></span> <span data-ttu-id="3a48d-159">如需詳細資訊，請參閱 [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-159">For more information, see [**WinBioGetProperty**](/windows/desktop/api/Winbio/nf-winbio-winbiogetproperty).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-160"><span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**WINBIO \_ OPERATION \_ SET \_ 屬性**</span><span class="sxs-lookup"><span data-stu-id="3a48d-160"><span id="WINBIO_OPERATION_SET_PROPERTY"></span><span id="winbio_operation_set_property"></span>**WINBIO\_OPERATION\_SET\_PROPERTY**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-161">14</span><span class="sxs-lookup"><span data-stu-id="3a48d-161">14</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-162">已設定生物識別會話、單位、範本或帳戶屬性。</span><span class="sxs-lookup"><span data-stu-id="3a48d-162">A biometric session, unit, template, or account property was set.</span></span> <span data-ttu-id="3a48d-163">如需詳細資訊，請參閱 [**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-163">For more information, see [**WinBioSetProperty**](/windows/desktop/api/winbio/nf-winbio-winbiosetproperty).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-164"><span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**WINBIO \_ 操作 \_ 取得 \_ 事件**</span><span class="sxs-lookup"><span data-stu-id="3a48d-164"><span id="WINBIO_OPERATION_GET_EVENT"></span><span id="winbio_operation_get_event"></span>**WINBIO\_OPERATION\_GET\_EVENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-165">15</span><span class="sxs-lookup"><span data-stu-id="3a48d-165">15</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-166">未使用。</span><span class="sxs-lookup"><span data-stu-id="3a48d-166">Not used.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-167"><span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**WINBIO \_ 操作 \_ 鎖定 \_ 單位**</span><span class="sxs-lookup"><span data-stu-id="3a48d-167"><span id="WINBIO_OPERATION_LOCK_UNIT"></span><span id="winbio_operation_lock_unit"></span>**WINBIO\_OPERATION\_LOCK\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-168">16</span><span class="sxs-lookup"><span data-stu-id="3a48d-168">16</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-169">已鎖定可供會話獨佔使用的生物識別單位。</span><span class="sxs-lookup"><span data-stu-id="3a48d-169">A biometric unit was locked for exclusive use by a session.</span></span> <span data-ttu-id="3a48d-170">如需詳細資訊，請參閱 [**WinBioLockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-170">For more information, see [**WinBioLockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiolockunit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-171"><span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**WINBIO \_ OPERATION \_ UNLOCK \_ UNIT**</span><span class="sxs-lookup"><span data-stu-id="3a48d-171"><span id="WINBIO_OPERATION_UNLOCK_UNIT"></span><span id="winbio_operation_unlock_unit"></span>**WINBIO\_OPERATION\_UNLOCK\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-172">17</span><span class="sxs-lookup"><span data-stu-id="3a48d-172">17</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-173">已釋放生物特徵辨識裝置上的會話鎖定。</span><span class="sxs-lookup"><span data-stu-id="3a48d-173">The session lock on a biometric unit was released.</span></span> <span data-ttu-id="3a48d-174">如需詳細資訊，請參閱 [**WinBioUnlockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-174">For more information, see [**WinBioUnlockUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiounlockunit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-175"><span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**WINBIO \_ 操作 \_ 控制 \_ 單位**</span><span class="sxs-lookup"><span data-stu-id="3a48d-175"><span id="WINBIO_OPERATION_CONTROL_UNIT"></span><span id="winbio_operation_control_unit"></span>**WINBIO\_OPERATION\_CONTROL\_UNIT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-176">18</span><span class="sxs-lookup"><span data-stu-id="3a48d-176">18</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-177">廠商定義的作業是在控制單位上執行。</span><span class="sxs-lookup"><span data-stu-id="3a48d-177">Vendor defined operations were performed on a control unit.</span></span> <span data-ttu-id="3a48d-178">如需詳細資訊，請參閱 [**WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-178">For more information, see [**WinBioControlUnit**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunit).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-179"><span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**WINBIO \_ 操作 \_ 控制 \_ 單位 \_ 許可權**</span><span class="sxs-lookup"><span data-stu-id="3a48d-179"><span id="WINBIO_OPERATION_CONTROL_UNIT_PRIVILEGED"></span><span id="winbio_operation_control_unit_privileged"></span>**WINBIO\_OPERATION\_CONTROL\_UNIT\_PRIVILEGED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-180">19</span><span class="sxs-lookup"><span data-stu-id="3a48d-180">19</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-181">具有特殊許可權的廠商定義作業是在控制單位上執行。</span><span class="sxs-lookup"><span data-stu-id="3a48d-181">Privileged vendor defined operations were performed on a control unit.</span></span> <span data-ttu-id="3a48d-182">如需詳細資訊，請參閱 [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-182">For more information, see [**WinBioControlUnitPrivileged**](/windows/desktop/api/Winbio/nf-winbio-winbiocontrolunitprivileged).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-183"><span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**WINBIO \_ OPERATION \_ OPEN \_ FRAMEWORK**</span><span class="sxs-lookup"><span data-stu-id="3a48d-183"><span id="WINBIO_OPERATION_OPEN_FRAMEWORK"></span><span id="winbio_operation_open_framework"></span>**WINBIO\_OPERATION\_OPEN\_FRAMEWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-184">20</span><span class="sxs-lookup"><span data-stu-id="3a48d-184">20</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-185">已開啟生物特徵辨識架構的控制碼。</span><span class="sxs-lookup"><span data-stu-id="3a48d-185">A handle to the biometric framework was opened.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-186"><span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**WINBIO \_ OPERATION \_ CLOSE \_ FRAMEWORK**</span><span class="sxs-lookup"><span data-stu-id="3a48d-186"><span id="WINBIO_OPERATION_CLOSE_FRAMEWORK"></span><span id="winbio_operation_close_framework"></span>**WINBIO\_OPERATION\_CLOSE\_FRAMEWORK**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-187">21</span><span class="sxs-lookup"><span data-stu-id="3a48d-187">21</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-188">生物識別架構的控制碼已關閉。</span><span class="sxs-lookup"><span data-stu-id="3a48d-188">A handle to the biometric framework was closed.</span></span> <span data-ttu-id="3a48d-189">如需詳細資訊，請參閱 [**WinBioCloseFramework**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-189">For more information, see [**WinBioCloseFramework**](/windows/desktop/api/Winbio/nf-winbio-winbiocloseframework).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-190"><span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**WINBIO \_ 作業 \_ 列舉 \_ 服務 \_ 供應商**</span><span class="sxs-lookup"><span data-stu-id="3a48d-190"><span id="WINBIO_OPERATION_ENUM_SERVICE_PROVIDERS"></span><span id="winbio_operation_enum_service_providers"></span>**WINBIO\_OPERATION\_ENUM\_SERVICE\_PROVIDERS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-191">22</span><span class="sxs-lookup"><span data-stu-id="3a48d-191">22</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-192">已列舉已安裝的生物識別服務提供者。</span><span class="sxs-lookup"><span data-stu-id="3a48d-192">The installed biometric service providers were enumerated.</span></span> <span data-ttu-id="3a48d-193">如需詳細資訊，請參閱 [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-193">For more information, see [**WinBioEnumServiceProviders**](/windows/desktop/api/Winbio/nf-winbio-winbioenumserviceproviders).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-194"><span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**WINBIO \_ 作業 \_ 列舉 \_ 生物特徵辨識 \_ 單位**</span><span class="sxs-lookup"><span data-stu-id="3a48d-194"><span id="WINBIO_OPERATION_ENUM_BIOMETRIC_UNITS"></span><span id="winbio_operation_enum_biometric_units"></span>**WINBIO\_OPERATION\_ENUM\_BIOMETRIC\_UNITS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-195">23</span><span class="sxs-lookup"><span data-stu-id="3a48d-195">23</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-196">已列舉附加的生物特徵辨識單位。</span><span class="sxs-lookup"><span data-stu-id="3a48d-196">The attached biometric units were enumerated.</span></span> <span data-ttu-id="3a48d-197">如需詳細資訊，請參閱 [**WinBioAsyncEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-197">For more information, see [**WinBioAsyncEnumBiometricUnits**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncenumbiometricunits).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-198"><span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**WINBIO \_ 作業 \_ 列舉 \_ 資料庫**</span><span class="sxs-lookup"><span data-stu-id="3a48d-198"><span id="WINBIO_OPERATION_ENUM_DATABASES"></span><span id="winbio_operation_enum_databases"></span>**WINBIO\_OPERATION\_ENUM\_DATABASES**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-199">24</span><span class="sxs-lookup"><span data-stu-id="3a48d-199">24</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-200">已列舉註冊的資料庫。</span><span class="sxs-lookup"><span data-stu-id="3a48d-200">The registered databases were enumerated.</span></span> <span data-ttu-id="3a48d-201">如需詳細資訊，請參閱 [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-201">For more information, see [**WinBioEnumDatabases**](/windows/desktop/api/Winbio/nf-winbio-winbioenumdatabases).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-202"><span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**WINBIO \_ 操作 \_ 單位 \_ 抵達**</span><span class="sxs-lookup"><span data-stu-id="3a48d-202"><span id="WINBIO_OPERATION_UNIT_ARRIVAL"></span><span id="winbio_operation_unit_arrival"></span>**WINBIO\_OPERATION\_UNIT\_ARRIVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-203">25</span><span class="sxs-lookup"><span data-stu-id="3a48d-203">25</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-204">已建立生物特徵辨識單位。</span><span class="sxs-lookup"><span data-stu-id="3a48d-204">A biometric unit was created.</span></span> <span data-ttu-id="3a48d-205">如需詳細資訊，請參閱 [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-205">For more information, see [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-206"><span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**WINBIO \_ 操作 \_ 單位 \_ 移除**</span><span class="sxs-lookup"><span data-stu-id="3a48d-206"><span id="WINBIO_OPERATION_UNIT_REMOVAL"></span><span id="winbio_operation_unit_removal"></span>**WINBIO\_OPERATION\_UNIT\_REMOVAL**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-207">26</span><span class="sxs-lookup"><span data-stu-id="3a48d-207">26</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-208">已刪除生物識別單位。</span><span class="sxs-lookup"><span data-stu-id="3a48d-208">A biometric unit was deleted.</span></span> <span data-ttu-id="3a48d-209">如需詳細資訊，請參閱 [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-209">For more information, see [**WinBioAsyncMonitorFrameworkChanges**](/windows/desktop/api/Winbio/nf-winbio-winbioasyncmonitorframeworkchanges).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-210"><span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**WINBIO \_ 作業 \_ 識別 \_ 和 \_ 發行 \_ 票證**</span><span class="sxs-lookup"><span data-stu-id="3a48d-210"><span id="WINBIO_OPERATION_IDENTIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_identify_and_release_ticket"></span>**WINBIO\_OPERATION\_IDENTIFY\_AND\_RELEASE\_TICKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-211">27</span><span class="sxs-lookup"><span data-stu-id="3a48d-211">27</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-212">保留的。</span><span class="sxs-lookup"><span data-stu-id="3a48d-212">Reserved.</span></span> <span data-ttu-id="3a48d-213">從 Windows 10 開始支援此值。</span><span class="sxs-lookup"><span data-stu-id="3a48d-213">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-214"><span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**WINBIO \_ 操作 \_ 驗證 \_ 和 \_ 發行 \_ 票證**</span><span class="sxs-lookup"><span data-stu-id="3a48d-214"><span id="WINBIO_OPERATION_VERIFY_AND_RELEASE_TICKET"></span><span id="winbio_operation_verify_and_release_ticket"></span>**WINBIO\_OPERATION\_VERIFY\_AND\_RELEASE\_TICKET**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-215">28</span><span class="sxs-lookup"><span data-stu-id="3a48d-215">28</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-216">保留的。</span><span class="sxs-lookup"><span data-stu-id="3a48d-216">Reserved.</span></span> <span data-ttu-id="3a48d-217">從 Windows 10 開始支援此值。</span><span class="sxs-lookup"><span data-stu-id="3a48d-217">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-218"><span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**WINBIO \_ 作業 \_ 監視器 \_ 狀態**</span><span class="sxs-lookup"><span data-stu-id="3a48d-218"><span id="WINBIO_OPERATION_MONITOR_PRESENCE"></span><span id="winbio_operation_monitor_presence"></span>**WINBIO\_OPERATION\_MONITOR\_PRESENCE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-219">29</span><span class="sxs-lookup"><span data-stu-id="3a48d-219">29</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-220">已開啟臉部辨識或鳶尾花監視機制。</span><span class="sxs-lookup"><span data-stu-id="3a48d-220">The facial recognition or iris monitoring mechanism was turned on.</span></span> <span data-ttu-id="3a48d-221">如需詳細資訊，請參閱 [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-221">For more information, see [**WinBioMonitorPresence**](/windows/desktop/api/winbio/nf-winbio-winbiomonitorpresence).</span></span> <span data-ttu-id="3a48d-222">從 Windows 10 開始支援此值。</span><span class="sxs-lookup"><span data-stu-id="3a48d-222">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="3a48d-223"><span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**WINBIO \_ 操作 \_ 註冊 \_ SELECT**</span><span class="sxs-lookup"><span data-stu-id="3a48d-223"><span id="WINBIO_OPERATION_ENROLL_SELECT"></span><span id="winbio_operation_enroll_select"></span>**WINBIO\_OPERATION\_ENROLL\_SELECT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="3a48d-224">30</span><span class="sxs-lookup"><span data-stu-id="3a48d-224">30</span></span>
</dt> <dt>



<span data-ttu-id="3a48d-225">由範例緩衝區中的資料所代表的一組個人的個人，已指定為要註冊的個人。</span><span class="sxs-lookup"><span data-stu-id="3a48d-225">An individual from a group of individuals that are represented by data in the sample buffer was specified as the individual to enroll.</span></span> <span data-ttu-id="3a48d-226">如需詳細資訊，請參閱 [**WinBioEnrollSelect**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect)。</span><span class="sxs-lookup"><span data-stu-id="3a48d-226">For more information, see [**WinBioEnrollSelect**](/windows/desktop/api/winbio/nf-winbio-winbioenrollselect).</span></span> <span data-ttu-id="3a48d-227">從 Windows 10 開始支援此值。</span><span class="sxs-lookup"><span data-stu-id="3a48d-227">This value is supported starting in Windows 10.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3a48d-228">規格需求</span><span class="sxs-lookup"><span data-stu-id="3a48d-228">Requirements</span></span>



| <span data-ttu-id="3a48d-229">需求</span><span class="sxs-lookup"><span data-stu-id="3a48d-229">Requirement</span></span> | <span data-ttu-id="3a48d-230">值</span><span class="sxs-lookup"><span data-stu-id="3a48d-230">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="3a48d-231">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3a48d-231">Minimum supported client</span></span><br/> | <span data-ttu-id="3a48d-232">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a48d-232">Windows 8 \[desktop apps only\]</span></span><br/>                                                                                                                               |
| <span data-ttu-id="3a48d-233">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3a48d-233">Minimum supported server</span></span><br/> | <span data-ttu-id="3a48d-234">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3a48d-234">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                                                                                                     |
| <span data-ttu-id="3a48d-235">標頭</span><span class="sxs-lookup"><span data-stu-id="3a48d-235">Header</span></span><br/>                   | <dl> <span data-ttu-id="3a48d-236"><dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt></span><span class="sxs-lookup"><span data-stu-id="3a48d-236"><dt>Winbio\_types.h (include Winbio.h for client applications or Winbio\_adapters.h for adapters)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3a48d-237">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3a48d-237">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3a48d-238">用戶端應用程式常數</span><span class="sxs-lookup"><span data-stu-id="3a48d-238">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





