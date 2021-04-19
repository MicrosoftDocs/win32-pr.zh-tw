---
description: 密碼編譯服務提供者 (CSP) 用來驗證 DLL 的簽章。
ms.assetid: 477a6c9f-05ac-485a-8b27-5605fc11c1d6
title: 'CRYPT_VERIFY_IMAGE 函式指標 (Cspdk) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CRYPT_VERIFY_IMAGE
- CRYPT_VERIFY_IMAGE_A
- CRYPT_VERIFY_IMAGE_W
api_type:
- UserDefined
api_location:
- Cspdk.h
ms.openlocfilehash: e95414d09a7869aa4a2ef512fcff2765ba4491bb
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997137"
---
# <a name="crypt_verify_image-function-pointer"></a><span data-ttu-id="00286-103">CRYPT \_ 驗證 \_ 影像函式指標</span><span class="sxs-lookup"><span data-stu-id="00286-103">CRYPT\_VERIFY\_IMAGE function pointer</span></span>

<span data-ttu-id="00286-104">[*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 使用 **FuncVerifyImage** 回呼函式來驗證 DLL 的簽章。</span><span class="sxs-lookup"><span data-stu-id="00286-104">The **FuncVerifyImage** callback function is used by a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) to verify the signature of a DLL.</span></span>

<span data-ttu-id="00286-105">CSP 進行函式呼叫的所有輔助 Dll 都必須以相同的方式進行簽署， (以及與主要 CSP DLL) 的金鑰相同。</span><span class="sxs-lookup"><span data-stu-id="00286-105">All auxiliary DLLs into which a CSP makes function calls must be signed in the same manner (and with the same key) as the primary CSP DLL.</span></span> <span data-ttu-id="00286-106">若要確保這個簽章，您必須使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 函式，以動態方式載入輔助 dll。</span><span class="sxs-lookup"><span data-stu-id="00286-106">To ensure this signature, the auxiliary DLLs must be loaded dynamically by using the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) function.</span></span> <span data-ttu-id="00286-107">但是在載入 DLL 之前，必須先驗證 DLL 的簽章。</span><span class="sxs-lookup"><span data-stu-id="00286-107">But before the DLL is loaded, the signature of the DLL must be verified.</span></span> <span data-ttu-id="00286-108">CSP 會藉由呼叫 **FuncVerifyImage** 函式來執行這項驗證，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="00286-108">The CSP performs this verification by calling the **FuncVerifyImage** function, as shown in the example below.</span></span>

## <a name="syntax"></a><span data-ttu-id="00286-109">語法</span><span class="sxs-lookup"><span data-stu-id="00286-109">Syntax</span></span>


```C++
typedef BOOL ( WINAPI *CRYPT_VERIFY_IMAGE)(
  _In_       LPCTSTR lpszImage,
  _In_ const BYTE    *pbSigData
);
```



## <a name="parameters"></a><span data-ttu-id="00286-110">參數</span><span class="sxs-lookup"><span data-stu-id="00286-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00286-111">*lpszImage* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00286-111">*lpszImage* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00286-112">以 null 終止之字串的位址，其中包含要驗證簽章之 DLL 的路徑和檔案名。</span><span class="sxs-lookup"><span data-stu-id="00286-112">The address of a null-terminated string that contains the path and file name of the DLL to verify the signature for.</span></span>

</dd> <dt>

<span data-ttu-id="00286-113">*pbSigData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="00286-113">*pbSigData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="00286-114">包含簽章之緩衝區的位址。</span><span class="sxs-lookup"><span data-stu-id="00286-114">The address of a buffer that contains the signature.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00286-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="00286-115">Return value</span></span>

<span data-ttu-id="00286-116">如果函式成功，則傳回 **TRUE** ，否則會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="00286-116">Returns **TRUE** if the function succeeds, **FALSE** if it fails.</span></span>

## <a name="examples"></a><span data-ttu-id="00286-117">範例</span><span class="sxs-lookup"><span data-stu-id="00286-117">Examples</span></span>

<span data-ttu-id="00286-118">下列範例示範如何使用 **FuncVerifyImage** 回呼函式，在 CSP 載入 DLL 之前先驗證其簽章。</span><span class="sxs-lookup"><span data-stu-id="00286-118">The following example shows how to use the **FuncVerifyImage** callback function to verify the signature of a DLL before it is loaded by a CSP.</span></span>


```C++
BOOL (FARPROC *ProvVerifyImage)(LPCSTR lpszImage, BYTE *pSigData);


//  "ProvVerifyImage" has been set to "pVTable->FuncVerifyImage"
//  within the CPAcquireContext function.

//  bSignature is a previously assigned BYTE array that contains the
//  signature that is stored in the C:\Winnt40\System32\signature.sig
//  file. During development, this file is created with the 
//  Sign.exe tool.
...


//  Verify the signature in the
//  C:\Winnt40\System32\Signature.dll file.
if(RCRYPT_FAILED(ProvVerifyImage
    ("c:\\winnt40\\system32\\signature.dll",
        bSignature)) {
    SetLastError(NTE_BAD_SIGNATURE);
    return CRYPT_FAILED;
}

//  Load the DLL with the LoadLibrary function, then acquire pointers 
//  to the functions with the GetProcAddress function.
//...
```



## <a name="requirements"></a><span data-ttu-id="00286-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="00286-119">Requirements</span></span>



| <span data-ttu-id="00286-120">需求</span><span class="sxs-lookup"><span data-stu-id="00286-120">Requirement</span></span> | <span data-ttu-id="00286-121">值</span><span class="sxs-lookup"><span data-stu-id="00286-121">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------|
| <span data-ttu-id="00286-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="00286-122">Minimum supported client</span></span><br/> | <span data-ttu-id="00286-123">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00286-123">Windows XP \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="00286-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="00286-124">Minimum supported server</span></span><br/> | <span data-ttu-id="00286-125">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00286-125">Windows Server 2003 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="00286-126">標頭</span><span class="sxs-lookup"><span data-stu-id="00286-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="00286-127"><dt>Cspdk。h</dt></span><span class="sxs-lookup"><span data-stu-id="00286-127"><dt>Cspdk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="00286-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="00286-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="00286-129">**CPAcquireCoNtext**</span><span class="sxs-lookup"><span data-stu-id="00286-129">**CPAcquireContext**</span></span>](https://www.bing.com/search?q=**CPAcquireContext**)
</dt> <dt>

[<span data-ttu-id="00286-130">**VTableProvStruc**</span><span class="sxs-lookup"><span data-stu-id="00286-130">**VTableProvStruc**</span></span>](vtableprovstruc.md)
</dt> </dl>

 

 
