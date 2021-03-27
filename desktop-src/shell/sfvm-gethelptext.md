---
description: 允許回呼物件指定功能表項目或工具列按鈕的解說文字字串。 由 IShellFolderViewCB：： MessageSFVCB 使用。
title: 'SFVM_GETHELPTEXT 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 9bd6d632-308c-4ba5-8ac6-2d0f65853947
api_name:
- SFVM_GETHELPTEXT
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5b33bd99c2dd1e6d1013da9015a5ff70bc111c79
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103693868"
---
# <a name="sfvm_gethelptext-message"></a><span data-ttu-id="e02ec-104">SFVM \_ GETHELPTEXT 訊息</span><span class="sxs-lookup"><span data-stu-id="e02ec-104">SFVM\_GETHELPTEXT message</span></span>

<span data-ttu-id="e02ec-105">允許回呼物件指定功能表項目或工具列按鈕的解說文字字串。</span><span class="sxs-lookup"><span data-stu-id="e02ec-105">Allows the callback object to specify a help text string for menu items or toolbar buttons.</span></span> <span data-ttu-id="e02ec-106">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="e02ec-106">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETHELPTEXT 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="e02ec-107">參數</span><span class="sxs-lookup"><span data-stu-id="e02ec-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="e02ec-108">中的 *idCmd \_ cchMax* \[\]</span><span class="sxs-lookup"><span data-stu-id="e02ec-108">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="e02ec-109">此參數的低序位字組會保存命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="e02ec-109">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="e02ec-110">高序位單字會保存 *pszText* 緩衝區中的字元數。</span><span class="sxs-lookup"><span data-stu-id="e02ec-110">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="e02ec-111">*pszText* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="e02ec-111">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="e02ec-112">包含解說文字且以 null 終止的字串。</span><span class="sxs-lookup"><span data-stu-id="e02ec-112">A null-terminated string containing the help text.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e02ec-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="e02ec-113">Requirements</span></span>



| <span data-ttu-id="e02ec-114">需求</span><span class="sxs-lookup"><span data-stu-id="e02ec-114">Requirement</span></span> | <span data-ttu-id="e02ec-115">值</span><span class="sxs-lookup"><span data-stu-id="e02ec-115">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="e02ec-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e02ec-116">Minimum supported client</span></span><br/> | <span data-ttu-id="e02ec-117">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e02ec-117">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="e02ec-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e02ec-118">Minimum supported server</span></span><br/> | <span data-ttu-id="e02ec-119">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e02ec-119">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="e02ec-120">標頭</span><span class="sxs-lookup"><span data-stu-id="e02ec-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="e02ec-121"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="e02ec-121"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
