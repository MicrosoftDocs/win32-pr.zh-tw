---
description: 抓取安全通訊端層通訊協定 (SSL) 提供者金鑰組象的命名屬性值。
ms.assetid: 01a7e82a-3888-4f96-85a2-e07811f1895e
title: 'SslGetKeyProperty 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslGetKeyProperty
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 42952b76bfb46eeeb31b9f76b1f677e7b3b8e3e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990400"
---
# <a name="sslgetkeyproperty-function"></a><span data-ttu-id="d61bb-103">SslGetKeyProperty 函式</span><span class="sxs-lookup"><span data-stu-id="d61bb-103">SslGetKeyProperty function</span></span>

<span data-ttu-id="d61bb-104">**SslGetKeyProperty** 函式會 (SSL) 提供者金鑰組象，抓取 [*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly)的命名屬性值。</span><span class="sxs-lookup"><span data-stu-id="d61bb-104">The **SslGetKeyProperty** function retrieves the value of a named property for a [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider key object.</span></span>

## <a name="syntax"></a><span data-ttu-id="d61bb-105">語法</span><span class="sxs-lookup"><span data-stu-id="d61bb-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslGetKeyProperty(
  _In_  NCRYPT_KEY_HANDLE hKey,
  _In_  LPCWSTR           pszProperty,
  _Out_ PBYTE             ppbOutput,
  _Out_ DWORD             *pcbOutput,
  _In_  DWORD             dwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="d61bb-106">參數</span><span class="sxs-lookup"><span data-stu-id="d61bb-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d61bb-107">*hKey* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d61bb-107">*hKey* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d61bb-108">SSL 提供者的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d61bb-108">The handle of the SSL provider.</span></span>

</dd> <dt>

<span data-ttu-id="d61bb-109">*pszProperty* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d61bb-109">*pszProperty* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d61bb-110">以 null 終止的 Unicode 字串指標，其中包含要取出的屬性名稱。</span><span class="sxs-lookup"><span data-stu-id="d61bb-110">A pointer to a null-terminated Unicode string that contains the name of the property to retrieve.</span></span> <span data-ttu-id="d61bb-111">這可以是其中一個預先定義的 [**金鑰存放區屬性識別碼**](key-storage-property-identifiers.md) 或自訂屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="d61bb-111">This can be one of the predefined [**Key Storage Property Identifiers**](key-storage-property-identifiers.md) or a custom property identifier.</span></span>

</dd> <dt>

<span data-ttu-id="d61bb-112">*ppbOutput* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d61bb-112">*ppbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d61bb-113">接收屬性值之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="d61bb-113">A pointer to a buffer that receives the property value.</span></span> <span data-ttu-id="d61bb-114">函式的呼叫者必須藉由呼叫 [**SslFreeBuffer**](sslfreebuffer.md) 函式來釋放此緩衝區。</span><span class="sxs-lookup"><span data-stu-id="d61bb-114">The caller of the function must free this buffer by calling the [**SslFreeBuffer**](sslfreebuffer.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="d61bb-115">*pcbOutput* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d61bb-115">*pcbOutput* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d61bb-116">*PbOutput* 緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="d61bb-116">The size, in bytes, of the *pbOutput* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="d61bb-117">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d61bb-117">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d61bb-118">這個參數保留給未來使用。</span><span class="sxs-lookup"><span data-stu-id="d61bb-118">This parameter is reserved for future use.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d61bb-119">傳回值</span><span class="sxs-lookup"><span data-stu-id="d61bb-119">Return value</span></span>

<span data-ttu-id="d61bb-120">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="d61bb-120">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="d61bb-121">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="d61bb-121">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="d61bb-122">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="d61bb-122">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="d61bb-123">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="d61bb-123">Return code/value</span></span>                                                                                                                                                       | <span data-ttu-id="d61bb-124">Description</span><span class="sxs-lookup"><span data-stu-id="d61bb-124">Description</span></span>                                             |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------|
| <dl> <span data-ttu-id="d61bb-125">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="d61bb-125"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl>    | <span data-ttu-id="d61bb-126">其中一個提供的控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="d61bb-126">One of the provided handles is not valid.</span></span><br/>    |
| <dl> <span data-ttu-id="d61bb-127">不 <dt>**超過 \_不正確 \_ 參數**</dt> <dt>0x80090027L</dt></span><span class="sxs-lookup"><span data-stu-id="d61bb-127"><dt>**NTE\_INVALID\_PARAMETER**</dt> <dt>0x80090027L</dt></span></span> </dl> | <span data-ttu-id="d61bb-128">其中一個提供的參數無效。</span><span class="sxs-lookup"><span data-stu-id="d61bb-128">One of the supplied parameters is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="d61bb-129">規格需求</span><span class="sxs-lookup"><span data-stu-id="d61bb-129">Requirements</span></span>



| <span data-ttu-id="d61bb-130">需求</span><span class="sxs-lookup"><span data-stu-id="d61bb-130">Requirement</span></span> | <span data-ttu-id="d61bb-131">值</span><span class="sxs-lookup"><span data-stu-id="d61bb-131">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="d61bb-132">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d61bb-132">Minimum supported client</span></span><br/> | <span data-ttu-id="d61bb-133">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d61bb-133">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="d61bb-134">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d61bb-134">Minimum supported server</span></span><br/> | <span data-ttu-id="d61bb-135">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d61bb-135">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="d61bb-136">標頭</span><span class="sxs-lookup"><span data-stu-id="d61bb-136">Header</span></span><br/>                   | <dl> <span data-ttu-id="d61bb-137"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="d61bb-137"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="d61bb-138">DLL</span><span class="sxs-lookup"><span data-stu-id="d61bb-138">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d61bb-139"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d61bb-139"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

