---
description: 將密碼編譯服務提供者的控制碼釋放 (CSP) ，並選擇性地刪除 PvkGetCryptProv 函式所建立的暫存容器。
ms.assetid: e7dcb5c5-dd80-4810-bf1f-4b7b921fa22c
title: PvkFreeCryptProv 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkFreeCryptProv
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 70ff29c968fe8f50c813f1da71b2e73a112f25f1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106975895"
---
# <a name="pvkfreecryptprov-function"></a><span data-ttu-id="ab132-103">PvkFreeCryptProv 函式</span><span class="sxs-lookup"><span data-stu-id="ab132-103">PvkFreeCryptProv function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ab132-104">此 API 即將淘汰。</span><span class="sxs-lookup"><span data-stu-id="ab132-104">This API is deprecated.</span></span> <span data-ttu-id="ab132-105">Microsoft 可能會在未來的版本中移除此 API。</span><span class="sxs-lookup"><span data-stu-id="ab132-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="ab132-106">**PvkFreeCryptProv** 函式會將 [*密碼編譯服務提供者*](../secgloss/c-gly.md) () 的控制碼釋出，並選擇性地刪除 [**PvkGetCryptProv**](pvkgetcryptprov.md)函數所建立的暫存容器。</span><span class="sxs-lookup"><span data-stu-id="ab132-106">The **PvkFreeCryptProv** function releases the handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and optionally deletes the temporary container created by the [**PvkGetCryptProv**](pvkgetcryptprov.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="ab132-107">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="ab132-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="ab132-108">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。</span><span class="sxs-lookup"><span data-stu-id="ab132-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="ab132-109">語法</span><span class="sxs-lookup"><span data-stu-id="ab132-109">Syntax</span></span>


```C++
void WINAPI PvkFreeCryptProv(
  _In_     HCRYPTPROV hProv,
  _In_     LPCWSTR    pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="ab132-110">參數</span><span class="sxs-lookup"><span data-stu-id="ab132-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab132-111">*hProv* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ab132-111">*hProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab132-112">CSP 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="ab132-112">A handle to the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="ab132-113">*pwszCapiProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ab132-113">*pwszCapiProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab132-114">CSP 名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="ab132-114">A pointer to a null-terminated string for the CSP name.</span></span>

</dd> <dt>

<span data-ttu-id="ab132-115">*dwProviderType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ab132-115">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ab132-116">代表密碼編譯提供者類型的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="ab132-116">A **DWORD** value that represents the cryptographic provider type.</span></span> <span data-ttu-id="ab132-117">如需詳細資訊，請參閱 [密碼編譯提供者類型](cryptographic-provider-types.md)。</span><span class="sxs-lookup"><span data-stu-id="ab132-117">For more information, see [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="ab132-118">*pwszTmpContainer* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="ab132-118">*pwszTmpContainer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="ab132-119">暫存金鑰容器名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="ab132-119">A pointer to a null-terminated string for the temporary key container name.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab132-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="ab132-120">Return value</span></span>

<span data-ttu-id="ab132-121">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="ab132-121">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab132-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab132-122">Requirements</span></span>



| <span data-ttu-id="ab132-123">需求</span><span class="sxs-lookup"><span data-stu-id="ab132-123">Requirement</span></span> | <span data-ttu-id="ab132-124">值</span><span class="sxs-lookup"><span data-stu-id="ab132-124">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="ab132-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab132-125">Minimum supported client</span></span><br/> | <span data-ttu-id="ab132-126">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab132-126">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="ab132-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab132-127">Minimum supported server</span></span><br/> | <span data-ttu-id="ab132-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab132-128">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="ab132-129">DLL</span><span class="sxs-lookup"><span data-stu-id="ab132-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ab132-130"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ab132-130"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
