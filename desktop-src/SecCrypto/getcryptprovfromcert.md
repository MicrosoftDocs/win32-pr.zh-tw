---
description: 取得密碼編譯服務提供者 (CSP) 的控制碼，以及憑證內容的金鑰規格。
ms.assetid: ff72231f-e10f-49d2-b0e0-0008923803cc
title: GetCryptProvFromCert 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GetCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: bcd396c45333dee42bae4cb8bdfdd52792f1bdd6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104321027"
---
# <a name="getcryptprovfromcert-function"></a><span data-ttu-id="c5ba3-103">GetCryptProvFromCert 函式</span><span class="sxs-lookup"><span data-stu-id="c5ba3-103">GetCryptProvFromCert function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c5ba3-104">此 API 即將淘汰。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-104">This API is deprecated.</span></span> <span data-ttu-id="c5ba3-105">Microsoft 可能會在未來的版本中移除此 API。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="c5ba3-106">**GetCryptProvFromCert** 函式會取得 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 的控制碼，以及 [*憑證*](../secgloss/c-gly.md)內容的金鑰規格。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-106">The **GetCryptProvFromCert** function gets a handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and a key specification for a [*certificate*](../secgloss/c-gly.md) context.</span></span> <span data-ttu-id="c5ba3-107">您可以使用此函式來取得憑證簽發者 [*私密金鑰*](../secgloss/p-gly.md) 的存取權。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-107">Use this function to get access to the [*private key*](../secgloss/p-gly.md) of the certificate issuer.</span></span>

> [!Note]  
> <span data-ttu-id="c5ba3-108">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="c5ba3-109">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-109">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="c5ba3-110">語法</span><span class="sxs-lookup"><span data-stu-id="c5ba3-110">Syntax</span></span>


```C++
BOOL WINAPI GetCryptProvFromCert(
  _In_      HWND           hwnd,
  _In_      PCCERT_CONTEXT pCert,
  _Out_     HCRYPTPROV     *phCryptProv,
  _Out_     DWORD          *pdwKeySpec,
  _In_      BOOL           *pfDidCryptAcquire,
  _Out_opt_ LPWSTR         *ppwszTmpContainer,
  _Out_opt_ LPWSTR         *ppwszProviderName,
  _Out_     DWORD          *pdwProviderType
);
```



## <a name="parameters"></a><span data-ttu-id="c5ba3-111">參數</span><span class="sxs-lookup"><span data-stu-id="c5ba3-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c5ba3-112">*hwnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5ba3-112">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ba3-113">要做為顯示之任何對話方塊擁有者使用的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-113">The handle of the window to use as the owner of any dialog boxes that are displayed.</span></span> <span data-ttu-id="c5ba3-114">目前未使用這個成員，所以會忽略。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-114">This member is not currently used and is ignored.</span></span> <span data-ttu-id="c5ba3-115">您可以安全地針對此參數傳遞 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-115">It is safe to pass **NULL** for this parameter.</span></span>

</dd> <dt>

<span data-ttu-id="c5ba3-116">*pCert* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5ba3-116">*pCert* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ba3-117">憑證的憑證 [**\_ 內容**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) 結構指標。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-117">A pointer to a [**CERT\_CONTEXT**](/windows/desktop/api/Wincrypt/ns-wincrypt-cert_context) structure for the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="c5ba3-118">*phCryptProv* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c5ba3-118">*phCryptProv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ba3-119">[**HCRYPTPROV**](hcryptprov.md)結構的指標，該結構為 CSP 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-119">A pointer to an [**HCRYPTPROV**](hcryptprov.md) structure that is a handle to the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="c5ba3-120">*pdwKeySpec* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c5ba3-120">*pdwKeySpec* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ba3-121">要取出之私密金鑰的規格。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-121">The specification of the private key to retrieve.</span></span> <span data-ttu-id="c5ba3-122">可能的值包括 **在 \_ KEYEXCHANGE** **或簽 \_** 章。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-122">Possible values include **AT\_KEYEXCHANGE** or **AT\_SIGNATURE**.</span></span>

</dd> <dt>

<span data-ttu-id="c5ba3-123">*pfDidCryptAcquire* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c5ba3-123">*pfDidCryptAcquire* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ba3-124">值，這個值會指定函數是否根據憑證取得提供者控制碼。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-124">A value that specifies whether the function acquired the provider handle based on the certificate.</span></span>

</dd> <dt>

<span data-ttu-id="c5ba3-125">*ppwszTmpContainer* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="c5ba3-125">*ppwszTmpContainer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ba3-126">暫存金鑰容器名稱之以 null 結束的字串指標的位址。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-126">The address of a pointer to a null-terminated string for the temporary key container name.</span></span> <span data-ttu-id="c5ba3-127">**GetCryptProvFromCert** 函式會提供並初始化暫存容器。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-127">The **GetCryptProvFromCert** function provides and initializes the temporary container.</span></span> <span data-ttu-id="c5ba3-128">呼叫 **GetCryptProvFromCert** 時，位址應該指向 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-128">When calling **GetCryptProvFromCert**, the address should point to a **NULL** value.</span></span>

</dd> <dt>

<span data-ttu-id="c5ba3-129">*ppwszProviderName* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="c5ba3-129">*ppwszProviderName* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ba3-130">提供者名稱之以 null 結束的字串指標的位址。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-130">The address of a pointer to a null-terminated string for the provider name.</span></span> <span data-ttu-id="c5ba3-131">**GetCryptProvFromCert** 函數會傳回提供者名稱。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-131">The **GetCryptProvFromCert** function returns the provider name.</span></span> <span data-ttu-id="c5ba3-132">呼叫 **GetCryptProvFromCert** 時，位址應該指向 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-132">When calling **GetCryptProvFromCert**, the address should point to a **NULL** value.</span></span>

</dd> <dt>

<span data-ttu-id="c5ba3-133">*pdwProviderType* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="c5ba3-133">*pdwProviderType* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="c5ba3-134">指定 CSP 類型。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-134">Specifies the CSP type.</span></span> <span data-ttu-id="c5ba3-135">這可以是零或其中一個 [密碼編譯提供者類型](cryptographic-provider-types.md)。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-135">This can be zero or one of the [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span> <span data-ttu-id="c5ba3-136">如果這個成員是零，金鑰容器就是其中一個 CNG 金鑰儲存提供者。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-136">If this member is zero, the key container is one of the CNG key storage providers.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c5ba3-137">傳回值</span><span class="sxs-lookup"><span data-stu-id="c5ba3-137">Return value</span></span>

<span data-ttu-id="c5ba3-138">成功時，此函數會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-138">Upon success, this function returns **TRUE**.</span></span> <span data-ttu-id="c5ba3-139">如果失敗， **GetCryptProvFromCert** 函數會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-139">The **GetCryptProvFromCert** function returns **FALSE** if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="c5ba3-140">備註</span><span class="sxs-lookup"><span data-stu-id="c5ba3-140">Remarks</span></span>

<span data-ttu-id="c5ba3-141">當您使用 **-是** 命令列選項叫用時， [MakeCert](makecert.md)工具會呼叫 **GetCryptProvFromCert** 。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-141">The [MakeCert](makecert.md) tool calls **GetCryptProvFromCert** when you invoke it by using the **-is** command line option.</span></span>

<span data-ttu-id="c5ba3-142">如果 *pfDidCryptAcquire* 參數設定為 **TRUE**，則函式會將 *phCryptProv*、 *pdwKeySpec* 和 *pdwProviderType* 參數設定為提供者的值。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-142">If the *pfDidCryptAcquire* parameter is set to **TRUE**, the function sets *phCryptProv*, *pdwKeySpec*, and *pdwProviderType* parameters to the provider values.</span></span>

<span data-ttu-id="c5ba3-143">當您使用完 CSP 之後，請呼叫 [**FreeCryptProvFromCert**](freecryptprovfromcert.md) 函式將它釋放。</span><span class="sxs-lookup"><span data-stu-id="c5ba3-143">When you have finished using the CSP, free it by calling the [**FreeCryptProvFromCert**](freecryptprovfromcert.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="c5ba3-144">規格需求</span><span class="sxs-lookup"><span data-stu-id="c5ba3-144">Requirements</span></span>



| <span data-ttu-id="c5ba3-145">需求</span><span class="sxs-lookup"><span data-stu-id="c5ba3-145">Requirement</span></span> | <span data-ttu-id="c5ba3-146">值</span><span class="sxs-lookup"><span data-stu-id="c5ba3-146">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="c5ba3-147">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c5ba3-147">Minimum supported client</span></span><br/> | <span data-ttu-id="c5ba3-148">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5ba3-148">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="c5ba3-149">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c5ba3-149">Minimum supported server</span></span><br/> | <span data-ttu-id="c5ba3-150">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c5ba3-150">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="c5ba3-151">DLL</span><span class="sxs-lookup"><span data-stu-id="c5ba3-151">DLL</span></span><br/>                      | <dl> <span data-ttu-id="c5ba3-152"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="c5ba3-152"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
