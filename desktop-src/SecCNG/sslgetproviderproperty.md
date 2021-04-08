---
description: 抓取所指定提供者屬性的值。
ms.assetid: 69235520-acaa-4ec4-9fd6-4b3297e14376
title: 'SslGetProviderProperty 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetProviderProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: ced0f32d45531a1220f7aae9fe0e660648e5d1bd
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103851551"
---
# <a name="sslgetproviderproperty-function"></a><span data-ttu-id="f1337-103">SslGetProviderProperty 函式</span><span class="sxs-lookup"><span data-stu-id="f1337-103">SslGetProviderProperty function</span></span>

<span data-ttu-id="f1337-104">**SslGetProviderProperty** 函式會捕獲指定之提供者屬性的值。</span><span class="sxs-lookup"><span data-stu-id="f1337-104">The **SslGetProviderProperty** function retrieves the value of a specified provider property.</span></span>

## <a name="syntax"></a><span data-ttu-id="f1337-105">語法</span><span class="sxs-lookup"><span data-stu-id="f1337-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGetProviderProperty(
  _In_    NCRYPT_PROV_HANDLE hSslProvider,
  _In_    LPCWSTR            pszProperty,
  _Out_   PBYTE              ppbOutput,
  _Out_   DWORD              *pcbOutput,
  _Inout_ PVOID              *ppEnumState,
  _In_    DWORD              dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="f1337-106">參數</span><span class="sxs-lookup"><span data-stu-id="f1337-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1337-107">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1337-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1337-108">[*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 提供者的控制碼，以取得此屬性。</span><span class="sxs-lookup"><span data-stu-id="f1337-108">The handle of the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider for which to retrieve the property.</span></span>

</dd> <dt>

<span data-ttu-id="f1337-109">*pszProperty* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1337-109">*pszProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1337-110">以 null 終止的 Unicode 字串指標，其中包含要取出的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="f1337-110">A pointer to a null-terminated Unicode string that contains the name of the property to retrieve.</span></span>

</dd> <dt>

<span data-ttu-id="f1337-111">*ppbOutput* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f1337-111">*ppbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1337-112">接收屬性值的緩衝區位址。</span><span class="sxs-lookup"><span data-stu-id="f1337-112">The address of a buffer that receives the property value.</span></span>

<span data-ttu-id="f1337-113">函式的呼叫者必須藉由呼叫 [**SslFreeBuffer**](sslfreebuffer.md) 函式來釋放此緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f1337-113">The caller of the function must free this buffer by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="f1337-114">*pcbOutput* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f1337-114">*pcbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1337-115">*PbOutput* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="f1337-115">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="f1337-116">*ppEnumState* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="f1337-116">*ppEnumState* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="f1337-117">**VOID** 指標的位址，這個位址會接收此函式後續呼叫中所使用的列舉狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="f1337-117">The address of a **VOID** pointer that receives enumeration state information that is used in subsequent calls to this function.</span></span> <span data-ttu-id="f1337-118">這項資訊只對 SSL 提供者有意義，對呼叫端而言是不透明的。</span><span class="sxs-lookup"><span data-stu-id="f1337-118">This information only has meaning to the SSL provider and is opaque to the caller.</span></span> <span data-ttu-id="f1337-119">SSL 提供者會使用這項資訊來判斷列舉中的下一個專案。</span><span class="sxs-lookup"><span data-stu-id="f1337-119">The SSL provider uses this information to determine which item is next in the enumeration.</span></span> <span data-ttu-id="f1337-120">如果這個參數所指向的變數包含 **Null**，則會從頭開始列舉。</span><span class="sxs-lookup"><span data-stu-id="f1337-120">If the variable pointed to by this parameter contains **NULL**, the enumeration is started from the beginning.</span></span>

<span data-ttu-id="f1337-121">函式的呼叫者必須藉由呼叫 [**SslFreeBuffer**](sslfreebuffer.md) 函式來釋放此記憶體。</span><span class="sxs-lookup"><span data-stu-id="f1337-121">The caller of the function must free this memory by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="f1337-122">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="f1337-122">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="f1337-123">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="f1337-123">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1337-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1337-124">Return value</span></span>

<span data-ttu-id="f1337-125">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="f1337-125">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="f1337-126">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="f1337-126">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="f1337-127">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="f1337-127">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="f1337-128">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="f1337-128">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="f1337-129">Description</span><span class="sxs-lookup"><span data-stu-id="f1337-129">Description</span></span>                                                              |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------|
| <dl> <span data-ttu-id="f1337-130">不 <dt>**超過 \_沒有 \_ 記憶體**</dt> <dt>0x8009000EL</dt></span><span class="sxs-lookup"><span data-stu-id="f1337-130"><dt>**NTE\_NO\_MEMORY**</dt> <dt>0x8009000EL</dt></span></span> </dl>         | <span data-ttu-id="f1337-131">可用的記憶體不足，無法配置必要的緩衝區。</span><span class="sxs-lookup"><span data-stu-id="f1337-131">Not enough memory is available to allocate necessary buffers.</span></span><br/> |
| <dl> <span data-ttu-id="f1337-132">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="f1337-132"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="f1337-133">*HSslProvider* 控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="f1337-133">The *hSslProvider* handle is not valid.</span></span><br/>                       |
| <dl> <span data-ttu-id="f1337-134">不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="f1337-134"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="f1337-135">其中一個提供的參數無效。</span><span class="sxs-lookup"><span data-stu-id="f1337-135">One of the supplied parameters is not valid.</span></span><br/>                  |



 

## <a name="requirements"></a><span data-ttu-id="f1337-136">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1337-136">Requirements</span></span>



| <span data-ttu-id="f1337-137">需求</span><span class="sxs-lookup"><span data-stu-id="f1337-137">Requirement</span></span> | <span data-ttu-id="f1337-138">值</span><span class="sxs-lookup"><span data-stu-id="f1337-138">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="f1337-139">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1337-139">Minimum supported client</span></span><br/> | <span data-ttu-id="f1337-140">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1337-140">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="f1337-141">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1337-141">Minimum supported server</span></span><br/> | <span data-ttu-id="f1337-142">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1337-142">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="f1337-143">標頭</span><span class="sxs-lookup"><span data-stu-id="f1337-143">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1337-144"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="f1337-144"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="f1337-145">DLL</span><span class="sxs-lookup"><span data-stu-id="f1337-145">DLL</span></span><br/>                      | <dl> <span data-ttu-id="f1337-146"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="f1337-146"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

