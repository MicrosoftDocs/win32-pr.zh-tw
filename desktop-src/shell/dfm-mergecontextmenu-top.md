---
description: 允許回呼將專案加入至擴充功能表的頂端。
title: 'DFM_MERGECONTEXTMENU_TOP 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: eed6aec6-11a0-4738-b5b9-a455d0e35eac
api_name:
- DFM_MERGECONTEXTMENU_TOP
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 5810b5b6a0fc862b4dd8a9605cb9aa5c0c83afc6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511047"
---
# <a name="dfm_mergecontextmenu_top-message"></a><span data-ttu-id="6c527-103">DFM \_ MERGECONTEXTMENU \_ TOP message</span><span class="sxs-lookup"><span data-stu-id="6c527-103">DFM\_MERGECONTEXTMENU\_TOP message</span></span>

<span data-ttu-id="6c527-104">允許回呼將專案加入至擴充功能表的頂端。</span><span class="sxs-lookup"><span data-stu-id="6c527-104">Allows the callback to add items to the top of the extended menu.</span></span>


```C++
DFM_MERGECONTEXTMENU_TOP

    lParam = (LPARAM)(LPQCMINFO) pqcminfo;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a><span data-ttu-id="6c527-105">參數</span><span class="sxs-lookup"><span data-stu-id="6c527-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="6c527-106">*pqcminfo* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c527-106">*pqcminfo* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c527-107">[**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo)結構的指標，其中包含合併中使用的資訊。</span><span class="sxs-lookup"><span data-stu-id="6c527-107">A pointer to a [**QCMINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-qcminfo) structure containing the information used in the merge.</span></span>

</dd> <dt>

<span data-ttu-id="6c527-108">*uFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="6c527-108">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="6c527-109">指定如何變更內容功能表的旗標。</span><span class="sxs-lookup"><span data-stu-id="6c527-109">Flags specifying how the context menu can be changed.</span></span> <span data-ttu-id="6c527-110">此參數會使用 \_ \* [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)中所述的 CM光圈值。</span><span class="sxs-lookup"><span data-stu-id="6c527-110">This parameter uses the CMF\_\* values described in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="6c527-111">備註</span><span class="sxs-lookup"><span data-stu-id="6c527-111">Remarks</span></span>

<span data-ttu-id="6c527-112">如果專案加入至擴充的內容功能表中，則在使用 [**DFM \_ INVOKECOMMAND**](dfm-invokecommand.md)叫用其中一個專案時，這些專案必須受到適當回應的常式支援。</span><span class="sxs-lookup"><span data-stu-id="6c527-112">If items are added to the extended context menu, they must be supported with routines that respond appropriately when one of those items is invoked using [**DFM\_INVOKECOMMAND**](dfm-invokecommand.md).</span></span>

<span data-ttu-id="6c527-113">這則訊息會傳送至回呼函式或回呼物件（根據預設的內容功能表物件的執行方式而定）。</span><span class="sxs-lookup"><span data-stu-id="6c527-113">This message is sent to either the callback function or the callback object depending on how the default context menu object is implemented.</span></span> <span data-ttu-id="6c527-114">有兩個 Api 適用于其實 [**CDefFolderMenu \_ Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2)、 [**SHCreateDefaultCoNtextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu)。</span><span class="sxs-lookup"><span data-stu-id="6c527-114">There are two APIs for its implementation, [**CDefFolderMenu\_Create2**](/windows/desktop/api/shlobj_core/nf-shlobj_core-cdeffoldermenu_create2), [**SHCreateDefaultContextMenu**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shcreatedefaultcontextmenu).</span></span>

<span data-ttu-id="6c527-115">[**DFM \_INVOKECOMMANDEX**](dfm-invokecommandex.md) 是此訊息的擴充版本，可提供更多的回呼資訊。</span><span class="sxs-lookup"><span data-stu-id="6c527-115">[**DFM\_INVOKECOMMANDEX**](dfm-invokecommandex.md) is an extended version of this message and provides more information to the callback.</span></span> <span data-ttu-id="6c527-116">如果您的實作需要該介面所提供的其他資訊，請使用 **DFM \_ INVOKECOMMANDEX** 。</span><span class="sxs-lookup"><span data-stu-id="6c527-116">Use **DFM\_INVOKECOMMANDEX** if the additional information provided by that interface is needed in your implementation.</span></span>

## <a name="requirements"></a><span data-ttu-id="6c527-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="6c527-117">Requirements</span></span>



| <span data-ttu-id="6c527-118">需求</span><span class="sxs-lookup"><span data-stu-id="6c527-118">Requirement</span></span> | <span data-ttu-id="6c527-119">值</span><span class="sxs-lookup"><span data-stu-id="6c527-119">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="6c527-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="6c527-120">Minimum supported client</span></span><br/> | <span data-ttu-id="6c527-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c527-121">Windows Vista \[desktop apps only\]</span></span><br/>                                      |
| <span data-ttu-id="6c527-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="6c527-122">Minimum supported server</span></span><br/> | <span data-ttu-id="6c527-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="6c527-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="6c527-124">標頭</span><span class="sxs-lookup"><span data-stu-id="6c527-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="6c527-125"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="6c527-125"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




