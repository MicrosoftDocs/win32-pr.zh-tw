---
description: 在密碼編譯服務提供者 (CSP) 中建立暫存容器，並將私密金鑰從記憶體載入至容器。
ms.assetid: 9388b49b-fad4-4499-a391-fe58ed672552
title: PvkPrivateKeyAcquireCoNtextFromMemory 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- PvkPrivateKeyAcquireContextFromMemory
api_type:
- DllExport
api_location:
- Mssign32.dll
ms.openlocfilehash: 1552d1e35845ffb7407d11d6e520b914ab805d50
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320371"
---
# <a name="pvkprivatekeyacquirecontextfrommemory-function"></a><span data-ttu-id="d3577-103">PvkPrivateKeyAcquireCoNtextFromMemory 函式</span><span class="sxs-lookup"><span data-stu-id="d3577-103">PvkPrivateKeyAcquireContextFromMemory function</span></span>

> [!IMPORTANT]
> <span data-ttu-id="d3577-104">此 API 即將淘汰。</span><span class="sxs-lookup"><span data-stu-id="d3577-104">This API is deprecated.</span></span> <span data-ttu-id="d3577-105">Microsoft 可能會在未來的版本中移除此 API。</span><span class="sxs-lookup"><span data-stu-id="d3577-105">Microsoft may remove this API in future releases.</span></span>

 

<span data-ttu-id="d3577-106">**PvkPrivateKeyAcquireCoNtextFromMemory** 函式會在 [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 中建立暫存容器，並將 [*私密金鑰*](../secgloss/p-gly.md)從記憶體載入至容器。</span><span class="sxs-lookup"><span data-stu-id="d3577-106">The **PvkPrivateKeyAcquireContextFromMemory** function creates a temporary container in the [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) and loads a [*private key*](../secgloss/p-gly.md) from memory into the container.</span></span>

> [!Note]  
> <span data-ttu-id="d3577-107">此函數沒有相關聯的標頭檔或匯入程式庫。</span><span class="sxs-lookup"><span data-stu-id="d3577-107">This function has no associated header file or import library.</span></span> <span data-ttu-id="d3577-108">若要呼叫這個函式，您必須建立使用者定義的標頭檔，並使用 [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) 和 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 函數動態連結至 Mssign32.dll。</span><span class="sxs-lookup"><span data-stu-id="d3577-108">To call this function, you must create a user-defined header file and use the [**LoadLibrary**](/windows/win32/api/libloaderapi/nf-libloaderapi-loadlibrarya) and [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) functions to dynamically link to Mssign32.dll.</span></span>

 

## <a name="syntax"></a><span data-ttu-id="d3577-109">語法</span><span class="sxs-lookup"><span data-stu-id="d3577-109">Syntax</span></span>


```C++
BOOL WINAPI PvkPrivateKeyAcquireContextFromMemory(
  _In_        LPCWSTR    pwszProvName,
  _In_        DWORD      dwProvType,
  _In_        BYTE       *pbData,
  _In_        DWORD      cbData,
  _In_        HWND       hwndOwner,
  _In_        LPCWSTR    pwszKeyName,
  _Inout_opt_ DWORD      *pdwKeySpec,
  _Out_       HCRYPTPROV *phCryptProv,
  _Out_       LPTSTR     *ppwszTmpContainer
);
```



## <a name="parameters"></a><span data-ttu-id="d3577-110">參數</span><span class="sxs-lookup"><span data-stu-id="d3577-110">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d3577-111">*pwszProvName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3577-111">*pwszProvName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3577-112">以 null 結束的字串指標，其中包含在 *dwProvType* 中要求其類型的 CSP 名稱。</span><span class="sxs-lookup"><span data-stu-id="d3577-112">A pointer to a null-terminated string that contains the name of the CSP whose type is requested in *dwProvType*.</span></span>

</dd> <dt>

<span data-ttu-id="d3577-113">*dwProvType* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3577-113">*dwProvType* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3577-114">CSP 類型的 **DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="d3577-114">A **DWORD** value for the CSP type.</span></span> <span data-ttu-id="d3577-115">如需 CSP 類型的詳細資訊，請參閱 [密碼編譯提供者類型](cryptographic-provider-types.md)。</span><span class="sxs-lookup"><span data-stu-id="d3577-115">For more information about CSP types, see [Cryptographic Provider Types](cryptographic-provider-types.md).</span></span>

</dd> <dt>

<span data-ttu-id="d3577-116">*>pbdata* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3577-116">*pbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3577-117">接收內容資料之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="d3577-117">A pointer to a buffer to receive the context data.</span></span> <span data-ttu-id="d3577-118">呼叫端必須提供此資源。</span><span class="sxs-lookup"><span data-stu-id="d3577-118">The caller must provide this resource.</span></span>

</dd> <dt>

<span data-ttu-id="d3577-119">*cbData* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3577-119">*cbData* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3577-120">**DWORD** 值，指定 *>pbdata* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d3577-120">A **DWORD** value that specifies the size, in bytes, of the *pbData* buffer.</span></span> <span data-ttu-id="d3577-121">呼叫端必須提供此值。</span><span class="sxs-lookup"><span data-stu-id="d3577-121">The caller must provide this value.</span></span>

</dd> <dt>

<span data-ttu-id="d3577-122">*hwndOwner* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3577-122">*hwndOwner* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3577-123">如果需要密碼來解密 *>pbdata* 參數所指向的內容資料，這個參數就是對話方塊父系的控制碼;否則，它會是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="d3577-123">If a password is required to decrypt the context data pointed to by the *pbData* parameter, this parameter is a handle to the parent of the dialog box; otherwise, it is **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="d3577-124">*pwszKeyName* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d3577-124">*pwszKeyName* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d3577-125">以 null 結束的字串指標，其中包含要取出的索引鍵名稱。</span><span class="sxs-lookup"><span data-stu-id="d3577-125">A pointer to a null-terminated string that contains the name of the key to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="d3577-126">*pdwKeySpec* \[in、out、optional\]</span><span class="sxs-lookup"><span data-stu-id="d3577-126">*pdwKeySpec* \[in, out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="d3577-127">**DWORD** 值的指標，指定索引鍵的類型。</span><span class="sxs-lookup"><span data-stu-id="d3577-127">A pointer to a **DWORD** value that specifies the type of key.</span></span> <span data-ttu-id="d3577-128">可能的值包括 **在 \_ KEYEXCHANGE** **或簽 \_** 章。</span><span class="sxs-lookup"><span data-stu-id="d3577-128">Possible values include **AT\_KEYEXCHANGE** or **AT\_SIGNATURE**.</span></span>

</dd> <dt>

<span data-ttu-id="d3577-129">*phCryptProv* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d3577-129">*phCryptProv* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3577-130">CSP 的控制碼指標。</span><span class="sxs-lookup"><span data-stu-id="d3577-130">A pointer to a handle for the CSP.</span></span>

</dd> <dt>

<span data-ttu-id="d3577-131">*ppwszTmpContainer* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d3577-131">*ppwszTmpContainer* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d3577-132">暫存容器名稱之以 null 結束的字串指標的位址。</span><span class="sxs-lookup"><span data-stu-id="d3577-132">The address of a pointer to a null-terminated string for the temporary container name.</span></span> <span data-ttu-id="d3577-133">**PvkPrivateKeyAcquireCoNtextFromMemory** 函式會提供這個字串的緩衝區，並將其初始化。</span><span class="sxs-lookup"><span data-stu-id="d3577-133">The **PvkPrivateKeyAcquireContextFromMemory** function provides the buffer for this string and initializes it.</span></span> <span data-ttu-id="d3577-134">呼叫 **PvkPrivateKeyAcquireCoNtextFromMemory** 時，位址應該指向 **Null** 值。</span><span class="sxs-lookup"><span data-stu-id="d3577-134">When calling **PvkPrivateKeyAcquireContextFromMemory**, the address should point to a **NULL** value.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d3577-135">傳回值</span><span class="sxs-lookup"><span data-stu-id="d3577-135">Return value</span></span>

<span data-ttu-id="d3577-136">成功時，此函數會傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="d3577-136">Upon success, this function returns **TRUE**.</span></span> <span data-ttu-id="d3577-137">如果失敗， **PvkPrivateKeyAcquireCoNtextFromMemory** 函數會傳回 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="d3577-137">The **PvkPrivateKeyAcquireContextFromMemory** function returns **FALSE** if it fails.</span></span>

## <a name="requirements"></a><span data-ttu-id="d3577-138">規格需求</span><span class="sxs-lookup"><span data-stu-id="d3577-138">Requirements</span></span>



| <span data-ttu-id="d3577-139">需求</span><span class="sxs-lookup"><span data-stu-id="d3577-139">Requirement</span></span> | <span data-ttu-id="d3577-140">值</span><span class="sxs-lookup"><span data-stu-id="d3577-140">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="d3577-141">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d3577-141">Minimum supported client</span></span><br/> | <span data-ttu-id="d3577-142">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3577-142">Windows XP \[desktop apps only\]</span></span><br/>                                             |
| <span data-ttu-id="d3577-143">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d3577-143">Minimum supported server</span></span><br/> | <span data-ttu-id="d3577-144">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d3577-144">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                    |
| <span data-ttu-id="d3577-145">DLL</span><span class="sxs-lookup"><span data-stu-id="d3577-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d3577-146"><dt>Mssign32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d3577-146"><dt>Mssign32.dll</dt></span></span> </dl> |



 

 
