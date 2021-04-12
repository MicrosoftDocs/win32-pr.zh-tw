---
description: 指出狀態且不表示錯誤的 WMI 傳回碼。
ms.assetid: 36faa3fb-9496-47ca-bdba-f8eb52a06ff7
ms.tgt_platform: multiple
title: WbemCli) 的 WMI 非錯誤常數 (
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0880c9fda00f03c1fa8b174242bfc84ed9d75ad8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104192189"
---
# <a name="wmi-non-error-constants"></a><span data-ttu-id="ffa04-103">WMI 非錯誤常數</span><span class="sxs-lookup"><span data-stu-id="ffa04-103">WMI Non-Error Constants</span></span>

<span data-ttu-id="ffa04-104">指出狀態且不表示錯誤的 WMI 傳回碼。</span><span class="sxs-lookup"><span data-stu-id="ffa04-104">WMI return codes that indicate status and do not indicate an error.</span></span>

<span data-ttu-id="ffa04-105">如果作業不會導致錯誤，WMI 會傳回下列其中一個程式碼做為 **HRESULT** ，指出作業的狀態。</span><span class="sxs-lookup"><span data-stu-id="ffa04-105">If an operation does not result in an error, WMI returns one of the following codes as an **HRESULT** that indicates the status of the operation.</span></span>

> [!Note]  
> <span data-ttu-id="ffa04-106">WMI 類別中的某些方法可以傳回系統和網路錯誤碼 (64，例如) 。</span><span class="sxs-lookup"><span data-stu-id="ffa04-106">Some methods in WMI classes can return system and network error codes (64 for example).</span></span> <span data-ttu-id="ffa04-107">您可以在 [命令提示字元] 視窗中，使用 **net helpmsg** 命令檢查這些類型之錯誤碼的定義。</span><span class="sxs-lookup"><span data-stu-id="ffa04-107">You can check the definition of these types of error codes by using the **net helpmsg** command in the command prompt window.</span></span> <span data-ttu-id="ffa04-108">例如， **net helpmsg 64** 命令會傳回訊息：指定的網路名稱已無法再使用。</span><span class="sxs-lookup"><span data-stu-id="ffa04-108">For example, the command **net helpmsg 64** returns the message: The specified network name is no longer available.</span></span>

 

<span data-ttu-id="ffa04-109">在 c + + 中，您可以呼叫 [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) 並指定 **C： \\ Windows \\ System32 \\ wbem \\wmiutils.dll** 作為訊息模組。</span><span class="sxs-lookup"><span data-stu-id="ffa04-109">In C++, you can call [**FormatMessage**](/windows/desktop/api/winbase/nf-winbase-formatmessage) and specify **C:\\Windows\\System32\\wbem\\wmiutils.dll** as the message module.</span></span>

<dl> <dt>

<span data-ttu-id="ffa04-110"><span id="WBEM_S_NO_ERROR"></span><span id="wbem_s_no_error"></span>**WBEM \_ S \_ 沒有 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="ffa04-110"><span id="WBEM_S_NO_ERROR"></span><span id="wbem_s_no_error"></span>**WBEM\_S\_NO\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffa04-111">0 (0x0) </span><span class="sxs-lookup"><span data-stu-id="ffa04-111">0 (0x0)</span></span>
</dt> <dt>



<span data-ttu-id="ffa04-112">作業成功。</span><span class="sxs-lookup"><span data-stu-id="ffa04-112">The operation was successful.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffa04-113"><span id="WBEM_S_FALSE"></span><span id="wbem_s_false"></span>**WBEM \_ S \_ FALSE**</span><span class="sxs-lookup"><span data-stu-id="ffa04-113"><span id="WBEM_S_FALSE"></span><span id="wbem_s_false"></span>**WBEM\_S\_FALSE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffa04-114">1 (0x1) </span><span class="sxs-lookup"><span data-stu-id="ffa04-114">1 (0x1)</span></span>
</dt> <dt>



<span data-ttu-id="ffa04-115">沒有其他可用的物件、傳回的物件數目小於要求的數目，或列舉的結尾。</span><span class="sxs-lookup"><span data-stu-id="ffa04-115">No more objects are available, the number of objects returned is less than the number requested, or this is the end of an enumeration.</span></span> <span data-ttu-id="ffa04-116">當呼叫這個方法時，如果 *uCount* 參數的值為0，也會傳回此值。</span><span class="sxs-lookup"><span data-stu-id="ffa04-116">This value is also returned when this method is called with a value of 0 for the *uCount* parameter.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffa04-117"><span id="WBEM_S_ALREADY_EXISTS"></span><span id="wbem_s_already_exists"></span>**WBEM \_ S \_ 已經 \_ 存在**</span><span class="sxs-lookup"><span data-stu-id="ffa04-117"><span id="WBEM_S_ALREADY_EXISTS"></span><span id="wbem_s_already_exists"></span>**WBEM\_S\_ALREADY\_EXISTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffa04-118">262145 (0x40001) </span><span class="sxs-lookup"><span data-stu-id="ffa04-118">262145 (0x40001)</span></span>
</dt> <dt>



<span data-ttu-id="ffa04-119">嘗試建立已存在的物件或類別。</span><span class="sxs-lookup"><span data-stu-id="ffa04-119">An attempt was made to create an object or class that already exists.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffa04-120"><span id="WBEM_S_RESET_TO_DEFAULT"></span><span id="wbem_s_reset_to_default"></span>**\_將 WBEM \_ 重設 \_ 為 \_ 預設值**</span><span class="sxs-lookup"><span data-stu-id="ffa04-120"><span id="WBEM_S_RESET_TO_DEFAULT"></span><span id="wbem_s_reset_to_default"></span>**WBEM\_S\_RESET\_TO\_DEFAULT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffa04-121">262146 (0x40002) </span><span class="sxs-lookup"><span data-stu-id="ffa04-121">262146 (0x40002)</span></span>
</dt> <dt>



<span data-ttu-id="ffa04-122">所覆寫的屬性已刪除。</span><span class="sxs-lookup"><span data-stu-id="ffa04-122">An overridden property was deleted.</span></span> <span data-ttu-id="ffa04-123">傳回這個值以表示原始的非覆寫值已還原為刪除的結果。</span><span class="sxs-lookup"><span data-stu-id="ffa04-123">This value is returned to signal that the original non-overridden value has been restored as a result of the deletion.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffa04-124"><span id="WBEM_S_DIFFERENT"></span><span id="wbem_s_different"></span>**WBEM \_ S \_ 不同**</span><span class="sxs-lookup"><span data-stu-id="ffa04-124"><span id="WBEM_S_DIFFERENT"></span><span id="wbem_s_different"></span>**WBEM\_S\_DIFFERENT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffa04-125">262147 (0x40003) </span><span class="sxs-lookup"><span data-stu-id="ffa04-125">262147 (0x40003)</span></span>
</dt> <dt>



<span data-ttu-id="ffa04-126">要比較的物件、類別等專案 (物件、類別等) 不相同。</span><span class="sxs-lookup"><span data-stu-id="ffa04-126">The items (objects, classes, and so on) that are being compared are not identical.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffa04-127"><span id="WBEM_S_TIMEDOUT"></span><span id="wbem_s_timedout"></span>**WBEM \_ S \_ 逾時**</span><span class="sxs-lookup"><span data-stu-id="ffa04-127"><span id="WBEM_S_TIMEDOUT"></span><span id="wbem_s_timedout"></span>**WBEM\_S\_TIMEDOUT**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffa04-128">262148 (0x40004) </span><span class="sxs-lookup"><span data-stu-id="ffa04-128">262148 (0x40004)</span></span>
</dt> <dt>



<span data-ttu-id="ffa04-129">呼叫超時。這不是錯誤狀況。</span><span class="sxs-lookup"><span data-stu-id="ffa04-129">A call timed out. This is not an error condition.</span></span> <span data-ttu-id="ffa04-130">因此，可能也會傳回某些結果。</span><span class="sxs-lookup"><span data-stu-id="ffa04-130">Therefore, some results may have also been returned.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffa04-131"><span id="WBEM_S_NO_MORE_DATA"></span><span id="wbem_s_no_more_data"></span>**WBEM \_ S \_ 沒有 \_ 其他 \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="ffa04-131"><span id="WBEM_S_NO_MORE_DATA"></span><span id="wbem_s_no_more_data"></span>**WBEM\_S\_NO\_MORE\_DATA**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffa04-132">262149 (0x40005) </span><span class="sxs-lookup"><span data-stu-id="ffa04-132">262149 (0x40005)</span></span>
</dt> <dt>



<span data-ttu-id="ffa04-133">列舉中沒有其他可用的資料，使用者必須終止列舉。</span><span class="sxs-lookup"><span data-stu-id="ffa04-133">No more data is available from the enumeration, and the user must terminate the enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffa04-134"><span id="WBEM_S_OPERATION_CANCELLED"></span><span id="wbem_s_operation_cancelled"></span>**WBEM \_ S 作業已 \_ \_ 取消**</span><span class="sxs-lookup"><span data-stu-id="ffa04-134"><span id="WBEM_S_OPERATION_CANCELLED"></span><span id="wbem_s_operation_cancelled"></span>**WBEM\_S\_OPERATION\_CANCELLED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffa04-135">262150 (0x40006) </span><span class="sxs-lookup"><span data-stu-id="ffa04-135">262150 (0x40006)</span></span>
</dt> <dt>



<span data-ttu-id="ffa04-136">作業刻意或不慎取消。</span><span class="sxs-lookup"><span data-stu-id="ffa04-136">The operation was intentionally or unintentionally canceled.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffa04-137"><span id="WBEM_S_PENDING"></span><span id="wbem_s_pending"></span>**WBEM \_ S \_ 擱置中**</span><span class="sxs-lookup"><span data-stu-id="ffa04-137"><span id="WBEM_S_PENDING"></span><span id="wbem_s_pending"></span>**WBEM\_S\_PENDING**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffa04-138">262151 (0x40007) </span><span class="sxs-lookup"><span data-stu-id="ffa04-138">262151 (0x40007)</span></span>
</dt> <dt>



<span data-ttu-id="ffa04-139">要求仍在進行中，但結果還無法使用。</span><span class="sxs-lookup"><span data-stu-id="ffa04-139">A request is still in progress, and the results are not yet available.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffa04-140"><span id="WBEM_S_DUPLICATE_OBJECTS"></span><span id="wbem_s_duplicate_objects"></span>**WBEM \_ S \_ 重複的 \_ 物件**</span><span class="sxs-lookup"><span data-stu-id="ffa04-140"><span id="WBEM_S_DUPLICATE_OBJECTS"></span><span id="wbem_s_duplicate_objects"></span>**WBEM\_S\_DUPLICATE\_OBJECTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffa04-141">262152 (0x40008) </span><span class="sxs-lookup"><span data-stu-id="ffa04-141">262152 (0x40008)</span></span>
</dt> <dt>



<span data-ttu-id="ffa04-142">在結果集 (Result Set) 中偵測出一個以上的相同物件。</span><span class="sxs-lookup"><span data-stu-id="ffa04-142">More than one copy of the same object was detected in the result set of an enumeration.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffa04-143"><span id="WBEM_S_ACCESS_DENIED"></span><span id="wbem_s_access_denied"></span>**WBEM \_ \_ 拒絕存取 \_**</span><span class="sxs-lookup"><span data-stu-id="ffa04-143"><span id="WBEM_S_ACCESS_DENIED"></span><span id="wbem_s_access_denied"></span>**WBEM\_S\_ACCESS\_DENIED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffa04-144">262153 (0x40009) </span><span class="sxs-lookup"><span data-stu-id="ffa04-144">262153 (0x40009)</span></span>
</dt> <dt>



<span data-ttu-id="ffa04-145">使用者被拒絕存取某些資源，但並非所有資源。</span><span class="sxs-lookup"><span data-stu-id="ffa04-145">The user was denied access to some but not all resources.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffa04-146"><span id="WBEM_S_PARTIAL_RESULTS"></span><span id="wbem_s_partial_results"></span>**WBEM \_ S \_ 部分 \_ 結果**</span><span class="sxs-lookup"><span data-stu-id="ffa04-146"><span id="WBEM_S_PARTIAL_RESULTS"></span><span id="wbem_s_partial_results"></span>**WBEM\_S\_PARTIAL\_RESULTS**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffa04-147">262160 (0x40010) </span><span class="sxs-lookup"><span data-stu-id="ffa04-147">262160 (0x40010)</span></span>
</dt> <dt>



<span data-ttu-id="ffa04-148">使用者未收到由於安全性違規) 以外的資源 (所要求的所有物件。</span><span class="sxs-lookup"><span data-stu-id="ffa04-148">The user did not receive all of the objects requested due to inaccessible resources (other than security violations).</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffa04-149"><span id="WBEM_S_LIMITED_SERVICE"></span><span id="wbem_s_limited_service"></span>**WBEM \_ S \_ 受限 \_ 服務**</span><span class="sxs-lookup"><span data-stu-id="ffa04-149"><span id="WBEM_S_LIMITED_SERVICE"></span><span id="wbem_s_limited_service"></span>**WBEM\_S\_LIMITED\_SERVICE**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffa04-150">274433 (0x43001) </span><span class="sxs-lookup"><span data-stu-id="ffa04-150">274433 (0x43001)</span></span>
</dt> <dt>



<span data-ttu-id="ffa04-151">提供者能夠提供有限的服務。</span><span class="sxs-lookup"><span data-stu-id="ffa04-151">The provider is capable of limited service.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="ffa04-152"><span id="WBEM_S_INDIRECTLY_UPDATED"></span><span id="wbem_s_indirectly_updated"></span>**\_ \_ \_ 已間接更新 WBEM**</span><span class="sxs-lookup"><span data-stu-id="ffa04-152"><span id="WBEM_S_INDIRECTLY_UPDATED"></span><span id="wbem_s_indirectly_updated"></span>**WBEM\_S\_INDIRECTLY\_UPDATED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="ffa04-153">274434 (0x43002) </span><span class="sxs-lookup"><span data-stu-id="ffa04-153">274434 (0x43002)</span></span>
</dt> <dt>



<span data-ttu-id="ffa04-154">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="ffa04-154">Reserved for future use.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="ffa04-155">規格需求</span><span class="sxs-lookup"><span data-stu-id="ffa04-155">Requirements</span></span>



| <span data-ttu-id="ffa04-156">需求</span><span class="sxs-lookup"><span data-stu-id="ffa04-156">Requirement</span></span> | <span data-ttu-id="ffa04-157">值</span><span class="sxs-lookup"><span data-stu-id="ffa04-157">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ffa04-158">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ffa04-158">Minimum supported client</span></span><br/> | <span data-ttu-id="ffa04-159">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="ffa04-159">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="ffa04-160">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ffa04-160">Minimum supported server</span></span><br/> | <span data-ttu-id="ffa04-161">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="ffa04-161">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="ffa04-162">標頭</span><span class="sxs-lookup"><span data-stu-id="ffa04-162">Header</span></span><br/>                   | <dl> <span data-ttu-id="ffa04-163"><dt>WbemCli。h</dt></span><span class="sxs-lookup"><span data-stu-id="ffa04-163"><dt>WbemCli.h</dt></span></span> </dl>   |
| <span data-ttu-id="ffa04-164">Idl</span><span class="sxs-lookup"><span data-stu-id="ffa04-164">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ffa04-165"><dt>WbemCli .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ffa04-165"><dt>WbemCli.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ffa04-166">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ffa04-166">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ffa04-167">WMI 傳回碼</span><span class="sxs-lookup"><span data-stu-id="ffa04-167">WMI Return Codes</span></span>](wmi-return-codes.md)
</dt> </dl>

 

