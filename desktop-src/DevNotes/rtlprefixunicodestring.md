---
description: 比較兩個 Unicode 字串，以判斷某個字串是否為另一個字串的前置詞。
ms.assetid: 7D859C0A-2F72-49A4-8B49-130DCA103F37
title: 'RtlPrefixUnicodeString 函式 (Ntddk) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlPrefixUnicodeString
api_type:
- DllExport
api_location:
- Ntdll.dll
ms.openlocfilehash: 47382daab1bac5e71098f79a601d89255f1cf0e9
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468153"
---
# <a name="rtlprefixunicodestring-function"></a><span data-ttu-id="d7006-103">RtlPrefixUnicodeString 函式</span><span class="sxs-lookup"><span data-stu-id="d7006-103">RtlPrefixUnicodeString function</span></span>

<span data-ttu-id="d7006-104">比較兩個 Unicode 字串，以判斷某個字串是否為另一個字串的前置詞。</span><span class="sxs-lookup"><span data-stu-id="d7006-104">Compares two Unicode strings to determine whether one string is a prefix of the other.</span></span>

## <a name="syntax"></a><span data-ttu-id="d7006-105">語法</span><span class="sxs-lookup"><span data-stu-id="d7006-105">Syntax</span></span>


```C++
BOOLEAN RtlPrefixUnicodeString(
  _In_ PCUNICODE_STRING String1,
  _In_ PCUNICODE_STRING String2,
  _In_ BOOLEAN          CaseInSensitive
);
```



## <a name="parameters"></a><span data-ttu-id="d7006-106">參數</span><span class="sxs-lookup"><span data-stu-id="d7006-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d7006-107">*String1* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d7006-107">*String1* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7006-108">第一個字串的指標，可能是位於 *String2* 之已緩衝處理的 Unicode 字串的前置詞。</span><span class="sxs-lookup"><span data-stu-id="d7006-108">Pointer to the first string, which might be a prefix of the buffered Unicode string at *String2*.</span></span>

</dd> <dt>

<span data-ttu-id="d7006-109">*String2* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d7006-109">*String2* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7006-110">第二個字串的指標。</span><span class="sxs-lookup"><span data-stu-id="d7006-110">Pointer to the second string.</span></span>

</dd> <dt>

<span data-ttu-id="d7006-111">*CaseInSensitive* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d7006-111">*CaseInSensitive* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d7006-112">若 **為 TRUE**，則在進行比較時應該忽略大小寫。</span><span class="sxs-lookup"><span data-stu-id="d7006-112">If **TRUE**, case should be ignored when doing the comparison.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d7006-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="d7006-113">Return value</span></span>

<span data-ttu-id="d7006-114">如果 *String1* 是 *string2* 的前置詞，**則為 TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="d7006-114">**TRUE** if *String1* is a prefix of *String2*.</span></span>

## <a name="requirements"></a><span data-ttu-id="d7006-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="d7006-115">Requirements</span></span>



| <span data-ttu-id="d7006-116">需求</span><span class="sxs-lookup"><span data-stu-id="d7006-116">Requirement</span></span> | <span data-ttu-id="d7006-117">值</span><span class="sxs-lookup"><span data-stu-id="d7006-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d7006-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d7006-118">Minimum supported client</span></span><br/> | <span data-ttu-id="d7006-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7006-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                                              |
| <span data-ttu-id="d7006-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d7006-120">Minimum supported server</span></span><br/> | <span data-ttu-id="d7006-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d7006-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                                                    |
| <span data-ttu-id="d7006-122">目標平台</span><span class="sxs-lookup"><span data-stu-id="d7006-122">Target platform</span></span><br/>          | <dl> <span data-ttu-id="d7006-123"><dt>[通用](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span><span class="sxs-lookup"><span data-stu-id="d7006-123"><dt>[Universal](https://msdn.microsoft.com/Library/Windows/Hardware/EB2264A4-BAE8-446B-B9A5-19893936DDCA)</dt></span></span> </dl> |
| <span data-ttu-id="d7006-124">標頭</span><span class="sxs-lookup"><span data-stu-id="d7006-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="d7006-125"><dt>Ntddk (包含 Ntddk) </dt></span><span class="sxs-lookup"><span data-stu-id="d7006-125"><dt>Ntddk.h (include Ntddk.h)</dt></span></span> </dl>                                    |
| <span data-ttu-id="d7006-126">程式庫</span><span class="sxs-lookup"><span data-stu-id="d7006-126">Library</span></span><br/>                  | <dl> <span data-ttu-id="d7006-127"><dt>Ntdll.dll .lib</dt></span><span class="sxs-lookup"><span data-stu-id="d7006-127"><dt>Ntdll.lib</dt></span></span> </dl>                                                    |
| <span data-ttu-id="d7006-128">DLL</span><span class="sxs-lookup"><span data-stu-id="d7006-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d7006-129"><dt>Ntdll.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d7006-129"><dt>Ntdll.dll</dt></span></span> </dl>                                                    |



## <a name="see-also"></a><span data-ttu-id="d7006-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d7006-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d7006-131">**RtlCompareUnicodeString**</span><span class="sxs-lookup"><span data-stu-id="d7006-131">**RtlCompareUnicodeString**</span></span>](rtlcompareunicodestring.md)
</dt> </dl>

 

 




