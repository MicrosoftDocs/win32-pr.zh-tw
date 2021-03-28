---
description: 通知系統 appbar 已啟用。 Appbar 應該呼叫此訊息以回應 WM \_ 啟動訊息。
ms.assetid: 16011302-7c2d-4c34-9953-51cceb96e4b3
title: 'ABM_ACTI加值稅E 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 94a44bcc33efcd3d1a9af5e7e2abca33893e9fe9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112365"
---
# <a name="abm_activate-message"></a><span data-ttu-id="c36ed-104">ABM \_ 啟動訊息</span><span class="sxs-lookup"><span data-stu-id="c36ed-104">ABM\_ACTIVATE message</span></span>

<span data-ttu-id="c36ed-105">通知系統 appbar 已啟用。</span><span class="sxs-lookup"><span data-stu-id="c36ed-105">Notifies the system that an appbar has been activated.</span></span> <span data-ttu-id="c36ed-106">Appbar 應該呼叫此訊息以回應 [**WM \_ 啟動**](/windows/desktop/inputdev/wm-activate) 訊息。</span><span class="sxs-lookup"><span data-stu-id="c36ed-106">An appbar should call this message in response to the [**WM\_ACTIVATE**](/windows/desktop/inputdev/wm-activate) message.</span></span>


```C++

SHAppBarMessage(ABM_ACTIVATE, pabd); 

            
```



## <a name="parameters"></a><span data-ttu-id="c36ed-107">參數</span><span class="sxs-lookup"><span data-stu-id="c36ed-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="c36ed-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="c36ed-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="c36ed-109">[**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的指標，此結構識別要啟用的 appbar。</span><span class="sxs-lookup"><span data-stu-id="c36ed-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that identifies the appbar to activate.</span></span> <span data-ttu-id="c36ed-110">傳送此訊息時，您必須指定 **cbSize** 和 **hWnd** 成員;所有其他成員都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="c36ed-110">You must specify the **cbSize** and **hWnd** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="c36ed-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="c36ed-111">Return value</span></span>

<span data-ttu-id="c36ed-112">一律傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="c36ed-112">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="c36ed-113">備註</span><span class="sxs-lookup"><span data-stu-id="c36ed-113">Remarks</span></span>

<span data-ttu-id="c36ed-114">如果 *pabd* 所指向之結構的 **hWnd** 成員識別自動隱藏 appbar，則會忽略此訊息。</span><span class="sxs-lookup"><span data-stu-id="c36ed-114">This message is ignored if the **hWnd** member of the structure pointed to by *pabd* identifies an autohide appbar.</span></span> <span data-ttu-id="c36ed-115">系統會自動設定自動隱藏透過像 appbars 的迭置順序。</span><span class="sxs-lookup"><span data-stu-id="c36ed-115">The system automatically sets the z-order for autohide appbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="c36ed-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="c36ed-116">Requirements</span></span>



| <span data-ttu-id="c36ed-117">需求</span><span class="sxs-lookup"><span data-stu-id="c36ed-117">Requirement</span></span> | <span data-ttu-id="c36ed-118">值</span><span class="sxs-lookup"><span data-stu-id="c36ed-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="c36ed-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="c36ed-119">Minimum supported client</span></span><br/> | <span data-ttu-id="c36ed-120">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c36ed-120">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="c36ed-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="c36ed-121">Minimum supported server</span></span><br/> | <span data-ttu-id="c36ed-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="c36ed-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="c36ed-123">標頭</span><span class="sxs-lookup"><span data-stu-id="c36ed-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="c36ed-124"><dt>Shellapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="c36ed-124"><dt>Shellapi.h</dt></span></span> </dl> |



 

