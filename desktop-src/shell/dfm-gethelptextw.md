---
description: 允許回呼物件指定解說文字字串。
title: 'DFM_GETHELPTEXTW 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 85bdd1d0-5b68-44a5-a1b0-4845b5be34d0
api_name:
- DFM_GETHELPTEXTW
- DFM_GETHELPTEXTW
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7ac1e41046b2d757df96e9acf5722710ae832bf4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972020"
---
# <a name="dfm_gethelptextw-message"></a><span data-ttu-id="49c6d-103">DFM \_ GETHELPTEXTW 訊息</span><span class="sxs-lookup"><span data-stu-id="49c6d-103">DFM\_GETHELPTEXTW message</span></span>

<span data-ttu-id="49c6d-104">允許回呼物件指定解說文字字串。</span><span class="sxs-lookup"><span data-stu-id="49c6d-104">Allows the callback object to specify a help text string.</span></span>


```C++
DFM_GETHELPTEXTW 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(WPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="49c6d-105">參數</span><span class="sxs-lookup"><span data-stu-id="49c6d-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="49c6d-106">中的 *idCmd \_ cchMax* \[\]</span><span class="sxs-lookup"><span data-stu-id="49c6d-106">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="49c6d-107">此參數的低序位字組會保存命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="49c6d-107">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="49c6d-108">高序位單字會保存 *pszText* 緩衝區中的字元數。</span><span class="sxs-lookup"><span data-stu-id="49c6d-108">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="49c6d-109">*pszText* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="49c6d-109">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="49c6d-110">包含解說文字且以 null 終止的 Unicode 字串。</span><span class="sxs-lookup"><span data-stu-id="49c6d-110">A null-terminated Unicode string containing the help text.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="49c6d-111">備註</span><span class="sxs-lookup"><span data-stu-id="49c6d-111">Remarks</span></span>

<span data-ttu-id="49c6d-112">這則訊息會根據預設內容功能表物件的建立方式，傳送至回呼函式或回呼物件。</span><span class="sxs-lookup"><span data-stu-id="49c6d-112">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="49c6d-113">有兩個 Api 適用于其結構： [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)、 [**SHCreateDefaultCoNtextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu)。</span><span class="sxs-lookup"><span data-stu-id="49c6d-113">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="49c6d-114">[**DFM \_INVOKECOMMANDEX**](dfm-invokecommandex.md) 是此訊息的擴充版本，可提供更多的回呼資訊。</span><span class="sxs-lookup"><span data-stu-id="49c6d-114">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="49c6d-115">如果您的實作需要該介面所提供的其他資訊，請使用 **DFM \_ INVOKECOMMANDEX** 。</span><span class="sxs-lookup"><span data-stu-id="49c6d-115">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="49c6d-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="49c6d-116">Requirements</span></span>



| <span data-ttu-id="49c6d-117">需求</span><span class="sxs-lookup"><span data-stu-id="49c6d-117">Requirement</span></span> | <span data-ttu-id="49c6d-118">值</span><span class="sxs-lookup"><span data-stu-id="49c6d-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="49c6d-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="49c6d-119">Minimum supported client</span></span><br/> | <span data-ttu-id="49c6d-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49c6d-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="49c6d-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="49c6d-121">Minimum supported server</span></span><br/> | <span data-ttu-id="49c6d-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="49c6d-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="49c6d-123">標頭</span><span class="sxs-lookup"><span data-stu-id="49c6d-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="49c6d-124"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="49c6d-124"><dt>Shlobj.h</dt></span></span> </dl> |
| <span data-ttu-id="49c6d-125">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="49c6d-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="49c6d-126">**DFM \_GETHELPTEXTW** (Unicode) </span><span class="sxs-lookup"><span data-stu-id="49c6d-126">**DFM\_GETHELPTEXTW** (Unicode)</span></span><br/>                                          |



 

 




