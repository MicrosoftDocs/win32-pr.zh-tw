---
title: 'EAP 認證登入要求 \_ \_ \_ (Eaptypes .h) '
description: 在 EAP 設定 \_ \_ 輸入 \_ 欄位 \_ 陣列結構內儲存 eap 安全性認證。
ms.assetid: 1F1A2F77-054D-4FD2-83A5-69C3D77418B3
keywords:
- EAP_CRED_LOGON_REQ
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2af29daa9d68e4cd2dd78f101585c2fa14d25200
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024864"
---
# <a name="eap_cred_logon_req"></a><span data-ttu-id="93b35-104">EAP 認證登入要求 \_ \_ \_</span><span class="sxs-lookup"><span data-stu-id="93b35-104">EAP\_CRED\_LOGON\_REQ</span></span>

<span data-ttu-id="93b35-105">**Eap 認證 \_ \_ 登 \_** 入要求結構會將 Eap 安全性認證儲存在 [**eap \_ CONFIG \_ 輸入 \_ 欄位 \_ 陣列**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)結構中。</span><span class="sxs-lookup"><span data-stu-id="93b35-105">The **EAP\_CRED\_LOGON\_REQ** structure stores EAP security credentials within an [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_LOGON_REQ;
```



<dl> <dt>

<span data-ttu-id="93b35-106">**EAP 認證登入要求 \_ \_ \_**</span><span class="sxs-lookup"><span data-stu-id="93b35-106">**EAP\_CRED\_LOGON\_REQ**</span></span>
</dt> <dd>

<span data-ttu-id="93b35-107">Eap **驗證 \_ \_ 登 \_** 入要求結構會在 eap 互動式 ui [**\_ \_ \_ 資料 \_ 類型**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)的 *dwDataType* 參數指定認證要求類型時，儲存 [**eap \_ 互動式 \_ ui \_ 資料**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)結構的 *pbUiData* 參數所指向的 eap 安全性認證。</span><span class="sxs-lookup"><span data-stu-id="93b35-107">The **EAP\_CRED\_LOGON\_REQ** structure stores EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential request type.</span></span> <span data-ttu-id="93b35-108">此結構中的輸入欄位與 [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)所傳回的輸入欄位相同。</span><span class="sxs-lookup"><span data-stu-id="93b35-108">The input fields in this structure are the same as the input fields returned by [**EapHostPeerQueryCredentialInputFields**](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields).</span></span> <span data-ttu-id="93b35-109">**EAP \_認證 \_ 登 \_** 入要求用於初始認證要求中，而 [**EAP \_ \_**](eap-cred-req.md) 認證要求則用於驗證期間的認證重試要求。</span><span class="sxs-lookup"><span data-stu-id="93b35-109">**EAP\_CRED\_LOGON\_REQ** is used in the initial credential request and [**EAP\_CRED\_REQ**](eap-cred-req.md) is used in the credential retry request during an authentication.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="93b35-110">備註</span><span class="sxs-lookup"><span data-stu-id="93b35-110">Remarks</span></span>

<span data-ttu-id="93b35-111">**EAP 認證 \_ \_ 登 \_** 入要求結構是用來支援單一登入 (SSO) 。</span><span class="sxs-lookup"><span data-stu-id="93b35-111">The **EAP\_CRED\_LOGON\_REQ** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="93b35-112">**Eap 認證 \_ \_ 登 \_** 入要求結構與 [**eap 認證登入 \_ \_ \_ RESP**](eap-cred-logon-resp.md)結構相同。</span><span class="sxs-lookup"><span data-stu-id="93b35-112">The **EAP\_CRED\_LOGON\_REQ** structure is identical to the [**EAP\_CRED\_LOGON\_RESP**](eap-cred-logon-resp.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="93b35-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="93b35-113">Requirements</span></span>



| <span data-ttu-id="93b35-114">需求</span><span class="sxs-lookup"><span data-stu-id="93b35-114">Requirement</span></span> | <span data-ttu-id="93b35-115">值</span><span class="sxs-lookup"><span data-stu-id="93b35-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="93b35-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="93b35-116">Minimum supported client</span></span><br/> | <span data-ttu-id="93b35-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93b35-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="93b35-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="93b35-118">Minimum supported server</span></span><br/> | <span data-ttu-id="93b35-119">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="93b35-119">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="93b35-120">標頭</span><span class="sxs-lookup"><span data-stu-id="93b35-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="93b35-121"><dt>Eaptypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="93b35-121"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="93b35-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93b35-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93b35-123">**EAP \_ 設定 \_ 輸入 \_ 欄位 \_ 陣列**</span><span class="sxs-lookup"><span data-stu-id="93b35-123">**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)
</dt> <dt>

[<span data-ttu-id="93b35-124">**EAP \_ 認證 \_ 需求**</span><span class="sxs-lookup"><span data-stu-id="93b35-124">**EAP\_CRED\_REQ**</span></span>](eap-cred-req.md)
</dt> <dt>

[<span data-ttu-id="93b35-125">**EAP \_ 互動式 \_ UI \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="93b35-125">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="93b35-126">**EAP \_ 互動式 \_ UI \_ 資料 \_ 類型**</span><span class="sxs-lookup"><span data-stu-id="93b35-126">**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**</span></span>](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)
</dt> <dt>

[<span data-ttu-id="93b35-127">**EapHostPeerQueryCredentialInputFields**</span><span class="sxs-lookup"><span data-stu-id="93b35-127">**EapHostPeerQueryCredentialInputFields**</span></span>](/previous-versions/windows/desktop/api/eaphostpeerconfigapis/nf-eaphostpeerconfigapis-eaphostpeerquerycredentialinputfields)
</dt> </dl>

 

 





