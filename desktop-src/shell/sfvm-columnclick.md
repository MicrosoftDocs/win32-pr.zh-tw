---
description: 通知回呼物件，使用者已按一下資料行標頭，以排序資料夾檢視中的物件清單。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_COLUMNCLICK 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 351be842-6ea5-4223-8162-0e6c4e6a5afb
api_name:
- SFVM_COLUMNCLICK
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bca80554e25378af1c078a36a02222390b771874
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469344"
---
# <a name="sfvm_columnclick-message"></a><span data-ttu-id="4fd5e-104">SFVM \_ COLUMNCLICK 訊息</span><span class="sxs-lookup"><span data-stu-id="4fd5e-104">SFVM\_COLUMNCLICK message</span></span>

<span data-ttu-id="4fd5e-105">通知回呼物件，使用者已按一下資料行標頭，以排序資料夾檢視中的物件清單。</span><span class="sxs-lookup"><span data-stu-id="4fd5e-105">Notifies the callback object that the user has clicked a column header to sort the list of objects in the folder view.</span></span> <span data-ttu-id="4fd5e-106">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="4fd5e-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_COLUMNCLICK 

    wParam = (WPARAM)(UINT)iColumn;

            
```



## <a name="parameters"></a><span data-ttu-id="4fd5e-107">參數</span><span class="sxs-lookup"><span data-stu-id="4fd5e-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="4fd5e-108">*iColumn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="4fd5e-108">*iColumn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="4fd5e-109">已按下之資料行的索引。</span><span class="sxs-lookup"><span data-stu-id="4fd5e-109">The index of the column that was clicked.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="4fd5e-110">備註</span><span class="sxs-lookup"><span data-stu-id="4fd5e-110">Remarks</span></span>

<span data-ttu-id="4fd5e-111">為了回應這項通知，您應該傳回 \_ [確定] 以自行重新排列清單。</span><span class="sxs-lookup"><span data-stu-id="4fd5e-111">In response to this notification, you should return S\_OK to rearrange the list yourself.</span></span> <span data-ttu-id="4fd5e-112">若要讓系統資料夾 view 物件重新排列清單，請傳回 \_ FALSE。</span><span class="sxs-lookup"><span data-stu-id="4fd5e-112">To have the system folder view object rearrange the list, return S\_FALSE.</span></span>

## <a name="requirements"></a><span data-ttu-id="4fd5e-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="4fd5e-113">Requirements</span></span>



| <span data-ttu-id="4fd5e-114">需求</span><span class="sxs-lookup"><span data-stu-id="4fd5e-114">Requirement</span></span> | <span data-ttu-id="4fd5e-115">值</span><span class="sxs-lookup"><span data-stu-id="4fd5e-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="4fd5e-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="4fd5e-116">Minimum supported client</span></span><br/> | <span data-ttu-id="4fd5e-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4fd5e-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="4fd5e-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="4fd5e-118">Minimum supported server</span></span><br/> | <span data-ttu-id="4fd5e-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="4fd5e-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="4fd5e-120">標頭</span><span class="sxs-lookup"><span data-stu-id="4fd5e-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="4fd5e-121"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="4fd5e-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
