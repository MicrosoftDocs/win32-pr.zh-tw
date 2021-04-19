---
description: 設定離線登錄區中已開啟登錄機碼的安全性。
ms.assetid: 002866bb-1532-41ad-a4db-a32d6e1c0a6a
title: 'ORSetKeySecurity 函式 (Offreg) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ORSetKeySecurity
api_type:
- DllExport
api_location:
- Offreg.dll
ms.openlocfilehash: ff63a7d896964f486b5fcb168c08513f8d5703be
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001495"
---
# <a name="orsetkeysecurity-function"></a><span data-ttu-id="0dd45-103">ORSetKeySecurity 函式</span><span class="sxs-lookup"><span data-stu-id="0dd45-103">ORSetKeySecurity function</span></span>

<span data-ttu-id="0dd45-104">設定離線登錄區中已開啟登錄機碼的安全性。</span><span class="sxs-lookup"><span data-stu-id="0dd45-104">Sets the security of an open registry key in an offline registry hive.</span></span>

## <a name="syntax"></a><span data-ttu-id="0dd45-105">語法</span><span class="sxs-lookup"><span data-stu-id="0dd45-105">Syntax</span></span>


```C++
DWORD ORSetKeySecurity(
  _In_ ORHKEY               Handle,
  _In_ SECURITY_INFORMATION SecurityInformation,
  _In_ PSECURITY_DESCRIPTOR pSecurityDescriptor
);
```



## <a name="parameters"></a><span data-ttu-id="0dd45-106">參數</span><span class="sxs-lookup"><span data-stu-id="0dd45-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0dd45-107">*控制碼* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0dd45-107">*Handle* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dd45-108">離線登錄 hive 中開啟登錄機碼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0dd45-108">A handle to an open registry key in an offline registry hive.</span></span>

</dd> <dt>

<span data-ttu-id="0dd45-109">*SecurityInformation* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0dd45-109">*SecurityInformation* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dd45-110">位旗標，表示要設定的安全性資訊類型。</span><span class="sxs-lookup"><span data-stu-id="0dd45-110">Bit flags that indicate the type of security information to set.</span></span> <span data-ttu-id="0dd45-111">這個參數可以是 [安全性 \_ 資訊](../secauthz/security-information.md) 位旗標的組合。</span><span class="sxs-lookup"><span data-stu-id="0dd45-111">This parameter can be a combination of the [SECURITY\_INFORMATION](../secauthz/security-information.md) bit flags.</span></span>

</dd> <dt>

<span data-ttu-id="0dd45-112">*pSecurityDescriptor* \[在\]</span><span class="sxs-lookup"><span data-stu-id="0dd45-112">*pSecurityDescriptor* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="0dd45-113">[安全 \_ 描述項](/windows/win32/api/winnt/ns-winnt-security_descriptor)結構的指標，指定要為指定的索引鍵設定的安全性屬性。</span><span class="sxs-lookup"><span data-stu-id="0dd45-113">A pointer to a [SECURITY\_DESCRIPTOR](/windows/win32/api/winnt/ns-winnt-security_descriptor) structure that specifies the security attributes to set for the specified key.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="0dd45-114">傳回值</span><span class="sxs-lookup"><span data-stu-id="0dd45-114">Return value</span></span>

<span data-ttu-id="0dd45-115">如果函式成功，函數會傳回錯誤 \_ SUCCESS。</span><span class="sxs-lookup"><span data-stu-id="0dd45-115">If the function succeeds, the function returns ERROR\_SUCCESS.</span></span>

<span data-ttu-id="0dd45-116">如果函式失敗，則會傳回 Winerror.h 中定義的非零錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="0dd45-116">If the function fails, it returns a nonzero error code defined in Winerror.h.</span></span> <span data-ttu-id="0dd45-117">您可以使用 [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) 函數搭配系統旗標的格式 \_ 訊息 \_ \_ ，以取得錯誤的一般描述。</span><span class="sxs-lookup"><span data-stu-id="0dd45-117">You can use the [FormatMessage](/windows/win32/api/winbase/nf-winbase-formatmessage) function with the FORMAT\_MESSAGE\_FROM\_SYSTEM flag to get a generic description of the error.</span></span>

## <a name="requirements"></a><span data-ttu-id="0dd45-118">規格需求</span><span class="sxs-lookup"><span data-stu-id="0dd45-118">Requirements</span></span>



| <span data-ttu-id="0dd45-119">需求</span><span class="sxs-lookup"><span data-stu-id="0dd45-119">Requirement</span></span> | <span data-ttu-id="0dd45-120">值</span><span class="sxs-lookup"><span data-stu-id="0dd45-120">Value</span></span> |
|----------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="0dd45-121">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="0dd45-121">Redistributable</span></span><br/> | <span data-ttu-id="0dd45-122">Windows Offline Registry library 1.0 版或更新版本</span><span class="sxs-lookup"><span data-stu-id="0dd45-122">Windows Offline Registry library version 1.0 or later</span></span><br/>                      |
| <span data-ttu-id="0dd45-123">標頭</span><span class="sxs-lookup"><span data-stu-id="0dd45-123">Header</span></span><br/>          | <dl> <span data-ttu-id="0dd45-124"><dt>Offreg。h</dt></span><span class="sxs-lookup"><span data-stu-id="0dd45-124"><dt>Offreg.h</dt></span></span> </dl>   |
| <span data-ttu-id="0dd45-125">DLL</span><span class="sxs-lookup"><span data-stu-id="0dd45-125">DLL</span></span><br/>             | <dl> <span data-ttu-id="0dd45-126"><dt>Offreg.dll</dt></span><span class="sxs-lookup"><span data-stu-id="0dd45-126"><dt>Offreg.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="0dd45-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0dd45-127">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0dd45-128">**ORCloseKey**</span><span class="sxs-lookup"><span data-stu-id="0dd45-128">**ORCloseKey**</span></span>](orclosekey.md)
</dt> <dt>

[<span data-ttu-id="0dd45-129">**ORDeleteKey**</span><span class="sxs-lookup"><span data-stu-id="0dd45-129">**ORDeleteKey**</span></span>](ordeletekey.md)
</dt> <dt>

[<span data-ttu-id="0dd45-130">**OROpenKey**</span><span class="sxs-lookup"><span data-stu-id="0dd45-130">**OROpenKey**</span></span>](oropenkey.md)
</dt> <dt>

[<span data-ttu-id="0dd45-131">**ORGetKeySecurity**</span><span class="sxs-lookup"><span data-stu-id="0dd45-131">**ORGetKeySecurity**</span></span>](orgetkeysecurity.md)
</dt> <dt>

[<span data-ttu-id="0dd45-132">安全 \_ 描述項</span><span class="sxs-lookup"><span data-stu-id="0dd45-132">SECURITY\_DESCRIPTOR</span></span>](/windows/win32/api/winnt/ns-winnt-security_descriptor)
</dt> <dt>

[<span data-ttu-id="0dd45-133">安全性 \_ 資訊</span><span class="sxs-lookup"><span data-stu-id="0dd45-133">SECURITY\_INFORMATION</span></span>](../secauthz/security-information.md)
</dt> </dl>

 

 
