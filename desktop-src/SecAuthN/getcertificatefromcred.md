---
description: 從使用者認證取得憑證。
ms.assetid: 3C79D049-89DC-4AF5-8C0A-5B7EBBBD69D3
title: 'GetCertificateFromCred 函式 (Lsaidprov) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCertificateFromCred
api_type:
- HeaderDef
api_location:
- Lsaidprov.h
ms.openlocfilehash: 1120e7859080657e2a04202e01a01464694a3450
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974392"
---
# <a name="getcertificatefromcred-function"></a><span data-ttu-id="23a0d-103">GetCertificateFromCred 函式</span><span class="sxs-lookup"><span data-stu-id="23a0d-103">GetCertificateFromCred function</span></span>

<span data-ttu-id="23a0d-104">從使用者認證取得憑證。</span><span class="sxs-lookup"><span data-stu-id="23a0d-104">Gets the certificate from the user credential.</span></span>

## <a name="syntax"></a><span data-ttu-id="23a0d-105">語法</span><span class="sxs-lookup"><span data-stu-id="23a0d-105">Syntax</span></span>


```C++
NTSTATUS GetCertificateFromCred(
  _In_  PVOID  ProviderHandle,
  _In_  HANDLE ClientToken,
  _In_  PVOID  SuppliedCred,
  _In_  ULONG  SuppliedCredSize,
  _Out_ PVOID  *CertContext
);
```



## <a name="parameters"></a><span data-ttu-id="23a0d-106">參數</span><span class="sxs-lookup"><span data-stu-id="23a0d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="23a0d-107">*ProviderHandle* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23a0d-107">*ProviderHandle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23a0d-108">身分識別提供者控制碼。</span><span class="sxs-lookup"><span data-stu-id="23a0d-108">Identity provider handle.</span></span>

</dd> <dt>

<span data-ttu-id="23a0d-109">*ClientToken* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23a0d-109">*ClientToken* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23a0d-110">正在抓取憑證之呼叫者的 Token。</span><span class="sxs-lookup"><span data-stu-id="23a0d-110">Token of the caller who is retrieving the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="23a0d-111">*SuppliedCred* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23a0d-111">*SuppliedCred* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23a0d-112">SECPKG 所提供之 [**\_ \_ 認證**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) 結構的指標，其中包含要求其憑證的線上識別碼認證。</span><span class="sxs-lookup"><span data-stu-id="23a0d-112">A pointer to a [**SECPKG\_SUPPLIED\_CREDENTIAL**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) structure that contains the credential of an online ID whose certificate is requested.</span></span> <span data-ttu-id="23a0d-113">身分識別提供者必須驗證輸入資料，就像是來自不受信任的來源一樣。</span><span class="sxs-lookup"><span data-stu-id="23a0d-113">The identity provider must validate the input data as if it is coming from an untrusted source.</span></span>

</dd> <dt>

<span data-ttu-id="23a0d-114">*SuppliedCredSize* \[在\]</span><span class="sxs-lookup"><span data-stu-id="23a0d-114">*SuppliedCredSize* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="23a0d-115">*SuppliedCred* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="23a0d-115">The size, in bytes, of the *SuppliedCred* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="23a0d-116">*CertCoNtext* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="23a0d-116">*CertContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="23a0d-117">如果函式成功，這個參數會是所傳回 CCERT \_ 內容指標的指標。</span><span class="sxs-lookup"><span data-stu-id="23a0d-117">If the function succeeds, this parameter is a pointer to the returned CCERT\_CONTEXT pointer.</span></span> <span data-ttu-id="23a0d-118">當您完成使用憑證內容之後，請呼叫 [**CertFreeCertificateCoNtext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) 函式來釋放它。</span><span class="sxs-lookup"><span data-stu-id="23a0d-118">When you have finished using the certificate context, release it by calling the [**CertFreeCertificateContext**](/windows/desktop/api/wincrypt/nf-wincrypt-certfreecertificatecontext) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="23a0d-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="23a0d-119">Return value</span></span>

<span data-ttu-id="23a0d-120">如果函式成功，函數會傳回狀態 \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="23a0d-120">If the function succeeds, the function returns STATUS\_SUCCESS.</span></span>

<span data-ttu-id="23a0d-121">如果函式失敗，函式可能會傳回下列其中一個 NTSTATUS 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="23a0d-121">If the function fails, the function may return one of the following NTSTATUS error codes.</span></span>



| <span data-ttu-id="23a0d-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="23a0d-122">Return value</span></span>                                                                                            | <span data-ttu-id="23a0d-123">描述</span><span class="sxs-lookup"><span data-stu-id="23a0d-123">Description</span></span>                                                                                                                                                                            |
|---------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="23a0d-124"><dt>\_不 \_ 支援的狀態</dt></span><span class="sxs-lookup"><span data-stu-id="23a0d-124"><dt>STATUS\_NOT\_SUPPORTED</dt></span></span> </dl>       | <span data-ttu-id="23a0d-125">身分識別提供者無法辨識所提供認證的認證類型。</span><span class="sxs-lookup"><span data-stu-id="23a0d-125">The identity provider does not recognize the credential type of the supplied credential.</span></span> <span data-ttu-id="23a0d-126">LSA 將會嘗試下一個身分識別提供者。</span><span class="sxs-lookup"><span data-stu-id="23a0d-126">LSA will try the next identity provider.</span></span><br/>                                           |
| <dl> <span data-ttu-id="23a0d-127"><dt>狀態 \_ 登入 \_ 失敗</dt></span><span class="sxs-lookup"><span data-stu-id="23a0d-127"><dt>STATUS\_LOGON\_FAILURE</dt></span></span> </dl>       | <span data-ttu-id="23a0d-128">認證不正確。</span><span class="sxs-lookup"><span data-stu-id="23a0d-128">The credential is incorrect.</span></span><br/>                                                                                                                                                |
| <dl> <span data-ttu-id="23a0d-129"><dt>狀態 \_ 不正確 \_ 參數</dt></span><span class="sxs-lookup"><span data-stu-id="23a0d-129"><dt>STATUS\_INVALID\_PARAMETER</dt></span></span> </dl>   | <span data-ttu-id="23a0d-130">參數無效。</span><span class="sxs-lookup"><span data-stu-id="23a0d-130">A parameter is not valid.</span></span> <span data-ttu-id="23a0d-131">認證的格式不正確，而不是定義的 [**SECPKG 提供的 \_ \_ 認證**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) 結構。</span><span class="sxs-lookup"><span data-stu-id="23a0d-131">The credential may be in an incorrect format and not in the defined [**SECPKG\_SUPPLIED\_CREDENTIAL**](/windows/desktop/api/Ntsecpkg/ns-ntsecpkg-secpkg_supplied_credential) structure.</span></span><br/> |
| <dl> <span data-ttu-id="23a0d-132"><dt>無法連線到狀態 \_ 網路 \_</dt></span><span class="sxs-lookup"><span data-stu-id="23a0d-132"><dt>STATUS\_NETWORK\_UNREACHABLE</dt></span></span> </dl> | <span data-ttu-id="23a0d-133">身分識別提供者無法連絡雲端以取得憑證。</span><span class="sxs-lookup"><span data-stu-id="23a0d-133">The identity provider cannot contact the cloud to obtain the certificate.</span></span><br/>                                                                                                   |
| <dl> <span data-ttu-id="23a0d-134"><dt>狀態 \_ 密碼已 \_ 過期</dt></span><span class="sxs-lookup"><span data-stu-id="23a0d-134"><dt>STATUS\_PASSWORD\_EXPIRED</dt></span></span> </dl>    | <span data-ttu-id="23a0d-135">帳戶密碼已過期。</span><span class="sxs-lookup"><span data-stu-id="23a0d-135">The account password has expired.</span></span><br/>                                                                                                                                           |
| <dl> <span data-ttu-id="23a0d-136"><dt>狀態 \_ 帳戶已 \_ 鎖定 \_</dt></span><span class="sxs-lookup"><span data-stu-id="23a0d-136"><dt>STATUS\_ACCOUNT\_LOCKED\_OUT</dt></span></span> </dl> | <span data-ttu-id="23a0d-137">帳戶已被鎖定。</span><span class="sxs-lookup"><span data-stu-id="23a0d-137">The account has been locked out.</span></span> <br/>                                                                                                                                           |
| <dl> <span data-ttu-id="23a0d-138"><dt>其他</dt></span><span class="sxs-lookup"><span data-stu-id="23a0d-138"><dt>Others</dt></span></span> </dl>                       | <span data-ttu-id="23a0d-139">其他提供者特定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="23a0d-139">Other provider-specific error codes.</span></span> <br/>                                                                                                                                       |



 

## <a name="remarks"></a><span data-ttu-id="23a0d-140">備註</span><span class="sxs-lookup"><span data-stu-id="23a0d-140">Remarks</span></span>

<span data-ttu-id="23a0d-141">從雲端提取憑證之前，身分識別提供者應該在使用者的「我的」憑證存放區中檢查此使用者是否有有效的憑證。</span><span class="sxs-lookup"><span data-stu-id="23a0d-141">Before fetching the certificate from the cloud, the identity provider should check that there is a valid certificate for this user in the user's "MY" certificate store.</span></span> <span data-ttu-id="23a0d-142">如果有有效的憑證，則提供者應該傳回此憑證，以避免不必要的網路流量。</span><span class="sxs-lookup"><span data-stu-id="23a0d-142">If a valid certificate exists, the provider should return this certificate to avoid unnecessary network traffic.</span></span>

<span data-ttu-id="23a0d-143">身分識別提供者也可以在本機快取憑證，只要該憑證受到目前使用者的保護。</span><span class="sxs-lookup"><span data-stu-id="23a0d-143">The identity provider can also cache the certificate locally as long as it is protected from the current user.</span></span>

## <a name="requirements"></a><span data-ttu-id="23a0d-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="23a0d-144">Requirements</span></span>



| <span data-ttu-id="23a0d-145">需求</span><span class="sxs-lookup"><span data-stu-id="23a0d-145">Requirement</span></span> | <span data-ttu-id="23a0d-146">值</span><span class="sxs-lookup"><span data-stu-id="23a0d-146">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="23a0d-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="23a0d-147">Minimum supported client</span></span><br/> | <span data-ttu-id="23a0d-148">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23a0d-148">Windows 8 \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="23a0d-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="23a0d-149">Minimum supported server</span></span><br/> | <span data-ttu-id="23a0d-150">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="23a0d-150">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="23a0d-151">標頭</span><span class="sxs-lookup"><span data-stu-id="23a0d-151">Header</span></span><br/>                   | <dl> <span data-ttu-id="23a0d-152"><dt>Lsaidprov。h</dt></span><span class="sxs-lookup"><span data-stu-id="23a0d-152"><dt>Lsaidprov.h</dt></span></span> </dl> |



 

