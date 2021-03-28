---
description: 由預設內容功能表程式傳送，以取得內容功能表中指定命令識別碼的動詞命令。
title: 'DFM_GETVERB 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: bd12a38e-4d50-43ad-9d1f-8fefa90b44f9
api_name:
- DFM_GETVERB
- DFM_GETVERBA
- DFM_GETVERBW
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: bbb1b2fb54aa2b0e4b66cf8fc559c56eb279504d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191174"
---
# <a name="dfm_getverb-message"></a><span data-ttu-id="67763-103">DFM \_ GETVERB 訊息</span><span class="sxs-lookup"><span data-stu-id="67763-103">DFM\_GETVERB message</span></span>

<span data-ttu-id="67763-104">由預設內容功能表程式傳送，以取得內容功能表中指定命令識別碼的動詞命令。</span><span class="sxs-lookup"><span data-stu-id="67763-104">Sent by the default context menu implementation to get the verb for the given command ID in the context menu.</span></span>


```C++

                DFM_GETVERB 

    wParam = (WPARAM)(int) idCmd,cchMax;

    lParam = (LPARAM)(LPTSTR) pszText;

            
```



## <a name="parameters"></a><span data-ttu-id="67763-105">參數</span><span class="sxs-lookup"><span data-stu-id="67763-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="67763-106">中的 *idCmd \_ cchMax* \[\]</span><span class="sxs-lookup"><span data-stu-id="67763-106">*idCmd\_cchMax* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="67763-107">此參數的低序位字組會保存命令識別碼。</span><span class="sxs-lookup"><span data-stu-id="67763-107">The low-order word of this parameter holds the command ID.</span></span> <span data-ttu-id="67763-108">高序位單字會保存 *pszText* 緩衝區中的字元數。</span><span class="sxs-lookup"><span data-stu-id="67763-108">The high-order word holds the number of characters in the *pszText* buffer.</span></span>

</dd> <dt>

<span data-ttu-id="67763-109">*pszText* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="67763-109">*pszText* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="67763-110">包含動詞文字之以 null 結束的字串指標。</span><span class="sxs-lookup"><span data-stu-id="67763-110">A pointer to a null-terminated string that contains the verb text.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="67763-111">備註</span><span class="sxs-lookup"><span data-stu-id="67763-111">Remarks</span></span>

<span data-ttu-id="67763-112">這則訊息會根據預設內容功能表物件的建立方式，傳送至回呼函式或回呼物件。</span><span class="sxs-lookup"><span data-stu-id="67763-112">This message is sent to either the callback function or the callback object depending on how the default context menu object is constructed.</span></span> <span data-ttu-id="67763-113">有兩個 Api 適用于其結構： [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)、 [**SHCreateDefaultCoNtextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu)。</span><span class="sxs-lookup"><span data-stu-id="67763-113">There are two APIs for its construction, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="67763-114">[**DFM \_INVOKECOMMANDEX**](dfm-invokecommandex.md) 是此訊息的擴充版本，可提供更多的回呼資訊。</span><span class="sxs-lookup"><span data-stu-id="67763-114">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="67763-115">如果您的實作需要該介面所提供的其他資訊，請使用 **DFM \_ INVOKECOMMANDEX** 。</span><span class="sxs-lookup"><span data-stu-id="67763-115">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="67763-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="67763-116">Requirements</span></span>



| <span data-ttu-id="67763-117">需求</span><span class="sxs-lookup"><span data-stu-id="67763-117">Requirement</span></span> | <span data-ttu-id="67763-118">值</span><span class="sxs-lookup"><span data-stu-id="67763-118">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="67763-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="67763-119">Minimum supported client</span></span><br/> | <span data-ttu-id="67763-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67763-120">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="67763-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="67763-121">Minimum supported server</span></span><br/> | <span data-ttu-id="67763-122">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="67763-122">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="67763-123">標頭</span><span class="sxs-lookup"><span data-stu-id="67763-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="67763-124"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="67763-124"><dt>Shlobj.h</dt></span></span> </dl> |
| <span data-ttu-id="67763-125">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="67763-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="67763-126">**DFM \_GETVERBW** (Unicode) 和 **DFM \_ GETVERBA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="67763-126">**DFM\_GETVERBW** (Unicode) and **DFM\_GETVERBA** (ANSI)</span></span><br/>                 |



 

 




