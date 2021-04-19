---
description: 為呼叫它的電腦新增替代局域網路名稱。
ms.assetid: e4d8355b-0492-4b6f-988f-3887e63a2bba
title: AddLocalAlternateComputerName 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddLocalAlternateComputerName
- AddLocalAlternateComputerNameA
- AddLocalAlternateComputerNameW
api_type:
- DllExport
api_location:
- Kernel32.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
- kernel32legacy.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
- API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
- API-Ms-Win-Core-Kernel32-Legacy-Ansi-L1-1-0.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
- API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
ms.openlocfilehash: 6027752a0e60f135f0cc8a1c0cdd536c59c09621
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106987889"
---
# <a name="addlocalalternatecomputername-function"></a><span data-ttu-id="92b0b-103">AddLocalAlternateComputerName 函式</span><span class="sxs-lookup"><span data-stu-id="92b0b-103">AddLocalAlternateComputerName function</span></span>

<span data-ttu-id="92b0b-104">為呼叫它的電腦新增替代局域網路名稱。</span><span class="sxs-lookup"><span data-stu-id="92b0b-104">Adds an alternate local network name for the computer from which it is called.</span></span>

## <a name="syntax"></a><span data-ttu-id="92b0b-105">語法</span><span class="sxs-lookup"><span data-stu-id="92b0b-105">Syntax</span></span>


```C++
DWORD AddLocalAlternateComputerName(
  _In_ LPCTSTR lpDnsFQHostname,
  _In_ ULONG   ulFlags
);
```



## <a name="parameters"></a><span data-ttu-id="92b0b-106">參數</span><span class="sxs-lookup"><span data-stu-id="92b0b-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="92b0b-107">*lpDnsFQHostname* \[在\]</span><span class="sxs-lookup"><span data-stu-id="92b0b-107">*lpDnsFQHostname* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92b0b-108">要加入的替代名稱。</span><span class="sxs-lookup"><span data-stu-id="92b0b-108">The alternate name to be added.</span></span> <span data-ttu-id="92b0b-109">名稱必須是 **ComputerNameDnsFullyQualified** 格式，如 [**電腦 \_ 名稱 \_ 格式**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format) 列舉中所定義，而且 [**DnsValidateName \_ W**](/windows/win32/api/windns/nf-windns-dnsvalidatename) 函數必須能夠驗證它的格式設定為 **DnsNameHostnameFull**。</span><span class="sxs-lookup"><span data-stu-id="92b0b-109">The name must be in the **ComputerNameDnsFullyQualified** format as defined in the [**COMPUTER\_NAME\_FORMAT**](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format) enumeration, and the [**DnsValidateName\_W**](/windows/win32/api/windns/nf-windns-dnsvalidatename) function must be able to validate it with its format set to **DnsNameHostnameFull**.</span></span>

</dd> <dt>

<span data-ttu-id="92b0b-110">*ulFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="92b0b-110">*ulFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="92b0b-111">此參數是保留的，而且必須設定為零。</span><span class="sxs-lookup"><span data-stu-id="92b0b-111">This parameter is reserved and must be set to zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="92b0b-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="92b0b-112">Return value</span></span>

<span data-ttu-id="92b0b-113">如果函式成功，函數會傳回 **錯誤 \_ SUCCESS**。</span><span class="sxs-lookup"><span data-stu-id="92b0b-113">If the function succeeds, the function returns **ERROR\_SUCCESS**.</span></span> <span data-ttu-id="92b0b-114">如果函式失敗，則會傳回非零的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="92b0b-114">If the function fails, it returns a nonzero error code.</span></span> <span data-ttu-id="92b0b-115">它傳回的錯誤碼如下：</span><span class="sxs-lookup"><span data-stu-id="92b0b-115">Among the error codes that it returns are the following:</span></span>



| <span data-ttu-id="92b0b-116">傳回碼</span><span class="sxs-lookup"><span data-stu-id="92b0b-116">Return code</span></span>                                                                                               | <span data-ttu-id="92b0b-117">Description</span><span class="sxs-lookup"><span data-stu-id="92b0b-117">Description</span></span>                                                                                                                                         |
|-----------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="92b0b-118"><dt>**錯誤 \_ 不正確 \_ 參數**</dt></span><span class="sxs-lookup"><span data-stu-id="92b0b-118"><dt>**ERROR\_INVALID\_PARAMETER**</dt></span></span> </dl>  | <span data-ttu-id="92b0b-119">指出 *lpDnsFQHostname* 參數未指向有效的 DNS 名稱，或 *ulFlags* 參數不等於零。</span><span class="sxs-lookup"><span data-stu-id="92b0b-119">Indicates that the *lpDnsFQHostname* parameter does not point to a valid DNS name, or that the *ulFlags* parameter is not equal to zero.</span></span><br/> |
| <dl> <span data-ttu-id="92b0b-120"><dt>**錯誤 \_ 沒有 \_ 足夠的 \_ 記憶體**</dt></span><span class="sxs-lookup"><span data-stu-id="92b0b-120"><dt>**ERROR\_NOT\_ENOUGH\_MEMORY**</dt></span></span> </dl> | <span data-ttu-id="92b0b-121">記憶體不足，無法完成此作業。</span><span class="sxs-lookup"><span data-stu-id="92b0b-121">There is not enough memory to complete the operation.</span></span><br/>                                                                                    |



 

## <a name="requirements"></a><span data-ttu-id="92b0b-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="92b0b-122">Requirements</span></span>



| <span data-ttu-id="92b0b-123">需求</span><span class="sxs-lookup"><span data-stu-id="92b0b-123">Requirement</span></span> | <span data-ttu-id="92b0b-124">值</span><span class="sxs-lookup"><span data-stu-id="92b0b-124">Value</span></span> |
|-----------------------------------|-------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92b0b-125">程式庫</span><span class="sxs-lookup"><span data-stu-id="92b0b-125">Library</span></span><br/>                | <dl> <span data-ttu-id="92b0b-126"><dt>Kernel32.lib</dt></span><span class="sxs-lookup"><span data-stu-id="92b0b-126"><dt>Kernel32.lib</dt></span></span> </dl>               |
| <span data-ttu-id="92b0b-127">DLL</span><span class="sxs-lookup"><span data-stu-id="92b0b-127">DLL</span></span><br/>                    | <dl> <span data-ttu-id="92b0b-128"><dt>Kernel32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="92b0b-128"><dt>Kernel32.dll</dt></span></span> </dl>               |
| <span data-ttu-id="92b0b-129">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="92b0b-129">Unicode and ANSI names</span></span><br/> | <span data-ttu-id="92b0b-130">**AddLocalAlternateComputerNameW** (Unicode) 和 **AddLocalAlternateComputerNameA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="92b0b-130">**AddLocalAlternateComputerNameW** (Unicode) and **AddLocalAlternateComputerNameA** (ANSI)</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92b0b-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92b0b-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92b0b-132">**電腦 \_ 名稱 \_ 格式**</span><span class="sxs-lookup"><span data-stu-id="92b0b-132">**COMPUTER\_NAME\_FORMAT**</span></span>](/windows/win32/api/sysinfoapi/ne-sysinfoapi-computer_name_format)
</dt> <dt>

[<span data-ttu-id="92b0b-133">**DnsValidateName \_ W**</span><span class="sxs-lookup"><span data-stu-id="92b0b-133">**DnsValidateName\_W**</span></span>](/windows/win32/api/windns/nf-windns-dnsvalidatename)
</dt> </dl>

 

 
