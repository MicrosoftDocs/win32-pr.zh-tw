---
description: 允許回呼修改 \_ 傳遞給 ICoNtextMenu：： QueryCoNtextMenu 的 CFM XXX 值。
title: 'DFM_MODIFYQCMFLAGS 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 2c87e14d-4cf4-425d-a5fe-9dc7530f0e59
api_name:
- DFM_MODIFYQCMFLAGS
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: ff90cfb0e0297e7d3276f00f314fce865920663a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847793"
---
# <a name="dfm_modifyqcmflags-message"></a><span data-ttu-id="c75b8-103">DFM \_ MODIFYQCMFLAGS 訊息</span><span class="sxs-lookup"><span data-stu-id="c75b8-103">DFM\_MODIFYQCMFLAGS message</span></span>

<span data-ttu-id="c75b8-104">允許回呼修改 \_ 傳遞給 [**ICoNtextMenu：： QUERYCONTEXTMENU**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)的 CFM XXX 值。</span><span class="sxs-lookup"><span data-stu-id="c75b8-104">Allows the callback to modify the CFM\_XXX values passed to [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>


```C++
DFM_MODIFYQCMFLAGS

    lParam = (LPARAM)(UINT) *puNewFlags;

    wParam = (WPARAM)(UINT) uFlags;         

            
```



## <a name="parameters"></a><span data-ttu-id="c75b8-105">參數</span><span class="sxs-lookup"><span data-stu-id="c75b8-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c75b8-106">*puNewFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c75b8-106">*puNewFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c75b8-107">新旗標值的指標。</span><span class="sxs-lookup"><span data-stu-id="c75b8-107">A pointer to the new flag values.</span></span>

</dd> <dt>

<span data-ttu-id="c75b8-108">*uFlags* \[在\]</span><span class="sxs-lookup"><span data-stu-id="c75b8-108">*uFlags* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="c75b8-109">指定如何變更內容功能表的旗標。</span><span class="sxs-lookup"><span data-stu-id="c75b8-109">Flags that specify how the context menu can be changed.</span></span> <span data-ttu-id="c75b8-110">此參數會使用 \_ [**ICoNtextMenu：： QueryCoNtextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu)中所述的 CMF XXX 值。</span><span class="sxs-lookup"><span data-stu-id="c75b8-110">This parameter uses the CMF\_XXX values described in [**IContextMenu::QueryContextMenu**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-icontextmenu-querycontextmenu).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="c75b8-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="c75b8-111">Requirements</span></span>



| <span data-ttu-id="c75b8-112">需求</span><span class="sxs-lookup"><span data-stu-id="c75b8-112">Requirement</span></span> | <span data-ttu-id="c75b8-113">值</span><span class="sxs-lookup"><span data-stu-id="c75b8-113">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="c75b8-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c75b8-114">Minimum supported client</span></span><br/> | <span data-ttu-id="c75b8-115">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c75b8-115">Windows 7 \[desktop apps only\]</span></span><br/>                                          |
| <span data-ttu-id="c75b8-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c75b8-116">Minimum supported server</span></span><br/> | <span data-ttu-id="c75b8-117">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c75b8-117">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                             |
| <span data-ttu-id="c75b8-118">標頭</span><span class="sxs-lookup"><span data-stu-id="c75b8-118">Header</span></span><br/>                   | <dl> <span data-ttu-id="c75b8-119"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="c75b8-119"><dt>Shlobj.h</dt></span></span> </dl> |



 

 




