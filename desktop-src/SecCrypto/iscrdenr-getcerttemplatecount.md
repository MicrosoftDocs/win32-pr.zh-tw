---
description: 抓取憑證範本的數目。
ms.assetid: f56e6e72-1562-4c53-b0da-b4bc69511559
title: ISCrdEnr：： getCertTemplateCount 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getCertTemplateCount
- SCrdEnr.getCertTemplateCount
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 86a78f03929bc6cdcfc7b611944b81c59a1c9fc9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852092"
---
# <a name="iscrdenrgetcerttemplatecount-method"></a><span data-ttu-id="6cd1e-103">ISCrdEnr：： getCertTemplateCount 方法</span><span class="sxs-lookup"><span data-stu-id="6cd1e-103">ISCrdEnr::getCertTemplateCount method</span></span>

<span data-ttu-id="6cd1e-104">**GetCertTemplateCount** 方法會抓取憑證範本的數目。</span><span class="sxs-lookup"><span data-stu-id="6cd1e-104">The **getCertTemplateCount** method retrieves the number of certificate templates.</span></span>

## <a name="syntax"></a><span data-ttu-id="6cd1e-105">語法</span><span class="sxs-lookup"><span data-stu-id="6cd1e-105">Syntax</span></span>


```C++
HRESULT getCertTemplateCount(
  [in]  DWORD     dwFlags,
  [out] LONG *pdwCertTemplateCount
);
```


```VB

SCrdEnr.getCertTemplateCount( _
  ByVal dwFlags, _
  ByRef pdwCertTemplateCount _
)
```





## <a name="parameters"></a><span data-ttu-id="6cd1e-106">參數</span><span class="sxs-lookup"><span data-stu-id="6cd1e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6cd1e-107">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6cd1e-107">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd1e-108">判斷範本是否適用于使用者或電腦憑證的值。</span><span class="sxs-lookup"><span data-stu-id="6cd1e-108">A value that determines whether the template is for user or machine certificates.</span></span> <span data-ttu-id="6cd1e-109">如果此值為捨棄 \_ 註冊 \_ 使用者 \_ \_ 憑證範本 (定義為 1) 則傳回的計數將會是使用者憑證範本。</span><span class="sxs-lookup"><span data-stu-id="6cd1e-109">If this value is SCARD\_ENROLL\_USER\_CERT\_TEMPLATE (defined as 1) then the returned count will be for user certificate templates.</span></span> <span data-ttu-id="6cd1e-110">如果此值為捨棄 \_ 註冊 \_ 電腦 \_ 證書 \_ 範本 (定義為 2) 則傳回的計數將會是電腦憑證範本。</span><span class="sxs-lookup"><span data-stu-id="6cd1e-110">If this value is SCARD\_ENROLL\_MACHINE\_CERT\_TEMPLATE (defined as 2) then the returned count will be for machine certificate templates.</span></span>

</dd> <dt>

<span data-ttu-id="6cd1e-111">*pdwCertTemplateCount* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6cd1e-111">*pdwCertTemplateCount* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6cd1e-112">傳回憑證範本數目的 **LONG** 指標。</span><span class="sxs-lookup"><span data-stu-id="6cd1e-112">A pointer to a **LONG** that returns the number of certificate templates.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6cd1e-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="6cd1e-113">Return value</span></span>

### <a name="c"></a><span data-ttu-id="6cd1e-114">C++</span><span class="sxs-lookup"><span data-stu-id="6cd1e-114">C++</span></span>

<span data-ttu-id="6cd1e-115">如果方法成功，則方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="6cd1e-115">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="6cd1e-116">如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="6cd1e-116">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="6cd1e-117">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="6cd1e-117">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="6cd1e-118">VB</span><span class="sxs-lookup"><span data-stu-id="6cd1e-118">VB</span></span>

<span data-ttu-id="6cd1e-119">代表憑證範本數目的 **Long** 值。</span><span class="sxs-lookup"><span data-stu-id="6cd1e-119">A **Long** value that represents the number of certificate templates.</span></span>

## <a name="requirements"></a><span data-ttu-id="6cd1e-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="6cd1e-120">Requirements</span></span>



| <span data-ttu-id="6cd1e-121">需求</span><span class="sxs-lookup"><span data-stu-id="6cd1e-121">Requirement</span></span> | <span data-ttu-id="6cd1e-122">值</span><span class="sxs-lookup"><span data-stu-id="6cd1e-122">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6cd1e-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6cd1e-123">Minimum supported client</span></span><br/> | <span data-ttu-id="6cd1e-124">都不支援</span><span class="sxs-lookup"><span data-stu-id="6cd1e-124">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6cd1e-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6cd1e-125">Minimum supported server</span></span><br/> | <span data-ttu-id="6cd1e-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6cd1e-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6cd1e-127">DLL</span><span class="sxs-lookup"><span data-stu-id="6cd1e-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6cd1e-128"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6cd1e-128"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="6cd1e-129">IID</span><span class="sxs-lookup"><span data-stu-id="6cd1e-129">IID</span></span><br/>                      | <span data-ttu-id="6cd1e-130">IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="6cd1e-130">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="6cd1e-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6cd1e-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6cd1e-132">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="6cd1e-132">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="6cd1e-133">**ISCrdEnr::enumCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="6cd1e-133">**ISCrdEnr::enumCertTemplateName**</span></span>](iscrdenr-enumcerttemplatename.md)
</dt> </dl>

 

 




