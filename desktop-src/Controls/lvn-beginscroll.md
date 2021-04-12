---
title: 'LVN_BEGINSCROLL (Commctrl 的通知碼) '
description: 當滾動操作開始時，通知清單視圖控制項的父視窗。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 67123db1-118c-43d7-8511-12a3c4413958
keywords:
- LVN_BEGINSCROLL 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- LVN_BEGINSCROLL
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ae09a05525ac6e9f08d8cc7a0b7de6ef51329baa
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464405"
---
# <a name="lvn_beginscroll-notification-code"></a><span data-ttu-id="986ce-105">LVN \_ BEGINSCROLL 通知碼</span><span class="sxs-lookup"><span data-stu-id="986ce-105">LVN\_BEGINSCROLL notification code</span></span>

<span data-ttu-id="986ce-106">當滾動操作開始時，通知清單視圖控制項的父視窗。</span><span class="sxs-lookup"><span data-stu-id="986ce-106">Notifies a list-view control's parent window when a scrolling operation starts.</span></span> <span data-ttu-id="986ce-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="986ce-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
LVN_BEGINSCROLL

    pnmLVScroll = (LPNMLVSCROLL) lParam;
```



## <a name="parameters"></a><span data-ttu-id="986ce-108">參數</span><span class="sxs-lookup"><span data-stu-id="986ce-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="986ce-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="986ce-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="986ce-110">[**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll)結構的指標，其中包含捲軸作業開始的水準或垂直位置。</span><span class="sxs-lookup"><span data-stu-id="986ce-110">Pointer to a [**NMLVSCROLL**](/windows/win32/api/commctrl/ns-commctrl-nmlvscroll) structure that contains the horizontal or vertical position of where the scroll operation starts.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="986ce-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="986ce-111">Return value</span></span>

<span data-ttu-id="986ce-112">未使用傳回值。</span><span class="sxs-lookup"><span data-stu-id="986ce-112">Return value not used.</span></span>

## <a name="remarks"></a><span data-ttu-id="986ce-113">備註</span><span class="sxs-lookup"><span data-stu-id="986ce-113">Remarks</span></span>

> [!Note]  
> <span data-ttu-id="986ce-114">若要使用此通知碼，您必須提供指定 Comclt32.dll 版本6.0 的資訊清單。</span><span class="sxs-lookup"><span data-stu-id="986ce-114">To use this notification code, you must provide a manifest specifying Comclt32.dll version 6.0.</span></span> <span data-ttu-id="986ce-115">如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。</span><span class="sxs-lookup"><span data-stu-id="986ce-115">For more information on manifests, see [Enabling Visual Styles](cookbook-overview.md).</span></span>

 

## <a name="requirements"></a><span data-ttu-id="986ce-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="986ce-116">Requirements</span></span>



| <span data-ttu-id="986ce-117">需求</span><span class="sxs-lookup"><span data-stu-id="986ce-117">Requirement</span></span> | <span data-ttu-id="986ce-118">值</span><span class="sxs-lookup"><span data-stu-id="986ce-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="986ce-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="986ce-119">Minimum supported client</span></span><br/> | <span data-ttu-id="986ce-120">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="986ce-120">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="986ce-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="986ce-121">Minimum supported server</span></span><br/> | <span data-ttu-id="986ce-122">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="986ce-122">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="986ce-123">標頭</span><span class="sxs-lookup"><span data-stu-id="986ce-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="986ce-124"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="986ce-124"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





