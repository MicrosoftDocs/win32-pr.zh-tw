---
description: 傳送至 view 回呼物件的通知，以指定應該註冊變更通知事件的位置和事件。
title: 'SFVM_GETNOTIFY 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.assetid: 87933217-dfa9-4aaf-9630-fa2c302b18fa
api_name:
- SFVM_GETNOTIFY
api_type:
- HeaderDef
api_location:
- Shlobj.h
topic_type:
- APIRef
- kbSyntax
ms.openlocfilehash: f766ee74463dd820c0b55d501d5002a3378a97b7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193576"
---
# <a name="sfvm_getnotify-message"></a><span data-ttu-id="9604a-103">SFVM \_ GETNOTIFY 訊息</span><span class="sxs-lookup"><span data-stu-id="9604a-103">SFVM\_GETNOTIFY message</span></span>

<span data-ttu-id="9604a-104">傳送至 view 回呼物件的通知，以指定應該註冊變更通知事件的位置和事件。</span><span class="sxs-lookup"><span data-stu-id="9604a-104">Notification sent to the view callback object to specify the locations and events that should be registered for change notification events.</span></span> <span data-ttu-id="9604a-105">註冊之後，在這些位置或事件上發生變更時，就會通知 view 回呼物件。</span><span class="sxs-lookup"><span data-stu-id="9604a-105">Once they are registered, when a change occurs in on of these locations or events, the view callback object is notified.</span></span> <span data-ttu-id="9604a-106">這些事件會透過 [**SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) 傳送至 view 回呼，然後由視圖處理。</span><span class="sxs-lookup"><span data-stu-id="9604a-106">These events are sent to the view callback through [**SFVM\_FSNOTIFY**](sfvm-fsnotify.md) and are then handled by the view.</span></span>


```C++
SFVM_GETNOTIFY 

    wParam = (WPARAM)(LPITEMIDLIST*) pidl;

    lParam = (LPARAM)(LONG*) lEvents;

            
```



## <a name="parameters"></a><span data-ttu-id="9604a-107">參數</span><span class="sxs-lookup"><span data-stu-id="9604a-107">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="9604a-108">*pidl* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9604a-108">*pidl* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9604a-109">專案之絕對 Idlist.txt 的指標，此專案應註冊以收到變更的通知。</span><span class="sxs-lookup"><span data-stu-id="9604a-109">A pointer to an absolute IDList of an item for which the view should register to be notified of changes.</span></span> <span data-ttu-id="9604a-110">一般來說，這與所要查看位置的 Idlist.txt 相同，但它可以是其他位置。</span><span class="sxs-lookup"><span data-stu-id="9604a-110">Typically, this is the same as the IDList of the location being viewed, but it can be another location.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="9604a-111">此值的存留期是由 view 回呼物件所擁有。</span><span class="sxs-lookup"><span data-stu-id="9604a-111">The lifetime of this value is owned by the view callback object.</span></span> <span data-ttu-id="9604a-112">若不再需要，您必須負責建立 view 回呼物件，然後釋放此值。</span><span class="sxs-lookup"><span data-stu-id="9604a-112">It is the responsibility of the view callback object to create and then free this value when it is no longer needed.</span></span> <span data-ttu-id="9604a-113">這需要 view 回呼物件儲存這個值。</span><span class="sxs-lookup"><span data-stu-id="9604a-113">This requires that the view callback object stores this value.</span></span> <span data-ttu-id="9604a-114">此值通常可以儲存在 view 回呼物件的 **\_ pidlMonitor** 成員中。</span><span class="sxs-lookup"><span data-stu-id="9604a-114">Usually, the value can be stored in the **\_pidlMonitor** member of the view callback object.</span></span> <span data-ttu-id="9604a-115">透過 *pidl* 所傳回之值的擁有權規則是非標準的，而且需要特別注意。</span><span class="sxs-lookup"><span data-stu-id="9604a-115">The ownership rules for the value returned through *pidl* are nonstandard and require special care.</span></span> <span data-ttu-id="9604a-116">View 回呼物件必須擁有此值，並確保不會釋出視圖回呼物件本身。</span><span class="sxs-lookup"><span data-stu-id="9604a-116">The view callback object must own this value and ensure that it is not freed until the view callback object itself is destroyed.</span></span>

 

</dd> <dt>

<span data-ttu-id="9604a-117">*lEvents* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="9604a-117">*lEvents* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="9604a-118">值，其中包含一或多個 SHCNE 值。</span><span class="sxs-lookup"><span data-stu-id="9604a-118">A value that contains one or more SHCNE values.</span></span> <span data-ttu-id="9604a-119">如需可能值的清單，請參閱 [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) 。</span><span class="sxs-lookup"><span data-stu-id="9604a-119">See [**SHChangeNotify**](/windows/desktop/api/shlobj_core/nf-shlobj_core-shchangenotify) for a list of possible values.</span></span> <span data-ttu-id="9604a-120">當任何相關聯的事件發生時，view 回呼物件將會註冊以接收 [**SFVM \_ FSNOTIFY**](sfvm-fsnotify.md) 訊息。</span><span class="sxs-lookup"><span data-stu-id="9604a-120">The view callback object will register to receive an [**SFVM\_FSNOTIFY**](sfvm-fsnotify.md) message when any of the associated events occurs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="9604a-121">傳回值</span><span class="sxs-lookup"><span data-stu-id="9604a-121">Return value</span></span>

<span data-ttu-id="9604a-122">已忽略，但應該傳回 S \_ OK。</span><span class="sxs-lookup"><span data-stu-id="9604a-122">Ignored, but should return S\_OK.</span></span>

## <a name="remarks"></a><span data-ttu-id="9604a-123">備註</span><span class="sxs-lookup"><span data-stu-id="9604a-123">Remarks</span></span>

<span data-ttu-id="9604a-124">如果此回呼訊息未針對 Idlist.txt 或事件遮罩傳回非零值，則此視圖將不會註冊變更通知。</span><span class="sxs-lookup"><span data-stu-id="9604a-124">If this callback message does not return a nonzero value for either the IDList or the events mask then the view will not register for change notifications.</span></span>

## <a name="examples"></a><span data-ttu-id="9604a-125">範例</span><span class="sxs-lookup"><span data-stu-id="9604a-125">Examples</span></span>

<span data-ttu-id="9604a-126">下列範例顯示 **SFVM \_ GETNOTIFY** 的 view 回呼函式處理常式程式碼的範例執行。</span><span class="sxs-lookup"><span data-stu-id="9604a-126">The following sample shows an example implementation of the view callback function's handler code for **SFVM\_GETNOTIFY**.</span></span>


```C++
case SFVM_GETNOTIFY:
  *((LPITEMIDLIST*)wParam) = _pidl;    // Pass a reference whose lifetime this 
                                       // class is responsible for.
                                      
  *((LONG*)lParam) = SHCNE_DISKEVENTS; // A combination of all of the 
                                       // disk event identifiers.
                                       
   return S_OK;
```



## <a name="requirements"></a><span data-ttu-id="9604a-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="9604a-127">Requirements</span></span>



| <span data-ttu-id="9604a-128">需求</span><span class="sxs-lookup"><span data-stu-id="9604a-128">Requirement</span></span> | <span data-ttu-id="9604a-129">值</span><span class="sxs-lookup"><span data-stu-id="9604a-129">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="9604a-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9604a-130">Minimum supported client</span></span><br/> | <span data-ttu-id="9604a-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9604a-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                          |
| <span data-ttu-id="9604a-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9604a-132">Minimum supported server</span></span><br/> | <span data-ttu-id="9604a-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9604a-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="9604a-134">標頭</span><span class="sxs-lookup"><span data-stu-id="9604a-134">Header</span></span><br/>                   | <dl> <span data-ttu-id="9604a-135"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="9604a-135"><dt>Shlobj.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9604a-136">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9604a-136">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9604a-137">**SFVM \_ QUERYFSNOTIFY**</span><span class="sxs-lookup"><span data-stu-id="9604a-137">**SFVM\_QUERYFSNOTIFY**</span></span>](sfvm-queryfsnotify.md)
</dt> <dt>

[<span data-ttu-id="9604a-138">**IShellFolderViewCB::MessageSFVCB**</span><span class="sxs-lookup"><span data-stu-id="9604a-138">**IShellFolderViewCB::MessageSFVCB**</span></span>](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)
</dt> </dl>

 

 
