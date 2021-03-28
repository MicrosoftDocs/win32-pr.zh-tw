---
description: 公開方法，讓 Shell 資料夾可在其內容上支援不同的視圖， (其資料) 的不同階層式版面配置。
title: IShellFolderViewType 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IShellFolderViewType
api_type:
- COM
api_location:
- Shell32.dll
ms.assetid: 9b597f6b-ef27-4fa1-ad00-e131dbd979e7
ms.openlocfilehash: 1440b6d14950ad70d2c76168b28bb1077b19b5a3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026730"
---
# <a name="ishellfolderviewtype-interface"></a><span data-ttu-id="ec2cd-103">IShellFolderViewType 介面</span><span class="sxs-lookup"><span data-stu-id="ec2cd-103">IShellFolderViewType interface</span></span>

<span data-ttu-id="ec2cd-104">公開方法，讓 Shell 資料夾可在其內容上支援不同的視圖， (其資料) 的不同階層式版面配置。</span><span class="sxs-lookup"><span data-stu-id="ec2cd-104">Exposes methods that enable a Shell folder to support different views on its content (different hierarchical layouts of its data).</span></span>

## <a name="members"></a><span data-ttu-id="ec2cd-105">成員</span><span class="sxs-lookup"><span data-stu-id="ec2cd-105">Members</span></span>

<span data-ttu-id="ec2cd-106">**IShellFolderViewType** 介面繼承自 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="ec2cd-106">The **IShellFolderViewType** interface inherits from the [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="ec2cd-107">**IShellFolderViewType** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="ec2cd-107">**IShellFolderViewType** also has these types of members:</span></span>

-   [<span data-ttu-id="ec2cd-108">方法</span><span class="sxs-lookup"><span data-stu-id="ec2cd-108">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="ec2cd-109">方法</span><span class="sxs-lookup"><span data-stu-id="ec2cd-109">Methods</span></span>

<span data-ttu-id="ec2cd-110">**IShellFolderViewType** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="ec2cd-110">The **IShellFolderViewType** interface has these methods.</span></span>



| <span data-ttu-id="ec2cd-111">方法</span><span class="sxs-lookup"><span data-stu-id="ec2cd-111">Method</span></span>                                                                      | <span data-ttu-id="ec2cd-112">描述</span><span class="sxs-lookup"><span data-stu-id="ec2cd-112">Description</span></span>                                                                                                                                                          |
|:----------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="ec2cd-113">**EnumViews**</span><span class="sxs-lookup"><span data-stu-id="ec2cd-113">**EnumViews**</span></span>](ishellfolderviewtype-enumviews.md)                         | <span data-ttu-id="ec2cd-114">抓取將為每個擴充視圖傳回一個 PIDL 的列舉值。</span><span class="sxs-lookup"><span data-stu-id="ec2cd-114">Retrieves an enumerator that will return one PIDL for every extended view.</span></span><br/>                                                                                |
| [<span data-ttu-id="ec2cd-115">**GetDefaultViewName**</span><span class="sxs-lookup"><span data-stu-id="ec2cd-115">**GetDefaultViewName**</span></span>](ishellfolderviewtype-getdefaultviewname.md)       | <span data-ttu-id="ec2cd-116">取得預設視圖的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec2cd-116">Gets the name of the default view.</span></span> <span data-ttu-id="ec2cd-117">呼叫 [**IShellFolder：： GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) ，以取出其他視圖的名稱。</span><span class="sxs-lookup"><span data-stu-id="ec2cd-117">Call [**IShellFolder::GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof) to retrieve the names of the other views.</span></span><br/> |
| [<span data-ttu-id="ec2cd-118">**GetViewTypeProperties**</span><span class="sxs-lookup"><span data-stu-id="ec2cd-118">**GetViewTypeProperties**</span></span>](ishellfolderviewtype-getviewtypeproperties.md) | <span data-ttu-id="ec2cd-119">取得視圖的屬性。</span><span class="sxs-lookup"><span data-stu-id="ec2cd-119">Gets the properties of the view.</span></span><br/>                                                                                                                          |
| [<span data-ttu-id="ec2cd-120">**TranslateViewPidl**</span><span class="sxs-lookup"><span data-stu-id="ec2cd-120">**TranslateViewPidl**</span></span>](ishellfolderviewtype-translateviewpidl.md)         | <span data-ttu-id="ec2cd-121">將 Shell 資料夾的階層式標記法中的 PIDL 重建為不同的標記法。</span><span class="sxs-lookup"><span data-stu-id="ec2cd-121">Reconstructs a PIDL from one hierarchical representation of the Shell folder into a different representation.</span></span><br/>                                             |



 

## <a name="remarks"></a><span data-ttu-id="ec2cd-122">備註</span><span class="sxs-lookup"><span data-stu-id="ec2cd-122">Remarks</span></span>

<span data-ttu-id="ec2cd-123">這個列舉值會傳回 Pidl，這是在 Shell 資料夾最上層的特殊隱藏資料夾，不是以其他方式列舉。</span><span class="sxs-lookup"><span data-stu-id="ec2cd-123">This enumerator returns PIDLs that are special hidden folders at the top level of the Shell folder, which are not otherwise enumerated.</span></span> <span data-ttu-id="ec2cd-124">預設視圖是 Shell 資料夾通常會顯示的一個。</span><span class="sxs-lookup"><span data-stu-id="ec2cd-124">The default view is the one the Shell folder displays normally.</span></span>

<span data-ttu-id="ec2cd-125">這個介面未定義在任何公用標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="ec2cd-125">This interface is not defined in any public header file.</span></span> <span data-ttu-id="ec2cd-126">如果您選擇執行這個介面，您可以使用下列 C/c + + 程式碼來宣告其方法。</span><span class="sxs-lookup"><span data-stu-id="ec2cd-126">Should you choose to implement this interface, you can use the following C/C++ code to declare its methods.</span></span>


```
#undef  INTERFACE
#define INTERFACE   IShellFolderViewType
DECLARE_INTERFACE_IID_(IShellFolderViewType, IUnknown, "49422C1E-1C03-11d2-8DAB-0000F87A556C")
{
    // **_ IUnknown methods _*_
    STDMETHOD(QueryInterface) (THIS_ REFIID riid, __out void _*ppv) PURE;
    STDMETHOD_(ULONG,AddRef)  (THIS) PURE;
    STDMETHOD_(ULONG,Release) (THIS) PURE;

    // **_ IShellFolderViewType Methods _*_

    // EnumViews:
    //   Returns an enumerator which will give out one pidl for every extended view.
    STDMETHOD(EnumViews)(THIS_ ULONG grfFlags, __out IEnumIDList _*ppenum) PURE;

    // GetDefaultViewName:
    //   Returns the name of the default view.  The names of the other views
    //   can be retrieved by calling GetDisplayNameOf.
    STDMETHOD(GetDefaultViewName)(THIS_ DWORD  uFlags, __out LPWSTR *ppwszName) PURE;
    STDMETHOD(GetViewTypeProperties)(THIS_ PCUITEMID_CHILD pidl, __out DWORD *pdwFlags)  PURE;

    // TranslateViewPidl:
    //   Attempts to take a pidl represented in one hierarchical representation of
    //   the Shell folder, and find it in a different representation.
    //   pidl should be relative to the root folder.
    //   Remember to ILFree ppidlOut
    STDMETHOD(TranslateViewPidl)(THIS_ PCUIDLIST_RELATIVE pidl, PCUIDLIST_RELATIVE pidlView,
              __out PIDLIST_RELATIVE *ppidlOut) PURE;
};

#define SFVTFLAG_NOTIFY_CREATE  0x00000001
#define SFVTFLAG_NOTIFY_RESORT  0x00000002
```



## <a name="requirements"></a><span data-ttu-id="ec2cd-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="ec2cd-127">Requirements</span></span>



| <span data-ttu-id="ec2cd-128">需求</span><span class="sxs-lookup"><span data-stu-id="ec2cd-128">Requirement</span></span> | <span data-ttu-id="ec2cd-129">值</span><span class="sxs-lookup"><span data-stu-id="ec2cd-129">Value</span></span> |
|-------------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="ec2cd-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ec2cd-130">Minimum supported client</span></span><br/> | <span data-ttu-id="ec2cd-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec2cd-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="ec2cd-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ec2cd-132">Minimum supported server</span></span><br/> | <span data-ttu-id="ec2cd-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ec2cd-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                   |
| <span data-ttu-id="ec2cd-134">DLL</span><span class="sxs-lookup"><span data-stu-id="ec2cd-134">DLL</span></span><br/>                      | <dl> <span data-ttu-id="ec2cd-135"><dt>Shell32.dll</dt></span><span class="sxs-lookup"><span data-stu-id="ec2cd-135"><dt>Shell32.dll</dt></span></span> </dl> |



 

 
