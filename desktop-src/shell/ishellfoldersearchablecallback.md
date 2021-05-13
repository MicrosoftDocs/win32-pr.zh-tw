---
description: 公開回呼常式來監視搜尋處理常式。
title: IShellFolderSearchableCallback 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderSearchableCallback
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 3412a01b-d5ea-44e1-819c-f10f81fac391
ms.openlocfilehash: cf1a3b03eed2a15e82e1313875a4ab8584243190
ms.sourcegitcommit: 3caaa3c92dcb1ef12f84464d14ce6262e65e988e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/12/2021
ms.locfileid: "109842779"
---
# <a name="ishellfoldersearchablecallback-interface"></a><span data-ttu-id="86733-103">IShellFolderSearchableCallback 介面</span><span class="sxs-lookup"><span data-stu-id="86733-103">IShellFolderSearchableCallback interface</span></span>

<span data-ttu-id="86733-104">公開回呼常式來監視搜尋處理常式。</span><span class="sxs-lookup"><span data-stu-id="86733-104">Exposes callback routines to monitor the search process.</span></span>

## <a name="members"></a><span data-ttu-id="86733-105">成員</span><span class="sxs-lookup"><span data-stu-id="86733-105">Members</span></span>

<span data-ttu-id="86733-106">**IShellFolderSearchableCallback** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="86733-106">The **IShellFolderSearchableCallback** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="86733-107">**IShellFolderSearchableCallback** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="86733-107">**IShellFolderSearchableCallback** also has these types of members:</span></span>

-   [<span data-ttu-id="86733-108">方法</span><span class="sxs-lookup"><span data-stu-id="86733-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="86733-109">方法</span><span class="sxs-lookup"><span data-stu-id="86733-109">Methods</span></span>

<span data-ttu-id="86733-110">**IShellFolderSearchableCallback** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="86733-110">The **IShellFolderSearchableCallback** interface has these methods.</span></span>



| <span data-ttu-id="86733-111">方法</span><span class="sxs-lookup"><span data-stu-id="86733-111">Method</span></span>                                                      | <span data-ttu-id="86733-112">描述</span><span class="sxs-lookup"><span data-stu-id="86733-112">Description</span></span>                                      |
|:------------------------------------------------------------|:-------------------------------------------------|
| [<span data-ttu-id="86733-113">**RunBegin**</span><span class="sxs-lookup"><span data-stu-id="86733-113">**RunBegin**</span></span>](ishellfoldersearchablecallback-runbegin.md) | <span data-ttu-id="86733-114">表示搜尋已啟動。</span><span class="sxs-lookup"><span data-stu-id="86733-114">Indicates that a search was started.</span></span><br/>  |
| [<span data-ttu-id="86733-115">**RunEnd**</span><span class="sxs-lookup"><span data-stu-id="86733-115">**RunEnd**</span></span>](ishellfoldersearchablecallback-runend.md)     | <span data-ttu-id="86733-116">表示搜尋已完成。</span><span class="sxs-lookup"><span data-stu-id="86733-116">Indicates that a search has finished.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="86733-117">備註</span><span class="sxs-lookup"><span data-stu-id="86733-117">Remarks</span></span>

<span data-ttu-id="86733-118">這個介面未定義在任何公用標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="86733-118">This interface is not defined in any public header files.</span></span> <span data-ttu-id="86733-119">如果您選擇執行這個介面，您可以使用下列 C/c + + 程式碼來宣告其方法。</span><span class="sxs-lookup"><span data-stu-id="86733-119">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


```
#undef  INTERFACE
#define INTERFACE IShellFolderSearchableCallback
DECLARE_INTERFACE_IID_(IShellFolderSearchableCallback, IUnknown, "F98D8294-2BBC-11d2-8DBD-0000F87A556C")
{
    // *** IUnknown methods ***
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void **ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // *** IShellFolderSearchableCallback Methods ***

    STDMETHOD(RunBegin)(THIS_ DWORD dwReserved) PURE;
    STDMETHOD(RunEnd)(THIS_ DWORD dwReserved) PURE;
};
```



## <a name="requirements"></a><span data-ttu-id="86733-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="86733-120">Requirements</span></span>



| <span data-ttu-id="86733-121">需求</span><span class="sxs-lookup"><span data-stu-id="86733-121">Requirement</span></span> | <span data-ttu-id="86733-122">值</span><span class="sxs-lookup"><span data-stu-id="86733-122">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="86733-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="86733-123">Minimum supported client</span></span><br/> | <span data-ttu-id="86733-124">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86733-124">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="86733-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="86733-125">Minimum supported server</span></span><br/> | <span data-ttu-id="86733-126">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="86733-126">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="86733-127">DLL</span><span class="sxs-lookup"><span data-stu-id="86733-127">DLL</span></span><br/>                      | <dl> <span data-ttu-id="86733-128"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="86733-128"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
