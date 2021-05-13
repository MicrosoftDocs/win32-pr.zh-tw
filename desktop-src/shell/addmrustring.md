---
description: 將字串加入最近使用的 (MRU) 清單的最上方。
title: AddMRUStringW 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- AddMRUStringW
- AddMRUStringW
api_type:
- DllExport
api_location:
- Comctl32.dll
ms.assetid: ad94a442-8492-412c-a4f2-ac6e7c5327d7
ms.openlocfilehash: b62e23cd0604273559e36e561970dd62f117c11d
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109841189"
---
# <a name="addmrustringw-function"></a><span data-ttu-id="d0b11-103">AddMRUStringW 函式</span><span class="sxs-lookup"><span data-stu-id="d0b11-103">AddMRUStringW function</span></span>

<span data-ttu-id="d0b11-104">\[您可以透過 Windows XP Service Pack 2 (SP2) 和 Windows Server 2003 來取得此函式。</span><span class="sxs-lookup"><span data-stu-id="d0b11-104">\[This function is available through Windows XP with Service Pack 2 (SP2) and Windows Server 2003.</span></span> <span data-ttu-id="d0b11-105">它可能會在後續版本的 Windows 中改變或無法使用。</span><span class="sxs-lookup"><span data-stu-id="d0b11-105">It might be altered or unavailable in subsequent versions of Windows.</span></span> <span data-ttu-id="d0b11-106">\]</span><span class="sxs-lookup"><span data-stu-id="d0b11-106">\]</span></span>

<span data-ttu-id="d0b11-107">將字串加入最近使用的 (MRU) 清單的最上方。</span><span class="sxs-lookup"><span data-stu-id="d0b11-107">Adds a string to the top of the most recently used (MRU) list.</span></span>

## <a name="syntax"></a><span data-ttu-id="d0b11-108">語法</span><span class="sxs-lookup"><span data-stu-id="d0b11-108">Syntax</span></span>


```C++
int AddMRUStringW(
  _In_ HANDLE  hMRU,
  _In_ LPCTSTR szString
);
```



## <a name="parameters"></a><span data-ttu-id="d0b11-109">參數</span><span class="sxs-lookup"><span data-stu-id="d0b11-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d0b11-110">*hMRU* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d0b11-110">*hMRU* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0b11-111">類型： **控制碼**</span><span class="sxs-lookup"><span data-stu-id="d0b11-111">Type: **HANDLE**</span></span>

<span data-ttu-id="d0b11-112">MRU 清單的控制碼。</span><span class="sxs-lookup"><span data-stu-id="d0b11-112">The handle of the MRU list.</span></span>

</dd> <dt>

<span data-ttu-id="d0b11-113">*szString* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d0b11-113">*szString* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d0b11-114">類型： **LPCTSTR**</span><span class="sxs-lookup"><span data-stu-id="d0b11-114">Type: **LPCTSTR**</span></span>

<span data-ttu-id="d0b11-115">資料的指標。</span><span class="sxs-lookup"><span data-stu-id="d0b11-115">A pointer to the data.</span></span> <span data-ttu-id="d0b11-116">這可以是字串，或者，如果使用 **mru \_ 二進位** 旗標的二進位資料來建立 mru 清單，則為。</span><span class="sxs-lookup"><span data-stu-id="d0b11-116">This can be either a string or, if the MRU list was created with the **MRU\_BINARY** flag, binary data.</span></span> <span data-ttu-id="d0b11-117">在二進位資料的情況下，第一個 **DWORD** 會指出其大小。</span><span class="sxs-lookup"><span data-stu-id="d0b11-117">In the case of binary data, the first **DWORD** indicates its size.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d0b11-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="d0b11-118">Return value</span></span>

<span data-ttu-id="d0b11-119">類型： **int**</span><span class="sxs-lookup"><span data-stu-id="d0b11-119">Type: **int**</span></span>

<span data-ttu-id="d0b11-120">如果成功，則傳回非負數值，否則為-1。</span><span class="sxs-lookup"><span data-stu-id="d0b11-120">Returns a non-negative value if successful, -1 otherwise.</span></span>

## <a name="remarks"></a><span data-ttu-id="d0b11-121">備註</span><span class="sxs-lookup"><span data-stu-id="d0b11-121">Remarks</span></span>

<span data-ttu-id="d0b11-122">此函式不包含在公用標頭或程式庫中。</span><span class="sxs-lookup"><span data-stu-id="d0b11-122">This function is not included in a public header or library.</span></span> <span data-ttu-id="d0b11-123">您可以透過 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 來存取它，也可以從 comctl32.dll 中解壓縮它的序數，也就是401（ **AddMRUStringW**）。</span><span class="sxs-lookup"><span data-stu-id="d0b11-123">It can be accessed through [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) or extracted from comctl32.dll by its ordinal, which is 401 for **AddMRUStringW**.</span></span>

## <a name="requirements"></a><span data-ttu-id="d0b11-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="d0b11-124">Requirements</span></span>



| <span data-ttu-id="d0b11-125">需求</span><span class="sxs-lookup"><span data-stu-id="d0b11-125">Requirement</span></span> | <span data-ttu-id="d0b11-126">值</span><span class="sxs-lookup"><span data-stu-id="d0b11-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d0b11-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d0b11-127">Minimum supported client</span></span><br/> | <span data-ttu-id="d0b11-128">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0b11-128">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                                                     |
| <span data-ttu-id="d0b11-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d0b11-129">Minimum supported server</span></span><br/> | <span data-ttu-id="d0b11-130">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d0b11-130">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                                           |
| <span data-ttu-id="d0b11-131">DLL</span><span class="sxs-lookup"><span data-stu-id="d0b11-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="d0b11-132"><dt>Comctl32.dll (5.0 版或更新版本) </dt></span><span class="sxs-lookup"><span data-stu-id="d0b11-132"><dt>Comctl32.dll (version 5.0 or later)</dt></span></span> </dl> |
| <span data-ttu-id="d0b11-133">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="d0b11-133">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="d0b11-134">**AddMRUStringW** (Unicode) </span><span class="sxs-lookup"><span data-stu-id="d0b11-134">**AddMRUStringW** (Unicode)</span></span><br/>                                                                         |



 

