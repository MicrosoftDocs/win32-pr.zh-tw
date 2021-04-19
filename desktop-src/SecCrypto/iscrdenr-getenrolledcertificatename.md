---
description: 抓取 ISCrdEnr：：註冊的先前成功呼叫所產生的憑證名稱。
ms.assetid: e33b217a-b717-49bd-b0f3-3ba9229a0696
title: ISCrdEnr：： getEnrolledCertificateName 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCrdEnr.getEnrolledCertificateName
- SCrdEnr.getEnrolledCertificateName
api_type:
- COM
api_location:
- Scrdenrl.dll
ms.openlocfilehash: e3c9640e7719d2b5ac0e576384246cda5e1b2bfe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981024"
---
# <a name="iscrdenrgetenrolledcertificatename-method"></a><span data-ttu-id="5d997-103">ISCrdEnr：： getEnrolledCertificateName 方法</span><span class="sxs-lookup"><span data-stu-id="5d997-103">ISCrdEnr::getEnrolledCertificateName method</span></span>

<span data-ttu-id="5d997-104">**GetEnrolledCertificateName** 方法會抓取先前成功呼叫 [**ISCrdEnr：：報名**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))所產生的憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="5d997-104">The **getEnrolledCertificateName** method retrieves the name of the certificate resulting from an earlier successful call to [**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)).</span></span>

<span data-ttu-id="5d997-105">這個方法也可以用來在對話方塊中顯示憑證。</span><span class="sxs-lookup"><span data-stu-id="5d997-105">This method can also be used to display the certificate in a dialog box.</span></span> <span data-ttu-id="5d997-106">這個方法會呼叫 [*CryptoAPI*](../secgloss/c-gly.md) 函數 [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)。</span><span class="sxs-lookup"><span data-stu-id="5d997-106">This method calls the [*CryptoAPI*](../secgloss/c-gly.md) function [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa).</span></span>

## <a name="syntax"></a><span data-ttu-id="5d997-107">語法</span><span class="sxs-lookup"><span data-stu-id="5d997-107">Syntax</span></span>


```C++
HRESULT getEnrolledCertificateName(
  [in]  DWORD     dwFlags,
  [out] BSTR *pBstrCertName
);
```


```VB

SCrdEnr.getEnrolledCertificateName( _
  ByVal dwFlags, _
  ByRef pBstrCertName _
)
```





## <a name="parameters"></a><span data-ttu-id="5d997-108">參數</span><span class="sxs-lookup"><span data-stu-id="5d997-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5d997-109">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5d997-109">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5d997-110">值，決定憑證是否顯示在對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="5d997-110">A value that determines whether the certificate is displayed in a dialog box.</span></span> <span data-ttu-id="5d997-111">如果此值為捨棄 \_ ，則不會將 \_ 任何 \_ 顯示 \_ 憑證 (定義為 0x01) ，也不會顯示已註冊的憑證; 任何其他值都會導致註冊的憑證顯示在 **憑證** 對話方塊中。</span><span class="sxs-lookup"><span data-stu-id="5d997-111">If this value is SCARD\_ENROLL\_NO\_DISPLAY\_CERT (defined as 0x01), the enrolled certificate is not displayed; any other values cause the enrolled certificate to be displayed in the **Certificate** dialog box.</span></span>

</dd> <dt>

<span data-ttu-id="5d997-112">*pBstrCertName* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="5d997-112">*pBstrCertName* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5d997-113">傳回已抓取憑證名稱之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="5d997-113">A pointer to a string that returns the retrieved certificate name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5d997-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="5d997-114">Return value</span></span>

### <a name="c"></a><span data-ttu-id="5d997-115">C++</span><span class="sxs-lookup"><span data-stu-id="5d997-115">C++</span></span>

<span data-ttu-id="5d997-116">如果方法成功，則方法會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="5d997-116">If the method succeeds, the method returns S\_OK.</span></span>

<span data-ttu-id="5d997-117">如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="5d997-117">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="5d997-118">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="5d997-118">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

### <a name="vb"></a><span data-ttu-id="5d997-119">VB</span><span class="sxs-lookup"><span data-stu-id="5d997-119">VB</span></span>

<span data-ttu-id="5d997-120">表示已取出憑證名稱的字串。</span><span class="sxs-lookup"><span data-stu-id="5d997-120">A string that represents the retrieved certificate name.</span></span>

## <a name="remarks"></a><span data-ttu-id="5d997-121">備註</span><span class="sxs-lookup"><span data-stu-id="5d997-121">Remarks</span></span>

<span data-ttu-id="5d997-122">因為這個方法是在現有的憑證上操作，所以您必須先成功呼叫 [**ISCrdEnr：：報名**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)) ，才能呼叫 **getEnrolledCertificateName**。</span><span class="sxs-lookup"><span data-stu-id="5d997-122">Because this method operates on an existing certificate, you must have successfully called [**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85)) before you can call **getEnrolledCertificateName**.</span></span>

<span data-ttu-id="5d997-123">**GetEnrolledCertificateName** 方法會呼叫 [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa)函式，根據 \_ \_ \_ \_ **CertGetNameString** 的 *dwType* 參數的 CERT name SIMPLE DISPLAY TYPE 值所述的順序，來取得憑證名稱。</span><span class="sxs-lookup"><span data-stu-id="5d997-123">The **getEnrolledCertificateName** method calls the [**CertGetNameString**](/windows/desktop/api/Wincrypt/nf-wincrypt-certgetnamestringa) function to retrieve the certificate name according to the sequence described for the CERT\_NAME\_SIMPLE\_DISPLAY\_TYPE value of **CertGetNameString**'s *dwType* parameter.</span></span>

## <a name="requirements"></a><span data-ttu-id="5d997-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="5d997-124">Requirements</span></span>



| <span data-ttu-id="5d997-125">需求</span><span class="sxs-lookup"><span data-stu-id="5d997-125">Requirement</span></span> | <span data-ttu-id="5d997-126">值</span><span class="sxs-lookup"><span data-stu-id="5d997-126">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5d997-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5d997-127">Minimum supported client</span></span><br/> | <span data-ttu-id="5d997-128">都不支援</span><span class="sxs-lookup"><span data-stu-id="5d997-128">None supported</span></span><br/>                                                               |
| <span data-ttu-id="5d997-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5d997-129">Minimum supported server</span></span><br/> | <span data-ttu-id="5d997-130">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5d997-130">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5d997-131">DLL</span><span class="sxs-lookup"><span data-stu-id="5d997-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5d997-132"><dt>Scrdenrl.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5d997-132"><dt>Scrdenrl.dll</dt></span></span> </dl> |
| <span data-ttu-id="5d997-133">IID</span><span class="sxs-lookup"><span data-stu-id="5d997-133">IID</span></span><br/>                      | <span data-ttu-id="5d997-134">IID \_ ISCrdEnr 定義為753988a1-1357-436d-9cf5-f089bdd67d64</span><span class="sxs-lookup"><span data-stu-id="5d997-134">IID\_ISCrdEnr is defined as 753988a1-1357-436d-9cf5-f089bdd67d64</span></span><br/>             |



## <a name="see-also"></a><span data-ttu-id="5d997-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5d997-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5d997-136">**ISCrdEnr**</span><span class="sxs-lookup"><span data-stu-id="5d997-136">**ISCrdEnr**</span></span>](iscrdenr.md)
</dt> <dt>

<span data-ttu-id="5d997-137">[**ISCrdEnr：：報名**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span><span class="sxs-lookup"><span data-stu-id="5d997-137">[**ISCrdEnr::enroll**](/previous-versions/windows/desktop/legacy/aa386564(v=vs.85))</span></span>
</dt> </dl>

 

 
