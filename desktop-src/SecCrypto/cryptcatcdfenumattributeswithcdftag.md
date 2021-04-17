---
description: 列舉目錄定義檔之 CatalogFiles 區段中的成員檔案屬性 (CDF) 。
ms.assetid: 056a5186-a37c-4255-aaa5-4c6e60f5392e
title: CryptCATCDFEnumAttributesWithCDFTag 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CryptCATCDFEnumAttributesWithCDFTag
api_type:
- DllExport
api_location:
- Wintrust.dll
ms.openlocfilehash: bd3c5905c57d234d42cd89d18c2a141c4026250f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511172"
---
# <a name="cryptcatcdfenumattributeswithcdftag-function"></a><span data-ttu-id="4d2d0-103">CryptCATCDFEnumAttributesWithCDFTag 函式</span><span class="sxs-lookup"><span data-stu-id="4d2d0-103">CryptCATCDFEnumAttributesWithCDFTag function</span></span>

<span data-ttu-id="4d2d0-104">\[**CryptCATCDFEnumAttributesWithCDFTag** 函式可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-104">\[The **CryptCATCDFEnumAttributesWithCDFTag** function is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="4d2d0-105">它在後續版本中可能會變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="4d2d0-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="4d2d0-106">**CryptCATCDFEnumAttributesWithCDFTag** 函式會列舉目錄定義檔之 **CatalogFiles** 區段中的成員檔案屬性 (CDF) 。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-106">The **CryptCATCDFEnumAttributesWithCDFTag** function enumerates the attributes of member files in the **CatalogFiles** section of a catalog definition file (CDF).</span></span> <span data-ttu-id="4d2d0-107">[MakeCat](makecat.md)會呼叫 **CryptCATCDFEnumAttributesWithCDFTag** 。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-107">**CryptCATCDFEnumAttributesWithCDFTag** is called by [MakeCat](makecat.md).</span></span>

> [!Note]  
> <span data-ttu-id="4d2d0-108">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-108">This function has no associated header file or import library.</span></span> <span data-ttu-id="4d2d0-109">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-109">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4d2d0-110">語法</span><span class="sxs-lookup"><span data-stu-id="4d2d0-110">Syntax</span></span>


```C++
CRYPTCATATTRIBUTE* WINAPI CryptCATCDFEnumAttributesWithCDFTag(
  _In_ CRYPTCATCDF                  *pCDF,
  _In_ LPWSTR                       pwszMemberTag,
  _In_ CRYPTCATMEMBER               *pMember,
  _In_ CRYPTCATATTRIBUTE            *pPrevAttr,
  _In_ PFN_CDF_PARSE_ERROR_CALLBACK pfnParseError
);
```



## <a name="parameters"></a><span data-ttu-id="4d2d0-111">參數</span><span class="sxs-lookup"><span data-stu-id="4d2d0-111">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4d2d0-112">*pCDF* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d2d0-112">*pCDF* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d2d0-113">[**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-113">A pointer to a [**CRYPTCATCDF**](/windows/win32/api/mscat/ns-mscat-cryptcatcdf) structure.</span></span>

</dd> <dt>

<span data-ttu-id="4d2d0-114">*pwszMemberTag* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d2d0-114">*pwszMemberTag* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d2d0-115">識別類別目錄檔案成員之以 **null** 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-115">A pointer to a **null**-terminated string that identifies the catalog file member.</span></span>

</dd> <dt>

<span data-ttu-id="4d2d0-116">*pMember* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d2d0-116">*pMember* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d2d0-117">[**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember)結構的指標，其中包含成員資訊。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-117">A pointer to a [**CRYPTCATMEMBER**](/windows/win32/api/mscat/ns-mscat-cryptcatmember) structure that contains the member information.</span></span>

</dd> <dt>

<span data-ttu-id="4d2d0-118">*pPrevAttr* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d2d0-118">*pPrevAttr* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d2d0-119">*PCDF* 所指向之 CDF 中檔案成員屬性的 [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute)結構指標。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-119">A pointer to a [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) structure for a file member attribute in the CDF pointed to by *pCDF*.</span></span>

</dd> <dt>

<span data-ttu-id="4d2d0-120">*pfnParseError* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4d2d0-120">*pfnParseError* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4d2d0-121">使用者定義函數的指標，用來處理檔案剖析錯誤。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-121">A pointer to a user-defined function to handle file parse errors.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4d2d0-122">傳回值</span><span class="sxs-lookup"><span data-stu-id="4d2d0-122">Return value</span></span>

<span data-ttu-id="4d2d0-123">成功時，此函式會傳回 [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-123">Upon success, this function returns a pointer to a [**CRYPTCATATTRIBUTE**](/windows/win32/api/mscat/ns-mscat-cryptcatattribute) structure.</span></span> <span data-ttu-id="4d2d0-124">如果 **CryptCATCDFEnumAttributesWithCDFTag** 函式失敗，則會傳回 **Null** 指標。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-124">The **CryptCATCDFEnumAttributesWithCDFTag** function returns a **NULL** pointer if it fails.</span></span>

## <a name="remarks"></a><span data-ttu-id="4d2d0-125">備註</span><span class="sxs-lookup"><span data-stu-id="4d2d0-125">Remarks</span></span>

<span data-ttu-id="4d2d0-126">您通常會在迴圈中呼叫此函式，以列舉 CDF 中的所有類別目錄檔案成員屬性。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-126">You typically call this function in a loop to enumerate all of the catalog file member attributes in a CDF.</span></span> <span data-ttu-id="4d2d0-127">進入迴圈之前，請將 *pPrevAttr* 設定為 **Null**。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-127">Before entering the loop, set *pPrevAttr* to **NULL**.</span></span> <span data-ttu-id="4d2d0-128">函數會傳回第一個屬性的指標。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-128">The function returns a pointer to the first attribute.</span></span> <span data-ttu-id="4d2d0-129">針對迴圈的後續反覆運算，將 *pPrevAttr* 設定為函式的傳回值。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-129">Set *pPrevAttr* to the return value of the function for subsequent iterations of the loop.</span></span>

## <a name="examples"></a><span data-ttu-id="4d2d0-130">範例</span><span class="sxs-lookup"><span data-stu-id="4d2d0-130">Examples</span></span>

<span data-ttu-id="4d2d0-131">下列範例顯示 *pPrevAttr* 參數 () 的正確指派順序 `pAttr` 。</span><span class="sxs-lookup"><span data-stu-id="4d2d0-131">The following example shows the correct sequence of assignments for the *pPrevAttr* parameter (`pAttr`).</span></span>


```C++
    CRYPTCATATTRIBUTE   *pAttr;
    CRYPTCATMEMBER      *pMember;
    LPWSTR              pwszMemberTag;
    CRYPTCATCDF         *pCDF;

    pCDF = CryptCATCDFOpen(L"myCDF", NULL);
    

    pMember = NULL;
    pwszMemberTag = NULL;

    while (pwszMemberTag = CryptCATCDFEnumMembersByCDFTagEx(pCDF,
                                                            pwszMemberTag,
                                                            NULL,
                                                            &pMember,
                                                            FALSE,
                                                            NULL))
    {
        pAttr = NULL;

        while (pAttr = CryptCATCDFEnumAttributesWithCDFTag(pCDF,
                                                           pwszMemberTag,
                                                           pMember,
                                                           pAttr,
                                                           DisplayParseError))
        {
            //do something with pAttr
        }

    }

    CryptCATCDFClose(pCDF);
```



## <a name="requirements"></a><span data-ttu-id="4d2d0-132">規格需求</span><span class="sxs-lookup"><span data-stu-id="4d2d0-132">Requirements</span></span>



| <span data-ttu-id="4d2d0-133">需求</span><span class="sxs-lookup"><span data-stu-id="4d2d0-133">Requirement</span></span> | <span data-ttu-id="4d2d0-134">值</span><span class="sxs-lookup"><span data-stu-id="4d2d0-134">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4d2d0-135">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4d2d0-135">Minimum supported client</span></span><br/> | <span data-ttu-id="4d2d0-136">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d2d0-136">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4d2d0-137">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4d2d0-137">Minimum supported server</span></span><br/> | <span data-ttu-id="4d2d0-138">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4d2d0-138">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4d2d0-139">DLL</span><span class="sxs-lookup"><span data-stu-id="4d2d0-139">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4d2d0-140"><dt>Wintrust.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4d2d0-140"><dt>Wintrust.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4d2d0-141">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4d2d0-141">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4d2d0-142">MakeCat</span><span class="sxs-lookup"><span data-stu-id="4d2d0-142">MakeCat</span></span>](makecat.md)
</dt> <dt>

[<span data-ttu-id="4d2d0-143">**CRYPTCATATTRIBUTE**</span><span class="sxs-lookup"><span data-stu-id="4d2d0-143">**CRYPTCATATTRIBUTE**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatattribute)
</dt> <dt>

[<span data-ttu-id="4d2d0-144">**CRYPTCATCDF**</span><span class="sxs-lookup"><span data-stu-id="4d2d0-144">**CRYPTCATCDF**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatcdf)
</dt> <dt>

[<span data-ttu-id="4d2d0-145">**CRYPTCATMEMBER**</span><span class="sxs-lookup"><span data-stu-id="4d2d0-145">**CRYPTCATMEMBER**</span></span>](/windows/win32/api/mscat/ns-mscat-cryptcatmember)
</dt> <dt>

[<span data-ttu-id="4d2d0-146">**GetProcAddress**</span><span class="sxs-lookup"><span data-stu-id="4d2d0-146">**GetProcAddress**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress)
</dt> <dt>

[<span data-ttu-id="4d2d0-147">**LoadLibrary**</span><span class="sxs-lookup"><span data-stu-id="4d2d0-147">**LoadLibrary**</span></span>](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya)
</dt> </dl>

 

 
