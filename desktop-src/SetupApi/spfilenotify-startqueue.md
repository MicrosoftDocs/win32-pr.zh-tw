---
description: '\_當佇列承諾程式啟動時，會將 SPFILENOTIFY STARTQUEUE 通知傳送至回呼常式。'
ms.assetid: 682c2ce0-0c82-402c-a487-db5f2c377f3f
title: 'SPFILENOTIFY_STARTQUEUE 訊息 (Setupapi.log .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 090e3f97dceb1843d75934dd99cca500e6f93086
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106980452"
---
# <a name="spfilenotify_startqueue-message"></a><span data-ttu-id="765fc-103">SPFILENOTIFY \_ STARTQUEUE 訊息</span><span class="sxs-lookup"><span data-stu-id="765fc-103">SPFILENOTIFY\_STARTQUEUE message</span></span>

<span data-ttu-id="765fc-104">當佇列承諾程式啟動時，會將 **SPFILENOTIFY \_ STARTQUEUE** 通知傳送至回呼常式。</span><span class="sxs-lookup"><span data-stu-id="765fc-104">The **SPFILENOTIFY\_STARTQUEUE** notification is sent to the callback routine when the queue commitment process starts.</span></span>


```C++
SPFILENOTIFY_STARTQUEUE
  Param1 = (UINT) OwnerWindow;
  Param2 = (UINT) 0;
            
```



## <a name="parameters"></a><span data-ttu-id="765fc-105">參數</span><span class="sxs-lookup"><span data-stu-id="765fc-105">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="765fc-106">*Param1*</span><span class="sxs-lookup"><span data-stu-id="765fc-106">*Param1*</span></span> 
</dt> <dd>

<span data-ttu-id="765fc-107">要擁有回呼常式產生之對話方塊的視窗控制碼。</span><span class="sxs-lookup"><span data-stu-id="765fc-107">Handle to the window that is to own the dialog boxes that the callback routine generates.</span></span>

</dd> <dt>

<span data-ttu-id="765fc-108">*Param2*</span><span class="sxs-lookup"><span data-stu-id="765fc-108">*Param2*</span></span> 
</dt> <dd>

<span data-ttu-id="765fc-109">未使用的。</span><span class="sxs-lookup"><span data-stu-id="765fc-109">Unused.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="765fc-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="765fc-110">Return value</span></span>

<span data-ttu-id="765fc-111">如果發生錯誤，回呼常式應呼叫 [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror)，並指定錯誤，然後傳回零。</span><span class="sxs-lookup"><span data-stu-id="765fc-111">If an error occurs, the callback routine should call [**SetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-setlasterror), specifying the error, and then return zero.</span></span> <span data-ttu-id="765fc-112">[**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)函式會傳回 **FALSE** ，而後續對 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)的呼叫將會傳回回呼常式所設定的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="765fc-112">The [**SetupCommitFileQueue**](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea) function will return **FALSE** and a subsequent call to [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror) will return the error code set by the callback routine.</span></span>

<span data-ttu-id="765fc-113">如果未發生任何錯誤，回呼常式應該會傳回非零值。</span><span class="sxs-lookup"><span data-stu-id="765fc-113">If no error occurs, the callback routine should return a nonzero value.</span></span>

## <a name="requirements"></a><span data-ttu-id="765fc-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="765fc-114">Requirements</span></span>



| <span data-ttu-id="765fc-115">需求</span><span class="sxs-lookup"><span data-stu-id="765fc-115">Requirement</span></span> | <span data-ttu-id="765fc-116">值</span><span class="sxs-lookup"><span data-stu-id="765fc-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="765fc-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="765fc-117">Minimum supported client</span></span><br/> | <span data-ttu-id="765fc-118">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="765fc-118">Windows XP \[desktop apps only\]</span></span><br/>                                           |
| <span data-ttu-id="765fc-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="765fc-119">Minimum supported server</span></span><br/> | <span data-ttu-id="765fc-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="765fc-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="765fc-121">標頭</span><span class="sxs-lookup"><span data-stu-id="765fc-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="765fc-122"><dt>Setupapi.log。h</dt></span><span class="sxs-lookup"><span data-stu-id="765fc-122"><dt>Setupapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="765fc-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="765fc-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="765fc-124">概觀</span><span class="sxs-lookup"><span data-stu-id="765fc-124">Overview</span></span>](overview.md)
</dt> <dt>

[<span data-ttu-id="765fc-125">通知</span><span class="sxs-lookup"><span data-stu-id="765fc-125">Notifications</span></span>](notifications.md)
</dt> <dt>

[<span data-ttu-id="765fc-126">**SetupCommitFileQueue**</span><span class="sxs-lookup"><span data-stu-id="765fc-126">**SetupCommitFileQueue**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupcommitfilequeuea)
</dt> <dt>

[<span data-ttu-id="765fc-127">**SetupDefaultQueueCallback**</span><span class="sxs-lookup"><span data-stu-id="765fc-127">**SetupDefaultQueueCallback**</span></span>](/windows/desktop/api/Setupapi/nf-setupapi-setupdefaultqueuecallbacka)
</dt> </dl>

 

