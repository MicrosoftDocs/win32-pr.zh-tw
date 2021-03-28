---
description: 將這個指標變成專案識別碼清單 (PIDL) Shell 資料夾的無效部分。
title: IShellFolderSearchable：： InvalidateSearch 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable.InvalidateSearch
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 6985a299-8547-4db4-99f9-d46dafe4789b
ms.openlocfilehash: 36c1de0a606fdfddbe8eb74b5cc6c20cdda8e983
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191614"
---
# <a name="ishellfoldersearchableinvalidatesearch-method"></a><span data-ttu-id="ef1ee-103">IShellFolderSearchable：： InvalidateSearch 方法</span><span class="sxs-lookup"><span data-stu-id="ef1ee-103">IShellFolderSearchable::InvalidateSearch method</span></span>

<span data-ttu-id="ef1ee-104">將這個指標變成專案識別碼清單 (PIDL) Shell 資料夾的無效部分。</span><span class="sxs-lookup"><span data-stu-id="ef1ee-104">Makes this pointer to an item identifier list (PIDL) an invalid portion of the Shell folder.</span></span>

## <a name="syntax"></a><span data-ttu-id="ef1ee-105">語法</span><span class="sxs-lookup"><span data-stu-id="ef1ee-105">Syntax</span></span>


```C++
HRESULT InvalidateSearch(
  [in] LPCITEMIDLIST pidlSearch,
  [in] DWORD         *pdwFlags
);
```



## <a name="parameters"></a><span data-ttu-id="ef1ee-106">參數</span><span class="sxs-lookup"><span data-stu-id="ef1ee-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ef1ee-107">*pidlSearch* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef1ee-107">*pidlSearch* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef1ee-108">類型： **LPCITEMIDLIST**</span><span class="sxs-lookup"><span data-stu-id="ef1ee-108">Type: **LPCITEMIDLIST**</span></span>

<span data-ttu-id="ef1ee-109">搜尋資料夾之 [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) 結構的指標。</span><span class="sxs-lookup"><span data-stu-id="ef1ee-109">A pointer to the [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) structure for the search folder.</span></span>

</dd> <dt>

<span data-ttu-id="ef1ee-110">*pdwFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="ef1ee-110">*pdwFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="ef1ee-111">類型： \**DWORD \** _</span><span class="sxs-lookup"><span data-stu-id="ef1ee-111">Type: \**DWORD\** _</span></span>

<span data-ttu-id="ef1ee-112">目前未定義任何旗標;設定為 _ \* Null \* \*。</span><span class="sxs-lookup"><span data-stu-id="ef1ee-112">No flags are currently defined; set to _\*NULL\*\*.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ef1ee-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="ef1ee-113">Return value</span></span>

<span data-ttu-id="ef1ee-114">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="ef1ee-114">Type: **HRESULT**</span></span>

<span data-ttu-id="ef1ee-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ef1ee-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ef1ee-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ef1ee-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="ef1ee-117">備註</span><span class="sxs-lookup"><span data-stu-id="ef1ee-117">Remarks</span></span>

<span data-ttu-id="ef1ee-118">當搜尋資料夾無效時，它可以對其使用的任何資源執行清除。</span><span class="sxs-lookup"><span data-stu-id="ef1ee-118">When a search folder is invalidated, it can perform cleanup of any resources it has used.</span></span> <span data-ttu-id="ef1ee-119">**IShellFolderSearchable：： InvalidateSearch** 方法可能會導致取消非同步搜尋，而且會產生 [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md)介面物件的最終版本。</span><span class="sxs-lookup"><span data-stu-id="ef1ee-119">The **IShellFolderSearchable::InvalidateSearch** method may cause an asynchronous search to be canceled and will result in the eventual release of the [**IShellFolderSearchableCallback**](ishellfoldersearchablecallback.md) interface object.</span></span>

## <a name="requirements"></a><span data-ttu-id="ef1ee-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="ef1ee-120">Requirements</span></span>



| <span data-ttu-id="ef1ee-121">需求</span><span class="sxs-lookup"><span data-stu-id="ef1ee-121">Requirement</span></span> | <span data-ttu-id="ef1ee-122">值</span><span class="sxs-lookup"><span data-stu-id="ef1ee-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ef1ee-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ef1ee-123">Minimum supported client</span></span><br/> | <span data-ttu-id="ef1ee-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef1ee-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ef1ee-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ef1ee-125">Minimum supported server</span></span><br/> | <span data-ttu-id="ef1ee-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ef1ee-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ef1ee-127">DLL</span><span class="sxs-lookup"><span data-stu-id="ef1ee-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ef1ee-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ef1ee-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 




