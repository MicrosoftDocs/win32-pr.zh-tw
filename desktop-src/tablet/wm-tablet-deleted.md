---
description: '\_ \_ 從 Windows 移除 TABLET 裝置時，會發佈 WM tablet DELETED 訊息。'
ms.assetid: af5be7f0-a213-49a1-800e-c922281522c8
title: 'WM_TABLET_DELETED 訊息 (Tpcshrd .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: da8ade03d199f8ee7a258b9db2aeea039fd725e4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106986333"
---
# <a name="wm_tablet_deleted-message"></a><span data-ttu-id="ea2bc-103">WM \_ TABLET \_ DELETED 訊息</span><span class="sxs-lookup"><span data-stu-id="ea2bc-103">WM\_TABLET\_DELETED message</span></span>

<span data-ttu-id="ea2bc-104">從 Windows 移除 TABLET 裝置時，會發佈 **WM \_ tablet \_ DELETED** 訊息。</span><span class="sxs-lookup"><span data-stu-id="ea2bc-104">The **WM\_TABLET\_DELETED** message is posted when a tablet device is removed from Windows.</span></span>


```C++
#define WM_TABLET_DEFBASE   0x02C0
#define WM_TABLET_DELETED   (WM_TABLET_DEFBASE + 9)     
```



## <a name="parameters"></a><span data-ttu-id="ea2bc-105">參數</span><span class="sxs-lookup"><span data-stu-id="ea2bc-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ea2bc-106">*wParam*</span><span class="sxs-lookup"><span data-stu-id="ea2bc-106">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea2bc-107">要移除的 tablet 裝置索引。</span><span class="sxs-lookup"><span data-stu-id="ea2bc-107">Index of tablet device being removed.</span></span>

</dd> <dt>

<span data-ttu-id="ea2bc-108">*lParam*</span><span class="sxs-lookup"><span data-stu-id="ea2bc-108">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="ea2bc-109">未使用的。</span><span class="sxs-lookup"><span data-stu-id="ea2bc-109">Unused.</span></span>

</dd> </dl>

## <a name="remarks"></a><span data-ttu-id="ea2bc-110">備註</span><span class="sxs-lookup"><span data-stu-id="ea2bc-110">Remarks</span></span>

<span data-ttu-id="ea2bc-111">這則訊息會傳送至系統中的所有最上層視窗，包括已停用或隱藏的無主視窗、重迭的視窗和快顯視窗;但是訊息不會傳送至子視窗。</span><span class="sxs-lookup"><span data-stu-id="ea2bc-111">This message is sent to all top-level windows in the system, including disabled or invisible unowned windows, overlapped windows, and pop-up windows; but the message is not sent to child windows.</span></span>

<span data-ttu-id="ea2bc-112">在 *wParam* 中傳遞的索引與 [**ITabletManager：： GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) 方法所使用的索引相關。</span><span class="sxs-lookup"><span data-stu-id="ea2bc-112">The indexes passed in *wParam* are related to the index used by the [**ITabletManager::GetTablet**](/previous-versions/windows/desktop/legacy/aa373683(v=vs.85)) method.</span></span>

## <a name="requirements"></a><span data-ttu-id="ea2bc-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ea2bc-113">Requirements</span></span>



| <span data-ttu-id="ea2bc-114">需求</span><span class="sxs-lookup"><span data-stu-id="ea2bc-114">Requirement</span></span> | <span data-ttu-id="ea2bc-115">值</span><span class="sxs-lookup"><span data-stu-id="ea2bc-115">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="ea2bc-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ea2bc-116">Minimum supported client</span></span><br/> | <span data-ttu-id="ea2bc-117">僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ea2bc-117">Windows XP Tablet PC Edition \[desktop apps only\]</span></span><br/>                        |
| <span data-ttu-id="ea2bc-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ea2bc-118">Minimum supported server</span></span><br/> | <span data-ttu-id="ea2bc-119">都不支援</span><span class="sxs-lookup"><span data-stu-id="ea2bc-119">None supported</span></span><br/>                                                            |
| <span data-ttu-id="ea2bc-120">標頭</span><span class="sxs-lookup"><span data-stu-id="ea2bc-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="ea2bc-121"><dt>Tpcshrd。h</dt></span><span class="sxs-lookup"><span data-stu-id="ea2bc-121"><dt>Tpcshrd.h</dt></span></span> </dl> |



 

 
