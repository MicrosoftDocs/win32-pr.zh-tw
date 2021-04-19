---
title: 'TDN_TIMER (Commctrl 的通知碼) '
description: 工作對話方塊大約每隔200毫秒傳送一次。
ms.assetid: 5a162d97-6912-45bc-8151-1ea56cc459ea
keywords:
- TDN_TIMER 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TDN_TIMER
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2eea7a1604c70c187299c9f2c99abbe934926317
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106966354"
---
# <a name="tdn_timer-notification-code"></a><span data-ttu-id="a6de4-104">TDN \_ 計時器通知碼</span><span class="sxs-lookup"><span data-stu-id="a6de4-104">TDN\_TIMER notification code</span></span>

<span data-ttu-id="a6de4-105">工作對話方塊大約每隔200毫秒傳送一次。</span><span class="sxs-lookup"><span data-stu-id="a6de4-105">Sent by a task dialog approximately every 200 milliseconds.</span></span> <span data-ttu-id="a6de4-106">當已 \_ \_ 在傳遞給 [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect)函式的 [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig)結構的 **dwFlags** 成員中設定 .tdf 回呼計時器旗標時，就會傳送此通知碼。</span><span class="sxs-lookup"><span data-stu-id="a6de4-106">This notification code is sent when the TDF\_CALLBACK\_TIMER flag has been set in the **dwFlags** member of the [**TASKDIALOGCONFIG**](/windows/desktop/api/Commctrl/ns-commctrl-taskdialogconfig) structure that was passed to the [**TaskDialogIndirect**](/windows/desktop/api/Commctrl/nf-commctrl-taskdialogindirect) function.</span></span> <span data-ttu-id="a6de4-107">此通知碼只會透過工作對話方塊回呼函式接收，此函式可以使用 **TaskDialogIndirect** 方法來註冊。</span><span class="sxs-lookup"><span data-stu-id="a6de4-107">This notification code is received only through the task dialog callback function, which can be registered using the **TaskDialogIndirect** method.</span></span>


```C++
TDN_TIMER    

   WPARAM wParam;
   LPARAM lParam;
```



## <a name="parameters"></a><span data-ttu-id="a6de4-108">參數</span><span class="sxs-lookup"><span data-stu-id="a6de4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="a6de4-109">*wParam*</span><span class="sxs-lookup"><span data-stu-id="a6de4-109">*wParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6de4-110">**DWORD** ，指定自建立對話方塊之後的毫秒數，或此通知碼傳回 **\_ FALSE**。</span><span class="sxs-lookup"><span data-stu-id="a6de4-110">A **DWORD** that specifies the number of milliseconds since the dialog was created or this notification code returned **S\_FALSE**.</span></span>

</dd> <dt>

<span data-ttu-id="a6de4-111">*lParam*</span><span class="sxs-lookup"><span data-stu-id="a6de4-111">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="a6de4-112">必須為零。</span><span class="sxs-lookup"><span data-stu-id="a6de4-112">Must be zero.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="a6de4-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="a6de4-113">Return value</span></span>

<span data-ttu-id="a6de4-114">若要重設 tickcount，應用程式必須 **傳回 \_ FALSE**，否則 tickcount 會繼續遞增。</span><span class="sxs-lookup"><span data-stu-id="a6de4-114">To reset the tickcount, the application must return **S\_FALSE**, otherwise the tickcount will continue to increment.</span></span>

## <a name="requirements"></a><span data-ttu-id="a6de4-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="a6de4-115">Requirements</span></span>



| <span data-ttu-id="a6de4-116">需求</span><span class="sxs-lookup"><span data-stu-id="a6de4-116">Requirement</span></span> | <span data-ttu-id="a6de4-117">值</span><span class="sxs-lookup"><span data-stu-id="a6de4-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a6de4-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a6de4-118">Minimum supported client</span></span><br/> | <span data-ttu-id="a6de4-119">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6de4-119">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="a6de4-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a6de4-120">Minimum supported server</span></span><br/> | <span data-ttu-id="a6de4-121">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a6de4-121">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="a6de4-122">標頭</span><span class="sxs-lookup"><span data-stu-id="a6de4-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="a6de4-123"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="a6de4-123"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





