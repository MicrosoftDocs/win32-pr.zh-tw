---
description: 列舉憑證範本名稱。
ms.assetid: 4741eb0d-b8e0-468c-8a00-9ccacb52a9a7
title: ISCrdEnr：： enumCertTemplateName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.enumCertTemplateName
- SCrdEnr.enumCertTemplateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a0a4850143cac48ef9b9b853f99153d4daeb4366
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978363"
---
# <a name="iscrdenrenumcerttemplatename-method"></a><span data-ttu-id="f5a42-103">ISCrdEnr：： enumCertTemplateName 方法</span><span class="sxs-lookup"><span data-stu-id="f5a42-103">ISCrdEnr::enumCertTemplateName method</span></span>

<span data-ttu-id="f5a42-104">**EnumCertTemplateName** 方法會列舉憑證範本名稱。</span><span class="sxs-lookup"><span data-stu-id="f5a42-104">The **enumCertTemplateName** method enumerates the certificate template names.</span></span>

## <a name="syntax"></a><span data-ttu-id="f5a42-105">語法</span><span class="sxs-lookup"><span data-stu-id="f5a42-105">Syntax</span></span>


```C++
HRESULT enumCertTemplateName(
  [in]  DWORD     dwIndex,
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrCertTemplateName
);
```


```VB

SCrdEnr.enumCertTemplateName( _
  ByVal dwIndex, _
  ByVal dwFlags, _
  ByRef pbstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="f5a42-106">參數</span><span class="sxs-lookup"><span data-stu-id="f5a42-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f5a42-107">*dwIndex* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f5a42-107">*dwIndex* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5a42-108">列舉序列的以零為基底的索引。</span><span class="sxs-lookup"><span data-stu-id="f5a42-108">The zero-based index for the enumeration sequence.</span></span>

</dd> <dt>

<span data-ttu-id="f5a42-109">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f5a42-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f5a42-110">值，這個值會決定列舉的憑證範本是否適用于使用者或電腦憑證。</span><span class="sxs-lookup"><span data-stu-id="f5a42-110">A value that determines whether the enumerated certificate template applies to user or machine certificates.</span></span> <span data-ttu-id="f5a42-111">如果此值為捨棄 \_ 註冊 \_ 使用者 \_ \_ 憑證範本 (定義為 1) ，則列舉會套用至使用者憑證範本。</span><span class="sxs-lookup"><span data-stu-id="f5a42-111">If this value is SCARD\_ENROLL\_USER\_CERT\_TEMPLATE (defined as 1), the enumeration applies to user certificate templates.</span></span> <span data-ttu-id="f5a42-112">如果此值為捨棄 \_ 註冊 \_ 電腦 \_ 證書 \_ 範本 (定義為 2) ，則列舉會套用至電腦憑證範本。</span><span class="sxs-lookup"><span data-stu-id="f5a42-112">If this value is SCARD\_ENROLL\_MACHINE\_CERT\_TEMPLATE (defined as 2), the enumeration applies to machine certificate templates.</span></span>

</dd> <dt>

<span data-ttu-id="f5a42-113">*pbstrCertTemplateName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f5a42-113">*pbstrCertTemplateName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f5a42-114">傳回列舉憑證範本名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="f5a42-114">A pointer to a string that returns the name of the enumerated certificate template.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f5a42-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="f5a42-115">Return value</span></span>

### <a name="c"></a><span data-ttu-id="f5a42-116">C++</span><span class="sxs-lookup"><span data-stu-id="f5a42-116">C++</span></span>

<span data-ttu-id="f5a42-117">如果方法成功，則方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="f5a42-117">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="f5a42-118">如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="f5a42-118">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="f5a42-119">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="f5a42-119">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="f5a42-120">VB</span><span class="sxs-lookup"><span data-stu-id="f5a42-120">VB</span></span>

<span data-ttu-id="f5a42-121">字串，包含列舉憑證範本的名稱。</span><span class="sxs-lookup"><span data-stu-id="f5a42-121">A string that contains the name of the enumerated certificate template.</span></span>

## <a name="requirements"></a><span data-ttu-id="f5a42-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="f5a42-122">Requirements</span></span>



| <span data-ttu-id="f5a42-123">需求</span><span class="sxs-lookup"><span data-stu-id="f5a42-123">Requirement</span></span> | <span data-ttu-id="f5a42-124">值</span><span class="sxs-lookup"><span data-stu-id="f5a42-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="f5a42-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f5a42-125">Minimum supported client</span></span><br/> | <span data-ttu-id="f5a42-126">都不支援</span><span class="sxs-lookup"><span data-stu-id="f5a42-126">None supported</span></span><br/>                                                               |
| <span data-ttu-id="f5a42-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f5a42-127">Minimum supported server</span></span><br/> | <span data-ttu-id="f5a42-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f5a42-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="f5a42-129">DLL</span><span class="sxs-lookup"><span data-stu-id="f5a42-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f5a42-130"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f5a42-130"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="f5a42-131">IID</span><span class="sxs-lookup"><span data-stu-id="f5a42-131">IID</span></span><br/>                      | <span data-ttu-id="f5a42-132">IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="f5a42-132">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="f5a42-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f5a42-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f5a42-134">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="f5a42-134">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="f5a42-135">**ISCrdEnr::getCertTemplateCount**</span><span class="sxs-lookup"><span data-stu-id="f5a42-135">**ISCrdEnr::getCertTemplateCount**</span></span>](iscrdenr-getcerttemplatecount.md)
</dt> <dt>

[<span data-ttu-id="f5a42-136">**ISCrdEnr::getCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="f5a42-136">**ISCrdEnr::getCertTemplateName**</span></span>](iscrdenr-getcerttemplatename.md)
</dt> <dt>

[<span data-ttu-id="f5a42-137">**ISCrdEnr::setCertTemplateName**</span><span class="sxs-lookup"><span data-stu-id="f5a42-137">**ISCrdEnr::setCertTemplateName**</span></span>](iscrdenr-setcerttemplatename.md)
</dt> </dl>

 

 




