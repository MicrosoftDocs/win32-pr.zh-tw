---
description: 允許回呼物件指定 HTML 說明檔及其內的主題。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_GETHELPTOPIC 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bbe92e9f-4074-4101-a945-072866ab20a8
api_name:
- SFVM_GETHELPTOPIC
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7ebe078934f467407710f0ad493b6088b34d0c8c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103850663"
---
# <a name="sfvm_gethelptopic-message"></a><span data-ttu-id="0a321-104">SFVM \_ GETHELPTOPIC 訊息</span><span class="sxs-lookup"><span data-stu-id="0a321-104">SFVM\_GETHELPTOPIC message</span></span>

<span data-ttu-id="0a321-105">允許回呼物件指定 HTML 說明檔及其內的主題。</span><span class="sxs-lookup"><span data-stu-id="0a321-105">Allows the callback object to specify an HTML Help file and a topic within it.</span></span> <span data-ttu-id="0a321-106">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="0a321-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETHELPTOPIC 

    lParam = (LPARAM)(SFVM_HELPTOPIC_DATA*) phtd;

            
```



## <a name="parameters"></a><span data-ttu-id="0a321-107">參數</span><span class="sxs-lookup"><span data-stu-id="0a321-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="0a321-108">*phtd* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="0a321-108">*phtd* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="0a321-109">[**SFVM \_ HELPTOPIC \_ 資料**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data)結構的位址，指定 HTML 說明檔和主題。</span><span class="sxs-lookup"><span data-stu-id="0a321-109">The address of a [**SFVM\_HELPTOPIC\_DATA**](/windows/desktop/api/shlobj_core/ns-shlobj_core-sfvm_helptopic_data) structure that specifies the HTML Help file and topic.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="0a321-110">規格需求</span><span class="sxs-lookup"><span data-stu-id="0a321-110">Requirements</span></span>



| <span data-ttu-id="0a321-111">需求</span><span class="sxs-lookup"><span data-stu-id="0a321-111">Requirement</span></span> | <span data-ttu-id="0a321-112">值</span><span class="sxs-lookup"><span data-stu-id="0a321-112">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="0a321-113">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0a321-113">Minimum supported client</span></span><br/> | <span data-ttu-id="0a321-114">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a321-114">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="0a321-115">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0a321-115">Minimum supported server</span></span><br/> | <span data-ttu-id="0a321-116">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="0a321-116">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="0a321-117">標頭</span><span class="sxs-lookup"><span data-stu-id="0a321-117">Header</span></span><br/>                   | <dl> <span data-ttu-id="0a321-118"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="0a321-118"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
