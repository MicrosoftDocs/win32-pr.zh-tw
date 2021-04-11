---
description: 搜尋指定的可執行檔。
ms.assetid: 32c6b054-7e47-4427-bdfe-6b5066db4ac3
title: SdbGetMatchingExe 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- SdbGetMatchingExe
api_type:
- DllExport
api_location:
- Apphelp.dll
ms.openlocfilehash: 9d9c8c8c5e9ba0c55068558698b40c7274929364
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847257"
---
# <a name="sdbgetmatchingexe-function"></a><span data-ttu-id="a60da-103">SdbGetMatchingExe 函式</span><span class="sxs-lookup"><span data-stu-id="a60da-103">SdbGetMatchingExe function</span></span>

<span data-ttu-id="a60da-104">搜尋指定的可執行檔。</span><span class="sxs-lookup"><span data-stu-id="a60da-104">Searches for the specified executable.</span></span>

## <a name="syntax"></a><span data-ttu-id="a60da-105">語法</span><span class="sxs-lookup"><span data-stu-id="a60da-105">Syntax</span></span>


```C++
BOOL WINAPI SdbGetMatchingExe(
  _In_opt_ HSDB            hSDB,
  _In_     LPCTSTR         szPath,
  _In_opt_ LPCTSTR         szModuleName,
  _In_opt_ LPCTSTR         pszEnvironment,
  _In_     DWORD           dwFlags,
  _Out_    PSDBQUERYRESULT pQueryResult
);
```



## <a name="parameters"></a><span data-ttu-id="a60da-106">參數</span><span class="sxs-lookup"><span data-stu-id="a60da-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a60da-107">*hSDB* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a60da-107">*hSDB* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a60da-108">[**SdbInitDatabase**](sdbinitdatabase.md)函式所傳回之填充碼資料庫的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a60da-108">A handle to the shim database returned by the [**SdbInitDatabase**](sdbinitdatabase.md) function.</span></span>

</dd> <dt>

<span data-ttu-id="a60da-109">*szPath* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a60da-109">*szPath* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a60da-110">可執行檔的路徑。</span><span class="sxs-lookup"><span data-stu-id="a60da-110">The path of the executable.</span></span>

</dd> <dt>

<span data-ttu-id="a60da-111">*szModuleName* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a60da-111">*szModuleName* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a60da-112">模組名稱。</span><span class="sxs-lookup"><span data-stu-id="a60da-112">The module name.</span></span>

</dd> <dt>

<span data-ttu-id="a60da-113">*pszEnvironment* \[在中，選擇性\]</span><span class="sxs-lookup"><span data-stu-id="a60da-113">*pszEnvironment* \[in, optional\]</span></span>
</dt> <dd>

<span data-ttu-id="a60da-114">要用作搜尋內容的環境變數。</span><span class="sxs-lookup"><span data-stu-id="a60da-114">The environment variables to be used as search context.</span></span>

</dd> <dt>

<span data-ttu-id="a60da-115">*dwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="a60da-115">*dwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="a60da-116">此參數可以是0或 **SDBGMEF \_ 忽略 \_ 環境** (0x1) 。</span><span class="sxs-lookup"><span data-stu-id="a60da-116">This parameter can be 0 or **SDBGMEF\_IGNORE\_ENVIRONMENT** (0x1).</span></span>

</dd> <dt>

<span data-ttu-id="a60da-117">*pQueryResult* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="a60da-117">*pQueryResult* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="a60da-118">[**SDBQUERYRESULT**](sdbqueryresult.md)結構。</span><span class="sxs-lookup"><span data-stu-id="a60da-118">An [**SDBQUERYRESULT**](sdbqueryresult.md) structure.</span></span> <span data-ttu-id="a60da-119">如果找不到相符項，則結構會包含 **TAGREF \_ Null**。</span><span class="sxs-lookup"><span data-stu-id="a60da-119">If no match is found, the structure contains **TAGREF\_NULL**.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a60da-120">傳回值</span><span class="sxs-lookup"><span data-stu-id="a60da-120">Return value</span></span>

<span data-ttu-id="a60da-121">當失敗時，函數會傳回 **TRUE** 或 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="a60da-121">The function returns **TRUE** on success or **FALSE** on failure.</span></span>

## <a name="remarks"></a><span data-ttu-id="a60da-122">備註</span><span class="sxs-lookup"><span data-stu-id="a60da-122">Remarks</span></span>

<span data-ttu-id="a60da-123">當您完成傳回的 [**TAGREF**](tagref.md)時，請使用 [**SdbReleaseMatchingExe**](sdbreleasematchingexe.md) 函式來釋放它。</span><span class="sxs-lookup"><span data-stu-id="a60da-123">When you have finished with the returned [**TAGREF**](tagref.md), free it using the [**SdbReleaseMatchingExe**](sdbreleasematchingexe.md) function.</span></span>

## <a name="requirements"></a><span data-ttu-id="a60da-124">規格需求</span><span class="sxs-lookup"><span data-stu-id="a60da-124">Requirements</span></span>



| <span data-ttu-id="a60da-125">需求</span><span class="sxs-lookup"><span data-stu-id="a60da-125">Requirement</span></span> | <span data-ttu-id="a60da-126">值</span><span class="sxs-lookup"><span data-stu-id="a60da-126">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="a60da-127">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a60da-127">Minimum supported client</span></span><br/> | <span data-ttu-id="a60da-128">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a60da-128">Windows Vista \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="a60da-129">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a60da-129">Minimum supported server</span></span><br/> | <span data-ttu-id="a60da-130">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a60da-130">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="a60da-131">DLL</span><span class="sxs-lookup"><span data-stu-id="a60da-131">DLL</span></span><br/>                      | <dl> <span data-ttu-id="a60da-132"><dt>Apphelp.dll</dt></span><span class="sxs-lookup"><span data-stu-id="a60da-132"><dt>Apphelp.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a60da-133">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a60da-133">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a60da-134">**SdbInitDatabase**</span><span class="sxs-lookup"><span data-stu-id="a60da-134">**SdbInitDatabase**</span></span>](sdbinitdatabase.md)
</dt> <dt>

[<span data-ttu-id="a60da-135">**SdbReleaseMatchingExe**</span><span class="sxs-lookup"><span data-stu-id="a60da-135">**SdbReleaseMatchingExe**</span></span>](sdbreleasematchingexe.md)
</dt> </dl>

 

 




