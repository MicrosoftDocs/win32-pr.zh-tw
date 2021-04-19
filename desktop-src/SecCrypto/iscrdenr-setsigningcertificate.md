---
description: 指定簽署憑證 (也稱為註冊代理程式憑證) 。
ms.assetid: db2437a9-46f6-48c3-9630-82ec556df645
title: ISCrdEnr：： setSigningCertificate 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.setSigningCertificate
- SCrdEnr.setSigningCertificate
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: dd00ba19872cb0ba2b21981c79e8f7be03aa4937
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997262"
---
# <a name="iscrdenrsetsigningcertificate-method"></a><span data-ttu-id="6eeff-103">ISCrdEnr：： setSigningCertificate 方法</span><span class="sxs-lookup"><span data-stu-id="6eeff-103">ISCrdEnr::setSigningCertificate method</span></span>

<span data-ttu-id="6eeff-104">**SetSigningCertificate** 方法會指定簽署憑證 (也稱為 *註冊代理程式憑證*) 。</span><span class="sxs-lookup"><span data-stu-id="6eeff-104">The **setSigningCertificate** method specifies a signing certificate (also known as the *enrollment agent certificate*).</span></span>

<span data-ttu-id="6eeff-105">代表使用者註冊之前，您必須選取或設定簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="6eeff-105">Before enrolling on behalf of users, you must select or set a signing certificate.</span></span> <span data-ttu-id="6eeff-106">與此簽署憑證相關聯的 [*私密金鑰*](../secgloss/p-gly.md) 會用來簽署 PKCS \# 7 要求。</span><span class="sxs-lookup"><span data-stu-id="6eeff-106">The [*private key*](../secgloss/p-gly.md) associated with this signing certificate is used to sign a PKCS \#7 request.</span></span> <span data-ttu-id="6eeff-107">PKCS \# 7 接著會包含使用者的 pkcs \# 10 要求 (使用) 的使用者私密金鑰進行簽署。</span><span class="sxs-lookup"><span data-stu-id="6eeff-107">The PKCS \#7, in turn, contains the user's PKCS \#10 request (which is signed with the user's private key).</span></span>

## <a name="syntax"></a><span data-ttu-id="6eeff-108">語法</span><span class="sxs-lookup"><span data-stu-id="6eeff-108">Syntax</span></span>


```C++
HRESULT setSigningCertificate(
  [in] DWORD dwFlags,
  [in] BSTR bstrCertTemplateName
);
```


```VB

SCrdEnr.setSigningCertificate( _
  ByVal dwFlags, _
  ByVal bstrCertTemplateName _
)
```





## <a name="parameters"></a><span data-ttu-id="6eeff-109">參數</span><span class="sxs-lookup"><span data-stu-id="6eeff-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6eeff-110">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6eeff-110">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eeff-111">保留供未來使用。</span><span class="sxs-lookup"><span data-stu-id="6eeff-111">Reserved for future use.</span></span> <span data-ttu-id="6eeff-112">將此值設定為零。</span><span class="sxs-lookup"><span data-stu-id="6eeff-112">Set this value to zero.</span></span>

</dd> <dt>

<span data-ttu-id="6eeff-113">*bstrCertTemplateName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6eeff-113">*bstrCertTemplateName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6eeff-114">簽署憑證的憑證範本名稱。</span><span class="sxs-lookup"><span data-stu-id="6eeff-114">Name of the certificate template for the signing certificate.</span></span> <span data-ttu-id="6eeff-115">如果您已取得 EnrollmentAgent 憑證，您可以使用 "EnrollmentAgent" 值。</span><span class="sxs-lookup"><span data-stu-id="6eeff-115">You can use the value "EnrollmentAgent" if you have obtained an EnrollmentAgent certificate.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6eeff-116">傳回值</span><span class="sxs-lookup"><span data-stu-id="6eeff-116">Return value</span></span>

### <a name="vb"></a><span data-ttu-id="6eeff-117">VB</span><span class="sxs-lookup"><span data-stu-id="6eeff-117">VB</span></span>

<span data-ttu-id="6eeff-118">如果方法成功，則方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="6eeff-118">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="6eeff-119">如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="6eeff-119">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="6eeff-120">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="6eeff-120">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6eeff-121">備註</span><span class="sxs-lookup"><span data-stu-id="6eeff-121">Remarks</span></span>

<span data-ttu-id="6eeff-122">代表使用者註冊之前，您必須先取得簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="6eeff-122">Before enrolling on behalf of a user, you must first obtain a signing certificate.</span></span> <span data-ttu-id="6eeff-123">您可以使用 [憑證管理員] MMC 嵌入式管理單元來取得簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="6eeff-123">You can obtain a signing certificate by using the Certificate Manager MMC snap-in.</span></span> <span data-ttu-id="6eeff-124">**SetSigningCertificate** 方法不會取得簽署憑證，但會通知先前取得要使用之簽署憑證的智慧卡註冊控制項。</span><span class="sxs-lookup"><span data-stu-id="6eeff-124">The **setSigningCertificate** method does not obtain the signing certificate but informs the Smart Card Enrollment Control which previously obtained signing certificate to use.</span></span> <span data-ttu-id="6eeff-125">**SetSigningCertificate** 方法會在呼叫端的 "My" 存放區中搜尋與 *bstrCertTemplateName* 所指定憑證範本對應的最新簽署憑證。</span><span class="sxs-lookup"><span data-stu-id="6eeff-125">The **setSigningCertificate** method searches the caller's "My" store for the most recent signing certificate corresponding to the certificate template specified by *bstrCertTemplateName*.</span></span>

<span data-ttu-id="6eeff-126">**SetSigningCertificate** 的替代方案是 **ISCrdEnr：： setSigningCertificate**。</span><span class="sxs-lookup"><span data-stu-id="6eeff-126">An alternative to **setSigningCertificate** is **ISCrdEnr::setSigningCertificate**.</span></span>

<span data-ttu-id="6eeff-127">設定簽署憑證之後，您可以藉由呼叫 [**ISCrdEnr：： getSigningCertificateName**](iscrdenr-getsigningcertificatename.md)來取出其名稱。</span><span class="sxs-lookup"><span data-stu-id="6eeff-127">After a signing certificate is set, its name can be retrieved by calling [**ISCrdEnr::getSigningCertificateName**](iscrdenr-getsigningcertificatename.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="6eeff-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="6eeff-128">Requirements</span></span>



| <span data-ttu-id="6eeff-129">需求</span><span class="sxs-lookup"><span data-stu-id="6eeff-129">Requirement</span></span> | <span data-ttu-id="6eeff-130">值</span><span class="sxs-lookup"><span data-stu-id="6eeff-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6eeff-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6eeff-131">Minimum supported client</span></span><br/> | <span data-ttu-id="6eeff-132">都不支援</span><span class="sxs-lookup"><span data-stu-id="6eeff-132">None supported</span></span><br/>                                                               |
| <span data-ttu-id="6eeff-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6eeff-133">Minimum supported server</span></span><br/> | <span data-ttu-id="6eeff-134">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6eeff-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6eeff-135">DLL</span><span class="sxs-lookup"><span data-stu-id="6eeff-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6eeff-136"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6eeff-136"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="6eeff-137">IID</span><span class="sxs-lookup"><span data-stu-id="6eeff-137">IID</span></span><br/>                      | <span data-ttu-id="6eeff-138">IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="6eeff-138">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="6eeff-139">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6eeff-139">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6eeff-140">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="6eeff-140">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="6eeff-141">**ISCrdEnr::getSigningCertificateName**</span><span class="sxs-lookup"><span data-stu-id="6eeff-141">**ISCrdEnr::getSigningCertificateName**</span></span>](iscrdenr-getsigningcertificatename.md)
</dt> </dl>

 

 
