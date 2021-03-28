---
description: 從系統的內部清單中移除 appbar，將其取消註冊。 系統不會再將通知訊息傳送至 appbar，或防止其他應用程式使用 appbar 所使用的螢幕區域。
title: 'ABM_REMOVE 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 3da73a52-3dbb-4133-a9bd-86540e1c4154
api_name:
- ABM_REMOVE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 7f4530869b9f68772c28fefd6130ff8e4b6ffbec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847801"
---
# <a name="abm_remove-message"></a><span data-ttu-id="a1924-104">ABM \_ 移除訊息</span><span class="sxs-lookup"><span data-stu-id="a1924-104">ABM\_REMOVE message</span></span>

<span data-ttu-id="a1924-105">從系統的內部清單中移除 appbar，將其取消註冊。</span><span class="sxs-lookup"><span data-stu-id="a1924-105">Unregisters an appbar by removing it from the system's internal list.</span></span> <span data-ttu-id="a1924-106">系統不會再將通知訊息傳送至 appbar，或防止其他應用程式使用 appbar 所使用的螢幕區域。</span><span class="sxs-lookup"><span data-stu-id="a1924-106">The system no longer sends notification messages to the appbar or prevents other applications from using the screen area used by the appbar.</span></span>


```C++
                SHAppBarMessage(ABM_REMOVE, pabd); 
            
```



## <a name="parameters"></a><span data-ttu-id="a1924-107">參數</span><span class="sxs-lookup"><span data-stu-id="a1924-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a1924-108">*pabd*</span><span class="sxs-lookup"><span data-stu-id="a1924-108">*pabd*</span></span> 
</dt> <dd>

<span data-ttu-id="a1924-109">[**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata)結構的指標，其中包含要取消註冊之 appbar 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a1924-109">A pointer to an [**APPBARDATA**](/windows/desktop/api/Shellapi/ns-shellapi-appbardata) structure that contains the handle to the appbar to unregister.</span></span> <span data-ttu-id="a1924-110">傳送此訊息時，您必須指定 **cbSize** 和 **hWnd** 成員;所有其他成員都會被忽略。</span><span class="sxs-lookup"><span data-stu-id="a1924-110">You must specify the **cbSize** and **hWnd** members when sending this message; all other members are ignored.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a1924-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="a1924-111">Return value</span></span>

<span data-ttu-id="a1924-112">一律傳回 **TRUE**。</span><span class="sxs-lookup"><span data-stu-id="a1924-112">Always returns **TRUE**.</span></span>

## <a name="remarks"></a><span data-ttu-id="a1924-113">備註</span><span class="sxs-lookup"><span data-stu-id="a1924-113">Remarks</span></span>

<span data-ttu-id="a1924-114">這則訊息會導致系統將 [**ABN \_ POSCHANGED**](abn-poschanged.md) 通知訊息傳送至所有透過像 appbars。</span><span class="sxs-lookup"><span data-stu-id="a1924-114">This message causes the system to send the [**ABN\_POSCHANGED**](abn-poschanged.md) notification message to all appbars.</span></span>

## <a name="requirements"></a><span data-ttu-id="a1924-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a1924-115">Requirements</span></span>



| <span data-ttu-id="a1924-116">需求</span><span class="sxs-lookup"><span data-stu-id="a1924-116">Requirement</span></span> | <span data-ttu-id="a1924-117">值</span><span class="sxs-lookup"><span data-stu-id="a1924-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a1924-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a1924-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a1924-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a1924-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="a1924-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a1924-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a1924-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a1924-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a1924-122">標頭</span><span class="sxs-lookup"><span data-stu-id="a1924-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a1924-123"><dt>Shellapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="a1924-123"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




