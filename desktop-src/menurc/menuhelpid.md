---
title: MENUHELPID 結構
description: '\_如果 POPUPMENUITEM 結構的 resInfo 成員設定為 MFR POPUP，則包含針對功能表或子功能表，寫入至 RT 功能表資源的最終資料 \_ 。'
ms.assetid: f17fdaaa-b37c-4902-bad4-a1181ffee9f9
keywords:
- MENUHELPID 結構功能表和其他資源
topic_type:
- apiref
api_name:
- MENUHELPID
api_type:
- NA
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: 0b90b5a4745433c92a859a168611aa1c14f1fa45
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106970455"
---
# <a name="menuhelpid-structure"></a><span data-ttu-id="3f100-104">MENUHELPID 結構</span><span class="sxs-lookup"><span data-stu-id="3f100-104">MENUHELPID structure</span></span>

<span data-ttu-id="3f100-105">如果 [**POPUPMENUITEM**](popupmenuitem.md)結構的 **resInfo** 成員設定為 **MFR \_ POPUP**，則包含針對功能表或子功能表，寫入至 [**RT \_ 功能表**](/windows/desktop/menurc/resource-types)資源的最終資料。</span><span class="sxs-lookup"><span data-stu-id="3f100-105">Contains the final data written to the [**RT\_MENU**](/windows/desktop/menurc/resource-types) resource for a menu or submenu if the **resInfo** member of the [**POPUPMENUITEM**](popupmenuitem.md) structure is set to **MFR\_POPUP**.</span></span> <span data-ttu-id="3f100-106">此處提供的結構定義僅供說明之用;它不會出現在任何標準標頭檔中。</span><span class="sxs-lookup"><span data-stu-id="3f100-106">The structure definition provided here is for explanation only; it is not present in any standard header file.</span></span>

## <a name="syntax"></a><span data-ttu-id="3f100-107">語法</span><span class="sxs-lookup"><span data-stu-id="3f100-107">Syntax</span></span>


```C++
typedef struct {
  DWORD helpID;
} MENUHELPID;
```



## <a name="members"></a><span data-ttu-id="3f100-108">成員</span><span class="sxs-lookup"><span data-stu-id="3f100-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="3f100-109">**h**</span><span class="sxs-lookup"><span data-stu-id="3f100-109">**helpID**</span></span>
</dt> <dd>

<span data-ttu-id="3f100-110">類型： **DWORD**</span><span class="sxs-lookup"><span data-stu-id="3f100-110">Type: **DWORD**</span></span>

</dd> <dd>

<span data-ttu-id="3f100-111">在 [**WM \_**](/windows/desktop/shell/wm-help) 說明處理期間用來識別功能表的識別碼。</span><span class="sxs-lookup"><span data-stu-id="3f100-111">The identifier used to identify the menu during [**WM\_HELP**](/windows/desktop/shell/wm-help) processing.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="3f100-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="3f100-112">Requirements</span></span>



| <span data-ttu-id="3f100-113">需求</span><span class="sxs-lookup"><span data-stu-id="3f100-113">Requirement</span></span> | <span data-ttu-id="3f100-114">值</span><span class="sxs-lookup"><span data-stu-id="3f100-114">Value</span></span> |
|-------------------------------------|------------------------------------------------------------|
| <span data-ttu-id="3f100-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3f100-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3f100-116">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f100-116">Windows 2000 Professional \[desktop apps only\]</span></span><br/> |
| <span data-ttu-id="3f100-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3f100-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3f100-118">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3f100-118">Windows 2000 Server \[desktop apps only\]</span></span><br/>       |



## <a name="see-also"></a><span data-ttu-id="3f100-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3f100-119">See also</span></span>

<dl> <dt>

<span data-ttu-id="3f100-120">**參考**</span><span class="sxs-lookup"><span data-stu-id="3f100-120">**Reference**</span></span>
</dt> <dt>

[<span data-ttu-id="3f100-121">**MENUHEADER**</span><span class="sxs-lookup"><span data-stu-id="3f100-121">**MENUHEADER**</span></span>](menuheader.md)
</dt> <dt>

[<span data-ttu-id="3f100-122">**POPUPMENUITEM**</span><span class="sxs-lookup"><span data-stu-id="3f100-122">**POPUPMENUITEM**</span></span>](popupmenuitem.md)
</dt> <dt>

<span data-ttu-id="3f100-123">**概念**</span><span class="sxs-lookup"><span data-stu-id="3f100-123">**Conceptual**</span></span>
</dt> <dt>

[<span data-ttu-id="3f100-124">資源</span><span class="sxs-lookup"><span data-stu-id="3f100-124">Resources</span></span>](resources.md)
</dt> </dl>

 

