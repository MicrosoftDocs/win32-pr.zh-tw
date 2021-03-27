---
description: 開始搜尋指定的搜尋字串。
ms.assetid: 6ecad03c-e8e0-45ba-8def-b55a029992f2
title: 'IShellFolderSearchable：： FindString 方法 (Mmc.exe) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.FindString
api_type:
- COM
api_location:
- Shell32.dll
ms.openlocfilehash: 3e256329bc235f7fe5a0428ba33710fa6b838f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691208"
---
# <a name="ishellfoldersearchablefindstring-method"></a><span data-ttu-id="84ffd-103">IShellFolderSearchable：： FindString 方法</span><span class="sxs-lookup"><span data-stu-id="84ffd-103">IShellFolderSearchable::FindString method</span></span>

<span data-ttu-id="84ffd-104">開始搜尋指定的搜尋字串。</span><span class="sxs-lookup"><span data-stu-id="84ffd-104">Begins a search for a specified search string.</span></span>

## <a name="syntax"></a><span data-ttu-id="84ffd-105">語法</span><span class="sxs-lookup"><span data-stu-id="84ffd-105">Syntax</span></span>


```C++
HRESULT FindString(
  [in]  LPCWSTR      pwszTarget,
  [in]  DWORD        *pdwFlags,
  [in]  IUnknown     *punkOnAsyncSearch,
  [out] LPITEMIDLIST ppidlOut
);
```



## <a name="parameters"></a><span data-ttu-id="84ffd-106">參數</span><span class="sxs-lookup"><span data-stu-id="84ffd-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="84ffd-107">*pwszTarget* \[在\]</span><span class="sxs-lookup"><span data-stu-id="84ffd-107">*pwszTarget* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84ffd-108">類型： **LPCWSTR**</span><span class="sxs-lookup"><span data-stu-id="84ffd-108">Type: **LPCWSTR**</span></span>

<span data-ttu-id="84ffd-109">指定搜尋關鍵字之字串的指標。</span><span class="sxs-lookup"><span data-stu-id="84ffd-109">A pointer to a string that specifies the search keyword.</span></span>

</dd> <dt>

<span data-ttu-id="84ffd-110">*pdwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="84ffd-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84ffd-111">類型： \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="84ffd-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="84ffd-112">目前未定義任何旗標;設定為 _ \* Null \* \*。</span><span class="sxs-lookup"><span data-stu-id="84ffd-112">No flags are currently defined; set to _\*NULL\*\*.</span></span>

</dd> <dt>

<span data-ttu-id="84ffd-113">*punkOnAsyncSearch* \[在\]</span><span class="sxs-lookup"><span data-stu-id="84ffd-113">*punkOnAsyncSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="84ffd-114">類型： \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) \** _</span><span class="sxs-lookup"><span data-stu-id="84ffd-114">Type: \**[**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)\** _</span></span>

<span data-ttu-id="84ffd-115">[_ *IUnknown* \*](/windows/win32/api/unknwn/nn-unknwn-iunknown)類型之物件的指標。</span><span class="sxs-lookup"><span data-stu-id="84ffd-115">A pointer to an object of type [_ *IUnknown*\*](/windows/win32/api/unknwn/nn-unknwn-iunknown).</span></span> <span data-ttu-id="84ffd-116">這個物件必須支援 [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) 介面。</span><span class="sxs-lookup"><span data-stu-id="84ffd-116">This object must support the [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) interface.</span></span> <span data-ttu-id="84ffd-117">如果不需要回呼，請設定為 **Null** 。</span><span class="sxs-lookup"><span data-stu-id="84ffd-117">Set to **NULL** if no callback is necessary.</span></span>

</dd> <dt>

<span data-ttu-id="84ffd-118">*ppidlOut* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="84ffd-118">*ppidlOut* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="84ffd-119">類型： **LPITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="84ffd-119">Type: **LPITEMIDLIST**</span></span>

<span data-ttu-id="84ffd-120">搜尋資料夾之 [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="84ffd-120">A pointer to an [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure for the search folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="84ffd-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="84ffd-121">Return value</span></span>

<span data-ttu-id="84ffd-122">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="84ffd-122">Type: **HRESULT**</span></span>

<span data-ttu-id="84ffd-123">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="84ffd-123">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="84ffd-124">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="84ffd-124">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="84ffd-125">規格需求</span><span class="sxs-lookup"><span data-stu-id="84ffd-125">Requirements</span></span>



| <span data-ttu-id="84ffd-126">需求</span><span class="sxs-lookup"><span data-stu-id="84ffd-126">Requirement</span></span> | <span data-ttu-id="84ffd-127">值</span><span class="sxs-lookup"><span data-stu-id="84ffd-127">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="84ffd-128">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="84ffd-128">Minimum supported client</span></span><br/> | <span data-ttu-id="84ffd-129">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84ffd-129">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="84ffd-130">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="84ffd-130">Minimum supported server</span></span><br/> | <span data-ttu-id="84ffd-131">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="84ffd-131">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="84ffd-132">標頭</span><span class="sxs-lookup"><span data-stu-id="84ffd-132">Header</span></span><br/>                   | <dl> <span data-ttu-id="84ffd-133"><dt>Mmc.exe</dt></span><span class="sxs-lookup"><span data-stu-id="84ffd-133"><dt>Mmc.h</dt></span></span> </dl>       |
| <span data-ttu-id="84ffd-134">DLL</span><span class="sxs-lookup"><span data-stu-id="84ffd-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="84ffd-135"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="84ffd-135"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
