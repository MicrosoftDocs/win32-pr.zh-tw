---
description: 這是在電話裝置上叫用作業時，執行所能傳回的錯誤碼清單。 請參閱個別的函式描述，以判斷每個函式可傳回的錯誤代碼。
ms.assetid: 763a9dc2-3e70-4169-a66e-3aac78ef8d33
title: 'PHONEERR_ 的常數 (Tapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6b41ba5d14f4aa12318dd4bc9f2b20e4e9e2e6b4
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987993"
---
# <a name="phoneerr_-constants"></a><span data-ttu-id="f057d-104">PHONEERR \_ 常數</span><span class="sxs-lookup"><span data-stu-id="f057d-104">PHONEERR\_ Constants</span></span>

<span data-ttu-id="f057d-105">這是在電話裝置上叫用作業時，執行所能傳回的錯誤碼清單。</span><span class="sxs-lookup"><span data-stu-id="f057d-105">This is the list of error codes that the implementation can return when invoking operations on phone devices.</span></span> <span data-ttu-id="f057d-106">請參閱個別的函式描述，以判斷每個函式可傳回的錯誤代碼。</span><span class="sxs-lookup"><span data-stu-id="f057d-106">Consult the individual function descriptions to determine which of these error codes each function can return.</span></span>

<dl> <dt>

<span data-ttu-id="f057d-107"><span id="PHONEERR_ALLOCATED"></span><span id="phoneerr_allocated"></span>**PHONEERR \_ 已配置**</span><span class="sxs-lookup"><span data-stu-id="f057d-107"><span id="PHONEERR_ALLOCATED"></span><span id="phoneerr_allocated"></span>**PHONEERR\_ALLOCATED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-108">已配置指定的資源。</span><span class="sxs-lookup"><span data-stu-id="f057d-108">The specified resource is already allocated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-109"><span id="PHONEERR_BADDEVICEID"></span><span id="phoneerr_baddeviceid"></span>**PHONEERR \_ BADDEVICEID**</span><span class="sxs-lookup"><span data-stu-id="f057d-109"><span id="PHONEERR_BADDEVICEID"></span><span id="phoneerr_baddeviceid"></span>**PHONEERR\_BADDEVICEID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-110">指定的裝置識別碼無效或超出範圍。</span><span class="sxs-lookup"><span data-stu-id="f057d-110">The specified device identifier is invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-111"><span id="PHONEERR_DISCONNECTED"></span><span id="phoneerr_disconnected"></span>**PHONEERR 已 \_ 中斷連線**</span><span class="sxs-lookup"><span data-stu-id="f057d-111"><span id="PHONEERR_DISCONNECTED"></span><span id="phoneerr_disconnected"></span>**PHONEERR\_DISCONNECTED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-112">呼叫已中斷連線。</span><span class="sxs-lookup"><span data-stu-id="f057d-112">The call was disconnected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-113"><span id="PHONEERR_INCOMPATIBLEAPIVERSION"></span><span id="phoneerr_incompatibleapiversion"></span>**PHONEERR \_ INCOMPATIBLEAPIVERSION**</span><span class="sxs-lookup"><span data-stu-id="f057d-113"><span id="PHONEERR_INCOMPATIBLEAPIVERSION"></span><span id="phoneerr_incompatibleapiversion"></span>**PHONEERR\_INCOMPATIBLEAPIVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-114">應用程式要求的是電話語音 API 或對應服務提供者無法支援的 API 版本或版本範圍。</span><span class="sxs-lookup"><span data-stu-id="f057d-114">The application requested an API version or version range that cannot be supported by the Telephony API implementation or the corresponding service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-115"><span id="PHONEERR_INCOMPATIBLEEXTVERSION"></span><span id="phoneerr_incompatibleextversion"></span>**PHONEERR \_ INCOMPATIBLEEXTVERSION**</span><span class="sxs-lookup"><span data-stu-id="f057d-115"><span id="PHONEERR_INCOMPATIBLEEXTVERSION"></span><span id="phoneerr_incompatibleextversion"></span>**PHONEERR\_INCOMPATIBLEEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-116">應用程式要求了服務提供者無法支援的延伸模組版本或版本範圍。</span><span class="sxs-lookup"><span data-stu-id="f057d-116">The application requested an extension version or version range that cannot be supported by the service provider.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-117"><span id="PHONEERR_INIFILECORRUPT"></span><span id="phoneerr_inifilecorrupt"></span>**PHONEERR \_ INIFILECORRUPT**</span><span class="sxs-lookup"><span data-stu-id="f057d-117"><span id="PHONEERR_INIFILECORRUPT"></span><span id="phoneerr_inifilecorrupt"></span>**PHONEERR\_INIFILECORRUPT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-118">由於 Telephon.ini 檔案中的內部不一致或格式化問題，TAPI 無法正確地讀取和瞭解。</span><span class="sxs-lookup"><span data-stu-id="f057d-118">Because of internal inconsistencies or formatting problems in the Telephon.ini file, it cannot be read and understood properly by TAPI.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-119"><span id="PHONEERR_INUSE"></span><span id="phoneerr_inuse"></span>**PHONEERR \_ INUSE**</span><span class="sxs-lookup"><span data-stu-id="f057d-119"><span id="PHONEERR_INUSE"></span><span id="phoneerr_inuse"></span>**PHONEERR\_INUSE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-120">裝置目前正在使用中。</span><span class="sxs-lookup"><span data-stu-id="f057d-120">The device is currently in use.</span></span> <span data-ttu-id="f057d-121">無法設定裝置。</span><span class="sxs-lookup"><span data-stu-id="f057d-121">The device cannot be configured.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-122"><span id="PHONEERR_INVALAPPHANDLE"></span><span id="phoneerr_invalapphandle"></span>**PHONEERR \_ INVALAPPHANDLE**</span><span class="sxs-lookup"><span data-stu-id="f057d-122"><span id="PHONEERR_INVALAPPHANDLE"></span><span id="phoneerr_invalapphandle"></span>**PHONEERR\_INVALAPPHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-123">應用程式指定的使用方式控制碼或註冊控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="f057d-123">The application's specified usage handle or registration handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-124"><span id="PHONEERR_INVALAPPNAME"></span><span id="phoneerr_invalappname"></span>**PHONEERR \_ INVALAPPNAME**</span><span class="sxs-lookup"><span data-stu-id="f057d-124"><span id="PHONEERR_INVALAPPNAME"></span><span id="phoneerr_invalappname"></span>**PHONEERR\_INVALAPPNAME**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-125">指定的應用程式名稱無效。</span><span class="sxs-lookup"><span data-stu-id="f057d-125">The specified application name is invalid.</span></span> <span data-ttu-id="f057d-126">如果應用程式名稱是由應用程式所指定，則會假設該字串不包含任何 nondisplayable 字元，而且是以 **Null** 結束。</span><span class="sxs-lookup"><span data-stu-id="f057d-126">If an application name is specified by the application, it is assumed that the string does not contain any nondisplayable characters and is **NULL**-terminated.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-127"><span id="PHONEERR_INVALBUTTONLAMPID"></span><span id="phoneerr_invalbuttonlampid"></span>**PHONEERR \_ INVALBUTTONLAMPID**</span><span class="sxs-lookup"><span data-stu-id="f057d-127"><span id="PHONEERR_INVALBUTTONLAMPID"></span><span id="phoneerr_invalbuttonlampid"></span>**PHONEERR\_INVALBUTTONLAMPID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-128">指定的按鈕/燈泡識別碼超出範圍或無效。</span><span class="sxs-lookup"><span data-stu-id="f057d-128">The specified button/lamp identifier is out of range or invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-129"><span id="PHONEERR_INVALBUTTONMODE"></span><span id="phoneerr_invalbuttonmode"></span>**PHONEERR \_ INVALBUTTONMODE**</span><span class="sxs-lookup"><span data-stu-id="f057d-129"><span id="PHONEERR_INVALBUTTONMODE"></span><span id="phoneerr_invalbuttonmode"></span>**PHONEERR\_INVALBUTTONMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-130">按鈕模式參數無效。</span><span class="sxs-lookup"><span data-stu-id="f057d-130">The button mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-131"><span id="PHONEERR_INVALBUTTONSTATE"></span><span id="phoneerr_invalbuttonstate"></span>**PHONEERR \_ INVALBUTTONSTATE**</span><span class="sxs-lookup"><span data-stu-id="f057d-131"><span id="PHONEERR_INVALBUTTONSTATE"></span><span id="phoneerr_invalbuttonstate"></span>**PHONEERR\_INVALBUTTONSTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-132">按鈕狀態參數無效。</span><span class="sxs-lookup"><span data-stu-id="f057d-132">The button states parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-133"><span id="PHONEERR_INVALDATAID"></span><span id="phoneerr_invaldataid"></span>**PHONEERR \_ INVALDATAID**</span><span class="sxs-lookup"><span data-stu-id="f057d-133"><span id="PHONEERR_INVALDATAID"></span><span id="phoneerr_invaldataid"></span>**PHONEERR\_INVALDATAID**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-134">指定的資料識別碼無效。</span><span class="sxs-lookup"><span data-stu-id="f057d-134">The specified data identifier is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-135"><span id="PHONEERR_INVALDEVICECLASS"></span><span id="phoneerr_invaldeviceclass"></span>**PHONEERR \_ INVALDEVICECLASS**</span><span class="sxs-lookup"><span data-stu-id="f057d-135"><span id="PHONEERR_INVALDEVICECLASS"></span><span id="phoneerr_invaldeviceclass"></span>**PHONEERR\_INVALDEVICECLASS**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-136">指定的電話不支援指定的裝置類別。</span><span class="sxs-lookup"><span data-stu-id="f057d-136">The specified phone does not support the indicated device class.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-137"><span id="PHONEERR_INVALEXTVERSION"></span><span id="phoneerr_invalextversion"></span>**PHONEERR \_ INVALEXTVERSION**</span><span class="sxs-lookup"><span data-stu-id="f057d-137"><span id="PHONEERR_INVALEXTVERSION"></span><span id="phoneerr_invalextversion"></span>**PHONEERR\_INVALEXTVERSION**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-138">服務提供者延伸模組版本號碼無效。</span><span class="sxs-lookup"><span data-stu-id="f057d-138">The service provider extension version number is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-139"><span id="PHONEERR_INVALHOOKSWITCHDEV"></span><span id="phoneerr_invalhookswitchdev"></span>**PHONEERR \_ INVALHOOKSWITCHDEV**</span><span class="sxs-lookup"><span data-stu-id="f057d-139"><span id="PHONEERR_INVALHOOKSWITCHDEV"></span><span id="phoneerr_invalhookswitchdev"></span>**PHONEERR\_INVALHOOKSWITCHDEV**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-140">Hookswitch 裝置參數無效。</span><span class="sxs-lookup"><span data-stu-id="f057d-140">The hookswitch device parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-141"><span id="PHONEERR_INVALHOOKSWITCHMODE"></span><span id="phoneerr_invalhookswitchmode"></span>**PHONEERR \_ INVALHOOKSWITCHMODE**</span><span class="sxs-lookup"><span data-stu-id="f057d-141"><span id="PHONEERR_INVALHOOKSWITCHMODE"></span><span id="phoneerr_invalhookswitchmode"></span>**PHONEERR\_INVALHOOKSWITCHMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-142">Hookswitch 模式參數無效。</span><span class="sxs-lookup"><span data-stu-id="f057d-142">The hookswitch mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-143"><span id="PHONEERR_INVALLAMPMODE"></span><span id="phoneerr_invallampmode"></span>**PHONEERR \_ INVALLAMPMODE**</span><span class="sxs-lookup"><span data-stu-id="f057d-143"><span id="PHONEERR_INVALLAMPMODE"></span><span id="phoneerr_invallampmode"></span>**PHONEERR\_INVALLAMPMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-144">指定的燈泡模式參數無效。</span><span class="sxs-lookup"><span data-stu-id="f057d-144">The specified lamp mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-145"><span id="PHONEERR_INVALPARAM"></span><span id="phoneerr_invalparam"></span>**PHONEERR \_ INVALPARAM**</span><span class="sxs-lookup"><span data-stu-id="f057d-145"><span id="PHONEERR_INVALPARAM"></span><span id="phoneerr_invalparam"></span>**PHONEERR\_INVALPARAM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-146">參數（例如，資料列或資料行值或視窗控制碼）無效或超出範圍。</span><span class="sxs-lookup"><span data-stu-id="f057d-146">A parameter, such as a row or column value or a window handle, is invalid or out of range.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-147"><span id="PHONEERR_INVALPHONEHANDLE"></span><span id="phoneerr_invalphonehandle"></span>**PHONEERR \_ INVALPHONEHANDLE**</span><span class="sxs-lookup"><span data-stu-id="f057d-147"><span id="PHONEERR_INVALPHONEHANDLE"></span><span id="phoneerr_invalphonehandle"></span>**PHONEERR\_INVALPHONEHANDLE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-148">指定的裝置控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="f057d-148">The specified device handle is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-149"><span id="PHONEERR_INVALPHONESTATE"></span><span id="phoneerr_invalphonestate"></span>**PHONEERR \_ INVALPHONESTATE**</span><span class="sxs-lookup"><span data-stu-id="f057d-149"><span id="PHONEERR_INVALPHONESTATE"></span><span id="phoneerr_invalphonestate"></span>**PHONEERR\_INVALPHONESTATE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-150">手機裝置對要求的作業不是處於有效的狀態。</span><span class="sxs-lookup"><span data-stu-id="f057d-150">The phone device is not in a valid state for the requested operation.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-151"><span id="PHONEERR_INVALPOINTER"></span><span id="phoneerr_invalpointer"></span>**PHONEERR \_ INVALPOINTER**</span><span class="sxs-lookup"><span data-stu-id="f057d-151"><span id="PHONEERR_INVALPOINTER"></span><span id="phoneerr_invalpointer"></span>**PHONEERR\_INVALPOINTER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-152">一或多個指定的指標參數無效。</span><span class="sxs-lookup"><span data-stu-id="f057d-152">One or more of the specified pointer parameters are invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-153"><span id="PHONEERR_INVALPRIVILEGE"></span><span id="phoneerr_invalprivilege"></span>**PHONEERR \_ INVALPRIVILEGE**</span><span class="sxs-lookup"><span data-stu-id="f057d-153"><span id="PHONEERR_INVALPRIVILEGE"></span><span id="phoneerr_invalprivilege"></span>**PHONEERR\_INVALPRIVILEGE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-154">*DwPrivilege* 參數無效。</span><span class="sxs-lookup"><span data-stu-id="f057d-154">The *dwPrivilege* parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-155"><span id="PHONEERR_INVALRINGMODE"></span><span id="phoneerr_invalringmode"></span>**PHONEERR \_ INVALRINGMODE**</span><span class="sxs-lookup"><span data-stu-id="f057d-155"><span id="PHONEERR_INVALRINGMODE"></span><span id="phoneerr_invalringmode"></span>**PHONEERR\_INVALRINGMODE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-156">信號模式參數無效。</span><span class="sxs-lookup"><span data-stu-id="f057d-156">The ring mode parameter is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-157"><span id="PHONEERR_NODEVICE"></span><span id="phoneerr_nodevice"></span>**PHONEERR \_ NODEVICE**</span><span class="sxs-lookup"><span data-stu-id="f057d-157"><span id="PHONEERR_NODEVICE"></span><span id="phoneerr_nodevice"></span>**PHONEERR\_NODEVICE**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-158">已不再接受指定的裝置識別碼，因為自從上次初始化 TAPI 之後，已從系統移除相關聯的裝置，或在初始化時未偵測到的已損毀。</span><span class="sxs-lookup"><span data-stu-id="f057d-158">The specified device identifier, which was previously valid, is no longer accepted because the associated device has been removed from the system since TAPI was last initialized or is corrupt in a way that was not detected at initialization.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-159"><span id="PHONEERR_NODRIVER"></span><span id="phoneerr_nodriver"></span>**PHONEERR \_ NODRIVER**</span><span class="sxs-lookup"><span data-stu-id="f057d-159"><span id="PHONEERR_NODRIVER"></span><span id="phoneerr_nodriver"></span>**PHONEERR\_NODRIVER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-160">指定之裝置的電話服務提供者發現其中一個元件遺失或損毀，但在初始化時未偵測到。</span><span class="sxs-lookup"><span data-stu-id="f057d-160">The telephone service provider for the specified device found that one of its components is missing or corrupt in a way that was not detected at initialization time.</span></span> <span data-ttu-id="f057d-161">應建議使用者使用電話語音主控台修正問題。</span><span class="sxs-lookup"><span data-stu-id="f057d-161">The user should be advised to use the Telephony Control Panel to correct the problem.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-162"><span id="PHONEERR_NOMEM"></span><span id="phoneerr_nomem"></span>**PHONEERR \_ NOMEM**</span><span class="sxs-lookup"><span data-stu-id="f057d-162"><span id="PHONEERR_NOMEM"></span><span id="phoneerr_nomem"></span>**PHONEERR\_NOMEM**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-163">記憶體不足，無法完成要求的操作，或無法配置或鎖定記憶體。</span><span class="sxs-lookup"><span data-stu-id="f057d-163">Insufficient memory to complete the requested operation, or unable to allocate or lock memory.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-164"><span id="PHONEERR_NOTOWNER"></span><span id="phoneerr_notowner"></span>**PHONEERR \_ NOTOWNER**</span><span class="sxs-lookup"><span data-stu-id="f057d-164"><span id="PHONEERR_NOTOWNER"></span><span id="phoneerr_notowner"></span>**PHONEERR\_NOTOWNER**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-165">應用程式沒有指定電話裝置的擁有者許可權。</span><span class="sxs-lookup"><span data-stu-id="f057d-165">The application does not have owner privilege to the specified phone device.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-166"><span id="PHONEERR_OPERATIONFAILED"></span><span id="phoneerr_operationfailed"></span>**PHONEERR \_ OPERATIONFAILED**</span><span class="sxs-lookup"><span data-stu-id="f057d-166"><span id="PHONEERR_OPERATIONFAILED"></span><span id="phoneerr_operationfailed"></span>**PHONEERR\_OPERATIONFAILED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-167">因為未指定的原因，導致作業失敗。</span><span class="sxs-lookup"><span data-stu-id="f057d-167">The operation failed for an unspecified reason.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-168"><span id="PHONEERR_OPERATIONUNAVAIL"></span><span id="phoneerr_operationunavail"></span>**PHONEERR \_ OPERATIONUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="f057d-168"><span id="PHONEERR_OPERATIONUNAVAIL"></span><span id="phoneerr_operationunavail"></span>**PHONEERR\_OPERATIONUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-169">無法使用操作。</span><span class="sxs-lookup"><span data-stu-id="f057d-169">The operation is not available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-170"><span id="PHONEERR_REINIT"></span><span id="phoneerr_reinit"></span>**PHONEERR \_ 重新初始化**</span><span class="sxs-lookup"><span data-stu-id="f057d-170"><span id="PHONEERR_REINIT"></span><span id="phoneerr_reinit"></span>**PHONEERR\_REINIT**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-171">如果已要求 TAPI 重新初始化（例如新增或移除電話語音服務提供者的結果），則 [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)、 [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) 或 [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) 要求會因為此錯誤而被拒絕，直到最後一個應用程式使用 [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)) 來關閉其 API (為止，此時新的設定就會生效，而應用程式會再次被允許呼叫 **phoneInitialize** 或 **phoneInitializeEx**。</span><span class="sxs-lookup"><span data-stu-id="f057d-171">If TAPI reinitialization has been requested, for example as a result of adding or removing a telephony service provider, then [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa) or [**phoneOpen**](/windows/desktop/api/Tapi/nf-tapi-phoneopen) requests are rejected with this error until the last application shuts down its usage of the API (using [**phoneShutdown**](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)), at which time the new configuration becomes effective and applications are once again permitted to call **phoneInitialize** or **phoneInitializeEx**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-172"><span id="PHONEERR_REQUESTOVERRUN"></span><span id="phoneerr_requestoverrun"></span>**PHONEERR \_ REQUESTOVERRUN**</span><span class="sxs-lookup"><span data-stu-id="f057d-172"><span id="PHONEERR_REQUESTOVERRUN"></span><span id="phoneerr_requestoverrun"></span>**PHONEERR\_REQUESTOVERRUN**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-173">已超過未完成電話要求的數目上限。</span><span class="sxs-lookup"><span data-stu-id="f057d-173">The maximum number of outstanding phone requests has been exceeded.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-174"><span id="PHONEERR_RESOURCEUNAVAIL"></span><span id="phoneerr_resourceunavail"></span>**PHONEERR \_ RESOURCEUNAVAIL**</span><span class="sxs-lookup"><span data-stu-id="f057d-174"><span id="PHONEERR_RESOURCEUNAVAIL"></span><span id="phoneerr_resourceunavail"></span>**PHONEERR\_RESOURCEUNAVAIL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-175">因為資源 overcommitment，所以無法完成操作。</span><span class="sxs-lookup"><span data-stu-id="f057d-175">The operation cannot be completed because of resource overcommitment.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-176"><span id="PHONEERR_STRUCTURETOOSMALL"></span><span id="phoneerr_structuretoosmall"></span>**PHONEERR \_ STRUCTURETOOSMALL**</span><span class="sxs-lookup"><span data-stu-id="f057d-176"><span id="PHONEERR_STRUCTURETOOSMALL"></span><span id="phoneerr_structuretoosmall"></span>**PHONEERR\_STRUCTURETOOSMALL**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-177">指定的電話上限結構太小。</span><span class="sxs-lookup"><span data-stu-id="f057d-177">The specified phone caps structure is too small.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="f057d-178"><span id="PHONEERR_UNINITIALIZED"></span><span id="phoneerr_uninitialized"></span>**PHONEERR \_ 未初始化**</span><span class="sxs-lookup"><span data-stu-id="f057d-178"><span id="PHONEERR_UNINITIALIZED"></span><span id="phoneerr_uninitialized"></span>**PHONEERR\_UNINITIALIZED**</span></span>
</dt> <dd> <dl> <dt>



<span data-ttu-id="f057d-179">作業是在任何名為 [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)、 [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)的應用程式之前叫用。</span><span class="sxs-lookup"><span data-stu-id="f057d-179">The operation was invoked before any application called [**phoneInitialize**](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize), [**phoneInitializeEx**](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa).</span></span>


</dt> </dl> </dd> </dl>

## <a name="remarks"></a><span data-ttu-id="f057d-180">備註</span><span class="sxs-lookup"><span data-stu-id="f057d-180">Remarks</span></span>

<span data-ttu-id="f057d-181">0xC0000000 至0xFFFFFFFF 的值適用于裝置專屬的延伸模組;0xBFFFFFFF 的值0x80000000 是保留的;以及使用0x00000000 到0x7FFFFFFF 作為要求識別碼。</span><span class="sxs-lookup"><span data-stu-id="f057d-181">The values 0xC0000000 through 0xFFFFFFFF are available for device-specific extensions; the values 0x80000000 through 0xBFFFFFFF are reserved; and 0x00000000 through 0x7FFFFFFF are used as request identifiers.</span></span>

<span data-ttu-id="f057d-182">如果應用程式收到錯誤訊息，指出它不會明確處理 (（例如裝置專屬延伸模組所定義的錯誤）) ，則應該將錯誤視為 PHONEERR \_ OPERATIONFAILED (，以找出未指定原因) 。</span><span class="sxs-lookup"><span data-stu-id="f057d-182">If an application gets an error return that it does not specifically handle (such as an error defined by a device-specific extension), it should treat the error as a PHONEERR\_OPERATIONFAILED (for an unspecified reason).</span></span>

## <a name="requirements"></a><span data-ttu-id="f057d-183">規格需求</span><span class="sxs-lookup"><span data-stu-id="f057d-183">Requirements</span></span>



| <span data-ttu-id="f057d-184">需求</span><span class="sxs-lookup"><span data-stu-id="f057d-184">Requirement</span></span> | <span data-ttu-id="f057d-185">值</span><span class="sxs-lookup"><span data-stu-id="f057d-185">Value</span></span> |
|-------------------------|-----------------------------------------------------------------------------------|
| <span data-ttu-id="f057d-186">TAPI 版本</span><span class="sxs-lookup"><span data-stu-id="f057d-186">TAPI version</span></span><br/> | <span data-ttu-id="f057d-187">需要 TAPI 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="f057d-187">Requires TAPI 2.0 or later</span></span><br/>                                             |
| <span data-ttu-id="f057d-188">標頭</span><span class="sxs-lookup"><span data-stu-id="f057d-188">Header</span></span><br/>       | <dl> <span data-ttu-id="f057d-189"><dt>Tapi</dt></span><span class="sxs-lookup"><span data-stu-id="f057d-189"><dt>Tapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f057d-190">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f057d-190">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f057d-191">**phoneInitialize**</span><span class="sxs-lookup"><span data-stu-id="f057d-191">**phoneInitialize**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitialize)
</dt> <dt>

[<span data-ttu-id="f057d-192">**phoneInitializeEx**</span><span class="sxs-lookup"><span data-stu-id="f057d-192">**phoneInitializeEx**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneinitializeexa)
</dt> <dt>

[<span data-ttu-id="f057d-193">**phoneOpen**</span><span class="sxs-lookup"><span data-stu-id="f057d-193">**phoneOpen**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneopen)
</dt> <dt>

[<span data-ttu-id="f057d-194">**phoneShutdown**</span><span class="sxs-lookup"><span data-stu-id="f057d-194">**phoneShutdown**</span></span>](/windows/desktop/api/Tapi/nf-tapi-phoneshutdown)
</dt> </dl>

 

 




