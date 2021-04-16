---
title: 'TBN_WRAPHOTITEM (Commctrl 的通知碼) '
description: 通知應用程式有兩個或多個最忙碌專案即將變更的工具列。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 169309ec-68dd-4cbb-8963-f842cf75b4fc
keywords:
- TBN_WRAPHOTITEM 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_WRAPHOTITEM
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 58eb513780da464ead40f8a4fb1264f6268d4370
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465029"
---
# <a name="tbn_wraphotitem-notification-code"></a><span data-ttu-id="00302-105">TBN \_ WRAPHOTITEM 通知碼</span><span class="sxs-lookup"><span data-stu-id="00302-105">TBN\_WRAPHOTITEM notification code</span></span>

<span data-ttu-id="00302-106">通知應用程式有兩個或多個最忙碌專案即將變更的工具列。</span><span class="sxs-lookup"><span data-stu-id="00302-106">Notifies an application with two or more toolbars that the hot item is about to change.</span></span> <span data-ttu-id="00302-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="00302-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_WRAPHOTITEM

    lpnmtb = (NMTBWRAPHOTITEM) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="00302-108">參數</span><span class="sxs-lookup"><span data-stu-id="00302-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="00302-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="00302-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="00302-110">結構的指標，其中包含舊的熱專案 (**iStart**) 以及新的熱專案是否早于 (**iDir** =-1) 或 (**iDir** = 1) 之後，以及熱專案變更的原因。</span><span class="sxs-lookup"><span data-stu-id="00302-110">A pointer to a structure that contains the old hot item (**iStart**) and whether the new hot item is before it (**iDir** = -1) or after it (**iDir** = 1), as well as a reason why the hot item is changing.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="00302-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="00302-111">Return value</span></span>

<span data-ttu-id="00302-112">如果應用程式正在處理熱專案變更本身，則為 **TRUE** ;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="00302-112">**TRUE** if the application is handling the hot item change itself; otherwise **FALSE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="00302-113">備註</span><span class="sxs-lookup"><span data-stu-id="00302-113">Remarks</span></span>

<span data-ttu-id="00302-114">**NMTBWRAPHOTITEM** 結構必須由應用程式定義，如下所示：</span><span class="sxs-lookup"><span data-stu-id="00302-114">The **NMTBWRAPHOTITEM** structure must be defined by the application as follows:</span></span>

``` syntax
typedef struct tagNMTBWRAPHOTITEM {
    NMHDR hdr;
    int iStart;
    int iDir;
    UINT nReason;       // HICF_* flags
} NMTBWRAPHOTITEM, *LPNMTBWRAPHOTITEM;
```

## <a name="requirements"></a><span data-ttu-id="00302-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="00302-115">Requirements</span></span>



| <span data-ttu-id="00302-116">需求</span><span class="sxs-lookup"><span data-stu-id="00302-116">Requirement</span></span> | <span data-ttu-id="00302-117">值</span><span class="sxs-lookup"><span data-stu-id="00302-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="00302-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="00302-118">Minimum supported client</span></span><br/> | <span data-ttu-id="00302-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00302-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="00302-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="00302-120">Minimum supported server</span></span><br/> | <span data-ttu-id="00302-121">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="00302-121">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="00302-122">標頭</span><span class="sxs-lookup"><span data-stu-id="00302-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="00302-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="00302-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





