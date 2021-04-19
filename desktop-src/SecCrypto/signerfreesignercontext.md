---
description: 釋放先前呼叫 SignerSignEx 函式所配置的簽署者 \_ 內容結構。
ms.assetid: 190de302-50fe-488e-90ed-c9efd39dae70
title: SignerFreeSignerCoNtext 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignerFreeSignerContext
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 284b1cbf5755da06e9454b86ac9eacef5fbf613f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980386"
---
# <a name="signerfreesignercontext-function"></a><span data-ttu-id="4bb98-103">SignerFreeSignerCoNtext 函式</span><span class="sxs-lookup"><span data-stu-id="4bb98-103">SignerFreeSignerContext function</span></span>

<span data-ttu-id="4bb98-104">**SignerFreeSignerCoNtext** 函式會釋放先前呼叫 [**SignerSignEx**](signersignex.md)函數所配置的 [**簽署者 \_ 內容**](signer-context.md)結構。</span><span class="sxs-lookup"><span data-stu-id="4bb98-104">The **SignerFreeSignerContext** function frees a [**SIGNER\_CONTEXT**](signer-context.md) structure allocated by a previous call to the [**SignerSignEx**](signersignex.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="4bb98-105">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="4bb98-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="4bb98-106">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。</span><span class="sxs-lookup"><span data-stu-id="4bb98-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="4bb98-107">語法</span><span class="sxs-lookup"><span data-stu-id="4bb98-107">Syntax</span></span>


```C++
HRESULT WINAPI SignerFreeSignerContext(
  _In_ SIGNER_CONTEXT *pSignerContext
);
```



## <a name="parameters"></a><span data-ttu-id="4bb98-108">參數</span><span class="sxs-lookup"><span data-stu-id="4bb98-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4bb98-109">*pSignerCoNtext* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4bb98-109">*pSignerContext* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4bb98-110">要釋放之 [**簽署者 \_ 內容**](signer-context.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="4bb98-110">A pointer to the [**SIGNER\_CONTEXT**](signer-context.md) structure to free.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4bb98-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="4bb98-111">Return value</span></span>

<span data-ttu-id="4bb98-112">如果函式成功，函數會傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="4bb98-112">If the function succeeds, the function returns S\_OK.</span></span>

<span data-ttu-id="4bb98-113">如果函式失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="4bb98-113">If the function fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="4bb98-114">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="4bb98-114">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="4bb98-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="4bb98-115">Requirements</span></span>



| <span data-ttu-id="4bb98-116">需求</span><span class="sxs-lookup"><span data-stu-id="4bb98-116">Requirement</span></span> | <span data-ttu-id="4bb98-117">值</span><span class="sxs-lookup"><span data-stu-id="4bb98-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="4bb98-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4bb98-118">Minimum supported client</span></span><br/> | <span data-ttu-id="4bb98-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4bb98-119">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="4bb98-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4bb98-120">Minimum supported server</span></span><br/> | <span data-ttu-id="4bb98-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4bb98-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="4bb98-122">DLL</span><span class="sxs-lookup"><span data-stu-id="4bb98-122">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4bb98-123"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4bb98-123"><dt>Mssign32.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="4bb98-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4bb98-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4bb98-125">**簽署者 \_ 內容**</span><span class="sxs-lookup"><span data-stu-id="4bb98-125">**SIGNER\_CONTEXT**</span></span>](signer-context.md)
</dt> <dt>

[<span data-ttu-id="4bb98-126">**SignerSignEx**</span><span class="sxs-lookup"><span data-stu-id="4bb98-126">**SignerSignEx**</span></span>](signersignex.md)
</dt> </dl>

 

 
