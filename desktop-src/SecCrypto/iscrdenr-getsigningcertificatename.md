---
description: 從簽署憑證抓取主體名稱。
ms.assetid: e50b1e12-ec89-4d58-aa57-dc24aa2409ef
title: ISCrdEnr：： getSigningCertificateName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getSigningCertificateName
- SCrdEnr.getSigningCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: 8d9a8a84067e82a18e5066721f3e7f39d075c339
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104386241"
---
# <a name="iscrdenrgetsigningcertificatename-method"></a><span data-ttu-id="dad1a-103">ISCrdEnr：： getSigningCertificateName 方法</span><span class="sxs-lookup"><span data-stu-id="dad1a-103">ISCrdEnr::getSigningCertificateName method</span></span>

<span data-ttu-id="dad1a-104">**GetSigningCertificateName** 方法會從簽署憑證抓取主體名稱。</span><span class="sxs-lookup"><span data-stu-id="dad1a-104">The **getSigningCertificateName** method retrieves the subject name from the signing certificate.</span></span>

<span data-ttu-id="dad1a-105">這個方法也可以用來在對話方塊中顯示憑證。</span><span class="sxs-lookup"><span data-stu-id="dad1a-105">This method can also be used to display the certificate in a dialog box.</span></span> <span data-ttu-id="dad1a-106">這個方法會呼叫 [*CryptoAPI*](../secgloss/c-gly.md) 函數 [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)。</span><span class="sxs-lookup"><span data-stu-id="dad1a-106">This method calls the [*CryptoAPI*](../secgloss/c-gly.md) function [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span></span>

## <a name="syntax"></a><span data-ttu-id="dad1a-107">語法</span><span class="sxs-lookup"><span data-stu-id="dad1a-107">Syntax</span></span>


```C++
HRESULT getSigningCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pbstrSigningCertName
);
```


```VB

SCrdEnr.getSigningCertificateName( _
  ByVal dwFlags, _
  ByRef pbstrSigningCertName _
)
```





## <a name="parameters"></a><span data-ttu-id="dad1a-108">參數</span><span class="sxs-lookup"><span data-stu-id="dad1a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dad1a-109">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dad1a-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dad1a-110">值，決定憑證是否顯示在對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="dad1a-110">A value that determines whether the certificate is displayed in a dialog box.</span></span> <span data-ttu-id="dad1a-111">如果此值為捨棄 \_ ，則不會將 \_ 任何 \_ 顯示 \_ 憑證 (定義為 0x01) ，也不會顯示簽署憑證; 任何其他值都會導致簽署憑證顯示在 [ **憑證** ] 對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="dad1a-111">If this value is SCARD\_ENROLL\_NO\_DISPLAY\_CERT (defined as 0x01), the signing certificate is not displayed; any other values result in the signing certificate being displayed in the **Certificate** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="dad1a-112">*pbstrSigningCertName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="dad1a-112">*pbstrSigningCertName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dad1a-113">傳回簽署憑證名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="dad1a-113">A pointer to a string that returns the name of the signing certificate.</span></span> <span data-ttu-id="dad1a-114">簽署憑證將用來簽署 [*憑證要求*](../secgloss/c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="dad1a-114">The signing certificate will be used to sign the [*certificate request*](../secgloss/c-gly.md).</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dad1a-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="dad1a-115">Return value</span></span>

### <a name="c"></a><span data-ttu-id="dad1a-116">C++</span><span class="sxs-lookup"><span data-stu-id="dad1a-116">C++</span></span>

<span data-ttu-id="dad1a-117">如果方法成功，則方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="dad1a-117">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="dad1a-118">如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="dad1a-118">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="dad1a-119">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="dad1a-119">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="dad1a-120">VB</span><span class="sxs-lookup"><span data-stu-id="dad1a-120">VB</span></span>

<span data-ttu-id="dad1a-121">字串，表示簽署憑證的名稱。</span><span class="sxs-lookup"><span data-stu-id="dad1a-121">A string that represents the name of the signing certificate.</span></span> <span data-ttu-id="dad1a-122">簽署憑證將用來簽署 [*憑證要求*](../secgloss/c-gly.md)。</span><span class="sxs-lookup"><span data-stu-id="dad1a-122">The signing certificate will be used to sign the [*certificate request*](../secgloss/c-gly.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="dad1a-123">備註</span><span class="sxs-lookup"><span data-stu-id="dad1a-123">Remarks</span></span>

<span data-ttu-id="dad1a-124">**GetSigningCertificateName** 方法會傳回您 (之憑證的主體名稱，或是在先前成功呼叫 [**ISCrdEnr：： selectSigningCertificate**](iscrdenr-selectsigningcertificate.md)或 [**ISCrdEnr：： setSigningCertificate**](iscrdenr-setsigningcertificate.md)時選取的另一個系統管理員) 。</span><span class="sxs-lookup"><span data-stu-id="dad1a-124">The **getSigningCertificateName** method returns the subject name of the certificate you (or another administrator) have selected in a previous successful call to [**ISCrdEnr::selectSigningCertificate**](iscrdenr-selectsigningcertificate.md) or [**ISCrdEnr::setSigningCertificate**](iscrdenr-setsigningcertificate.md).</span></span> <span data-ttu-id="dad1a-125">這個方法會呼叫 [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) 函式，根據 \_ \_ \_ \_ **CertGetNameString** 的 *dwType* 參數的 CERT name SIMPLE DISPLAY TYPE 值所述的順序，來取得主體名稱。</span><span class="sxs-lookup"><span data-stu-id="dad1a-125">This method calls the [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) function to retrieve the subject name according to the sequence described for the CERT\_NAME\_SIMPLE\_DISPLAY\_TYPE value of **CertGetNameString**'s *dwType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="dad1a-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="dad1a-126">Requirements</span></span>



| <span data-ttu-id="dad1a-127">需求</span><span class="sxs-lookup"><span data-stu-id="dad1a-127">Requirement</span></span> | <span data-ttu-id="dad1a-128">值</span><span class="sxs-lookup"><span data-stu-id="dad1a-128">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="dad1a-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dad1a-129">Minimum supported client</span></span><br/> | <span data-ttu-id="dad1a-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="dad1a-130">None supported</span></span><br/>                                                               |
| <span data-ttu-id="dad1a-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dad1a-131">Minimum supported server</span></span><br/> | <span data-ttu-id="dad1a-132">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dad1a-132">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="dad1a-133">DLL</span><span class="sxs-lookup"><span data-stu-id="dad1a-133">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dad1a-134"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dad1a-134"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="dad1a-135">IID</span><span class="sxs-lookup"><span data-stu-id="dad1a-135">IID</span></span><br/>                      | <span data-ttu-id="dad1a-136">IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="dad1a-136">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="dad1a-137">另請參閱</span><span class="sxs-lookup"><span data-stu-id="dad1a-137">See also</span></span>

<dl> <dt>

[<span data-ttu-id="dad1a-138">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="dad1a-138">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

[<span data-ttu-id="dad1a-139">**ISCrdEnr::selectSigningCertificate**</span><span class="sxs-lookup"><span data-stu-id="dad1a-139">**ISCrdEnr::selectSigningCertificate**</span></span>](iscrdenr-selectsigningcertificate.md)
</dt> </dl>

 

 
