---
description: 設定 Windows 工作列的自動隱藏和 alwayson 最上層狀態。
title: 'ABM_SETSTATE 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: a60e156d-19ef-49b9-83fc-138d1a2169f2
api_name:
- ABM_SETSTATE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 3cd21ca49d1a57d870c26e010420f978f1d9b88a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972093"
---
# <a name="abm_setstate-message"></a><span data-ttu-id="46d1b-103">ABM \_ SETSTATE 訊息</span><span class="sxs-lookup"><span data-stu-id="46d1b-103">ABM\_SETSTATE message</span></span>

<span data-ttu-id="46d1b-104">設定 Windows 工作列的自動隱藏和 alwayson 最上層狀態。</span><span class="sxs-lookup"><span data-stu-id="46d1b-104">Sets the autohide and always-on-top states of the Windows taskbar.</span></span>


```C++
SHAppBarMessage(ABM_SETSTATE, pabd); 
```



## <a name="parameters"></a><span data-ttu-id="46d1b-105">參數</span><span class="sxs-lookup"><span data-stu-id="46d1b-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="46d1b-106">*pabd*</span><span class="sxs-lookup"><span data-stu-id="46d1b-106">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="46d1b-107">[**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的指標。</span><span class="sxs-lookup"><span data-stu-id="46d1b-107">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure.</span></span> <span data-ttu-id="46d1b-108">傳送此訊息時，您必須指定 **cbSize** 和 **hWnd** 成員。</span><span class="sxs-lookup"><span data-stu-id="46d1b-108">You must specify the **cbSize** and **hWnd** members when sending this message.</span></span> <span data-ttu-id="46d1b-109">您可以使用下列其中一個值，在 **lParam** 成員中傳送所需狀態的資料。</span><span class="sxs-lookup"><span data-stu-id="46d1b-109">Data for the desired state is sent in the **lParam** member using one of the following values.</span></span>

<dt>

<span id="0"></span>

<span data-ttu-id="46d1b-110"><span id="0"></span>**0**</span><span class="sxs-lookup"><span data-stu-id="46d1b-110"><span id="0"></span>**0**</span></span>


</dt> <dd>

<span data-ttu-id="46d1b-111">自動隱藏和永遠開啟-頂端</span><span class="sxs-lookup"><span data-stu-id="46d1b-111">Autohide and always-on-top both off</span></span>

</dd> <dt>

<span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>

<span data-ttu-id="46d1b-112"><span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>**ABS \_ ALWAYSONTOP**</span><span class="sxs-lookup"><span data-stu-id="46d1b-112"><span id="ABS_ALWAYSONTOP"></span><span id="abs_alwaysontop"></span>**ABS\_ALWAYSONTOP**</span></span>


</dt> <dd>

<span data-ttu-id="46d1b-113">Always on-頂端開啟，自動隱藏</span><span class="sxs-lookup"><span data-stu-id="46d1b-113">Always-on-top on, autohide off</span></span>

</dd> <dt>

<span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>

<span data-ttu-id="46d1b-114"><span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>**ABS 自動 \_ 隱藏**</span><span class="sxs-lookup"><span data-stu-id="46d1b-114"><span id="ABS_AUTOHIDE"></span><span id="abs_autohide"></span>**ABS\_AUTOHIDE**</span></span>


</dt> <dd>

<span data-ttu-id="46d1b-115">自動隱藏開啟、永遠開啟</span><span class="sxs-lookup"><span data-stu-id="46d1b-115">Autohide on, always-on-top off</span></span>

</dd> <dt>

<span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>

<span data-ttu-id="46d1b-116"><span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>**ABS 自動 \_ 隱藏 \| ABS \_ ALWAYSONTOP**</span><span class="sxs-lookup"><span data-stu-id="46d1b-116"><span id="ABS_AUTOHIDE___ABS_ALWAYSONTOP"></span><span id="abs_autohide___abs_alwaysontop"></span>**ABS\_AUTOHIDE \| ABS\_ALWAYSONTOP**</span></span>


</dt> <dd>

<span data-ttu-id="46d1b-117">自動隱藏和隨時開啟</span><span class="sxs-lookup"><span data-stu-id="46d1b-117">Autohide and always-on-top both on</span></span>

</dd> </dl> </dd> </dl>

## <a name="return-value"></a><span data-ttu-id="46d1b-118">傳回值</span><span class="sxs-lookup"><span data-stu-id="46d1b-118">Return value</span></span>

<span data-ttu-id="46d1b-119">一律傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="46d1b-119">Always returns **TRUE**.</span></span>

## <a name="requirements"></a><span data-ttu-id="46d1b-120">規格需求</span><span class="sxs-lookup"><span data-stu-id="46d1b-120">Requirements</span></span>



| <span data-ttu-id="46d1b-121">需求</span><span class="sxs-lookup"><span data-stu-id="46d1b-121">Requirement</span></span> | <span data-ttu-id="46d1b-122">值</span><span class="sxs-lookup"><span data-stu-id="46d1b-122">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="46d1b-123">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="46d1b-123">Minimum supported client</span></span><br/> | <span data-ttu-id="46d1b-124">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46d1b-124">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="46d1b-125">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="46d1b-125">Minimum supported server</span></span><br/> | <span data-ttu-id="46d1b-126">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="46d1b-126">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="46d1b-127">標頭</span><span class="sxs-lookup"><span data-stu-id="46d1b-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="46d1b-128"><dt>Shellapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="46d1b-128"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




