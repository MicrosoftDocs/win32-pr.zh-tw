---
title: 'LVN_ENDSCROLL 訊息 (Commctrl .h) '
description: 當滾動操作結束時，通知清單視圖控制項的父視窗。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 2838dcd0-ac0f-48c7-94ba-dc36febedb94
keywords:
- LVN_ENDSCROLL message Windows 控制項
topic_type:
- apiref
api_name:
- LVN_ENDSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3b9dcdcff2d0bcfc28e1818d5add6d37838e5f9b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103844479"
---
# <a name="lvn_endscroll-message"></a><span data-ttu-id="f1bd6-105">LVN \_ ENDSCROLL 訊息</span><span class="sxs-lookup"><span data-stu-id="f1bd6-105">LVN\_ENDSCROLL message</span></span>

<span data-ttu-id="f1bd6-106">當滾動操作結束時，通知清單視圖控制項的父視窗。</span><span class="sxs-lookup"><span data-stu-id="f1bd6-106">Notifies a list-view control's parent window when a scrolling operation ends.</span></span> <span data-ttu-id="f1bd6-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="f1bd6-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_ENDSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a><span data-ttu-id="f1bd6-108">參數</span><span class="sxs-lookup"><span data-stu-id="f1bd6-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f1bd6-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="f1bd6-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="f1bd6-110">[**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll)結構的指標，其中包含捲軸操作結束位置的水準或垂直位置。</span><span class="sxs-lookup"><span data-stu-id="f1bd6-110">Pointer to a [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) structure that contains the horizontal or vertical position of where the scroll operation ends.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f1bd6-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="f1bd6-111">Return value</span></span>

<span data-ttu-id="f1bd6-112">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="f1bd6-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="f1bd6-113">備註</span><span class="sxs-lookup"><span data-stu-id="f1bd6-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="f1bd6-114">若要使用此通知碼，您必須提供指定 Comclt32.dll 版本6.0 的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="f1bd6-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="f1bd6-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="f1bd6-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="f1bd6-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="f1bd6-116">Requirements</span></span>



| <span data-ttu-id="f1bd6-117">需求</span><span class="sxs-lookup"><span data-stu-id="f1bd6-117">Requirement</span></span> | <span data-ttu-id="f1bd6-118">值</span><span class="sxs-lookup"><span data-stu-id="f1bd6-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f1bd6-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f1bd6-119">Minimum supported client</span></span><br/> | <span data-ttu-id="f1bd6-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1bd6-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f1bd6-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f1bd6-121">Minimum supported server</span></span><br/> | <span data-ttu-id="f1bd6-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f1bd6-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f1bd6-123">標頭</span><span class="sxs-lookup"><span data-stu-id="f1bd6-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="f1bd6-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="f1bd6-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





