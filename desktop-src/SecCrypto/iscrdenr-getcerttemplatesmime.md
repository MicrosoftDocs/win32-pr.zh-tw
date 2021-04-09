---
description: 用來判斷憑證範本是否包含 szOID PKIX 的 \_ \_ \_ 電子郵件 \_ 保護金鑰使用方式。
ms.assetid: 1f0512e0-68b6-4b79-84bd-614babb4151d
title: ISCrdEnr：： getCertTemplateSMIME 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateSMIME
- SCrdEnr.getCertTemplateSMIME
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 4ed66af6a8a91855fbfc5a972a8bf00358314663
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851283"
---
# <a name="iscrdenrgetcerttemplatesmime-method"></a><span data-ttu-id="3ad52-103">ISCrdEnr：： getCertTemplateSMIME 方法</span><span class="sxs-lookup"><span data-stu-id="3ad52-103">ISCrdEnr::getCertTemplateSMIME method</span></span>

<span data-ttu-id="3ad52-104">**GetCertTemplateSMIME** 方法是用來判斷憑證範本是否包含 szOID PKIX 的的 \_ \_ \_ 電子郵件 \_ 保護金鑰使用方式。</span><span class="sxs-lookup"><span data-stu-id="3ad52-104">The **getCertTemplateSMIME** method is used to determine whether a certificate template contains the szOID\_PKIX\_KP\_EMAIL\_PROTECTION key usage.</span></span>

<span data-ttu-id="3ad52-105">如果此金鑰使用方式是憑證範本的一部分，憑證範本支援 [*安全/多用途網際網路郵件延伸*](../secgloss/s-gly.md) (S/MIME) 作業。</span><span class="sxs-lookup"><span data-stu-id="3ad52-105">If this key usage is part of the certificate template, the certificate template supports [*Secure/Multipurpose Internet Mail Extensions*](../secgloss/s-gly.md) (S/MIME) operations.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ad52-106">語法</span><span class="sxs-lookup"><span data-stu-id="3ad52-106">Syntax</span></span>


```C++
HRESULT getCertTemplateSMIME(
  [in]  BSTR      bstrCertTemplateName,
  [out] DWORD *pdwCertTemplateSMIME
);
```


```VB

SCrdEnr.getCertTemplateSMIME( _
  ByVal bstrCertTemplateName, _
  ByRef pdwCertTemplateSMIME _
)
```





## <a name="parameters"></a><span data-ttu-id="3ad52-107">參數</span><span class="sxs-lookup"><span data-stu-id="3ad52-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ad52-108">*bstrCertTemplateName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ad52-108">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ad52-109">要查詢 S/MIME 金鑰使用方式的憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="3ad52-109">The name of the certificate being queried for the S/MIME key usage.</span></span>

</dd> <dt>

<span data-ttu-id="3ad52-110">*pdwCertTemplateSMIME* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3ad52-110">*pdwCertTemplateSMIME* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3ad52-111">**DWORD** 的指標，如果 *bstrCertTemplateName* 支援 S/MIME，則會傳回一個值。否則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="3ad52-111">A pointer to a **DWORD** that returns a value of one if *bstrCertTemplateName* supports S/MIME; otherwise it returns zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ad52-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ad52-112">Return value</span></span>

### <a name="c"></a><span data-ttu-id="3ad52-113">C++</span><span class="sxs-lookup"><span data-stu-id="3ad52-113">C++</span></span>

<span data-ttu-id="3ad52-114">如果方法成功，則方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="3ad52-114">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="3ad52-115">如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="3ad52-115">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="3ad52-116">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="3ad52-116">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="3ad52-117">VB</span><span class="sxs-lookup"><span data-stu-id="3ad52-117">VB</span></span>

<span data-ttu-id="3ad52-118">如果 *bstrCertTemplateName* 支援 S/MIME，則會有 **Long** 值。否則為零。</span><span class="sxs-lookup"><span data-stu-id="3ad52-118">**Long** value of one if *bstrCertTemplateName* supports S/MIME; otherwise zero.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ad52-119">備註</span><span class="sxs-lookup"><span data-stu-id="3ad52-119">Remarks</span></span>

<span data-ttu-id="3ad52-120">SzOID \_ PKIX \_ KP \_ 電子郵件保護的常數 \_ 定義于 Wincrypt 中。</span><span class="sxs-lookup"><span data-stu-id="3ad52-120">The constant for szOID\_PKIX\_KP\_EMAIL\_PROTECTION is defined in Wincrypt.h.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ad52-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ad52-121">Requirements</span></span>



| <span data-ttu-id="3ad52-122">需求</span><span class="sxs-lookup"><span data-stu-id="3ad52-122">Requirement</span></span> | <span data-ttu-id="3ad52-123">值</span><span class="sxs-lookup"><span data-stu-id="3ad52-123">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3ad52-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ad52-124">Minimum supported client</span></span><br/> | <span data-ttu-id="3ad52-125">都不支援</span><span class="sxs-lookup"><span data-stu-id="3ad52-125">None supported</span></span><br/>                                                               |
| <span data-ttu-id="3ad52-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ad52-126">Minimum supported server</span></span><br/> | <span data-ttu-id="3ad52-127">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ad52-127">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3ad52-128">DLL</span><span class="sxs-lookup"><span data-stu-id="3ad52-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3ad52-129"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3ad52-129"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="3ad52-130">IID</span><span class="sxs-lookup"><span data-stu-id="3ad52-130">IID</span></span><br/>                      | <span data-ttu-id="3ad52-131">IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="3ad52-131">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="3ad52-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ad52-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ad52-133">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="3ad52-133">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

<span data-ttu-id="3ad52-134">[**ISCrdEnr：：報名**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="3ad52-134">[**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span></span>
</dt> </dl>

 

 
