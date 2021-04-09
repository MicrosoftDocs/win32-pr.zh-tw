---
description: 時間戳記指定的主體。 此函數支援 Authenticode 時間戳記。 若要執行 x.509 公開金鑰基礎結構 (RFC 3161) 時間戳記，請使用 SignerTimeStampEx2 函數。
ms.assetid: fb2c149b-dba2-4879-be97-831037e1110b
title: SignerTimeStamp 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerTimeStamp
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: c4c57f231f70477a76b4d4f6156354ebc847a715
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944949"
---
# <a name="signertimestamp-function"></a><span data-ttu-id="872d0-105">SignerTimeStamp 函式</span><span class="sxs-lookup"><span data-stu-id="872d0-105">SignerTimeStamp function</span></span>

<span data-ttu-id="872d0-106">**SignerTimeStamp** 函數時間會將指定的主旨戳記。</span><span class="sxs-lookup"><span data-stu-id="872d0-106">The **SignerTimeStamp** function time stamps the specified subject.</span></span> <span data-ttu-id="872d0-107">此函數支援 Authenticode 時間戳記。</span><span class="sxs-lookup"><span data-stu-id="872d0-107">This function supports Authenticode time stamping.</span></span> <span data-ttu-id="872d0-108">若要執行 x.509 公開金鑰基礎結構 (RFC 3161) 時間戳記，請使用 [**SignerTimeStampEx2**](signertimestampex2.md) 函數。</span><span class="sxs-lookup"><span data-stu-id="872d0-108">To perform X.509 Public Key Infrastructure (RFC 3161) time stamping, use the [**SignerTimeStampEx2**](signertimestampex2.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="872d0-109">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="872d0-109">This function has no associated header file or import library.</span></span> <span data-ttu-id="872d0-110">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。</span><span class="sxs-lookup"><span data-stu-id="872d0-110">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="872d0-111">語法</span><span class="sxs-lookup"><span data-stu-id="872d0-111">Syntax</span></span>


```C++
HRESULT WINAPI SignerTimeStamp(
  _In_     SIGNER_SUBJECT_INFO *pSubjectInfo,
  _In_     LPCWSTR             pwszHttpTimeStamp,
  _In_opt_ PCRYPT_ATTRIBUTES   psRequest,
  _In_opt_ LPVOID              pSipData
);
```



## <a name="parameters"></a><span data-ttu-id="872d0-112">參數</span><span class="sxs-lookup"><span data-stu-id="872d0-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="872d0-113">*pSubjectInfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="872d0-113">*pSubjectInfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="872d0-114">[**簽署者 \_ 主體 \_ 資訊**](signer-subject-info.md)結構的位址，其代表要加上時間戳記的主旨。</span><span class="sxs-lookup"><span data-stu-id="872d0-114">The address of a [**SIGNER\_SUBJECT\_INFO**](signer-subject-info.md) structure that represents the subject to be time stamped.</span></span>

</dd> <dt>

<span data-ttu-id="872d0-115">*pwszHttpTimeStamp* \[在\]</span><span class="sxs-lookup"><span data-stu-id="872d0-115">*pwszHttpTimeStamp* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="872d0-116">以 null 終止的 Unicode 字串的位址，其中包含時間戳記伺服器的 URL。</span><span class="sxs-lookup"><span data-stu-id="872d0-116">The address of a null-terminated Unicode string that contains the URL of a time stamp server.</span></span>

</dd> <dt>

<span data-ttu-id="872d0-117">*psRequest* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="872d0-117">*psRequest* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="872d0-118">[**CRYPT \_ 屬性**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes)結構的位址，其中包含新增至時間戳記要求的其他屬性。</span><span class="sxs-lookup"><span data-stu-id="872d0-118">The address of a [**CRYPT\_ATTRIBUTES**](/windows/desktop/api/Wincrypt/ns-wincrypt-crypt_attributes) structure that contains additional attributes that are added to the time stamp request.</span></span>

<span data-ttu-id="872d0-119">這個參數是選擇性的，如果未包含，則可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="872d0-119">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> <dt>

<span data-ttu-id="872d0-120">*pSipData* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="872d0-120">*pSipData* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="872d0-121">以其他資料形式傳遞至 SIP 函數的32位值。</span><span class="sxs-lookup"><span data-stu-id="872d0-121">A 32-bit value that is passed as additional data to SIP functions.</span></span> <span data-ttu-id="872d0-122">此的格式和內容是由 SIP 提供者定義。</span><span class="sxs-lookup"><span data-stu-id="872d0-122">The format and content of this is defined by the SIP provider.</span></span>

<span data-ttu-id="872d0-123">這個參數是選擇性的，如果未包含，則可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="872d0-123">This parameter is optional and can be **NULL** if it is not included.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="872d0-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="872d0-124">Return value</span></span>

<span data-ttu-id="872d0-125">如果函式成功，函數會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="872d0-125">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="872d0-126">如果函式失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="872d0-126">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="872d0-127">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="872d0-127">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="872d0-128">規格需求</span><span class="sxs-lookup"><span data-stu-id="872d0-128">Requirements</span></span>



| <span data-ttu-id="872d0-129">需求</span><span class="sxs-lookup"><span data-stu-id="872d0-129">Requirement</span></span> | <span data-ttu-id="872d0-130">值</span><span class="sxs-lookup"><span data-stu-id="872d0-130">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="872d0-131">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="872d0-131">Minimum supported client</span></span><br/> | <span data-ttu-id="872d0-132">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="872d0-132">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="872d0-133">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="872d0-133">Minimum supported server</span></span><br/> | <span data-ttu-id="872d0-134">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="872d0-134">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="872d0-135">DLL</span><span class="sxs-lookup"><span data-stu-id="872d0-135">DLL</span></span><br/>                      | <dl> <span data-ttu-id="872d0-136"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="872d0-136"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
