---
title: 'TBN_MAPACCELERATOR (Commctrl 的通知碼) '
description: 要求工具列中對應至指定之快速鍵字元的按鈕索引。 此通知碼會以 WM 通知訊息的形式傳送 \_ 。
ms.assetid: 16d16560-62ef-4457-bf8c-bc6dddb520d7
keywords:
- TBN_MAPACCELERATOR 通知碼 Windows 控制項
topic_type:
- apiref
api_name:
- TBN_MAPACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: d4b20f1908f441c38e23aa7428f8c8edb8a192c7
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933907"
---
# <a name="tbn_mapaccelerator-notification-code"></a><span data-ttu-id="78841-105">TBN \_ MAPACCELERATOR 通知碼</span><span class="sxs-lookup"><span data-stu-id="78841-105">TBN\_MAPACCELERATOR notification code</span></span>

<span data-ttu-id="78841-106">要求工具列中對應至指定之快速鍵字元的按鈕索引。</span><span class="sxs-lookup"><span data-stu-id="78841-106">Requests the index of the button in the toolbar corresponding to the specified accelerator character.</span></span> <span data-ttu-id="78841-107">此通知碼會以 [**WM \_ 通知**](wm-notify.md) 訊息的形式傳送。</span><span class="sxs-lookup"><span data-stu-id="78841-107">This notification code is sent in the form of a [**WM\_NOTIFY**](wm-notify.md) message.</span></span>


```C++
TBN_MAPACCELERATOR

    lpnmtb = (NMCHAR*) lParam; 
```



## <a name="parameters"></a><span data-ttu-id="78841-108">參數</span><span class="sxs-lookup"><span data-stu-id="78841-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="78841-109">*lParam*</span><span class="sxs-lookup"><span data-stu-id="78841-109">*lParam*</span></span> 
</dt> <dd>

<span data-ttu-id="78841-110">[**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar)結構的指標，其中包含快速鍵字元，並會接收對應按鈕的索引。</span><span class="sxs-lookup"><span data-stu-id="78841-110">A pointer to an [**NMCHAR**](/windows/win32/api/commctrl/ns-commctrl-nmchar) structure that contains the accelerator key character and that receives the index of the corresponding button.</span></span> <span data-ttu-id="78841-111">如果快速鍵未對應至命令， **dwItemNext** 欄位會是-1。</span><span class="sxs-lookup"><span data-stu-id="78841-111">The **dwItemNext** field is -1 if the accelerator does not correspond to a command.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="78841-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="78841-112">Return value</span></span>

<span data-ttu-id="78841-113">如果 **NMCHAR. dwItemNext** 設定為值，則為 TRUE。</span><span class="sxs-lookup"><span data-stu-id="78841-113">TRUE if **NMCHAR.dwItemNext** is set to a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="78841-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="78841-114">Requirements</span></span>



| <span data-ttu-id="78841-115">需求</span><span class="sxs-lookup"><span data-stu-id="78841-115">Requirement</span></span> | <span data-ttu-id="78841-116">值</span><span class="sxs-lookup"><span data-stu-id="78841-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="78841-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="78841-117">Minimum supported client</span></span><br/> | <span data-ttu-id="78841-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78841-118">Windows Vista \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="78841-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="78841-119">Minimum supported server</span></span><br/> | <span data-ttu-id="78841-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="78841-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="78841-121">標頭</span><span class="sxs-lookup"><span data-stu-id="78841-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="78841-122"><dt>Commctrl。h</dt></span><span class="sxs-lookup"><span data-stu-id="78841-122"><dt>Commctrl.h</dt></span></span> </dl> |



 

 





