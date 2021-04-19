---
description: '\_ \_ 當 tablet 裝置新增至 Windows 時，會發佈 WM 平板電腦新增的訊息。'
ms.assetid: 74323b34-2364-47eb-b8ac-b97546e43b32
title: 'WM_TABLET_ADDED 訊息 (Tpcshrd .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 9a721f83cbab3c520a5502fa2f1262de9a26b25a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106979729"
---
# <a name="wm_tablet_added-message"></a><span data-ttu-id="91a82-103">WM \_ TABLET \_ 已新增訊息</span><span class="sxs-lookup"><span data-stu-id="91a82-103">WM\_TABLET\_ADDED message</span></span>

<span data-ttu-id="91a82-104">當 tablet 裝置新增至 Windows 時，會發佈 **WM \_ 平板電腦 \_ 新增** 的訊息。</span><span class="sxs-lookup"><span data-stu-id="91a82-104">The **WM\_TABLET\_ADDED** message is posted when a tablet device is added to Windows.</span></span>


```C++
#define WM_TABLET_DEFBASE  0x02C0
#define WM_TABLET_ADDED    (WM_TABLET_DEFBASE + 8)      
```



## <a name="parameters"></a><span data-ttu-id="91a82-105">參數</span><span class="sxs-lookup"><span data-stu-id="91a82-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="91a82-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="91a82-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91a82-107">要新增的平板電腦裝置索引</span><span class="sxs-lookup"><span data-stu-id="91a82-107">Index of tablet device being added</span></span>

</dd> <dt>

<span data-ttu-id="91a82-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="91a82-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="91a82-109">未使用的。</span><span class="sxs-lookup"><span data-stu-id="91a82-109">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="91a82-110">備註</span><span class="sxs-lookup"><span data-stu-id="91a82-110">Remarks</span></span>

<span data-ttu-id="91a82-111">這則訊息會傳送至系統中的所有最上層視窗，包括已停用或隱藏的無主視窗、重迭的視窗和快顯視窗;但是訊息不會傳送至子視窗。</span><span class="sxs-lookup"><span data-stu-id="91a82-111">This message is sent to all top-level windows in the system, including disabled or invisible unowned windows, overlapped windows, and pop-up windows; but the message is not sent to child windows.</span></span>

<span data-ttu-id="91a82-112">在 *wParam* 中傳遞的索引與 [**ITabletManager：： GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) 方法所使用的索引相關。</span><span class="sxs-lookup"><span data-stu-id="91a82-112">The indexes passed in *wParam* are related to the index used by the [**ITabletManager::GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="91a82-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="91a82-113">Requirements</span></span>



| <span data-ttu-id="91a82-114">需求</span><span class="sxs-lookup"><span data-stu-id="91a82-114">Requirement</span></span> | <span data-ttu-id="91a82-115">值</span><span class="sxs-lookup"><span data-stu-id="91a82-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="91a82-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="91a82-116">Minimum supported client</span></span><br/> | <span data-ttu-id="91a82-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="91a82-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="91a82-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="91a82-118">Minimum supported server</span></span><br/> | <span data-ttu-id="91a82-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="91a82-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="91a82-120">標頭</span><span class="sxs-lookup"><span data-stu-id="91a82-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="91a82-121"><dt>Tpcshrd。h</dt></span><span class="sxs-lookup"><span data-stu-id="91a82-121"><dt>Tpcshrd.h</dt></span></span> </dl> |



 

 
