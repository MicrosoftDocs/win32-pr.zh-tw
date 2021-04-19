---
description: 將參考計數遞增至安全通訊端層的通訊協定 (SSL) 提供者實例。
ms.assetid: 67e7b8b4-b073-4936-b1e0-3fc7c1c011a2
title: 'SslIncrementProviderReferenceCount 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslIncrementProviderReferenceCount
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 862697035d978db082c303c6e1df6f2a444d8be3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989061"
---
# <a name="sslincrementproviderreferencecount-function"></a><span data-ttu-id="0f5ee-103">SslIncrementProviderReferenceCount 函式</span><span class="sxs-lookup"><span data-stu-id="0f5ee-103">SslIncrementProviderReferenceCount function</span></span>

<span data-ttu-id="0f5ee-104">**SslIncrementProviderReferenceCount** 函式會將參考計數遞增 [*安全通訊端層的通訊協定*](/windows/desktop/SecGloss/s-gly) (SSL) 提供者實例。</span><span class="sxs-lookup"><span data-stu-id="0f5ee-104">The **SslIncrementProviderReferenceCount** function increments the reference count to a [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider instance.</span></span>

## <a name="syntax"></a><span data-ttu-id="0f5ee-105">語法</span><span class="sxs-lookup"><span data-stu-id="0f5ee-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslIncrementProviderReferenceCount(
  _In_ NCRYPT_PROV_HANDLE hSslProvider
);
```



## <a name="parameters"></a><span data-ttu-id="0f5ee-106">參數</span><span class="sxs-lookup"><span data-stu-id="0f5ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0f5ee-107">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0f5ee-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0f5ee-108">SSL 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0f5ee-108">The handle to the SSL protocol provider instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0f5ee-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="0f5ee-109">Return value</span></span>

<span data-ttu-id="0f5ee-110">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="0f5ee-110">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="0f5ee-111">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="0f5ee-111">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="0f5ee-112">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="0f5ee-112">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="0f5ee-113">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="0f5ee-113">Return code/value</span></span>                                                                                                                                                    | <span data-ttu-id="0f5ee-114">Description</span><span class="sxs-lookup"><span data-stu-id="0f5ee-114">Description</span></span>                                        |
|----------------------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------------------------------|
| <dl> <span data-ttu-id="0f5ee-115">不 <dt>**超過 \_不正確 \_ 控制碼**</dt> <dt>0x80090026L</dt></span><span class="sxs-lookup"><span data-stu-id="0f5ee-115"><dt>**NTE\_INVALID\_HANDLE**</dt> <dt>0x80090026L</dt></span></span> </dl> | <span data-ttu-id="0f5ee-116">*HSslProvider* 控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="0f5ee-116">The *hSslProvider* handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="0f5ee-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="0f5ee-117">Requirements</span></span>



| <span data-ttu-id="0f5ee-118">需求</span><span class="sxs-lookup"><span data-stu-id="0f5ee-118">Requirement</span></span> | <span data-ttu-id="0f5ee-119">值</span><span class="sxs-lookup"><span data-stu-id="0f5ee-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="0f5ee-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0f5ee-120">Minimum supported client</span></span><br/> | <span data-ttu-id="0f5ee-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0f5ee-121">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="0f5ee-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0f5ee-122">Minimum supported server</span></span><br/> | <span data-ttu-id="0f5ee-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0f5ee-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="0f5ee-124">標頭</span><span class="sxs-lookup"><span data-stu-id="0f5ee-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="0f5ee-125"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="0f5ee-125"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="0f5ee-126">DLL</span><span class="sxs-lookup"><span data-stu-id="0f5ee-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="0f5ee-127"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0f5ee-127"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

