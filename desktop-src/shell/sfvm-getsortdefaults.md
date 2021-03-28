---
description: 允許回呼物件指定預設排序參數。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_GETSORTDEFAULTS 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: edd428f2-50d9-4819-ba77-df51262e33ff
api_name:
- SFVM_GETSORTDEFAULTS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: db6477cc9660f8084e2bf8298e028ed7a445f26c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973813"
---
# <a name="sfvm_getsortdefaults-message"></a><span data-ttu-id="3c802-104">SFVM \_ GETSORTDEFAULTS 訊息</span><span class="sxs-lookup"><span data-stu-id="3c802-104">SFVM\_GETSORTDEFAULTS message</span></span>

<span data-ttu-id="3c802-105">允許回呼物件指定預設排序參數。</span><span class="sxs-lookup"><span data-stu-id="3c802-105">Allows the callback object to specify a default sorting parameter.</span></span> <span data-ttu-id="3c802-106">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="3c802-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETSORTDEFAULTS 

    wParam = (WPARAM)(int*) iDirection;

    lParam = (LPARAM)(int*) iColumn;

            
```



## <a name="parameters"></a><span data-ttu-id="3c802-107">參數</span><span class="sxs-lookup"><span data-stu-id="3c802-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3c802-108">*iDirection* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3c802-108">*iDirection* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c802-109">預設的排序方向。</span><span class="sxs-lookup"><span data-stu-id="3c802-109">The default sorting direction.</span></span> <span data-ttu-id="3c802-110">將此參數設定為正數值，以遞增順序排序。</span><span class="sxs-lookup"><span data-stu-id="3c802-110">Set this parameter to a positive value to sort in ascending order.</span></span> <span data-ttu-id="3c802-111">將此參數設定為零或負數值，以遞減順序排序。</span><span class="sxs-lookup"><span data-stu-id="3c802-111">Set this parameter to zero or a negative value to sort in descending order.</span></span>

</dd> <dt>

<span data-ttu-id="3c802-112">*iColumn* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3c802-112">*iColumn* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3c802-113">用於排序的資料行。</span><span class="sxs-lookup"><span data-stu-id="3c802-113">The column used for the sort.</span></span> <span data-ttu-id="3c802-114">這會在其 *lParam* 值的較低16位中傳遞給 [**IShellFolder：： CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) 。</span><span class="sxs-lookup"><span data-stu-id="3c802-114">This will be passed to the [**IShellFolder::CompareIDs**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids) in the lower 16 bits of its *lParam* value.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="3c802-115">備註</span><span class="sxs-lookup"><span data-stu-id="3c802-115">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="3c802-116">：系統資料夾 view 物件無法辨識 **SFVM \_ GETSORTDEFAULTS** 。</span><span class="sxs-lookup"><span data-stu-id="3c802-116">: **SFVM\_GETSORTDEFAULTS** is not recognized by the system folder view object.</span></span>

 

## <a name="requirements"></a><span data-ttu-id="3c802-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3c802-117">Requirements</span></span>



| <span data-ttu-id="3c802-118">需求</span><span class="sxs-lookup"><span data-stu-id="3c802-118">Requirement</span></span> | <span data-ttu-id="3c802-119">值</span><span class="sxs-lookup"><span data-stu-id="3c802-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="3c802-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3c802-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3c802-121">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c802-121">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="3c802-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3c802-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3c802-123">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3c802-123">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="3c802-124">標頭</span><span class="sxs-lookup"><span data-stu-id="3c802-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3c802-125"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="3c802-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
