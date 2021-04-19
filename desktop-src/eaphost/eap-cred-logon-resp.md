---
title: 'EAP \_ 認證 \_ 登入 \_ RESP (Eaptypes .h) '
description: '在 EAP 設定 \_ \_ 輸入 \_ 欄位 \_ 陣列結構內儲存 eap 安全性認證。 |EAP \_ 認證 \_ 登入 \_ RESP (Eaptypes .h) '
ms.assetid: 1244A40F-6999-4053-97C4-1C4FB107B2F5
keywords:
- EAP_CRED_LOGON_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b0e1bbabc30918efaed0e286b5df231537ed5543
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "107000552"
---
# <a name="eap_cred_logon_resp"></a><span data-ttu-id="6daaa-105">EAP \_ 認證 \_ 登入 \_ RESP</span><span class="sxs-lookup"><span data-stu-id="6daaa-105">EAP\_CRED\_LOGON\_RESP</span></span>

<span data-ttu-id="6daaa-106">**Eap 認證 \_ 登 \_ 入 \_ RESP** 結構會在 [**eap 設定 \_ \_ 輸入 \_ 欄位 \_ 陣列**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)結構中儲存 eap 安全性認證。</span><span class="sxs-lookup"><span data-stu-id="6daaa-106">The **EAP\_CRED\_LOGON\_RESP** structure stores EAP security credentials within a [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_RESP;
```



<dl> <dt>

<span data-ttu-id="6daaa-107">**EAP \_ 認證 \_ 登入 \_ RESP**</span><span class="sxs-lookup"><span data-stu-id="6daaa-107">**EAP\_CRED\_LOGON\_RESP**</span></span>
</dt> <dd>

<span data-ttu-id="6daaa-108">Eap [**\_ 互動式 \_ ui \_ 資料 \_ 類型**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)的 *dwDataType* 參數指定認證要求類型時， **eap 認證登入 \_ \_ \_ RESP** 結構會儲存 [**eap \_ 互動式 \_ ui \_ 資料**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)結構的 *pbUiData* 參數所指向的 eap 安全性認證。</span><span class="sxs-lookup"><span data-stu-id="6daaa-108">The **EAP\_CRED\_LOGON\_RESP** structure stores EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential request type.</span></span> <span data-ttu-id="6daaa-109">此結構中的輸入欄位會與 [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)所傳回的輸入欄位相同。</span><span class="sxs-lookup"><span data-stu-id="6daaa-109">The input fields in this structure will be same as the input fields returned by [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span></span> <span data-ttu-id="6daaa-110">**EAP \_認證 \_ 登入 \_ RESP** 用於初始認證要求中，而 [**EAP \_ 認證 \_ RESP**](eap-cred-resp.md) 則用於驗證期間的認證重試要求。</span><span class="sxs-lookup"><span data-stu-id="6daaa-110">**EAP\_CRED\_LOGON\_RESP** is used in the initial credential request and [**EAP\_CRED\_RESP**](eap-cred-resp.md) is used in the credential retry request during an authentication.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6daaa-111">備註</span><span class="sxs-lookup"><span data-stu-id="6daaa-111">Remarks</span></span>

<span data-ttu-id="6daaa-112">**EAP 認證 \_ 登 \_ 入 \_ RESP** 結構是用來支援單一登入 (SSO) 。</span><span class="sxs-lookup"><span data-stu-id="6daaa-112">The **EAP\_CRED\_LOGON\_RESP** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="6daaa-113">**Eap 認證 \_ 登 \_ 入 \_ RESP** 結構等同于 eap 認證 [**\_ \_ 登 \_**](eap-cred-logon-req.md)入要求結構。</span><span class="sxs-lookup"><span data-stu-id="6daaa-113">The **EAP\_CRED\_LOGON\_RESP** structure is identical to the [**EAP\_CRED\_LOGON\_REQ**](eap-cred-logon-req.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="6daaa-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="6daaa-114">Requirements</span></span>



| <span data-ttu-id="6daaa-115">需求</span><span class="sxs-lookup"><span data-stu-id="6daaa-115">Requirement</span></span> | <span data-ttu-id="6daaa-116">值</span><span class="sxs-lookup"><span data-stu-id="6daaa-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="6daaa-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6daaa-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6daaa-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6daaa-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="6daaa-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6daaa-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6daaa-120">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6daaa-120">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="6daaa-121">標頭</span><span class="sxs-lookup"><span data-stu-id="6daaa-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6daaa-122"><dt>Eaptypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="6daaa-122"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6daaa-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6daaa-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6daaa-124">**EapHostPeerQueryCredentialInputFields**</span><span class="sxs-lookup"><span data-stu-id="6daaa-124">**EapHostPeerQueryCredentialInputFields**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> <dt>

[<span data-ttu-id="6daaa-125">**EAP \_ 設定 \_ 輸入 \_ 欄位 \_ 陣列**</span><span class="sxs-lookup"><span data-stu-id="6daaa-125">**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[<span data-ttu-id="6daaa-126">**EAP 認證登入要求 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="6daaa-126">**EAP\_CRED\_LOGON\_REQ**</span></span>](eap-cred-logon-req.md)
</dt> <dt>

[<span data-ttu-id="6daaa-127">**EAP \_ 互動式 \_ UI \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="6daaa-127">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="6daaa-128">**EAP \_ 互動式 \_ UI \_ 資料 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="6daaa-128">**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> </dl>

 

 





