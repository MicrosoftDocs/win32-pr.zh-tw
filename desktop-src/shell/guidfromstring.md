---
description: 將字串轉換成 GUID。
ms.assetid: 109b99e6-7409-44e0-932c-658be66651f4
title: GUIDFromString 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- GUIDFromString
- GUIDFromStringA
- GUIDFromStringW
api_type:
- DllExport
api_location:
- Shell32.dll
- API-MS-Win-shlwapi-ie-l1-1-0.dll
- shlwapi.dll
ms.openlocfilehash: a29a2138f4bcc7435a0d7864f65dd60ab16519c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103849201"
---
# <a name="guidfromstring-function"></a><span data-ttu-id="dac53-103">GUIDFromString 函式</span><span class="sxs-lookup"><span data-stu-id="dac53-103">GUIDFromString function</span></span>

<span data-ttu-id="dac53-104">\[**GUIDFromString** 可透過 Windows XP Service Pack 2 (SP2) 或 windows Vista 取得。</span><span class="sxs-lookup"><span data-stu-id="dac53-104">\[**GUIDFromString** is available through Windows XP with Service Pack 2 (SP2) or Windows Vista.</span></span> <span data-ttu-id="dac53-105">它可能會在後續版本中變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="dac53-105">It might be altered or unavailable in subsequent versions.</span></span> <span data-ttu-id="dac53-106">應用程式應該使用 [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) 或 [**IIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) 來取代此函式。\]</span><span class="sxs-lookup"><span data-stu-id="dac53-106">Applications should use [**CLSIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-clsidfromstring) or [**IIDFromString**](/windows/win32/api/combaseapi/nf-combaseapi-iidfromstring) in place of this function.\]</span></span>

<span data-ttu-id="dac53-107">將字串轉換成 GUID。</span><span class="sxs-lookup"><span data-stu-id="dac53-107">Converts a string to a GUID.</span></span>

## <a name="syntax"></a><span data-ttu-id="dac53-108">語法</span><span class="sxs-lookup"><span data-stu-id="dac53-108">Syntax</span></span>


```C++
BOOL GUIDFromString(
  _In_  LPCTSTR psz,
  _Out_ LPGUID  pguid
);
```



## <a name="parameters"></a><span data-ttu-id="dac53-109">參數</span><span class="sxs-lookup"><span data-stu-id="dac53-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="dac53-110">*psz* \[在\]</span><span class="sxs-lookup"><span data-stu-id="dac53-110">*psz* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="dac53-111">類型： **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="dac53-111">Type: **LPCTSTR**</span></span>

<span data-ttu-id="dac53-112">要轉換之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="dac53-112">A pointer to the null-terminated string to convert.</span></span> <span data-ttu-id="dac53-113">字串的格式應該如下：</span><span class="sxs-lookup"><span data-stu-id="dac53-113">The string should be in the following form:</span></span>

{00000000-0000-0000-0000-000000000000}

</dd> <dt>

<span data-ttu-id="dac53-114">*pguid* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="dac53-114">*pguid* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="dac53-115">類型： **LPGUID**</span><span class="sxs-lookup"><span data-stu-id="dac53-115">Type: **LPGUID**</span></span>

<span data-ttu-id="dac53-116">當此方法傳回時，用來接收 GUID 之緩衝區的指標。</span><span class="sxs-lookup"><span data-stu-id="dac53-116">Pointer to a buffer to receive the GUID when this method returns.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="dac53-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="dac53-117">Return value</span></span>

<span data-ttu-id="dac53-118">類型： **BOOL**</span><span class="sxs-lookup"><span data-stu-id="dac53-118">Type: **BOOL**</span></span>

<span data-ttu-id="dac53-119">如果已成功建立 GUID，則 **為 TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="dac53-119">**TRUE** if the GUID was created successfully; otherwise, **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="dac53-120">備註</span><span class="sxs-lookup"><span data-stu-id="dac53-120">Remarks</span></span>

<span data-ttu-id="dac53-121">這個函式不是在標頭中宣告，也不是由 .dll 檔中的名稱所匯出。</span><span class="sxs-lookup"><span data-stu-id="dac53-121">This function is not declared in a header or exported by name from a .dll file.</span></span> <span data-ttu-id="dac53-122">它必須從 Shell32.dll 載入為 **GUIDFromStringA** 的序數703，以及 **GUIDFromStringW** 的序數704。</span><span class="sxs-lookup"><span data-stu-id="dac53-122">It must be loaded from Shell32.dll as ordinal 703 for **GUIDFromStringA** and ordinal 704 for **GUIDFromStringW**.</span></span>

<span data-ttu-id="dac53-123">您也可以從 Shlwapi.dll 將其存取為 **GUIDFromStringA** 的序數269，以及 **GUIDFromStringW** 的序數270。</span><span class="sxs-lookup"><span data-stu-id="dac53-123">It can also be accessed from Shlwapi.dll as ordinal 269 for **GUIDFromStringA** and ordinal 270 for **GUIDFromStringW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="dac53-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="dac53-124">Requirements</span></span>



| <span data-ttu-id="dac53-125">需求</span><span class="sxs-lookup"><span data-stu-id="dac53-125">Requirement</span></span> | <span data-ttu-id="dac53-126">值</span><span class="sxs-lookup"><span data-stu-id="dac53-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="dac53-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="dac53-127">Minimum supported client</span></span><br/> | <span data-ttu-id="dac53-128">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dac53-128">Windows XP \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="dac53-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="dac53-129">Minimum supported server</span></span><br/> | <span data-ttu-id="dac53-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="dac53-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="dac53-131">DLL</span><span class="sxs-lookup"><span data-stu-id="dac53-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="dac53-132"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="dac53-132"><dt>Shell32.dll</dt></span></span> </dl> |
| <span data-ttu-id="dac53-133">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="dac53-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="dac53-134">**GUIDFromStringW** (Unicode) 和 **GUIDFromStringA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="dac53-134">**GUIDFromStringW** (Unicode) and **GUIDFromStringA** (ANSI)</span></span><br/>                |



 

 
