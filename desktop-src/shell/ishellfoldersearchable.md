---
description: 公開允許 Shell 延伸模組提供可搜尋的命名空間的方法。
title: IShellFolderSearchable 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchable
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 359def5c-d7ad-46bd-bdda-30a7b3eea56c
ms.openlocfilehash: 1f42b3af012361bfd24c93e03c38e6954eb5326e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972344"
---
# <a name="ishellfoldersearchable-interface"></a><span data-ttu-id="56b90-103">IShellFolderSearchable 介面</span><span class="sxs-lookup"><span data-stu-id="56b90-103">IShellFolderSearchable interface</span></span>

<span data-ttu-id="56b90-104">公開允許 Shell 延伸模組提供可搜尋的命名空間的方法。</span><span class="sxs-lookup"><span data-stu-id="56b90-104">Exposes methods that allow a Shell extension to provide a searchable namespace.</span></span>

## <a name="members"></a><span data-ttu-id="56b90-105">成員</span><span class="sxs-lookup"><span data-stu-id="56b90-105">Members</span></span>

<span data-ttu-id="56b90-106">**IShellFolderSearchable** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="56b90-106">The **IShellFolderSearchable** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="56b90-107">**IShellFolderSearchable** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="56b90-107">**IShellFolderSearchable** also has these types of members:</span></span>

-   [<span data-ttu-id="56b90-108">方法</span><span class="sxs-lookup"><span data-stu-id="56b90-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="56b90-109">方法</span><span class="sxs-lookup"><span data-stu-id="56b90-109">Methods</span></span>

<span data-ttu-id="56b90-110">**IShellFolderSearchable** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="56b90-110">The **IShellFolderSearchable** interface has these methods.</span></span>



| <span data-ttu-id="56b90-111">方法</span><span class="sxs-lookup"><span data-stu-id="56b90-111">Method</span></span>                                                                | <span data-ttu-id="56b90-112">描述</span><span class="sxs-lookup"><span data-stu-id="56b90-112">Description</span></span>                                                               |
|:----------------------------------------------------------------------|:--------------------------------------------------------------------------|
| [<span data-ttu-id="56b90-113">**CancelAsyncSearch**</span><span class="sxs-lookup"><span data-stu-id="56b90-113">**CancelAsyncSearch**</span></span>](ishellfoldersearchable-cancelasyncsearch.md) | <span data-ttu-id="56b90-114">開始取消暫止之非同步搜尋的進程。</span><span class="sxs-lookup"><span data-stu-id="56b90-114">Begins the process of canceling a pending asynchronous search.</span></span><br/> |
| [<span data-ttu-id="56b90-115">**FindString**</span><span class="sxs-lookup"><span data-stu-id="56b90-115">**FindString**</span></span>](ishellfoldersearchable-findstring.md)               | <span data-ttu-id="56b90-116">開始搜尋指定的搜尋字串。</span><span class="sxs-lookup"><span data-stu-id="56b90-116">Begins a search for a specified search string.</span></span><br/>                 |
| [<span data-ttu-id="56b90-117">**InvalidateSearch**</span><span class="sxs-lookup"><span data-stu-id="56b90-117">**InvalidateSearch**</span></span>](ishellfoldersearchable-invalidatesearch.md)   | <span data-ttu-id="56b90-118">讓這個 PIDL 成為 Shell 資料夾的無效部分。</span><span class="sxs-lookup"><span data-stu-id="56b90-118">Makes this PIDL an invalid portion of the Shell folder.</span></span><br/>        |



 

## <a name="remarks"></a><span data-ttu-id="56b90-119">備註</span><span class="sxs-lookup"><span data-stu-id="56b90-119">Remarks</span></span>

<span data-ttu-id="56b90-120">這個介面未定義在任何公用標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="56b90-120">This interface is not defined in any public header files.</span></span> <span data-ttu-id="56b90-121">如果您選擇執行這個介面，您可以使用下列 C/c + + 程式碼來宣告其方法。</span><span class="sxs-lookup"><span data-stu-id="56b90-121">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


```
#undef  INTERFACE
#define INTERFACE IShellFolderSearchable
DECLARE_INTERFACE_IID_(IShellFolderSearchable, IUnknown, "4E1AE66C-204B-11d2-8DB3-0000F87A556C")
{
    // **_ IUnknown methods _*_
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void _*ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // **_ IShellFolderSearchable methods _*_

    // FindString -
    //  The returned Shell folder's enumerator will have any
    //   search hits for the given search string.
    //  punkOnAsyncSearch will be QI'd for IShellFolderSearchableCallback
    STDMETHOD(FindString)(THIS_ LPCWSTR pwszTarget, __inout_opt DWORD _pdwFlags,
                          __in_opt IUnknown *punkOnAsyncSearch, __out LPITEMIDLIST *ppidlOut)   PURE;
    // CancelAsyncSearch -
    //   Begins the process of canceling any pending
    //    asynchronous search from this pidl.
    //    When the search is actually canceled, RunEnd will be called
    //   Returns: S_OK => cancelling, S_FALSE => not running
    STDMETHOD(CancelAsyncSearch) (THIS_ LPCITEMIDLIST pidlSearch, __inout_opt DWORD *pdwFlags) PURE;

    // InvalidateSearch -
    //   Makes this pidl no longer a valid portion of the Shell folder
    //    Also does some cleanup of any databases used in the search and
    //    will cause the eventual release of the callback
    //   May cause async search to be canceled
    STDMETHOD(InvalidateSearch)  (THIS_ LPCITEMIDLIST pidlSearch, __inout_opt DWORD *pdwFlags) PURE;
};
```



## <a name="requirements"></a><span data-ttu-id="56b90-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="56b90-122">Requirements</span></span>



| <span data-ttu-id="56b90-123">需求</span><span class="sxs-lookup"><span data-stu-id="56b90-123">Requirement</span></span> | <span data-ttu-id="56b90-124">值</span><span class="sxs-lookup"><span data-stu-id="56b90-124">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="56b90-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="56b90-125">Minimum supported client</span></span><br/> | <span data-ttu-id="56b90-126">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56b90-126">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="56b90-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="56b90-127">Minimum supported server</span></span><br/> | <span data-ttu-id="56b90-128">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="56b90-128">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="56b90-129">DLL</span><span class="sxs-lookup"><span data-stu-id="56b90-129">DLL</span></span><br/>                      | <dl> <span data-ttu-id="56b90-130"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="56b90-130"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
