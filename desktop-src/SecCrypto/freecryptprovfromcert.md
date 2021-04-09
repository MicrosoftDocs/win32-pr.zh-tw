---
description: 將密碼編譯服務提供者的控制碼釋放 (CSP) ，並選擇性地刪除 GetCryptProvFromCert 函式所建立的暫存容器。
ms.assetid: 4462eef2-7056-4e48-aa96-c46f29b701d6
title: FreeCryptProvFromCert 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCert
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 8201de475a4224aea58267405ccde244e56d59f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851307"
---
# <a name="freecryptprovfromcert-function"></a><span data-ttu-id="316cc-103">FreeCryptProvFromCert 函式</span><span class="sxs-lookup"><span data-stu-id="316cc-103">FreeCryptProvFromCert function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="316cc-104">此 API 即將淘汰。</span><span class="sxs-lookup"><span data-stu-id="316cc-104">This API is deprecated.</span></span> <span data-ttu-id="316cc-105">Microsoft 可能會在未來的版本中移除此 API。</span><span class="sxs-lookup"><span data-stu-id="316cc-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="316cc-106">**FreeCryptProvFromCert** 函式會將 [*密碼編譯服務提供者*](../secgloss/c-gly.md) () 的控制碼釋出，並選擇性地刪除 [**GetCryptProvFromCert**](getcryptprovfromcert.md)函數所建立的暫存容器。</span><span class="sxs-lookup"><span data-stu-id="316cc-106">The **FreeCryptProvFromCert** function releases the handle to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and optionally deletes the temporary container created by the [**GetCryptProvFromCert**](getcryptprovfromcert.md) function.</span></span>

> [!Note]  
> <span data-ttu-id="316cc-107">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="316cc-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="316cc-108">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。</span><span class="sxs-lookup"><span data-stu-id="316cc-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="316cc-109">語法</span><span class="sxs-lookup"><span data-stu-id="316cc-109">Syntax</span></span>


```C++
void WINAPI FreeCryptProvFromCert(
  _In_     BOOL       fAcquired,
  _In_     HCRYPTPROV hProv,
  _In_opt_ LPWSTR     pwszCapiProvider,
  _In_     DWORD      dwProviderType,
  _In_opt_ LPWSTR     pwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="316cc-110">參數</span><span class="sxs-lookup"><span data-stu-id="316cc-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="316cc-111">*fAcquired* \[在\]</span><span class="sxs-lookup"><span data-stu-id="316cc-111">*fAcquired* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="316cc-112">值，指定是否從 [*憑證*](../secgloss/c-gly.md)取得提供者控制碼。</span><span class="sxs-lookup"><span data-stu-id="316cc-112">A value that specifies whether the provider handle was acquired from the [*certificate*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="316cc-113">*hProv* \[在\]</span><span class="sxs-lookup"><span data-stu-id="316cc-113">*hProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="316cc-114">CSP [**HCRYPTPROV**](hcryptprov.md) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="316cc-114">A pointer to an [**HCRYPTPROV**](hcryptprov.md) structure for the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="316cc-115">*pwszCapiProvider* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="316cc-115">*pwszCapiProvider* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="316cc-116">提供者名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="316cc-116">A pointer to a null-terminated string for the provider name.</span></span>

</dd> <dt>

<span data-ttu-id="316cc-117">*dwProviderType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="316cc-117">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="316cc-118">指定 CSP 類型。</span><span class="sxs-lookup"><span data-stu-id="316cc-118">Specifies the CSP type.</span></span> <span data-ttu-id="316cc-119">這可以是零或其中一個 [密碼編譯提供者類型](cryptographic-provider-types.md)。</span><span class="sxs-lookup"><span data-stu-id="316cc-119">This can be zero or one of the [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span> <span data-ttu-id="316cc-120">如果這個成員是零，金鑰容器就是其中一個 CNG 金鑰儲存提供者。</span><span class="sxs-lookup"><span data-stu-id="316cc-120">If this member is zero, the key container is one of the CNG key storage providers.</span></span>

</dd> <dt>

<span data-ttu-id="316cc-121">*pwszTmpContainer* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="316cc-121">*pwszTmpContainer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="316cc-122">暫時金鑰容器名稱的以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="316cc-122">A pointer to a null-terminated string for the name of the temporary key container.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="316cc-123">傳回值</span><span class="sxs-lookup"><span data-stu-id="316cc-123">Return value</span></span>

<span data-ttu-id="316cc-124">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="316cc-124">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="316cc-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="316cc-125">Requirements</span></span>



| <span data-ttu-id="316cc-126">需求</span><span class="sxs-lookup"><span data-stu-id="316cc-126">Requirement</span></span> | <span data-ttu-id="316cc-127">值</span><span class="sxs-lookup"><span data-stu-id="316cc-127">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="316cc-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="316cc-128">Minimum supported client</span></span><br/> | <span data-ttu-id="316cc-129">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="316cc-129">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="316cc-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="316cc-130">Minimum supported server</span></span><br/> | <span data-ttu-id="316cc-131">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="316cc-131">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="316cc-132">DLL</span><span class="sxs-lookup"><span data-stu-id="316cc-132">DLL</span></span><br/>                      | <dl> <span data-ttu-id="316cc-133"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="316cc-133"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
