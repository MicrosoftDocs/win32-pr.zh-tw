---
title: 'RBN_AUTOSIZE (Commctrl 的通知碼) '
description: 當 Rebar 自動調整大小時，以 RBS AUTOSIZE 樣式建立的 Rebar 控制項傳送 \_ 。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: d174fe99-13cc-404c-9dc5-d5a93e9807a2
keywords:
- RBN_AUTOSIZE 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- RBN_AUTOSIZE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18ecfac5a4f84d69d444c25a24956cb911fd90a4
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106976976"
---
# <a name="rbn_autosize-notification-code"></a><span data-ttu-id="3163b-105">RBN 自動 \_ 調整通知碼</span><span class="sxs-lookup"><span data-stu-id="3163b-105">RBN\_AUTOSIZE notification code</span></span>

<span data-ttu-id="3163b-106">當 Rebar 自動調整大小時，以 [**RBS \_ AUTOSIZE**](rebar-control-styles.md) 樣式建立的 Rebar 控制項傳送。</span><span class="sxs-lookup"><span data-stu-id="3163b-106">Sent by a rebar control created with the [**RBS\_AUTOSIZE**](rebar-control-styles.md) style when the rebar automatically resizes itself.</span></span> <span data-ttu-id="3163b-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="3163b-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
RBN_AUTOSIZE

    lpnmas = (LPNMRBAUTOSIZE) lParam;
```



## <a name="parameters"></a><span data-ttu-id="3163b-108">參數</span><span class="sxs-lookup"><span data-stu-id="3163b-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3163b-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="3163b-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="3163b-110">[**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize)結構的指標，其中包含調整大小作業的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="3163b-110">Pointer to an [**NMRBAUTOSIZE**](/windows/win32/api/commctrl/ns-commctrl-nmrbautosize) structure that contains information about the resize operation.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3163b-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="3163b-111">Return value</span></span>

<span data-ttu-id="3163b-112">未使用此通知的傳回值。</span><span class="sxs-lookup"><span data-stu-id="3163b-112">The return value for this notification is not used.</span></span>

## <a name="requirements"></a><span data-ttu-id="3163b-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="3163b-113">Requirements</span></span>



| <span data-ttu-id="3163b-114">需求</span><span class="sxs-lookup"><span data-stu-id="3163b-114">Requirement</span></span> | <span data-ttu-id="3163b-115">值</span><span class="sxs-lookup"><span data-stu-id="3163b-115">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="3163b-116">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3163b-116">Minimum supported client</span></span><br/> | <span data-ttu-id="3163b-117">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3163b-117">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3163b-118">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3163b-118">Minimum supported server</span></span><br/> | <span data-ttu-id="3163b-119">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3163b-119">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="3163b-120">標頭</span><span class="sxs-lookup"><span data-stu-id="3163b-120">Header</span></span><br/>                   | <dl> <span data-ttu-id="3163b-121"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="3163b-121"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





