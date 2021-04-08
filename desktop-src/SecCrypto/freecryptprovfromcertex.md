---
description: 將控制碼釋放給密碼編譯服務提供者 (CSP) 或密碼編譯 API：新一代 (CNG) 金鑰。
ms.assetid: 76cbf8ae-c4ab-43d9-b06d-ea0b2a66368a
title: FreeCryptProvFromCertEx 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- FreeCryptProvFromCertEx
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1be6270ebf9320a9c7527736b9fc4894cd50de9a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851304"
---
# <a name="freecryptprovfromcertex-function"></a><span data-ttu-id="18987-103">FreeCryptProvFromCertEx 函式</span><span class="sxs-lookup"><span data-stu-id="18987-103">FreeCryptProvFromCertEx function</span></span>

<span data-ttu-id="18987-104">**FreeCryptProvFromCertEx** 函式會將控制碼釋放給 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 或密碼編譯 API：新一代 (CNG) 金鑰。</span><span class="sxs-lookup"><span data-stu-id="18987-104">The **FreeCryptProvFromCertEx** function releases the handle either to a [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) or to a Cryptography API: Next Generation (CNG) key.</span></span>

> [!Note]  
> <span data-ttu-id="18987-105">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="18987-105">This function has no associated header file or import library.</span></span> <span data-ttu-id="18987-106">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。</span><span class="sxs-lookup"><span data-stu-id="18987-106">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="18987-107">語法</span><span class="sxs-lookup"><span data-stu-id="18987-107">Syntax</span></span>


```C++
void WINAPI FreeCryptProvFromCertEx(
  _In_     BOOL                            fAcquired,
  _In_     HCRYPTPROV_OR_NCRYPT_KEY_HANDLE hProv,
           DWORD                           dwKeySpec,
  _In_opt_ LPWSTR                          pwszCapiProvider,
  _In_     DWORD                           dwProviderType,
  _In_opt_ LPWSTR                          pwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="18987-108">參數</span><span class="sxs-lookup"><span data-stu-id="18987-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="18987-109">*fAcquired* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18987-109">*fAcquired* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18987-110">值，指定是否從 [*憑證*](../secgloss/c-gly.md)取得提供者控制碼。</span><span class="sxs-lookup"><span data-stu-id="18987-110">A value that specifies whether the provider handle was acquired from the [*certificate*](../secgloss/c-gly.md).</span></span>

</dd> <dt>

<span data-ttu-id="18987-111">*hProv* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18987-111">*hProv* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18987-112">CAPICOM CSP 的控制碼或 CNG 金鑰的控制碼。</span><span class="sxs-lookup"><span data-stu-id="18987-112">A handle to a CAPICOM CSP or a handle to a CNG key.</span></span>

</dd> <dt>

<span data-ttu-id="18987-113">*dwKeySpec*</span><span class="sxs-lookup"><span data-stu-id="18987-113">*dwKeySpec*</span></span> 
</dt> <dd>

<span data-ttu-id="18987-114">接收有關金鑰之其他資訊的 **DWORD** 變數位址。</span><span class="sxs-lookup"><span data-stu-id="18987-114">The address of a **DWORD** variable that receives additional information about the key.</span></span> <span data-ttu-id="18987-115">這可以是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="18987-115">This can be one of the following values.</span></span>



| <span data-ttu-id="18987-116">值</span><span class="sxs-lookup"><span data-stu-id="18987-116">Value</span></span>                                                                                                                                                                                | <span data-ttu-id="18987-117">意義</span><span class="sxs-lookup"><span data-stu-id="18987-117">Meaning</span></span>                                                                                                          |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------|
| <span id="AT_KEYEXCHANGE"></span><span id="at_keyexchange"></span><dl> <span data-ttu-id="18987-118"><dt>**在 \_ KEYEXCHANGE**</dt></span><span class="sxs-lookup"><span data-stu-id="18987-118"><dt>**AT\_KEYEXCHANGE**</dt></span></span> </dl>                     | <span data-ttu-id="18987-119">金鑰組是一組金鑰交換。</span><span class="sxs-lookup"><span data-stu-id="18987-119">The key pair is a key exchange pair.</span></span><br/>                                                                  |
| <span id="AT_SIGNATURE"></span><span id="at_signature"></span><dl> <span data-ttu-id="18987-120"><dt>**AT \_ SIGNATURE**</dt></span><span class="sxs-lookup"><span data-stu-id="18987-120"><dt>**AT\_SIGNATURE**</dt></span></span> </dl>                           | <span data-ttu-id="18987-121">金鑰組是一組簽章組。</span><span class="sxs-lookup"><span data-stu-id="18987-121">The key pair is a signature pair.</span></span><br/>                                                                     |
| <span id="CERT_NCRYPT_KEY_SPEC"></span><span id="cert_ncrypt_key_spec"></span><dl> <span data-ttu-id="18987-122"><dt>**CERT \_ NCRYPT \_ 金鑰 \_ 規格**</dt></span><span class="sxs-lookup"><span data-stu-id="18987-122"><dt>**CERT\_NCRYPT\_KEY\_SPEC**</dt></span></span> </dl> | <span data-ttu-id="18987-123">金鑰是 CNG 金鑰。</span><span class="sxs-lookup"><span data-stu-id="18987-123">The key is a CNG key.</span></span><br/> <span data-ttu-id="18987-124">**Windows Server 2003 和 WINDOWS XP：** 不支援這個值。</span><span class="sxs-lookup"><span data-stu-id="18987-124">**Windows Server 2003 and Windows XP:** This value is not supported.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="18987-125">*pwszCapiProvider* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="18987-125">*pwszCapiProvider* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="18987-126">提供者名稱之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="18987-126">A pointer to a null-terminated string for the provider name.</span></span>

</dd> <dt>

<span data-ttu-id="18987-127">*dwProviderType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="18987-127">*dwProviderType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="18987-128">指定 CSP 類型。</span><span class="sxs-lookup"><span data-stu-id="18987-128">Specifies the CSP type.</span></span> <span data-ttu-id="18987-129">這可以是零或其中一個 [密碼編譯提供者類型](cryptographic-provider-types.md)。</span><span class="sxs-lookup"><span data-stu-id="18987-129">This can be zero or one of the [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span> <span data-ttu-id="18987-130">如果這個成員是零，金鑰容器就是其中一個 CNG 金鑰儲存提供者。</span><span class="sxs-lookup"><span data-stu-id="18987-130">If this member is zero, the key container is one of the CNG key storage providers.</span></span>

</dd> <dt>

<span data-ttu-id="18987-131">*pwszTmpContainer* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="18987-131">*pwszTmpContainer* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="18987-132">暫時金鑰容器名稱的以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="18987-132">A pointer to a null-terminated string for the name of the temporary key container.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="18987-133">傳回值</span><span class="sxs-lookup"><span data-stu-id="18987-133">Return value</span></span>

<span data-ttu-id="18987-134">此函式不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="18987-134">This function does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="18987-135">規格需求</span><span class="sxs-lookup"><span data-stu-id="18987-135">Requirements</span></span>



| <span data-ttu-id="18987-136">需求</span><span class="sxs-lookup"><span data-stu-id="18987-136">Requirement</span></span> | <span data-ttu-id="18987-137">值</span><span class="sxs-lookup"><span data-stu-id="18987-137">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="18987-138">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="18987-138">Minimum supported client</span></span><br/> | <span data-ttu-id="18987-139">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18987-139">Windows 7 \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="18987-140">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="18987-140">Minimum supported server</span></span><br/> | <span data-ttu-id="18987-141">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="18987-141">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="18987-142">DLL</span><span class="sxs-lookup"><span data-stu-id="18987-142">DLL</span></span><br/>                      | <dl> <span data-ttu-id="18987-143"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="18987-143"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
