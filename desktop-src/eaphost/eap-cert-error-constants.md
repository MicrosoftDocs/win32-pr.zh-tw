---
title: 'EAP 憑證 \_ 錯誤常數 (Eaphosterror .h) '
description: 定義所有 EAPHost API 技術通用的憑證相關錯誤。
ms.assetid: 12f626e1-520a-4aba-954b-769c3062a38c
topic_type:
- apiref
api_name:
- _EAP_CERT_FIRST
- _EAP_CERT_LAST
- _EAP_CERT_NOT_FOUND
- _EAP_CERT_INVALID
- _EAP_CERT_EXPIRED
- _EAP_CERT_REVOKED
- _EAP_CERT_OTHER_ERROR
- _EAP_CERT_REJECTED
- _EAP_CERT_NAME_REQUIRED
- _EAP_GENERAL_FIRST
- _EAP_GENERAL_LAST
api_location:
- eaphosterror.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0543636f36d823b5557ad2f5a5f7cb000d93259a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508400"
---
# <a name="eap_cert-error-constants"></a><span data-ttu-id="4a2b7-103">EAP 憑證 \_ 錯誤常數</span><span class="sxs-lookup"><span data-stu-id="4a2b7-103">EAP\_CERT Error Constants</span></span>

<span data-ttu-id="4a2b7-104">這些常數會定義所有 EAPHost API 技術通用的憑證相關錯誤。</span><span class="sxs-lookup"><span data-stu-id="4a2b7-104">These constants define certificate-related errors common to all EAPHost API technologies.</span></span>

<dl> <dt>

<span data-ttu-id="4a2b7-105"><span id="_EAP_CERT_FIRST"></span><span id="_eap_cert_first"></span>**\_EAP \_ 憑證 \_ 優先**</span><span class="sxs-lookup"><span data-stu-id="4a2b7-105"><span id="_EAP_CERT_FIRST"></span><span id="_eap_cert_first"></span>**\_EAP\_CERT\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a2b7-106">0x0</span><span class="sxs-lookup"><span data-stu-id="4a2b7-106">0x0</span></span>
</dt> <dt>



<span data-ttu-id="4a2b7-107">定義錯誤報表的界限;**\_ eap 憑證 \_ \_ FIRST** 和 **\_ eap \_ \_** 憑證之間會發生任何憑證錯誤。</span><span class="sxs-lookup"><span data-stu-id="4a2b7-107">Defines the boundary of error reports; any certificate error will occur between **\_EAP\_CERT\_FIRST** and **\_EAP\_CERT\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a2b7-108"><span id="_EAP_CERT_LAST"></span><span id="_eap_cert_last"></span>**\_EAP \_ 憑證 \_ LAST**</span><span class="sxs-lookup"><span data-stu-id="4a2b7-108"><span id="_EAP_CERT_LAST"></span><span id="_eap_cert_last"></span>**\_EAP\_CERT\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a2b7-109">0xF</span><span class="sxs-lookup"><span data-stu-id="4a2b7-109">0xF</span></span>
</dt> <dt>



<span data-ttu-id="4a2b7-110">定義錯誤報表的界限;**\_ eap 憑證 \_ \_ FIRST** 和 **\_ eap \_ \_** 憑證之間會發生任何憑證錯誤。</span><span class="sxs-lookup"><span data-stu-id="4a2b7-110">Defines the boundary of error reports; any certificate error will occur between **\_EAP\_CERT\_FIRST** and **\_EAP\_CERT\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a2b7-111"><span id="_EAP_CERT_NOT_FOUND"></span><span id="_eap_cert_not_found"></span>**\_\_ \_ \_ 找不到 EAP 憑證**</span><span class="sxs-lookup"><span data-stu-id="4a2b7-111"><span id="_EAP_CERT_NOT_FOUND"></span><span id="_eap_cert_not_found"></span>**\_EAP\_CERT\_NOT\_FOUND**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a2b7-112">0x1</span><span class="sxs-lookup"><span data-stu-id="4a2b7-112">0x1</span></span>
</dt> <dt>



<span data-ttu-id="4a2b7-113">找不到任何使用者憑證。</span><span class="sxs-lookup"><span data-stu-id="4a2b7-113">No user certificate was found.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a2b7-114"><span id="_EAP_CERT_INVALID"></span><span id="_eap_cert_invalid"></span>**\_EAP \_ 憑證 \_ 無效**</span><span class="sxs-lookup"><span data-stu-id="4a2b7-114"><span id="_EAP_CERT_INVALID"></span><span id="_eap_cert_invalid"></span>**\_EAP\_CERT\_INVALID**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a2b7-115">0x2</span><span class="sxs-lookup"><span data-stu-id="4a2b7-115">0x2</span></span>
</dt> <dt>



<span data-ttu-id="4a2b7-116">使用者憑證無效。</span><span class="sxs-lookup"><span data-stu-id="4a2b7-116">The user certificate is invalid.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a2b7-117"><span id="_EAP_CERT_EXPIRED"></span><span id="_eap_cert_expired"></span>**\_EAP 憑證已 \_ \_ 過期**</span><span class="sxs-lookup"><span data-stu-id="4a2b7-117"><span id="_EAP_CERT_EXPIRED"></span><span id="_eap_cert_expired"></span>**\_EAP\_CERT\_EXPIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a2b7-118">0x3</span><span class="sxs-lookup"><span data-stu-id="4a2b7-118">0x3</span></span>
</dt> <dt>



<span data-ttu-id="4a2b7-119">使用者憑證已過期。</span><span class="sxs-lookup"><span data-stu-id="4a2b7-119">The user certificate has expired.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a2b7-120"><span id="_EAP_CERT_REVOKED"></span><span id="_eap_cert_revoked"></span>**\_已 \_ 撤銷 EAP 憑證 \_**</span><span class="sxs-lookup"><span data-stu-id="4a2b7-120"><span id="_EAP_CERT_REVOKED"></span><span id="_eap_cert_revoked"></span>**\_EAP\_CERT\_REVOKED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a2b7-121">0x4</span><span class="sxs-lookup"><span data-stu-id="4a2b7-121">0x4</span></span>
</dt> <dt>



<span data-ttu-id="4a2b7-122">使用者憑證已撤銷。</span><span class="sxs-lookup"><span data-stu-id="4a2b7-122">The user certificate was revoked.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a2b7-123"><span id="_EAP_CERT_OTHER_ERROR"></span><span id="_eap_cert_other_error"></span>**\_EAP \_ 憑證 \_ 其他 \_ 錯誤**</span><span class="sxs-lookup"><span data-stu-id="4a2b7-123"><span id="_EAP_CERT_OTHER_ERROR"></span><span id="_eap_cert_other_error"></span>**\_EAP\_CERT\_OTHER\_ERROR**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a2b7-124">0x5</span><span class="sxs-lookup"><span data-stu-id="4a2b7-124">0x5</span></span>
</dt> <dt>



<span data-ttu-id="4a2b7-125">有未知的憑證相關錯誤。</span><span class="sxs-lookup"><span data-stu-id="4a2b7-125">There is an unknown certificate related error.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a2b7-126"><span id="_EAP_CERT_REJECTED"></span><span id="_eap_cert_rejected"></span>**\_已 \_ 拒絕 EAP 憑證 \_**</span><span class="sxs-lookup"><span data-stu-id="4a2b7-126"><span id="_EAP_CERT_REJECTED"></span><span id="_eap_cert_rejected"></span>**\_EAP\_CERT\_REJECTED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a2b7-127">0x6</span><span class="sxs-lookup"><span data-stu-id="4a2b7-127">0x6</span></span>
</dt> <dt>



<span data-ttu-id="4a2b7-128">使用者憑證遭到拒絕。</span><span class="sxs-lookup"><span data-stu-id="4a2b7-128">The user certificate was rejected.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a2b7-129"><span id="_EAP_CERT_NAME_REQUIRED"></span><span id="_eap_cert_name_required"></span>**\_需要 EAP 憑證 \_ \_ 名稱 \_**</span><span class="sxs-lookup"><span data-stu-id="4a2b7-129"><span id="_EAP_CERT_NAME_REQUIRED"></span><span id="_eap_cert_name_required"></span>**\_EAP\_CERT\_NAME\_REQUIRED**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a2b7-130">0x7</span><span class="sxs-lookup"><span data-stu-id="4a2b7-130">0x7</span></span>
</dt> <dt>



<span data-ttu-id="4a2b7-131">使用者憑證需要名稱。</span><span class="sxs-lookup"><span data-stu-id="4a2b7-131">The user certificate requires a name.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a2b7-132"><span id="_EAP_GENERAL_FIRST"></span><span id="_eap_general_first"></span>**\_EAP \_ 一般 \_ 優先**</span><span class="sxs-lookup"><span data-stu-id="4a2b7-132"><span id="_EAP_GENERAL_FIRST"></span><span id="_eap_general_first"></span>**\_EAP\_GENERAL\_FIRST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a2b7-133">0x10</span><span class="sxs-lookup"><span data-stu-id="4a2b7-133">0x10</span></span>
</dt> <dt>



<span data-ttu-id="4a2b7-134">定義錯誤報表的界限;任何一般 EAP 錯誤都會在 **\_ eap \_ 一般 \_ 優先** 和 **\_ eap \_ 一般 \_** 之間發生。</span><span class="sxs-lookup"><span data-stu-id="4a2b7-134">Defines the boundary of error reports; any general EAP error will occur between **\_EAP\_GENERAL\_FIRST** and **\_EAP\_GENERAL\_LAST**.</span></span>


</dt> </dl> </dd> <dt>

<span data-ttu-id="4a2b7-135"><span id="_EAP_GENERAL_LAST"></span><span id="_eap_general_last"></span>**\_EAP \_ 一般 \_ 最後**</span><span class="sxs-lookup"><span data-stu-id="4a2b7-135"><span id="_EAP_GENERAL_LAST"></span><span id="_eap_general_last"></span>**\_EAP\_GENERAL\_LAST**</span></span>
</dt> <dd> <dl> <dt>

<span data-ttu-id="4a2b7-136">0x3F</span><span class="sxs-lookup"><span data-stu-id="4a2b7-136">0x3F</span></span>
</dt> <dt>



<span data-ttu-id="4a2b7-137">定義錯誤報表的界限;任何一般 EAP 錯誤都會在 **\_ eap \_ 一般 \_ 優先** 和 **\_ eap \_ 一般 \_** 之間發生。</span><span class="sxs-lookup"><span data-stu-id="4a2b7-137">Defines the boundary of error reports; any general EAP error will occur between **\_EAP\_GENERAL\_FIRST** and **\_EAP\_GENERAL\_LAST**.</span></span>


</dt> </dl> </dd> </dl>

## <a name="requirements"></a><span data-ttu-id="4a2b7-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="4a2b7-138">Requirements</span></span>



| <span data-ttu-id="4a2b7-139">需求</span><span class="sxs-lookup"><span data-stu-id="4a2b7-139">Requirement</span></span> | <span data-ttu-id="4a2b7-140">值</span><span class="sxs-lookup"><span data-stu-id="4a2b7-140">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------------|
| <span data-ttu-id="4a2b7-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4a2b7-141">Minimum supported client</span></span><br/> | <span data-ttu-id="4a2b7-142">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a2b7-142">Windows Vista \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="4a2b7-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4a2b7-143">Minimum supported server</span></span><br/> | <span data-ttu-id="4a2b7-144">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4a2b7-144">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="4a2b7-145">標頭</span><span class="sxs-lookup"><span data-stu-id="4a2b7-145">Header</span></span><br/>                   | <dl> <span data-ttu-id="4a2b7-146"><dt>Eaphosterror。h</dt></span><span class="sxs-lookup"><span data-stu-id="4a2b7-146"><dt>Eaphosterror.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4a2b7-147">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4a2b7-147">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4a2b7-148">常見的 EAPHost 常數</span><span class="sxs-lookup"><span data-stu-id="4a2b7-148">Common EAPHost Constants</span></span>](common-eap-host-error-constants.md)
</dt> </dl>

 

 





