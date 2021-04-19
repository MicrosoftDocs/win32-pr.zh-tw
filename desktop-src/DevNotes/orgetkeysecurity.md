---
description: 抓取保護離線登錄區中指定之開啟登錄機碼的安全描述項複本。
ms.assetid: 676d5be5-d9d8-48c6-848a-917d1a0474c6
title: 'ORGetKeySecurity 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORGetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: 13594493af2e7992471d13dce30f0a848501c4bb
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991140"
---
# <a name="orgetkeysecurity-function"></a><span data-ttu-id="8a92d-103">ORGetKeySecurity 函式</span><span class="sxs-lookup"><span data-stu-id="8a92d-103">ORGetKeySecurity function</span></span>

<span data-ttu-id="8a92d-104">抓取保護離線登錄區中指定之開啟登錄機碼的安全描述項複本。</span><span class="sxs-lookup"><span data-stu-id="8a92d-104">Retrieves a copy of the security descriptor protecting the specified open registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="8a92d-105">語法</span><span class="sxs-lookup"><span data-stu-id="8a92d-105">Syntax</span></span>


```C++
DWORD ORGetKeySecurity(
  _In_      ORHKEY               Handle,
  _In_      SECURITY_INFORMATION SecurityInformation,
  _Out_opt_ PSECURITY_DESCRIPTOR pSecurityDescriptor,
  _Inout_   PDWORD               lpcbSecurityDescriptor
);
```



## <a name="parameters"></a><span data-ttu-id="8a92d-106">參數</span><span class="sxs-lookup"><span data-stu-id="8a92d-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="8a92d-107">*控制碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8a92d-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a92d-108">離線登錄 hive 中開啟登錄機碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="8a92d-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="8a92d-109">*SecurityInformation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="8a92d-109">*SecurityInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="8a92d-110">表示所要求之安全性資訊的 [安全性 \_ 資訊](../secauthz/security-information.md) 值。</span><span class="sxs-lookup"><span data-stu-id="8a92d-110">A [SECURITY\_INFORMATION](../secauthz/security-information.md) value that indicates the requested security information.</span></span>

</dd> <dt>

<span data-ttu-id="8a92d-111">*pSecurityDescriptor* \[out、optional\]</span><span class="sxs-lookup"><span data-stu-id="8a92d-111">*pSecurityDescriptor* \[out, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="8a92d-112">緩衝區的指標，此緩衝區會接收所要求之安全描述項的複本。</span><span class="sxs-lookup"><span data-stu-id="8a92d-112">A pointer to a buffer that receives a copy of the requested security descriptor.</span></span> <span data-ttu-id="8a92d-113">此參數可以是 **Null**。</span><span class="sxs-lookup"><span data-stu-id="8a92d-113">This parameter can be **NULL**.</span></span>

</dd> <dt>

<span data-ttu-id="8a92d-114">*lpcbSecurityDescriptor* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="8a92d-114">*lpcbSecurityDescriptor* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="8a92d-115">變數的指標，這個變數會指定 *pSecurityDescriptor* 參數所指向之緩衝區的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="8a92d-115">A pointer to a variable that specifies the size, in bytes, of the buffer pointed to by the *pSecurityDescriptor* parameter.</span></span> <span data-ttu-id="8a92d-116">當函式傳回時，變數會包含寫入至緩衝區的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="8a92d-116">When the function returns, the variable contains the number of bytes written to the buffer.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="8a92d-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="8a92d-117">Return value</span></span>

<span data-ttu-id="8a92d-118">如果函式成功，函數會傳回錯誤 \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="8a92d-118">If the function succeeds, the function returns ERROR\_SUCCESS.</span></span>

<span data-ttu-id="8a92d-119">如果函式失敗，則會傳回 Winerror.h 中定義的非零錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="8a92d-119">If the function fails, it returns a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="8a92d-120">您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。</span><span class="sxs-lookup"><span data-stu-id="8a92d-120">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

<span data-ttu-id="8a92d-121">如果 *pSecurityDescriptor* 參數所指定的緩衝區太小，則函式會傳回錯誤 \_ 的 \_ 緩衝區，而 *lpcbSecurityDescriptor* 參數會包含要求的安全描述項所需的位元組數目。</span><span class="sxs-lookup"><span data-stu-id="8a92d-121">If the buffer specified by the *pSecurityDescriptor* parameter is too small, the function returns ERROR\_INSUFFICIENT\_BUFFER and the *lpcbSecurityDescriptor* parameter contains the number of bytes required for the requested security descriptor.</span></span>

## <a name="requirements"></a><span data-ttu-id="8a92d-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="8a92d-122">Requirements</span></span>



| <span data-ttu-id="8a92d-123">需求</span><span class="sxs-lookup"><span data-stu-id="8a92d-123">Requirement</span></span> | <span data-ttu-id="8a92d-124">值</span><span class="sxs-lookup"><span data-stu-id="8a92d-124">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="8a92d-125">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="8a92d-125">Redistributable</span></span><br/> | <span data-ttu-id="8a92d-126">Windows Offline Registry library 1.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="8a92d-126">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="8a92d-127">標頭</span><span class="sxs-lookup"><span data-stu-id="8a92d-127">Header</span></span><br/>          | <dl> <span data-ttu-id="8a92d-128"><dt>Offreg。h</dt></span><span class="sxs-lookup"><span data-stu-id="8a92d-128"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="8a92d-129">DLL</span><span class="sxs-lookup"><span data-stu-id="8a92d-129">DLL</span></span><br/>             | <dl> <span data-ttu-id="8a92d-130"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="8a92d-130"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="8a92d-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8a92d-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8a92d-132">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="8a92d-132">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="8a92d-133">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="8a92d-133">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="8a92d-134">**ORSetKeySecurity**</span><span class="sxs-lookup"><span data-stu-id="8a92d-134">**ORSetKeySecurity**</span></span>](orsetkeysecurity.md)
</dt> <dt>

[<span data-ttu-id="8a92d-135">安全性 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="8a92d-135">SECURITY\_INFORMATION</span></span>](../secauthz/security-information.md)
</dt> </dl>

 

 
