---
description: 比較兩個 Unicode 字串。
ms.assetid: D2703180-946C-4762-AFBA-1E882B01B944
title: 'RtlCompareUnicodeString 函式 (Wdm) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlCompareUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 9de12f218c37916c7e30393c0701efcf1889973f
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847260"
---
# <a name="rtlcompareunicodestring-function"></a><span data-ttu-id="4933a-103">RtlCompareUnicodeString 函式</span><span class="sxs-lookup"><span data-stu-id="4933a-103">RtlCompareUnicodeString function</span></span>

<span data-ttu-id="4933a-104">比較兩個 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="4933a-104">Compares two Unicode strings.</span></span>

## <a name="syntax"></a><span data-ttu-id="4933a-105">語法</span><span class="sxs-lookup"><span data-stu-id="4933a-105">Syntax</span></span>


```C++
LONG RtlCompareUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a><span data-ttu-id="4933a-106">參數</span><span class="sxs-lookup"><span data-stu-id="4933a-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4933a-107">*String1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4933a-107">*String1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4933a-108">第一個字串的指標。</span><span class="sxs-lookup"><span data-stu-id="4933a-108">Pointer to the first string.</span></span>

</dd> <dt>

<span data-ttu-id="4933a-109">*String2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4933a-109">*String2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4933a-110">第二個字串的指標。</span><span class="sxs-lookup"><span data-stu-id="4933a-110">Pointer to the second string.</span></span>

</dd> <dt>

<span data-ttu-id="4933a-111">*CaseInSensitive* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4933a-111">*CaseInSensitive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4933a-112">若 **為 TRUE**，則在進行比較時應該忽略大小寫。</span><span class="sxs-lookup"><span data-stu-id="4933a-112">If **TRUE**, case should be ignored when doing the comparison.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="4933a-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="4933a-113">Return value</span></span>

<span data-ttu-id="4933a-114">提供比較結果的帶正負號值：</span><span class="sxs-lookup"><span data-stu-id="4933a-114">A signed value that gives the results of the comparison:</span></span>



| <span data-ttu-id="4933a-115">傳回碼</span><span class="sxs-lookup"><span data-stu-id="4933a-115">Return code</span></span>                                                                               | <span data-ttu-id="4933a-116">Description</span><span class="sxs-lookup"><span data-stu-id="4933a-116">Description</span></span>                                     |
|-------------------------------------------------------------------------------------------|-------------------------------------------------|
| <dl> <span data-ttu-id="4933a-117"><dt>**零個**</dt></span><span class="sxs-lookup"><span data-stu-id="4933a-117"><dt>**Zero**</dt></span></span> </dl>       | <span data-ttu-id="4933a-118">*String2* 等於 *String2*。</span><span class="sxs-lookup"><span data-stu-id="4933a-118">*String1* equals *String2*.</span></span><br/>          |
| <dl> <span data-ttu-id="4933a-119"><dt>**< 零**</dt></span><span class="sxs-lookup"><span data-stu-id="4933a-119"><dt>**< Zero**</dt></span></span> </dl>  | <span data-ttu-id="4933a-120">*String1* 小於 *string2*。</span><span class="sxs-lookup"><span data-stu-id="4933a-120">*String1* is less than *String2*.</span></span><br/>    |
| <dl> <span data-ttu-id="4933a-121"><dt>**> 零**</dt></span><span class="sxs-lookup"><span data-stu-id="4933a-121"><dt>**> Zero** </dt></span></span> </dl> | <span data-ttu-id="4933a-122">*String1* 大於 *string2*。</span><span class="sxs-lookup"><span data-stu-id="4933a-122">*String1* is greater than *String2*.</span></span><br/> |



 

## <a name="requirements"></a><span data-ttu-id="4933a-123">規格需求</span><span class="sxs-lookup"><span data-stu-id="4933a-123">Requirements</span></span>



| <span data-ttu-id="4933a-124">需求</span><span class="sxs-lookup"><span data-stu-id="4933a-124">Requirement</span></span> | <span data-ttu-id="4933a-125">值</span><span class="sxs-lookup"><span data-stu-id="4933a-125">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4933a-126">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4933a-126">Minimum supported client</span></span><br/> | <span data-ttu-id="4933a-127">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4933a-127">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="4933a-128">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4933a-128">Minimum supported server</span></span><br/> | <span data-ttu-id="4933a-129">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4933a-129">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="4933a-130">目標平台</span><span class="sxs-lookup"><span data-stu-id="4933a-130">Target platform</span></span><br/>          | <dl> <span data-ttu-id="4933a-131"><dt>[通用](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="4933a-131"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="4933a-132">標頭</span><span class="sxs-lookup"><span data-stu-id="4933a-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="4933a-133"><dt>Wdm (包括 Wdm、Ntddk .h 或 Ntifs. h) </dt></span><span class="sxs-lookup"><span data-stu-id="4933a-133"><dt>Wdm.h (include Wdm.h, Ntddk.h, or Ntifs.h)</dt></span></span> </dl>                   |
| <span data-ttu-id="4933a-134">程式庫</span><span class="sxs-lookup"><span data-stu-id="4933a-134">Library</span></span><br/>                  | <dl> <span data-ttu-id="4933a-135"><dt>Ntdll.dll .lib</dt></span><span class="sxs-lookup"><span data-stu-id="4933a-135"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="4933a-136">DLL</span><span class="sxs-lookup"><span data-stu-id="4933a-136">DLL</span></span><br/>                      | <dl> <span data-ttu-id="4933a-137"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="4933a-137"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="4933a-138">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4933a-138">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4933a-139">**RtlCompareString**</span><span class="sxs-lookup"><span data-stu-id="4933a-139">**RtlCompareString**</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlcomparestring)
</dt> <dt>

[<span data-ttu-id="4933a-140">**RtlEqualString**</span><span class="sxs-lookup"><span data-stu-id="4933a-140">**RtlEqualString**</span></span>](/windows-hardware/drivers/ddi/ntddk/nf-ntddk-rtlequalstring)
</dt> </dl>

 

 
