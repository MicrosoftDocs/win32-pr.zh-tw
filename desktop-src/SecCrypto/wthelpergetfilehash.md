---
description: 驗證已簽署檔案的簽章，並取得檔案的雜湊值和演算法識別碼。
ms.assetid: 130b3c3e-cc67-44ec-acc7-daa87b714299
title: WTHelperGetFileHash 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WTHelperGetFileHash
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 1597dfda630b1ae8cbc0d3b700b6ed9bc1a09472
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103944359"
---
# <a name="wthelpergetfilehash-function"></a><span data-ttu-id="7490b-103">WTHelperGetFileHash 函式</span><span class="sxs-lookup"><span data-stu-id="7490b-103">WTHelperGetFileHash function</span></span>

<span data-ttu-id="7490b-104">\[**WTHelperGetFileHash** 函式可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="7490b-104">\[The **WTHelperGetFileHash** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="7490b-105">它在後續版本中可能會變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="7490b-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="7490b-106">**WTHelperGetFileHash** 函式會驗證已簽署檔案的簽章，並取得檔案的雜湊值和演算法識別碼。</span><span class="sxs-lookup"><span data-stu-id="7490b-106">The **WTHelperGetFileHash** function verifies the signature of a signed file and obtains the hash value and algorithm identifier for the file.</span></span>

> [!Note]  
> <span data-ttu-id="7490b-107">未在已發行的標頭檔中宣告此函式。</span><span class="sxs-lookup"><span data-stu-id="7490b-107">This function is not declared in a published header file.</span></span> <span data-ttu-id="7490b-108">若要使用此函式，請使用所示的確切格式來宣告。</span><span class="sxs-lookup"><span data-stu-id="7490b-108">To use this function, declare it in the exact format shown.</span></span> <span data-ttu-id="7490b-109">此函數也沒有相關聯的匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="7490b-109">This function also has no associated import library.</span></span> <span data-ttu-id="7490b-110">您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數，以動態方式連結至 Wintrust.dll。</span><span class="sxs-lookup"><span data-stu-id="7490b-110">You must use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Wintrust.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="7490b-111">語法</span><span class="sxs-lookup"><span data-stu-id="7490b-111">Syntax</span></span>


```C++
LONG WINAPI WTHelperGetFileHash(
  _In_        LPCWSTR pwszFilename,
  _In_        DWORD   dwFlags,
  _Inout_opt_ PVOID   pvReserved,
  _Out_opt_   BYTE    *pbFileHash,
  _Inout_opt_ DWORD   *pcbFileHash,
  _Out_opt_   ALG_ID  *pHashAlgid
);
```



## <a name="parameters"></a><span data-ttu-id="7490b-112">參數</span><span class="sxs-lookup"><span data-stu-id="7490b-112">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="7490b-113">*pwszFilename* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7490b-113">*pwszFilename* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7490b-114">以 null 終止的 Unicode 字串指標，其中包含要取得雜湊之檔案的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="7490b-114">A pointer to a null-terminated Unicode string that contains the path and file name of the file to get the hash for.</span></span>

</dd> <dt>

<span data-ttu-id="7490b-115">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="7490b-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="7490b-116">未使用此參數，且應為零。</span><span class="sxs-lookup"><span data-stu-id="7490b-116">This parameter is not used and should be zero.</span></span>

</dd> <dt>

<span data-ttu-id="7490b-117">*pvReserved* \[in、out、optional\]</span><span class="sxs-lookup"><span data-stu-id="7490b-117">*pvReserved* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7490b-118">未使用此參數，且應為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="7490b-118">This parameter is not used and should be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="7490b-119">*pbFileHash* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="7490b-119">*pbFileHash* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7490b-120">緩衝區的指標，用來接收檔案的雜湊值。</span><span class="sxs-lookup"><span data-stu-id="7490b-120">A pointer to a buffer to receive the hash value for the file.</span></span> <span data-ttu-id="7490b-121">*PcbFileHash* 參數包含這個緩衝區的大小。</span><span class="sxs-lookup"><span data-stu-id="7490b-121">The *pcbFileHash* parameter contains the size of this buffer.</span></span>

</dd> <dt>

<span data-ttu-id="7490b-122">*pcbFileHash* \[in、out、optional\]</span><span class="sxs-lookup"><span data-stu-id="7490b-122">*pcbFileHash* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7490b-123">**DWORD** 變數的指標，該變數在輸入時會包含 *pbFileHash* 緩衝區的大小（以位元組為單位），而在輸出時則會接收雜湊值的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="7490b-123">A pointer to a **DWORD** variable that, on input, contains the size, in bytes, of the *pbFileHash* buffer and, on output, receives the size, in bytes, of the hash value.</span></span>

<span data-ttu-id="7490b-124">若要取得雜湊值所需的大小，請針對 *pbFileHash* 參數傳遞 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="7490b-124">To obtain the required size of the hash value, pass **NULL** for the *pbFileHash* parameter.</span></span> <span data-ttu-id="7490b-125">此函式會將所需的大小（以位元組為單位）放在此位置中的雜湊值。</span><span class="sxs-lookup"><span data-stu-id="7490b-125">This function will place the required size, in bytes, of the hash value in this location.</span></span>

<span data-ttu-id="7490b-126">如果 *pbFileHash* 參數不是 **Null**，而且大小不夠大，無法接收雜湊值，則此函式會將所需的大小（以位元組為單位）放在此位置，並傳回 **錯誤的 \_ \_ 資料**。</span><span class="sxs-lookup"><span data-stu-id="7490b-126">If the *pbFileHash* parameter is not **NULL**, and the size is not large enough to receive the hash value, this function will place the required size, in bytes, in this location and return **ERROR\_MORE\_DATA**.</span></span>

</dd> <dt>

<span data-ttu-id="7490b-127">*pHashAlgid* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="7490b-127">*pHashAlgid* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="7490b-128">要接收用來建立雜湊值之演算法識別碼的 [**ALG \_**](alg-id.md) 識別碼變數指標。</span><span class="sxs-lookup"><span data-stu-id="7490b-128">A pointer to an [**ALG\_ID**](alg-id.md) variable to receive the identifier of the algorithm used to create the hash value.</span></span> <span data-ttu-id="7490b-129">如果不需要這項資訊，則此參數可以是 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="7490b-129">This parameter can be **NULL** if this information is not needed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="7490b-130">傳回值</span><span class="sxs-lookup"><span data-stu-id="7490b-130">Return value</span></span>

<span data-ttu-id="7490b-131">傳回表示函式成功或失敗的狀態碼。</span><span class="sxs-lookup"><span data-stu-id="7490b-131">Returns a status code that indicates the success or failure of the function.</span></span>

<span data-ttu-id="7490b-132">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="7490b-132">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="7490b-133">傳回碼</span><span class="sxs-lookup"><span data-stu-id="7490b-133">Return code</span></span>                                                                                               | <span data-ttu-id="7490b-134">Description</span><span class="sxs-lookup"><span data-stu-id="7490b-134">Description</span></span>                                                                                                                                           |
|-----------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="7490b-135"><dt>**錯誤 \_ 成功**</dt></span><span class="sxs-lookup"><span data-stu-id="7490b-135"><dt>**ERROR\_SUCCESS**</dt></span></span> </dl>             | <span data-ttu-id="7490b-136">檔案已簽署，並已驗證簽章。</span><span class="sxs-lookup"><span data-stu-id="7490b-136">The file is signed, and the signature was verified.</span></span><br/>                                                                                        |
| <dl> <span data-ttu-id="7490b-137"><dt>**錯誤 \_ 的 \_ 資料**</dt></span><span class="sxs-lookup"><span data-stu-id="7490b-137"><dt>**ERROR\_MORE\_DATA**</dt></span></span> </dl>          | <span data-ttu-id="7490b-138">*PbFileHash* 參數不是 **Null**，而且 *pcbFileHash* 參數所指定的大小不夠大，無法接收雜湊。</span><span class="sxs-lookup"><span data-stu-id="7490b-138">The *pbFileHash* parameter is not **NULL**, and the size specified by the *pcbFileHash* parameter is not large enough to receive the hash.</span></span><br/> |
| <dl> <span data-ttu-id="7490b-139"><dt>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</dt></span><span class="sxs-lookup"><span data-stu-id="7490b-139"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="7490b-140">發生記憶體配置失敗。</span><span class="sxs-lookup"><span data-stu-id="7490b-140">A memory allocation failure occurred.</span></span><br/>                                                                                                      |
| <dl> <span data-ttu-id="7490b-141"><dt>**信任 \_ 電子 \_ 不良 \_ 摘要**</dt></span><span class="sxs-lookup"><span data-stu-id="7490b-141"><dt>**TRUST\_E\_BAD\_DIGEST**</dt></span></span> </dl>      | <span data-ttu-id="7490b-142">未驗證檔案的簽章。</span><span class="sxs-lookup"><span data-stu-id="7490b-142">The signature of the file was not verified.</span></span><br/>                                                                                                |
| <dl> <span data-ttu-id="7490b-143"><dt>**信任 \_ 電子 \_ NOSIGNATURE**</dt></span><span class="sxs-lookup"><span data-stu-id="7490b-143"><dt>**TRUST\_E\_NOSIGNATURE**</dt></span></span> </dl>      | <span data-ttu-id="7490b-144">檔案未簽署或簽章無效。</span><span class="sxs-lookup"><span data-stu-id="7490b-144">The file was not signed or had a signature that is not valid.</span></span><br/>                                                                              |



 

## <a name="requirements"></a><span data-ttu-id="7490b-145">規格需求</span><span class="sxs-lookup"><span data-stu-id="7490b-145">Requirements</span></span>



| <span data-ttu-id="7490b-146">需求</span><span class="sxs-lookup"><span data-stu-id="7490b-146">Requirement</span></span> | <span data-ttu-id="7490b-147">值</span><span class="sxs-lookup"><span data-stu-id="7490b-147">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="7490b-148">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="7490b-148">Minimum supported client</span></span><br/> | <span data-ttu-id="7490b-149">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7490b-149">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="7490b-150">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="7490b-150">Minimum supported server</span></span><br/> | <span data-ttu-id="7490b-151">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="7490b-151">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="7490b-152">DLL</span><span class="sxs-lookup"><span data-stu-id="7490b-152">DLL</span></span><br/>                      | <dl> <span data-ttu-id="7490b-153"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="7490b-153"><dt>Wintrust.dll</dt></span></span> </dl> |



 

 
