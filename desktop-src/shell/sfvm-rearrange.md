---
description: 通知 IShellView 重新排列其專案。 由 SHShellFolderView \_ 訊息使用。
title: 'SFVM_REARRANGE 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: d745bafc-f2f5-40a1-b7e8-e16e4cf0153d
api_name:
- SFVM_REARRANGE
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 524b507ed5af08fbf70b51d9252e7bcb12af1f27
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027504"
---
# <a name="sfvm_rearrange-message"></a><span data-ttu-id="6c3f6-104">SFVM \_ 重新排列訊息</span><span class="sxs-lookup"><span data-stu-id="6c3f6-104">SFVM\_REARRANGE message</span></span>

<span data-ttu-id="6c3f6-105">通知 [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) 重新排列其專案。</span><span class="sxs-lookup"><span data-stu-id="6c3f6-105">Notifies the [**IShellView**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview) to rearrange its items.</span></span> <span data-ttu-id="6c3f6-106">由 [**SHShellFolderView \_ 訊息**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message)使用。</span><span class="sxs-lookup"><span data-stu-id="6c3f6-106">Used by [**SHShellFolderView\_Message**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shshellfolderview_message).</span></span>


```C++
SFVM_REARRANGE 

    lParam = (LPARAM) lparam;

            
```



## <a name="parameters"></a><span data-ttu-id="6c3f6-107">參數</span><span class="sxs-lookup"><span data-stu-id="6c3f6-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c3f6-108">*lParam* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c3f6-108">*lParam* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c3f6-109">傳遞至 [**IShellFolder：： CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids)。</span><span class="sxs-lookup"><span data-stu-id="6c3f6-109">Passed to [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids).</span></span> <span data-ttu-id="6c3f6-110">如需此參數的詳細資訊，請參閱 [**IShellFolder：： CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) 。</span><span class="sxs-lookup"><span data-stu-id="6c3f6-110">See [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) for more information on this parameter.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="6c3f6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="6c3f6-111">Return value</span></span>

<span data-ttu-id="6c3f6-112">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="6c3f6-112">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="6c3f6-113">備註</span><span class="sxs-lookup"><span data-stu-id="6c3f6-113">Remarks</span></span>

## <a name="requirements"></a><span data-ttu-id="6c3f6-114">需求</span><span class="sxs-lookup"><span data-stu-id="6c3f6-114">Requirements</span></span>



| <span data-ttu-id="6c3f6-115">需求</span><span class="sxs-lookup"><span data-stu-id="6c3f6-115">Requirement</span></span> | <span data-ttu-id="6c3f6-116">值</span><span class="sxs-lookup"><span data-stu-id="6c3f6-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6c3f6-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c3f6-117">Minimum supported client</span></span><br/> | <span data-ttu-id="6c3f6-118">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c3f6-118">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="6c3f6-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c3f6-119">Minimum supported server</span></span><br/> | <span data-ttu-id="6c3f6-120">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c3f6-120">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6c3f6-121">標頭</span><span class="sxs-lookup"><span data-stu-id="6c3f6-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c3f6-122"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c3f6-122"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




