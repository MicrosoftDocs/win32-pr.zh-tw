---
description: 指定憑證範本的名稱。
ms.assetid: 15d22130-e614-4505-94e8-83c2efbf6d87
title: ISCrdEnr：： setCertTemplateName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setCertTemplateName
- SCrdEnr.setCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 53ba18626a7d2bb703ed4d11953fb4872cf9257c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983516"
---
# <a name="iscrdenrsetcerttemplatename-method"></a><span data-ttu-id="38ac5-103">ISCrdEnr：： setCertTemplateName 方法</span><span class="sxs-lookup"><span data-stu-id="38ac5-103">ISCrdEnr::setCertTemplateName method</span></span>

<span data-ttu-id="38ac5-104">**SetCertTemplateName** 方法會指定憑證範本的名稱。</span><span class="sxs-lookup"><span data-stu-id="38ac5-104">The **setCertTemplateName** method specifies the name of the certificate template.</span></span>

## <a name="syntax"></a><span data-ttu-id="38ac5-105">語法</span><span class="sxs-lookup"><span data-stu-id="38ac5-105">Syntax</span></span>


```C++
HRESULT setCertTemplateName(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setCertTemplateName( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="38ac5-106">參數</span><span class="sxs-lookup"><span data-stu-id="38ac5-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="38ac5-107">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="38ac5-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38ac5-108">值，決定是否要設定憑證範本的真實名稱或顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="38ac5-108">Value which determines if the certificate template's real name or display name is being set.</span></span> <span data-ttu-id="38ac5-109">如果 *dwFlags* 的值為捨棄 \_ 註冊 \_ \_ 憑證範本 \_ 顯示 \_ 名稱，則會設定憑證範本的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="38ac5-109">If *dwFlags* has the value SCARD\_ENROLL\_CERT\_TEMPLATE\_DISPLAY\_NAME, the certificate template's display name is set.</span></span> <span data-ttu-id="38ac5-110">否則，會設定憑證範本的真實名稱。</span><span class="sxs-lookup"><span data-stu-id="38ac5-110">Otherwise, the real name of the certificate template is set.</span></span>

</dd> <dt>

<span data-ttu-id="38ac5-111">*bstrCertTemplateName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="38ac5-111">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="38ac5-112">將在憑證要求中使用的憑證範本名稱。</span><span class="sxs-lookup"><span data-stu-id="38ac5-112">Name of the certificate template which will be used in the certificate request.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="38ac5-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="38ac5-113">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="38ac5-114">VB</span><span class="sxs-lookup"><span data-stu-id="38ac5-114">VB</span></span>

<span data-ttu-id="38ac5-115">如果方法成功，則方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="38ac5-115">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="38ac5-116">如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="38ac5-116">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="38ac5-117">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="38ac5-117">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="38ac5-118">備註</span><span class="sxs-lookup"><span data-stu-id="38ac5-118">Remarks</span></span>

<span data-ttu-id="38ac5-119">如果您未藉由呼叫 **ISCrdEnr：： setCertTemplateName** 來設定憑證範本名稱，則名稱會預設為可用憑證範本清單中的第一個名稱。</span><span class="sxs-lookup"><span data-stu-id="38ac5-119">If you do not set the certificate template name by calling **ISCrdEnr::setCertTemplateName**, the name defaults to the first name in the list of available certificate templates.</span></span>

## <a name="requirements"></a><span data-ttu-id="38ac5-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="38ac5-120">Requirements</span></span>



| <span data-ttu-id="38ac5-121">需求</span><span class="sxs-lookup"><span data-stu-id="38ac5-121">Requirement</span></span> | <span data-ttu-id="38ac5-122">值</span><span class="sxs-lookup"><span data-stu-id="38ac5-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="38ac5-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="38ac5-123">Minimum supported client</span></span><br/> | <span data-ttu-id="38ac5-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="38ac5-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="38ac5-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="38ac5-125">Minimum supported server</span></span><br/> | <span data-ttu-id="38ac5-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="38ac5-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="38ac5-127">DLL</span><span class="sxs-lookup"><span data-stu-id="38ac5-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="38ac5-128"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="38ac5-128"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="38ac5-129">IID</span><span class="sxs-lookup"><span data-stu-id="38ac5-129">IID</span></span><br/>                      | <span data-ttu-id="38ac5-130">IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="38ac5-130">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="38ac5-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="38ac5-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="38ac5-132">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="38ac5-132">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="38ac5-133">**ISCrdEnr::getCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="38ac5-133">**ISCrdEnr::getCertTemplateName**</span></span>](iscrdenr-getcerttemplatename.md)
</dt> </dl>

 

 




