---
description: 顯示 [選取憑證] 對話方塊，允許簽署憑證 (也稱為註冊代理程式憑證) 選取。
ms.assetid: b8198f65-4ffb-4dfa-8286-e62ef483ab16
title: ISCrdEnr：： selectSigningCertificate 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.selectSigningCertificate
- SCrdEnr.selectSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: a4ef3be0ef16797597f57c12e90736ba50109601
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852091"
---
# <a name="iscrdenrselectsigningcertificate-method"></a><span data-ttu-id="ff950-103">ISCrdEnr：： selectSigningCertificate 方法</span><span class="sxs-lookup"><span data-stu-id="ff950-103">ISCrdEnr::selectSigningCertificate method</span></span>

<span data-ttu-id="ff950-104">**SelectSigningCertificate** 方法會顯示 [**選取憑證**] 對話方塊，允許簽署憑證 (也稱為 [*註冊代理程式憑證*]) 選取。</span><span class="sxs-lookup"><span data-stu-id="ff950-104">The **selectSigningCertificate** method displays a **Select Certificate** dialog box, allowing a signing certificate (also known as the *enrollment agent certificate*) to be selected.</span></span>

<span data-ttu-id="ff950-105">代表使用者註冊之前，您必須先選取簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="ff950-105">Before enrolling on behalf of users, you must select a signing certificate.</span></span> <span data-ttu-id="ff950-106">與此簽署憑證相關聯的 [*私密金鑰*](../secgloss/p-gly.md) 會用來簽署 PKCS \# 7 要求。</span><span class="sxs-lookup"><span data-stu-id="ff950-106">The [*private key*](../secgloss/p-gly.md) associated with this signing certificate is used to sign a PKCS \#7 request.</span></span> <span data-ttu-id="ff950-107">PKCS \# 7 接著會包含使用者的 pkcs \# 10 要求 (使用) 的使用者私密金鑰進行簽署。</span><span class="sxs-lookup"><span data-stu-id="ff950-107">The PKCS \#7, in turn, contains the user's PKCS \#10 request (which is signed with the user's private key).</span></span>

## <a name="syntax"></a><span data-ttu-id="ff950-108">語法</span><span class="sxs-lookup"><span data-stu-id="ff950-108">Syntax</span></span>


```C++
HRESULT selectSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.selectSigningCertificate( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="ff950-109">參數</span><span class="sxs-lookup"><span data-stu-id="ff950-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ff950-110">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ff950-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff950-111">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="ff950-111">Reserved for future use.</span></span> <span data-ttu-id="ff950-112">將此值設定為零。</span><span class="sxs-lookup"><span data-stu-id="ff950-112">Set this value to zero.</span></span>

</dd> <dt>

<span data-ttu-id="ff950-113">*bstrCertTemplateName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ff950-113">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ff950-114">字串，表示簽署憑證的憑證範本名稱。</span><span class="sxs-lookup"><span data-stu-id="ff950-114">A string that represents the name of the certificate template for the signing certificate.</span></span> <span data-ttu-id="ff950-115">如果您已取得 EnrollmentAgent 憑證，您可以使用 "EnrollmentAgent" 值。</span><span class="sxs-lookup"><span data-stu-id="ff950-115">You can use the value "EnrollmentAgent" if you have obtained an EnrollmentAgent certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ff950-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="ff950-116">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="ff950-117">VB</span><span class="sxs-lookup"><span data-stu-id="ff950-117">VB</span></span>

<span data-ttu-id="ff950-118">如果方法成功，則方法會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ff950-118">If the method succeeds, the method returns **S\_OK**.</span></span>

<span data-ttu-id="ff950-119">如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="ff950-119">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="ff950-120">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="ff950-120">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="ff950-121">備註</span><span class="sxs-lookup"><span data-stu-id="ff950-121">Remarks</span></span>

<span data-ttu-id="ff950-122">代表使用者註冊之前，您必須先取得簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="ff950-122">Before enrolling on behalf of a user, you must first obtain a signing certificate.</span></span> <span data-ttu-id="ff950-123">您可以使用 [憑證管理員] MMC 嵌入式管理單元來取得簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="ff950-123">You can obtain a signing certificate by using the Certificate Manager MMC snap-in.</span></span> <span data-ttu-id="ff950-124">**SelectSigningCertificate** 方法不會取得簽署憑證，但會顯示先前取得之簽署憑證的對話方塊，可讓您選擇要使用哪一個憑證來簽署代表註冊的要求。</span><span class="sxs-lookup"><span data-stu-id="ff950-124">The **selectSigningCertificate** method does not obtain the signing certificate but displays a dialog box of previously obtained signing certificates, allowing you to choose which certificate will be used to sign the enroll-on-behalf requests.</span></span>

<span data-ttu-id="ff950-125">**SelectSigningCertificate** 的替代方案是 [**ISCrdEnr：： setSigningCertificate**](iscrdenr-setsigningcertificate.md)。</span><span class="sxs-lookup"><span data-stu-id="ff950-125">An alternative to **selectSigningCertificate** is [**ISCrdEnr::setSigningCertificate**](iscrdenr-setsigningcertificate.md).</span></span>

<span data-ttu-id="ff950-126">選取簽署憑證之後，就可以藉由呼叫 [**ISCrdEnr：： getSigningCertificateName**](iscrdenr-getsigningcertificatename.md)來取出其名稱。</span><span class="sxs-lookup"><span data-stu-id="ff950-126">After a signing certificate is selected, its name can be retrieved by calling [**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ff950-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="ff950-127">Requirements</span></span>



| <span data-ttu-id="ff950-128">需求</span><span class="sxs-lookup"><span data-stu-id="ff950-128">Requirement</span></span> | <span data-ttu-id="ff950-129">值</span><span class="sxs-lookup"><span data-stu-id="ff950-129">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ff950-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ff950-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ff950-131">都不支援</span><span class="sxs-lookup"><span data-stu-id="ff950-131">None supported</span></span><br/>                                                               |
| <span data-ttu-id="ff950-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ff950-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ff950-133">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ff950-133">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ff950-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ff950-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ff950-135"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ff950-135"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="ff950-136">IID</span><span class="sxs-lookup"><span data-stu-id="ff950-136">IID</span></span><br/>                      | <span data-ttu-id="ff950-137">IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="ff950-137">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="ff950-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ff950-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ff950-139">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="ff950-139">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="ff950-140">**ISCrdEnr::getSigningCertificateName**</span><span class="sxs-lookup"><span data-stu-id="ff950-140">**ISCrdEnr::getSigningCertificateName**</span></span>](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 
