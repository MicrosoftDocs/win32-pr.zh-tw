---
title: 'EAP \_ 認證 \_ RESP (Eaptypes .h) '
description: '在 EAP 設定 \_ \_ 輸入 \_ 欄位 \_ 陣列結構內儲存 eap 安全性認證。 |EAP \_ 認證 \_ RESP (Eaptypes .h) '
ms.assetid: 714c75d8-71c7-4c3f-802a-a5e4f6ca65c2
keywords:
- EAP_CRED_RESP
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e5c2176377dbde0f7c02d2a7d8083ad1bcff9e71
ms.sourcegitcommit: 92e74c99f8f4d097676959d0c317f533c2400a80
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/09/2021
ms.locfileid: "107000537"
---
# <a name="eap_cred_resp"></a><span data-ttu-id="127b6-105">EAP \_ 認證 \_ RESP</span><span class="sxs-lookup"><span data-stu-id="127b6-105">EAP\_CRED\_RESP</span></span>

<span data-ttu-id="127b6-106">**Eap 認證 \_ \_ RESP** 結構會在 [**eap 設定 \_ \_ 輸入 \_ 欄位 \_ 陣列**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array)結構中儲存 eap 安全性認證。</span><span class="sxs-lookup"><span data-stu-id="127b6-106">The **EAP\_CRED\_RESP** structure stores EAP security credentials within a [**EAP\_CONFIG\_INPUT\_FIELD\_ARRAY**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_config_input_field_array) structure.</span></span>


```C++
typedef EAP_CONFIG_INPUT_FIELD_ARRAY EAP_CRED_RESP;
```



<dl> <dt>

<span data-ttu-id="127b6-107">**EAP \_ 認證 \_ RESP**</span><span class="sxs-lookup"><span data-stu-id="127b6-107">**EAP\_CRED\_RESP**</span></span>
</dt> <dd>

<span data-ttu-id="127b6-108">Eap [**\_ 互動式 \_ ui \_ 資料 \_ 類型**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type)的 *dwDataType* 參數指定認證回應類型時， **eap 認證 \_ \_ RESP** 結構會儲存 [**eap \_ 互動式 \_ ui \_ 資料**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)結構的 *pbUiData* 參數所指向的舊和新 EAP 安全性認證。</span><span class="sxs-lookup"><span data-stu-id="127b6-108">The **EAP\_CRED\_RESP** structure stores both the old and new EAP security credentials pointed to by the *pbUiData* parameter of the [**EAP\_INTERACTIVE\_UI\_DATA**](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data) structure when the *dwDataType* parameter of [**EAP\_INTERACTIVE\_UI\_DATA\_TYPE**](/windows/desktop/api/eaptypes/ne-eaptypes-eap_interactive_ui_data_type) specifies a credential response type.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="127b6-109">備註</span><span class="sxs-lookup"><span data-stu-id="127b6-109">Remarks</span></span>

<span data-ttu-id="127b6-110">**EAP 認證 \_ \_ RESP** 結構是用來支援單一登入 (SSO) 。</span><span class="sxs-lookup"><span data-stu-id="127b6-110">The **EAP\_CRED\_RESP** structure is used to support Single-Sign-On (SSO).</span></span>

<span data-ttu-id="127b6-111">**Eap 認證 \_ \_ RESP** 結構與 [**eap 認證 \_ \_ 需求**](eap-cred-req.md)結構相同。</span><span class="sxs-lookup"><span data-stu-id="127b6-111">The **EAP\_CRED\_RESP** structure is identical to the [**EAP\_CRED\_REQ**](eap-cred-req.md) structure.</span></span>

## <a name="requirements"></a><span data-ttu-id="127b6-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="127b6-112">Requirements</span></span>



| <span data-ttu-id="127b6-113">需求</span><span class="sxs-lookup"><span data-stu-id="127b6-113">Requirement</span></span> | <span data-ttu-id="127b6-114">值</span><span class="sxs-lookup"><span data-stu-id="127b6-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="127b6-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="127b6-115">Minimum supported client</span></span><br/> | <span data-ttu-id="127b6-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="127b6-116">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="127b6-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="127b6-117">Minimum supported server</span></span><br/> | <span data-ttu-id="127b6-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="127b6-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="127b6-119">標頭</span><span class="sxs-lookup"><span data-stu-id="127b6-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="127b6-120"><dt>Eaptypes。h</dt></span><span class="sxs-lookup"><span data-stu-id="127b6-120"><dt>Eaptypes.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="127b6-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="127b6-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="127b6-122">EAPHost 要求者結構</span><span class="sxs-lookup"><span data-stu-id="127b6-122">EAPHost Supplicant Structures</span></span>](eap-host-supplicant-structures.md)
</dt> <dt>

[<span data-ttu-id="127b6-123">**EAP \_ 認證 \_ 需求**</span><span class="sxs-lookup"><span data-stu-id="127b6-123">**EAP\_CRED\_REQ**</span></span>](eap-cred-req.md)
</dt> <dt>

[<span data-ttu-id="127b6-124">**EAP \_ 認證 \_ 到期 \_ 申請**</span><span class="sxs-lookup"><span data-stu-id="127b6-124">**EAP\_CRED\_EXPIRY\_REQ**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_cred_expiry_req)
</dt> <dt>

<span data-ttu-id="127b6-125">[**EAP \_ 認證 \_ 到期 \_ RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="127b6-125">[**EAP\_CRED\_EXPIRY\_RESP**](/previous-versions/windows/desktop/legacy/bb530539(v=vs.85))</span></span>
</dt> <dt>

[<span data-ttu-id="127b6-126">**EAP \_ 互動式 \_ UI \_ 資料**</span><span class="sxs-lookup"><span data-stu-id="127b6-126">**EAP\_INTERACTIVE\_UI\_DATA**</span></span>](/windows/desktop/api/eaptypes/ns-eaptypes-eap_interactive_ui_data)
</dt> <dt>

[<span data-ttu-id="127b6-127">SSO 和 PLAP</span><span class="sxs-lookup"><span data-stu-id="127b6-127">SSO and PLAP</span></span>](understanding-sso-and-plap.md)
</dt> </dl>

 

