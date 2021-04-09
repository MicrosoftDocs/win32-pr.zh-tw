---
title: 'TBN_GETINFOTIP (Commctrl 的通知碼) '
description: 抓取工具列專案的資訊提示資訊。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 877de60c-f6e1-440a-81f0-d66ab443c985
keywords:
- TBN_GETINFOTIP 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_GETINFOTIP
- TBN_GETINFOTIPA
- TBN_GETINFOTIPW
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: fda2c1b181ebea1840b153b8b2df8328b3f2cc8d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104024841"
---
# <a name="tbn_getinfotip-notification-code"></a><span data-ttu-id="371f3-105">TBN \_ GETINFOTIP 通知碼</span><span class="sxs-lookup"><span data-stu-id="371f3-105">TBN\_GETINFOTIP notification code</span></span>

<span data-ttu-id="371f3-106">抓取工具列專案的資訊提示資訊。</span><span class="sxs-lookup"><span data-stu-id="371f3-106">Retrieves infotip information for a toolbar item.</span></span> <span data-ttu-id="371f3-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="371f3-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_GETINFOTIP

    lptbgit = (LPNMTBGETINFOTIP) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="371f3-108">參數</span><span class="sxs-lookup"><span data-stu-id="371f3-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="371f3-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="371f3-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="371f3-110">[**NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa)結構的指標，其中包含專案資訊和接收資訊提示資訊。</span><span class="sxs-lookup"><span data-stu-id="371f3-110">Pointer to an [**NMTBGETINFOTIP**](/windows/win32/api/commctrl/ns-commctrl-nmtbgetinfotipa) structure that contains item information and receives infotip information.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="371f3-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="371f3-111">Return value</span></span>

<span data-ttu-id="371f3-112">控制項會忽略傳回值。</span><span class="sxs-lookup"><span data-stu-id="371f3-112">The return value is ignored by the control.</span></span>

## <a name="remarks"></a><span data-ttu-id="371f3-113">備註</span><span class="sxs-lookup"><span data-stu-id="371f3-113">Remarks</span></span>

<span data-ttu-id="371f3-114">工具列中的提示支援可讓工具列顯示最大 INFOTIPSIZE 字元之專案的工具提示。</span><span class="sxs-lookup"><span data-stu-id="371f3-114">The infotip support in the toolbar allows the toolbar to display tooltips for items that are as large as INFOTIPSIZE characters.</span></span> <span data-ttu-id="371f3-115">如果未處理此通知碼，工具列將會使用專案提示的文字。</span><span class="sxs-lookup"><span data-stu-id="371f3-115">If this notification code is not processed, the toolbar will use the item's text for the infotip.</span></span>

## <a name="requirements"></a><span data-ttu-id="371f3-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="371f3-116">Requirements</span></span>



| <span data-ttu-id="371f3-117">需求</span><span class="sxs-lookup"><span data-stu-id="371f3-117">Requirement</span></span> | <span data-ttu-id="371f3-118">值</span><span class="sxs-lookup"><span data-stu-id="371f3-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="371f3-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="371f3-119">Minimum supported client</span></span><br/> | <span data-ttu-id="371f3-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="371f3-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="371f3-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="371f3-121">Minimum supported server</span></span><br/> | <span data-ttu-id="371f3-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="371f3-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="371f3-123">標頭</span><span class="sxs-lookup"><span data-stu-id="371f3-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="371f3-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="371f3-124"><dt>Commctrl.h</dt></span></span> </dl> |
| <span data-ttu-id="371f3-125">Unicode 與 ANSI 名稱</span><span class="sxs-lookup"><span data-stu-id="371f3-125">Unicode and ANSI names</span></span><br/>   | <span data-ttu-id="371f3-126">**TBN \_GETINFOTIPW** (Unicode) 和 **TBN \_ GETINFOTIPA** (ANSI) </span><span class="sxs-lookup"><span data-stu-id="371f3-126">**TBN\_GETINFOTIPW** (Unicode) and **TBN\_GETINFOTIPA** (ANSI)</span></span><br/>             |



 

 





