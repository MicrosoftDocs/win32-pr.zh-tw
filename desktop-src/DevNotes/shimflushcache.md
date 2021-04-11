---
description: 清空填充碼資料庫快取。 在安裝新的填充碼資料庫之後，應該呼叫此函式。
ms.assetid: 7e5bbdca-7b58-4c51-9cd1-105b05ee7fbe
title: ShimFlushCache 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ShimFlushCache
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 35e279c5036142ec87c5bad6d7c512388033bc94
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025810"
---
# <a name="shimflushcache-function"></a><span data-ttu-id="6e01a-104">ShimFlushCache 函式</span><span class="sxs-lookup"><span data-stu-id="6e01a-104">ShimFlushCache function</span></span>

<span data-ttu-id="6e01a-105">清空填充碼資料庫快取。</span><span class="sxs-lookup"><span data-stu-id="6e01a-105">Flushes the shim database cache.</span></span> <span data-ttu-id="6e01a-106">在安裝新的填充碼資料庫之後，應該呼叫此函式。</span><span class="sxs-lookup"><span data-stu-id="6e01a-106">This function should be called after installing a new shim database.</span></span>

## <a name="syntax"></a><span data-ttu-id="6e01a-107">語法</span><span class="sxs-lookup"><span data-stu-id="6e01a-107">Syntax</span></span>


```C++
BOOL WINAPI ShimFlushCache(
  _In_opt_ HWND      hwnd,
  _In_opt_ HINSTANCE hInstance,
  _In_opt_ LPCSTR    lpszCmdLine,
  _In_     int       nCmdShow
);
```



## <a name="parameters"></a><span data-ttu-id="6e01a-108">參數</span><span class="sxs-lookup"><span data-stu-id="6e01a-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6e01a-109">*hwnd* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="6e01a-109">*hwnd* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6e01a-110">尚未必須是0。</span><span class="sxs-lookup"><span data-stu-id="6e01a-110">Unused; must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="6e01a-111">*hInstance* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="6e01a-111">*hInstance* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6e01a-112">尚未必須是0。</span><span class="sxs-lookup"><span data-stu-id="6e01a-112">Unused; must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="6e01a-113">*lpszCmdLine* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="6e01a-113">*lpszCmdLine* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="6e01a-114">尚未必須是0。</span><span class="sxs-lookup"><span data-stu-id="6e01a-114">Unused; must be 0.</span></span>

</dd> <dt>

<span data-ttu-id="6e01a-115">*nCmdShow* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6e01a-115">*nCmdShow* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6e01a-116">尚未必須是0。</span><span class="sxs-lookup"><span data-stu-id="6e01a-116">Unused; must be 0.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6e01a-117">傳回值</span><span class="sxs-lookup"><span data-stu-id="6e01a-117">Return value</span></span>

<span data-ttu-id="6e01a-118">當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="6e01a-118">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="6e01a-119">備註</span><span class="sxs-lookup"><span data-stu-id="6e01a-119">Remarks</span></span>

<span data-ttu-id="6e01a-120">呼叫端必須是系統管理員。</span><span class="sxs-lookup"><span data-stu-id="6e01a-120">The caller must be an administrator.</span></span>

## <a name="requirements"></a><span data-ttu-id="6e01a-121">規格需求</span><span class="sxs-lookup"><span data-stu-id="6e01a-121">Requirements</span></span>



| <span data-ttu-id="6e01a-122">需求</span><span class="sxs-lookup"><span data-stu-id="6e01a-122">Requirement</span></span> | <span data-ttu-id="6e01a-123">值</span><span class="sxs-lookup"><span data-stu-id="6e01a-123">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="6e01a-124">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6e01a-124">Minimum supported client</span></span><br/> | <span data-ttu-id="6e01a-125">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e01a-125">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="6e01a-126">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6e01a-126">Minimum supported server</span></span><br/> | <span data-ttu-id="6e01a-127">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6e01a-127">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="6e01a-128">DLL</span><span class="sxs-lookup"><span data-stu-id="6e01a-128">DLL</span></span><br/>                      | <dl> <span data-ttu-id="6e01a-129"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="6e01a-129"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="6e01a-130">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6e01a-130">See also</span></span>

<dl> <dt>

[<span data-ttu-id="6e01a-131">**BaseFlushAppcompatCache**</span><span class="sxs-lookup"><span data-stu-id="6e01a-131">**BaseFlushAppcompatCache**</span></span>](baseflushappcompatcache.md)
</dt> </dl>

 

 




