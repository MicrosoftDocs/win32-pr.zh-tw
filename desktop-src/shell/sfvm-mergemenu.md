---
description: 允許回呼物件將功能表項目合併到 Windows 檔案總管功能表中。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_MERGEMENU 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 59bb99a3-9a5a-4ea5-9830-b04d7d886b3f
api_name:
- SFVM_MERGEMENU
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5cf95a7576c15ab1c3e64ebe55e244feffa6d86d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973788"
---
# <a name="sfvm_mergemenu-message"></a><span data-ttu-id="aae09-104">SFVM \_ MERGEMENU 訊息</span><span class="sxs-lookup"><span data-stu-id="aae09-104">SFVM\_MERGEMENU message</span></span>

<span data-ttu-id="aae09-105">允許回呼物件將功能表項目合併到 Windows 檔案總管功能表中。</span><span class="sxs-lookup"><span data-stu-id="aae09-105">Allows the callback object to merge menu items into the Windows Explorer menus.</span></span> <span data-ttu-id="aae09-106">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="aae09-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_MERGEMENU 

    lParam = (LPARAM)(LPQCMINFO) pInfo;

            
```



## <a name="parameters"></a><span data-ttu-id="aae09-107">參數</span><span class="sxs-lookup"><span data-stu-id="aae09-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="aae09-108">*pInfo* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="aae09-108">*pInfo* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="aae09-109">[**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo)結構，其中包含將專案合併到功能表中所需的資訊。</span><span class="sxs-lookup"><span data-stu-id="aae09-109">A [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) structure containing the information needed to merge the items into the menu.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="aae09-110">備註</span><span class="sxs-lookup"><span data-stu-id="aae09-110">Remarks</span></span>

<span data-ttu-id="aae09-111">此訊息基本上與自訂資料夾檢視中的 [**IShellBrowser：： InsertMenusSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) 和 [**IShellBrowser：： SetMenuSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) 具有相同的用途。</span><span class="sxs-lookup"><span data-stu-id="aae09-111">This message serves essentially the same purpose as the [**IShellBrowser::InsertMenusSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-insertmenussb) and [**IShellBrowser::SetMenuSB**](/windows/win32/api/shobjidl_core/nf-shobjidl_core-ishellbrowser-setmenusb) in a custom folder view.</span></span> <span data-ttu-id="aae09-112">如需進一步討論，請參閱 *使用 IShellBrowser 來與*[執行資料夾檢視](../lwef/nse-folderview.md)的 Windows 檔案總管一節。</span><span class="sxs-lookup"><span data-stu-id="aae09-112">See the *Using IShellBrowser to Communicate with Windows Explorer* section of [Implementing a Folder View](../lwef/nse-folderview.md) for further discussion.</span></span>

## <a name="requirements"></a><span data-ttu-id="aae09-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="aae09-113">Requirements</span></span>



| <span data-ttu-id="aae09-114">需求</span><span class="sxs-lookup"><span data-stu-id="aae09-114">Requirement</span></span> | <span data-ttu-id="aae09-115">值</span><span class="sxs-lookup"><span data-stu-id="aae09-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="aae09-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="aae09-116">Minimum supported client</span></span><br/> | <span data-ttu-id="aae09-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aae09-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="aae09-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="aae09-118">Minimum supported server</span></span><br/> | <span data-ttu-id="aae09-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="aae09-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="aae09-120">標頭</span><span class="sxs-lookup"><span data-stu-id="aae09-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="aae09-121"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="aae09-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
