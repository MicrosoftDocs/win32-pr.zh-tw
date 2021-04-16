---
description: 列舉目錄定義檔之 CatalogFiles 區段中的個別檔案成員 (CDF) 。
ms.assetid: 38e17ef2-65dc-45f8-a484-8eedcf4ce3e3
title: CryptCATCDFEnumMembersByCDFTagEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumMembersByCDFTagEx
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: 633f78377e3c4f23f4b93ba2f76dc113eda11a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511173"
---
# <a name="cryptcatcdfenummembersbycdftagex-function"></a><span data-ttu-id="5fd05-103">CryptCATCDFEnumMembersByCDFTagEx 函式</span><span class="sxs-lookup"><span data-stu-id="5fd05-103">CryptCATCDFEnumMembersByCDFTagEx function</span></span>

<span data-ttu-id="5fd05-104">\[**CryptCATCDFEnumMembersByCDFTagEx** 函式可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="5fd05-104">\[The **CryptCATCDFEnumMembersByCDFTagEx** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="5fd05-105">它在後續版本中可能會變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="5fd05-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="5fd05-106">**CryptCATCDFEnumMembersByCDFTagEx** 函式會列舉目錄定義檔之 **CatalogFiles** 區段中的個別檔案成員， (CDF) 。</span><span class="sxs-lookup"><span data-stu-id="5fd05-106">The **CryptCATCDFEnumMembersByCDFTagEx** function enumerates the individual file members in the **CatalogFiles** section of a catalog definition file (CDF).</span></span> <span data-ttu-id="5fd05-107">[MakeCat](makecat.md)會呼叫 **CryptCATCDFEnumMembersByCDFTagEx** 。</span><span class="sxs-lookup"><span data-stu-id="5fd05-107">**CryptCATCDFEnumMembersByCDFTagEx** is called by [MakeCat](makecat.md).</span></span>

> [!Note]  
> <span data-ttu-id="5fd05-108">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="5fd05-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="5fd05-109">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。</span><span class="sxs-lookup"><span data-stu-id="5fd05-109">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="5fd05-110">語法</span><span class="sxs-lookup"><span data-stu-id="5fd05-110">Syntax</span></span>


```C++
LPWSTR WINAPI CryptCATCDFEnumMembersByCDFTagEx(
  _In_    CRYPTCATCDF                  *pCDF,
  _Inout_ LPWSTR                       pwszPrevCDFTag,
  _In_    PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError,
  _In_    CRYPTCATMEMBER               **ppMember,
  _In_    BOOL                         fContinueOnError,
  _In_    LPVOID                       pvReserved
);
```



## <a name="parameters"></a><span data-ttu-id="5fd05-111">參數</span><span class="sxs-lookup"><span data-stu-id="5fd05-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5fd05-112">*pCDF* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5fd05-112">*pCDF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fd05-113">[**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="5fd05-113">A pointer to a [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) structure.</span></span>

</dd> <dt>

<span data-ttu-id="5fd05-114">*pwszPrevCDFTag* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="5fd05-114">*pwszPrevCDFTag* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5fd05-115">識別類別目錄檔案成員之以 **null** 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="5fd05-115">A pointer to a **null**-terminated string that identifies the catalog file member.</span></span>

</dd> <dt>

<span data-ttu-id="5fd05-116">*pfnParseError* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5fd05-116">*pfnParseError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fd05-117">使用者定義函數的指標，用來處理檔案剖析錯誤。</span><span class="sxs-lookup"><span data-stu-id="5fd05-117">A pointer to a user-defined function to handle file parse errors.</span></span>

</dd> <dt>

<span data-ttu-id="5fd05-118">*ppMember* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5fd05-118">*ppMember* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fd05-119">[**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember)結構的指標，其中包含檔案成員資訊。</span><span class="sxs-lookup"><span data-stu-id="5fd05-119">A pointer to a [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) structure that contains the file member information.</span></span>

</dd> <dt>

<span data-ttu-id="5fd05-120">*fContinueOnError* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5fd05-120">*fContinueOnError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fd05-121">值，指定是否要在記憶體中保留最後一個列舉成員的參考。</span><span class="sxs-lookup"><span data-stu-id="5fd05-121">A value that specifies whether to keep in memory a reference to the last enumerated member.</span></span>

</dd> <dt>

<span data-ttu-id="5fd05-122">*pvReserved* \[在\]</span><span class="sxs-lookup"><span data-stu-id="5fd05-122">*pvReserved* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="5fd05-123">此參數為 reserved;請勿使用它。</span><span class="sxs-lookup"><span data-stu-id="5fd05-123">This parameter is reserved; do not use it.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5fd05-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="5fd05-124">Return value</span></span>

<span data-ttu-id="5fd05-125">成功時，此函式會傳回以 **null** 結束的字串指標，以識別 CDF **CatalogFiles** 區段中的檔案成員。</span><span class="sxs-lookup"><span data-stu-id="5fd05-125">Upon success, this function returns a pointer to a **null**-terminated string that identifies a file member in the **CatalogFiles** section of a CDF.</span></span> <span data-ttu-id="5fd05-126">如果 **CryptCATCDFEnumMembersByCDFTagEx** 函式失敗，則會傳回 **Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="5fd05-126">The **CryptCATCDFEnumMembersByCDFTagEx** function returns a **NULL** pointer if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="5fd05-127">備註</span><span class="sxs-lookup"><span data-stu-id="5fd05-127">Remarks</span></span>

<span data-ttu-id="5fd05-128">您通常會在迴圈中呼叫此函式，以列舉 CDF 中的所有類別目錄檔案成員。</span><span class="sxs-lookup"><span data-stu-id="5fd05-128">You typically call this function in a loop to enumerate all of the catalog file members in a CDF.</span></span> <span data-ttu-id="5fd05-129">進入迴圈之前，請將 *pwszPrevCDFTag* 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="5fd05-129">Before entering the loop, set *pwszPrevCDFTag* to **NULL**.</span></span> <span data-ttu-id="5fd05-130">函數會傳回第一個成員的指標。</span><span class="sxs-lookup"><span data-stu-id="5fd05-130">The function returns a pointer to the first member.</span></span> <span data-ttu-id="5fd05-131">針對迴圈的後續反覆運算，將 *pwszPrevCDFTag* 設定為函式的傳回值。</span><span class="sxs-lookup"><span data-stu-id="5fd05-131">Set *pwszPrevCDFTag* to the return value of the function for subsequent iterations of the loop.</span></span>

## <a name="examples"></a><span data-ttu-id="5fd05-132">範例</span><span class="sxs-lookup"><span data-stu-id="5fd05-132">Examples</span></span>

<span data-ttu-id="5fd05-133">下列範例顯示 *pwszPrevCDFTag* 參數 () 的正確指派順序 `pwszMemberTag` 。</span><span class="sxs-lookup"><span data-stu-id="5fd05-133">The following example shows the correct sequence of assignments for the *pwszPrevCDFTag* parameter (`pwszMemberTag`).</span></span>


```C++
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L'myCDF', NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        //do something with pwszMemberTag and pMember
    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a><span data-ttu-id="5fd05-134">規格需求</span><span class="sxs-lookup"><span data-stu-id="5fd05-134">Requirements</span></span>



| <span data-ttu-id="5fd05-135">需求</span><span class="sxs-lookup"><span data-stu-id="5fd05-135">Requirement</span></span> | <span data-ttu-id="5fd05-136">值</span><span class="sxs-lookup"><span data-stu-id="5fd05-136">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="5fd05-137">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5fd05-137">Minimum supported client</span></span><br/> | <span data-ttu-id="5fd05-138">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5fd05-138">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="5fd05-139">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5fd05-139">Minimum supported server</span></span><br/> | <span data-ttu-id="5fd05-140">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5fd05-140">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="5fd05-141">DLL</span><span class="sxs-lookup"><span data-stu-id="5fd05-141">DLL</span></span><br/>                      | <dl> <span data-ttu-id="5fd05-142"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="5fd05-142"><dt>Wintrust.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5fd05-143">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5fd05-143">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5fd05-144">MakeCat</span><span class="sxs-lookup"><span data-stu-id="5fd05-144">MakeCat</span></span>](makecat.md)
</dt> <dt>

[<span data-ttu-id="5fd05-145">**CRYPTCATCDF**</span><span class="sxs-lookup"><span data-stu-id="5fd05-145">**CRYPTCATCDF**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[<span data-ttu-id="5fd05-146">**CRYPTCATMEMBER**</span><span class="sxs-lookup"><span data-stu-id="5fd05-146">**CRYPTCATMEMBER**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[<span data-ttu-id="5fd05-147">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="5fd05-147">**GetProcAddress**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="5fd05-148">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="5fd05-148">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
