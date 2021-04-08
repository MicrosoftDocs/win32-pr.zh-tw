---
description: 時間戳記指定的主體，並選擇性地傳回 \_ 包含 BLOB 指標之簽署者內容結構的指標。
ms.assetid: f3a910f6-64f8-4cf5-b008-2a16872f9a98
title: SignerTimeStampEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStampEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: a4562ca84f8b3376a22d00a5e9501947152ed875
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103694488"
---
# <a name="signertimestampex-function"></a><span data-ttu-id="3c425-103">SignerTimeStampEx 函式</span><span class="sxs-lookup"><span data-stu-id="3c425-103">SignerTimeStampEx function</span></span>

<span data-ttu-id="3c425-104">**SignerTimeStampEx** 函式時間會為指定的主旨加上戳記，並選擇性地將指標傳回至包含 [*BLOB*](../secgloss/b-gly.md)指標的 [**簽署者 \_ 內容**](signer-context.md)結構。</span><span class="sxs-lookup"><span data-stu-id="3c425-104">The **SignerTimeStampEx** function time stamps the specified subject and optionally returns a pointer to a [**SIGNER\_CONTEXT**](signer-context.md) structure that contains a pointer to a [*BLOB*](../secgloss/b-gly.md).</span></span> <span data-ttu-id="3c425-105">此函數支援 Authenticode 時間戳記。</span><span class="sxs-lookup"><span data-stu-id="3c425-105">This function supports Authenticode time stamping.</span></span> <span data-ttu-id="3c425-106">若要執行 x.509 公開金鑰基礎結構 (RFC 3161) 時間戳記，請使用 [**SignerTimeStampEx2**](signertimestampex2.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="3c425-106">To perform X.509 Public Key Infrastructure (RFC 3161) time stamping, use the [**SignerTimeStampEx2**](signertimestampex2.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="3c425-107">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="3c425-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="3c425-108">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。</span><span class="sxs-lookup"><span data-stu-id="3c425-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="3c425-109">語法</span><span class="sxs-lookup"><span data-stu-id="3c425-109">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStampEx(
  _Reserved_ DWORD               dwFlags,
  _In_       SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_       LPCWSTR             pwszHttpTimeStamp,
  _In_       PCRYPT_ATTRIBUTES   psRequest,
  _In_       LPVOID              pSipData,
  _Out_      SIGNER_CONTEXT      **ppSignerContext 
);
```



## <a name="parameters"></a><span data-ttu-id="3c425-110">參數</span><span class="sxs-lookup"><span data-stu-id="3c425-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c425-111">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c425-111">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c425-112">保留的。</span><span class="sxs-lookup"><span data-stu-id="3c425-112">Reserved.</span></span> <span data-ttu-id="3c425-113">此參數必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="3c425-113">This parameter must be set to zero.</span></span>

</dd> <dt>

<span data-ttu-id="3c425-114">*pSubjectInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c425-114">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c425-115">[**簽署者 \_ 主體 \_ 資訊**](signer-subject-info.md)結構的位址，其代表要加上時間戳記的主旨。</span><span class="sxs-lookup"><span data-stu-id="3c425-115">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="3c425-116">*pwszHttpTimeStamp* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c425-116">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c425-117">以 null 終止的 Unicode 字串的位址，其中包含時間戳記伺服器的 URL。</span><span class="sxs-lookup"><span data-stu-id="3c425-117">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="3c425-118">*psRequest* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c425-118">*psRequest* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c425-119">選擇性。</span><span class="sxs-lookup"><span data-stu-id="3c425-119">Optional.</span></span> <span data-ttu-id="3c425-120">[**CRYPT \_ 屬性**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes)結構的位址，其中包含新增至時間戳記要求的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="3c425-120">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="3c425-121">這個參數是選擇性的，如果未包含，則可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="3c425-121">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="3c425-122">*pSipData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3c425-122">*pSipData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3c425-123">選擇性。</span><span class="sxs-lookup"><span data-stu-id="3c425-123">Optional.</span></span> <span data-ttu-id="3c425-124">以其他資料的形式傳遞至 [*主體介面封裝*](../secgloss/s-gly.md) 的32位值 (SIP) 函式。</span><span class="sxs-lookup"><span data-stu-id="3c425-124">A 32-bit value that is passed as additional data to [*subject interface package*](../secgloss/s-gly.md) (SIP) functions.</span></span> <span data-ttu-id="3c425-125">此參數的格式和內容是由 SIP 提供者定義。</span><span class="sxs-lookup"><span data-stu-id="3c425-125">The format and content of this parameter is defined by the SIP provider.</span></span>

<span data-ttu-id="3c425-126">這個參數是選擇性的，如果未包含，則可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="3c425-126">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="3c425-127">*ppSignerCoNtext* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3c425-127">*ppSignerContext* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c425-128">選擇性。</span><span class="sxs-lookup"><span data-stu-id="3c425-128">Optional.</span></span> <span data-ttu-id="3c425-129">包含已簽署 BLOB 之 [**簽署者 \_ 內容**](signer-context.md) 結構的指標位址。</span><span class="sxs-lookup"><span data-stu-id="3c425-129">The address of a pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure that contains the signed BLOB.</span></span> <span data-ttu-id="3c425-130">當您完成使用 **簽署者 \_ 內容** 結構時，請呼叫 [**SignerFreeSignerCoNtext**](signerfreesignercontext.md) 函式來釋放它。</span><span class="sxs-lookup"><span data-stu-id="3c425-130">When you have finished using the **SIGNER\_CONTEXT** structure, free it by calling the [**SignerFreeSignerContext**](signerfreesignercontext.md) function.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3c425-131">傳回值</span><span class="sxs-lookup"><span data-stu-id="3c425-131">Return value</span></span>

<span data-ttu-id="3c425-132">如果函式成功，函數會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="3c425-132">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="3c425-133">如果函式失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="3c425-133">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="3c425-134">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="3c425-134">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="3c425-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c425-135">Requirements</span></span>



| <span data-ttu-id="3c425-136">需求</span><span class="sxs-lookup"><span data-stu-id="3c425-136">Requirement</span></span> | <span data-ttu-id="3c425-137">值</span><span class="sxs-lookup"><span data-stu-id="3c425-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3c425-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c425-138">Minimum supported client</span></span><br/> | <span data-ttu-id="3c425-139">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c425-139">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="3c425-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c425-140">Minimum supported server</span></span><br/> | <span data-ttu-id="3c425-141">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c425-141">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="3c425-142">DLL</span><span class="sxs-lookup"><span data-stu-id="3c425-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3c425-143"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3c425-143"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3c425-144">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3c425-144">See also</span></span>

<dl> <span data-ttu-id="3c425-145"><dt>


</dt> <dt></span><span class="sxs-lookup"><span data-stu-id="3c425-145"><dt>


</dt> <dt></span></span>

[<span data-ttu-id="3c425-146">**SignerTimeStamp**</span><span class="sxs-lookup"><span data-stu-id="3c425-146">**SignerTimeStamp**</span></span>](signertimestamp.md)
</dt> </dl>

 

 
