---
description: 根據私密金鑰檔案或金鑰容器名稱，取得密碼編譯服務提供者 (CSP) 的控制碼。
ms.assetid: 82cdaa6f-e747-4c9d-8d2d-5fa206891eed
title: PvkGetCryptProv 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkGetCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 026b31d021dc6ff2569ad9ce8f17d2e7f0d17b29
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103852884"
---
# <a name="pvkgetcryptprov-function"></a><span data-ttu-id="6ab95-103">PvkGetCryptProv 函式</span><span class="sxs-lookup"><span data-stu-id="6ab95-103">PvkGetCryptProv function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="6ab95-104">此 API 即將淘汰。</span><span class="sxs-lookup"><span data-stu-id="6ab95-104">This API is deprecated.</span></span> <span data-ttu-id="6ab95-105">Microsoft 可能會在未來的版本中移除此 API。</span><span class="sxs-lookup"><span data-stu-id="6ab95-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="6ab95-106">**PvkGetCryptProv** 函式會根據 [*私密金鑰*](../secgloss/p-gly.md)檔案或金鑰容器名稱，取得 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="6ab95-106">The **PvkGetCryptProv** function gets a handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) based on either a [*private key*](../secgloss/p-gly.md) file or a key container name.</span></span>

> [!Note]  
> <span data-ttu-id="6ab95-107">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="6ab95-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="6ab95-108">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。</span><span class="sxs-lookup"><span data-stu-id="6ab95-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="6ab95-109">語法</span><span class="sxs-lookup"><span data-stu-id="6ab95-109">Syntax</span></span>


```C++
HRESULT WINAPI PvkGetCryptProv(
  _In_      HWND       hwnd,
  _In_      LPCWSTR    pwszCaption,
  _In_      LPCWSTR    pwszCapiProvider,
  _In_      DWORD      dwProviderType,
  _In_      LPCWSTR    pwszPvkFile,
  _In_      LPCWSTR    pwszKeyContainerName,
  _Out_     DWORD      *pdwKeySpec,
  _Out_opt_ LPWSTR     *ppwszTmpContainer,
  _Out_     HCRYPTPROV *phCryptProv
);
```



## <a name="parameters"></a><span data-ttu-id="6ab95-110">參數</span><span class="sxs-lookup"><span data-stu-id="6ab95-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6ab95-111">*hwnd* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ab95-111">*hwnd* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab95-112">如果需要密碼來解密私密金鑰檔案，此參數是密碼對話方塊父系的控制碼;否則，它會是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="6ab95-112">If a password is required to decrypt the private key file, this parameter is a handle to the parent of the password dialog box; otherwise, it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="6ab95-113">*pwszCaption* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ab95-113">*pwszCaption* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab95-114">對話方塊標題之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="6ab95-114">A pointer to a null-terminated string for the dialog box caption.</span></span>

</dd> <dt>

<span data-ttu-id="6ab95-115">*pwszCapiProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ab95-115">*pwszCapiProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab95-116">CSP 名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="6ab95-116">A pointer to a null-terminated string for the CSP name.</span></span>

</dd> <dt>

<span data-ttu-id="6ab95-117">*dwProviderType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ab95-117">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab95-118">代表密碼編譯提供者類型的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="6ab95-118">A **DWORD** value that represents the cryptographic provider type.</span></span> <span data-ttu-id="6ab95-119">如需詳細資訊，請參閱 [密碼編譯提供者類型](cryptographic-provider-types.md)。</span><span class="sxs-lookup"><span data-stu-id="6ab95-119">For more information, see [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="6ab95-120">*pwszPvkFile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ab95-120">*pwszPvkFile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab95-121">以 null 結束的字串指標，其中包含私密金鑰檔案的名稱。</span><span class="sxs-lookup"><span data-stu-id="6ab95-121">A pointer to a null-terminated string that contains the name of a private key file.</span></span>

</dd> <dt>

<span data-ttu-id="6ab95-122">*pwszKeyContainerName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6ab95-122">*pwszKeyContainerName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab95-123">私密金鑰容器名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="6ab95-123">A pointer to a null-terminated string for the private key container name.</span></span>

</dd> <dt>

<span data-ttu-id="6ab95-124">*pdwKeySpec* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6ab95-124">*pdwKeySpec* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab95-125">*PhCryptProv* 和 *ppwszTmpContainer* 所傳回之容器的索引鍵類型的 **DWORD** 值指標。</span><span class="sxs-lookup"><span data-stu-id="6ab95-125">A pointer to a **DWORD** value for the type of key of the container returned with *phCryptProv* and *ppwszTmpContainer*.</span></span>

</dd> <dt>

<span data-ttu-id="6ab95-126">*ppwszTmpContainer* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="6ab95-126">*ppwszTmpContainer* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab95-127">暫存金鑰容器名稱之以 null 結束的字串指標的位址。</span><span class="sxs-lookup"><span data-stu-id="6ab95-127">The address of a pointer to a null-terminated string for the temporary key container name.</span></span> <span data-ttu-id="6ab95-128">**PvkGetCryptProv** 函式會提供並初始化暫存容器。</span><span class="sxs-lookup"><span data-stu-id="6ab95-128">The **PvkGetCryptProv** function provides and initializes the temporary container.</span></span> <span data-ttu-id="6ab95-129">呼叫 **PvkGetCryptProv** 時，位址應該指向 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="6ab95-129">When calling **PvkGetCryptProv**, the address should point to a **NULL** value.</span></span>

</dd> <dt>

<span data-ttu-id="6ab95-130">*phCryptProv* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="6ab95-130">*phCryptProv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="6ab95-131">CSP 的控制碼指標。</span><span class="sxs-lookup"><span data-stu-id="6ab95-131">A pointer to a handle for the CSP.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6ab95-132">傳回值</span><span class="sxs-lookup"><span data-stu-id="6ab95-132">Return value</span></span>

<span data-ttu-id="6ab95-133">如果方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="6ab95-133">If the method succeeds, it returns **S\_OK**.</span></span>

<span data-ttu-id="6ab95-134">如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="6ab95-134">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="6ab95-135">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="6ab95-135">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="6ab95-136">備註</span><span class="sxs-lookup"><span data-stu-id="6ab95-136">Remarks</span></span>

<span data-ttu-id="6ab95-137">**PvkGetCryptProv** 函式會先嘗試從 *pwszKeyContainerName* 參數所指定的金鑰容器名稱取得提供者控制碼。</span><span class="sxs-lookup"><span data-stu-id="6ab95-137">The **PvkGetCryptProv** function first tries to get the provider handle from the key container name specified by the *pwszKeyContainerName* parameter.</span></span> <span data-ttu-id="6ab95-138">如果您傳遞 **Null** 給 *PwszKeyContainerName* 參數， **PvkGetCryptProv** 會嘗試從 *pwszPvkFile* 參數中指定的私密金鑰檔案取得提供者。</span><span class="sxs-lookup"><span data-stu-id="6ab95-138">If you pass **NULL** for the *pwszKeyContainerName* parameter, **PvkGetCryptProv** tries to get the provider from the private key file specified in the *pwszPvkFile* parameter.</span></span>

<span data-ttu-id="6ab95-139">當您完成使用 CSP 之後，請呼叫 [**PvkFreeCryptProv**](pvkfreecryptprov.md) 函式來釋出提供者控制碼和暫存金鑰容器。</span><span class="sxs-lookup"><span data-stu-id="6ab95-139">When you have finished using the CSP, free the provider handle and temporary key container by calling the [**PvkFreeCryptProv**](pvkfreecryptprov.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="6ab95-140">規格需求</span><span class="sxs-lookup"><span data-stu-id="6ab95-140">Requirements</span></span>



| <span data-ttu-id="6ab95-141">需求</span><span class="sxs-lookup"><span data-stu-id="6ab95-141">Requirement</span></span> | <span data-ttu-id="6ab95-142">值</span><span class="sxs-lookup"><span data-stu-id="6ab95-142">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="6ab95-143">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6ab95-143">Minimum supported client</span></span><br/> | <span data-ttu-id="6ab95-144">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ab95-144">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="6ab95-145">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6ab95-145">Minimum supported server</span></span><br/> | <span data-ttu-id="6ab95-146">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6ab95-146">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="6ab95-147">DLL</span><span class="sxs-lookup"><span data-stu-id="6ab95-147">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6ab95-148"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6ab95-148"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
