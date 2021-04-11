---
description: 呼叫 GetLastError 函數，並將傳回碼轉換成 HRESULT。
ms.assetid: 7b8eab85-212b-44bc-9d1b-60587652380d
title: SignError 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SignError
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 7a405bef4666721e485e8b5ad6905209b2244bef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026281"
---
# <a name="signerror-function"></a><span data-ttu-id="51c08-103">SignError 函式</span><span class="sxs-lookup"><span data-stu-id="51c08-103">SignError function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="51c08-104">此 API 即將淘汰。</span><span class="sxs-lookup"><span data-stu-id="51c08-104">This API is deprecated.</span></span> <span data-ttu-id="51c08-105">Microsoft 可能會在未來的版本中移除此 API。</span><span class="sxs-lookup"><span data-stu-id="51c08-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="51c08-106">**SignError** 函式會呼叫 [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror)函數，並將傳回碼轉換成 **HRESULT**。</span><span class="sxs-lookup"><span data-stu-id="51c08-106">The **SignError** function calls the [**GetLastError**](/windows/win32/api/errhandlingapi/nf-errhandlingapi-getlasterror) function and converts the return code to an **HRESULT**.</span></span>

> [!Note]  
> <span data-ttu-id="51c08-107">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="51c08-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="51c08-108">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。</span><span class="sxs-lookup"><span data-stu-id="51c08-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="51c08-109">語法</span><span class="sxs-lookup"><span data-stu-id="51c08-109">Syntax</span></span>


```C++
HRESULT WINAPI SignError(void);
```



## <a name="parameters"></a><span data-ttu-id="51c08-110">參數</span><span class="sxs-lookup"><span data-stu-id="51c08-110">Parameters</span></span>

<span data-ttu-id="51c08-111">此函式沒有參數。</span><span class="sxs-lookup"><span data-stu-id="51c08-111">This function has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="51c08-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="51c08-112">Return value</span></span>

<span data-ttu-id="51c08-113">如果方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="51c08-113">If the method succeeds, it returns **S\_OK**.</span></span>

<span data-ttu-id="51c08-114">如果方法失敗，則會傳回表示錯誤的 **HRESULT** 值。</span><span class="sxs-lookup"><span data-stu-id="51c08-114">If the method fails, it returns an **HRESULT** value that indicates the error.</span></span> <span data-ttu-id="51c08-115">如需常見錯誤碼的清單，請參閱 [常見的 HRESULT 值](common-hresult-values.md)。</span><span class="sxs-lookup"><span data-stu-id="51c08-115">For a list of common error codes, see [Common HRESULT Values](common-hresult-values.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="51c08-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="51c08-116">Requirements</span></span>



| <span data-ttu-id="51c08-117">需求</span><span class="sxs-lookup"><span data-stu-id="51c08-117">Requirement</span></span> | <span data-ttu-id="51c08-118">值</span><span class="sxs-lookup"><span data-stu-id="51c08-118">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="51c08-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="51c08-119">Minimum supported client</span></span><br/> | <span data-ttu-id="51c08-120">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51c08-120">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="51c08-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="51c08-121">Minimum supported server</span></span><br/> | <span data-ttu-id="51c08-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="51c08-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="51c08-123">DLL</span><span class="sxs-lookup"><span data-stu-id="51c08-123">DLL</span></span><br/>                      | <dl> <span data-ttu-id="51c08-124"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="51c08-124"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
