---
description: 如果 URL 代表實際的 Shell 資料來源 (也稱為 Shell 命名空間延伸) ，則取得 ISearchItem 物件。
ms.assetid: 7da6344d-b433-48c3-8f75-7bef0295b9ea
title: ISearchItem：： GetParentFolder 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISearchItem.GetParentFolder
api_type:
- COM
api_location: ''
ms.openlocfilehash: 4209b319e066d5481c669bcca021684f87532a3a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973230"
---
# <a name="isearchitemgetparentfolder-method"></a><span data-ttu-id="fb0fa-103">ISearchItem：： GetParentFolder 方法</span><span class="sxs-lookup"><span data-stu-id="fb0fa-103">ISearchItem::GetParentFolder method</span></span>

<span data-ttu-id="fb0fa-104">如果 URL 代表實際的 Shell 資料來源 (也稱為 Shell 命名空間延伸) ，則取得 [**ISearchItem**](-search-isearchitem.md) 物件。</span><span class="sxs-lookup"><span data-stu-id="fb0fa-104">Gets the [**ISearchItem**](-search-isearchitem.md) object if the URL represents an actual Shell data source (also known as a Shell namespace extension).</span></span>

## <a name="syntax"></a><span data-ttu-id="fb0fa-105">語法</span><span class="sxs-lookup"><span data-stu-id="fb0fa-105">Syntax</span></span>


```C++
HRESULT GetParentFolder(
  [out] ppShellFolder **IShellFolder,
  [out] ppidl         *LPITEMIDLIST
);
```



## <a name="parameters"></a><span data-ttu-id="fb0fa-106">參數</span><span class="sxs-lookup"><span data-stu-id="fb0fa-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="fb0fa-107">*IShellFolder* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fb0fa-107">*IShellFolder* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb0fa-108">類型： **ppShellFolder \* \***</span><span class="sxs-lookup"><span data-stu-id="fb0fa-108">Type: **ppShellFolder\*\***</span></span>

<span data-ttu-id="fb0fa-109">傳回時，包含包含目前 URL 之資料夾的指標位址。</span><span class="sxs-lookup"><span data-stu-id="fb0fa-109">On return, contains the address of a pointer to the folder that contains the current URL.</span></span> <span data-ttu-id="fb0fa-110">[IShellFolder 介面](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) 會由所有 Shell 命名空間資料夾物件公開，並使用其方法來管理資料夾。</span><span class="sxs-lookup"><span data-stu-id="fb0fa-110">[IShellFolder Interface](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishellfolder) is exposed by all Shell namespace folder objects, and its methods are used to manage folders.</span></span>

</dd> <dt>

<span data-ttu-id="fb0fa-111">*LPITEMIDLIST* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="fb0fa-111">*LPITEMIDLIST* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="fb0fa-112">類型： \**ppidl \** _</span><span class="sxs-lookup"><span data-stu-id="fb0fa-112">Type: \**ppidl\** _</span></span>

<span data-ttu-id="fb0fa-113">傳回時，包含識別父資料夾 (PIDL) 之專案識別碼清單的指標位址。</span><span class="sxs-lookup"><span data-stu-id="fb0fa-113">On return, contains the address of a pointer to an item identifier list (PIDL) that identifies the parent folder.</span></span> <span data-ttu-id="fb0fa-114">_LPITEMIDLIST \* 參數可以參考命名空間階層中父資料夾底下任何層級的物件，因此可以是 **pidl** 相對於父資料夾的多層指標。</span><span class="sxs-lookup"><span data-stu-id="fb0fa-114">The _LPITEMIDLIST\* parameter can refer to an object at any level below the parent folder in the namespace hierarchy, and can thus be a multi-level pointer to a **pidl** relative to the parent folder.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="fb0fa-115">傳回值</span><span class="sxs-lookup"><span data-stu-id="fb0fa-115">Return value</span></span>

<span data-ttu-id="fb0fa-116">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="fb0fa-116">Type: **HRESULT**</span></span>

<span data-ttu-id="fb0fa-117">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="fb0fa-117">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="fb0fa-118">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="fb0fa-118">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="fb0fa-119">備註</span><span class="sxs-lookup"><span data-stu-id="fb0fa-119">Remarks</span></span>

<span data-ttu-id="fb0fa-120">只有在 Windows XP 和 Windows Server 2003 上才支援 **ISearchItem：： GetParentFolder** 方法，且不應再使用。</span><span class="sxs-lookup"><span data-stu-id="fb0fa-120">The **ISearchItem::GetParentFolder** method is supported only on Windows XP and Windows Server 2003, and should no longer be used.</span></span>

<span data-ttu-id="fb0fa-121">若要在執行 Windows XP 或 Windows Server 2003 的電腦上使用協力廠商通訊協定處理常式來預覽附件，可能需要使用 [**ISearchItem**](-search-isearchitem.md) 介面和下列 Api： [**IItemPreviewerExt**](-search-iitempreviewerext.md)、 [**IItemPropertyBag**](iitempropertybag.md)和 [**ISearchProtocolUI**](-search-isearchprotocolui.md) 介面、 [**LINKINFO**](-search-linkinfo.md) 結構和 [**LINKTYPE**](-search-linktype.md) 列舉。</span><span class="sxs-lookup"><span data-stu-id="fb0fa-121">To preview attachments with a third-party protocol handler on computers running Windows XP or Windows Server 2003, it may be necessary to use the [**ISearchItem**](-search-isearchitem.md) interface, and the following APIs: the [**IItemPreviewerExt**](-search-iitempreviewerext.md), [**IItemPropertyBag**](iitempropertybag.md), and [**ISearchProtocolUI**](-search-isearchprotocolui.md) interfaces, the [**LINKINFO**](-search-linkinfo.md) structure, and the [**LINKTYPE**](-search-linktype.md) enumeration.</span></span>

## <a name="requirements"></a><span data-ttu-id="fb0fa-122">規格需求</span><span class="sxs-lookup"><span data-stu-id="fb0fa-122">Requirements</span></span>



| <span data-ttu-id="fb0fa-123">需求</span><span class="sxs-lookup"><span data-stu-id="fb0fa-123">Requirement</span></span> | <span data-ttu-id="fb0fa-124">值</span><span class="sxs-lookup"><span data-stu-id="fb0fa-124">Value</span></span> |
|-------------------------------------|------------------------------------------------------|
| <span data-ttu-id="fb0fa-125">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="fb0fa-125">Minimum supported client</span></span><br/> | <span data-ttu-id="fb0fa-126">僅限 Windows XP （含 SP2） \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb0fa-126">Windows XP with SP2 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fb0fa-127">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="fb0fa-127">Minimum supported server</span></span><br/> | <span data-ttu-id="fb0fa-128">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="fb0fa-128">Windows Server 2003 \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="fb0fa-129">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="fb0fa-129">Redistributable</span></span><br/>          | <span data-ttu-id="fb0fa-130">Windows 桌面搜尋 (WDS) 3。0</span><span class="sxs-lookup"><span data-stu-id="fb0fa-130">Windows Desktop Search (WDS) 3.0</span></span><br/>          |



## <a name="see-also"></a><span data-ttu-id="fb0fa-131">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb0fa-131">See also</span></span>

<dl> <dt>

[<span data-ttu-id="fb0fa-132">**ISearchItem**</span><span class="sxs-lookup"><span data-stu-id="fb0fa-132">**ISearchItem**</span></span>](-search-isearchitem.md)
</dt> </dl>

 

 
