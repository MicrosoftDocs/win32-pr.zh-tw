---
description: 將安全通訊端層通訊協定的參考遞減 (SSL) 提供者。
ms.assetid: 67bfa4b5-c02c-4a76-871d-93f3bf4e3602
title: 'SslDecrementProviderReferenceCount 函式 (Sslprovider) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SslDecrementProviderReferenceCount
api_type:
- DllExport
api_location:
- Ncrypt.dll
ms.openlocfilehash: 4d3fe072c02f22b713115dd5191b0b5e0cedbb37
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943928"
---
# <a name="ssldecrementproviderreferencecount-function"></a><span data-ttu-id="aab74-103">SslDecrementProviderReferenceCount 函式</span><span class="sxs-lookup"><span data-stu-id="aab74-103">SslDecrementProviderReferenceCount function</span></span>

<span data-ttu-id="aab74-104">**SslDecrementProviderReferenceCount** 函式會將 [*安全通訊端層通訊協定*](/windows/desktop/SecGloss/s-gly)的參考減少 (SSL) 提供者。</span><span class="sxs-lookup"><span data-stu-id="aab74-104">The **SslDecrementProviderReferenceCount** function decrements the references to the [*Secure Sockets Layer protocol*](/windows/desktop/SecGloss/s-gly) (SSL) provider.</span></span>

## <a name="syntax"></a><span data-ttu-id="aab74-105">語法</span><span class="sxs-lookup"><span data-stu-id="aab74-105">Syntax</span></span>


```C++
SECURITY_STATUS WINAPI SslDecrementProviderReferenceCount(
  _In_ NCRYPT_PROV_HANDLE hSslProvider
);
```



## <a name="parameters"></a><span data-ttu-id="aab74-106">參數</span><span class="sxs-lookup"><span data-stu-id="aab74-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aab74-107">*hSslProvider* \[在\]</span><span class="sxs-lookup"><span data-stu-id="aab74-107">*hSslProvider* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="aab74-108">SSL 通訊協定提供者實例的控制碼。</span><span class="sxs-lookup"><span data-stu-id="aab74-108">The handle of the SSL protocol provider instance.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="aab74-109">傳回值</span><span class="sxs-lookup"><span data-stu-id="aab74-109">Return value</span></span>

<span data-ttu-id="aab74-110">如果函式成功，則會傳回零。</span><span class="sxs-lookup"><span data-stu-id="aab74-110">If the function succeeds, it returns zero.</span></span>

<span data-ttu-id="aab74-111">如果函式失敗，則會傳回非零的錯誤值。</span><span class="sxs-lookup"><span data-stu-id="aab74-111">If the function fails, it returns a nonzero error value.</span></span>

<span data-ttu-id="aab74-112">可能的傳回碼包括（但不限於）下列各項。</span><span class="sxs-lookup"><span data-stu-id="aab74-112">Possible return codes include, but are not limited to, the following.</span></span>



| <span data-ttu-id="aab74-113">傳回碼/值</span><span class="sxs-lookup"><span data-stu-id="aab74-113">Return code/value</span></span>                                                                                                                                                        | <span data-ttu-id="aab74-114">Description</span><span class="sxs-lookup"><span data-stu-id="aab74-114">Description</span></span>                                      |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <span data-ttu-id="aab74-115"><dt>**狀態 \_ 不正確 \_ 控制碼**</dt> <dt>0xC0000008L</dt></span><span class="sxs-lookup"><span data-stu-id="aab74-115"><dt>**STATUS\_INVALID\_HANDLE** </dt> <dt>0xC0000008L</dt></span></span> </dl> | <span data-ttu-id="aab74-116">SSL 提供者控制碼無效。</span><span class="sxs-lookup"><span data-stu-id="aab74-116">The SSL provider handle is not valid.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="aab74-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="aab74-117">Requirements</span></span>



| <span data-ttu-id="aab74-118">需求</span><span class="sxs-lookup"><span data-stu-id="aab74-118">Requirement</span></span> | <span data-ttu-id="aab74-119">值</span><span class="sxs-lookup"><span data-stu-id="aab74-119">Value</span></span> |
|-------------------------------------|------------------------------------------------------------------------------------------|
| <span data-ttu-id="aab74-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aab74-120">Minimum supported client</span></span><br/> | <span data-ttu-id="aab74-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aab74-121">Windows Vista \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="aab74-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aab74-122">Minimum supported server</span></span><br/> | <span data-ttu-id="aab74-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aab74-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                     |
| <span data-ttu-id="aab74-124">標頭</span><span class="sxs-lookup"><span data-stu-id="aab74-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="aab74-125"><dt>Sslprovider。h</dt></span><span class="sxs-lookup"><span data-stu-id="aab74-125"><dt>Sslprovider.h</dt></span></span> </dl> |
| <span data-ttu-id="aab74-126">DLL</span><span class="sxs-lookup"><span data-stu-id="aab74-126">DLL</span></span><br/>                      | <dl> <span data-ttu-id="aab74-127"><dt>Ncrypt.dll</dt></span><span class="sxs-lookup"><span data-stu-id="aab74-127"><dt>Ncrypt.dll</dt></span></span> </dl>    |



 

