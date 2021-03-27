---
description: 通知 appbar，使用者已從工作列的快捷方式功能表中選取了 [Cascade]、[水準並排] 或 [垂直並排顯示] 命令。
title: 'ABN_WINDOWARRANGE 訊息 (Shellapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 32eb7298-75ca-4ff8-86cf-7c9ca9d71868
api_name:
- ABN_WINDOWARRANGE
api_type:
- HeaderDef
api_location:
- Shellapi.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: 9e7d19c7233b235a1a73e160eeacb3c51415d0bf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511069"
---
# <a name="abn_windowarrange-message"></a><span data-ttu-id="df1ea-103">ABN \_ WINDOWARRANGE 訊息</span><span class="sxs-lookup"><span data-stu-id="df1ea-103">ABN\_WINDOWARRANGE message</span></span>

<span data-ttu-id="df1ea-104">通知 appbar，使用者已從工作列的快捷方式功能表中選取了 [Cascade]、[水準並排] 或 [垂直並排顯示] 命令。</span><span class="sxs-lookup"><span data-stu-id="df1ea-104">Notifies an appbar that the user has selected the Cascade, Tile Horizontally, or Tile Vertically command from the taskbar's shortcut menu.</span></span>


```C++
ABN_WINDOWARRANGE 



    fBeginning = (BOOL) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="df1ea-105">參數</span><span class="sxs-lookup"><span data-stu-id="df1ea-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="df1ea-106">*fBeginning*</span><span class="sxs-lookup"><span data-stu-id="df1ea-106">*fBeginning*</span></span> 
</dt> <dd>

<span data-ttu-id="df1ea-107">旗標，指定是否要開始串聯或磚作業。</span><span class="sxs-lookup"><span data-stu-id="df1ea-107">A flag specifying whether the cascade or tile operation is beginning.</span></span> <span data-ttu-id="df1ea-108">如果作業正在啟動，而且 windows 尚未移動，這個參數就是 **TRUE** 。</span><span class="sxs-lookup"><span data-stu-id="df1ea-108">This parameter is **TRUE** if the operation is beginning and the windows have not yet been moved.</span></span> <span data-ttu-id="df1ea-109">如果作業已完成，則為 **FALSE** 。</span><span class="sxs-lookup"><span data-stu-id="df1ea-109">It is **FALSE** if the operation has completed.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="df1ea-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="df1ea-110">Return value</span></span>

<span data-ttu-id="df1ea-111">沒有傳回值。</span><span class="sxs-lookup"><span data-stu-id="df1ea-111">No return value.</span></span>

## <a name="remarks"></a><span data-ttu-id="df1ea-112">備註</span><span class="sxs-lookup"><span data-stu-id="df1ea-112">Remarks</span></span>

<span data-ttu-id="df1ea-113">系統會先傳送這則通知訊息，將 *lParam* 設為 **TRUE** ，然後將 *lParam* 設定為 **FALSE**。</span><span class="sxs-lookup"><span data-stu-id="df1ea-113">The system sends this notification message twice first with *lParam* set to **TRUE** and then with *lParam* set to **FALSE**.</span></span> <span data-ttu-id="df1ea-114">第一個通知是在視窗進行串聯或並排顯示之前傳送，而第二個通知則是在發生 cascade 或磚作業之後傳送。</span><span class="sxs-lookup"><span data-stu-id="df1ea-114">The first notification is sent before the windows are cascaded or tiled, and the second is sent after the cascade or tile operation has occurred.</span></span>

## <a name="requirements"></a><span data-ttu-id="df1ea-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="df1ea-115">Requirements</span></span>



| <span data-ttu-id="df1ea-116">需求</span><span class="sxs-lookup"><span data-stu-id="df1ea-116">Requirement</span></span> | <span data-ttu-id="df1ea-117">值</span><span class="sxs-lookup"><span data-stu-id="df1ea-117">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="df1ea-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="df1ea-118">Minimum supported client</span></span><br/> | <span data-ttu-id="df1ea-119">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df1ea-119">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="df1ea-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="df1ea-120">Minimum supported server</span></span><br/> | <span data-ttu-id="df1ea-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="df1ea-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="df1ea-122">標頭</span><span class="sxs-lookup"><span data-stu-id="df1ea-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="df1ea-123"><dt>Shellapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="df1ea-123"><dt>Shellapi.h</dt></span></span> </dl> |



 

 




