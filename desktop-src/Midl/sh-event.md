---
title: sh_event 關鍵字
description: '\ Sh \_ 事件 \ 關鍵字指定系統物件是事件的控制碼。'
keywords:
- sh_event 關鍵字 MIDL
topic_type:
- apiref
api_name:
- sh_event
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 1a9b6dc7cc9dc4de4abd5dcc88a53588167db59d
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "106985790"
---
# <a name="sh_event-keyword"></a><span data-ttu-id="5152a-104">sh \_ 事件關鍵字</span><span class="sxs-lookup"><span data-stu-id="5152a-104">sh\_event keyword</span></span>

<span data-ttu-id="5152a-105">**Sh \_ 事件** 關鍵字會指定 `system_handle` 保留事件的控制碼。</span><span class="sxs-lookup"><span data-stu-id="5152a-105">The **sh\_event** keyword specifies that a `system_handle` holds a handle to an event.</span></span>

``` syntax
[system_handle(sh_event)]

[system_handle(sh_event, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="5152a-106">參數</span><span class="sxs-lookup"><span data-stu-id="5152a-106">Parameters</span></span>

<span data-ttu-id="5152a-107">這個關鍵字是 [**system_handle**](system-handle.md)的參數。</span><span class="sxs-lookup"><span data-stu-id="5152a-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="5152a-108">[**System_handle**](system-handle.md)檔也包含選擇性使用 *存取權限* 參數的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5152a-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="5152a-109">預設行為是 `DUPLICATE_SAME_ACCESS` 根據 [ **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)函式規格。</span><span class="sxs-lookup"><span data-stu-id="5152a-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="5152a-110">備註</span><span class="sxs-lookup"><span data-stu-id="5152a-110">Remarks</span></span>

<span data-ttu-id="5152a-111">若要使用這個關鍵字搭配 `system_handle` 屬性，在執行 `-target` midl.exe 時，旗標必須設定為 `NT100` (或更高的) 。</span><span class="sxs-lookup"><span data-stu-id="5152a-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="5152a-112">範例</span><span class="sxs-lookup"><span data-stu-id="5152a-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT NotifyThisEvent([in, system_handle(sh_event)] HANDLE listeningToThisEvent);
}
```

## <a name="requirements"></a><span data-ttu-id="5152a-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="5152a-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="5152a-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5152a-114">Minimum supported client</span></span> | <span data-ttu-id="5152a-115">Windows 10 年度更新版 (1607 版、組建 14393) </span><span class="sxs-lookup"><span data-stu-id="5152a-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="5152a-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5152a-116">Minimum supported server</span></span> | <span data-ttu-id="5152a-117">Windows Server 2016 (build 14393) </span><span class="sxs-lookup"><span data-stu-id="5152a-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="5152a-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5152a-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5152a-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="5152a-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="5152a-120">事件物件</span><span class="sxs-lookup"><span data-stu-id="5152a-120">Event Objects</span></span>](../sync/event-objects.md)
</dt> <dt>

[<span data-ttu-id="5152a-121">同步處理物件安全性和存取權限</span><span class="sxs-lookup"><span data-stu-id="5152a-121">Synchronization Object Security and Access Rights</span></span>](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="5152a-122">**CreateEvent** 函數</span><span class="sxs-lookup"><span data-stu-id="5152a-122">**CreateEvent** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createeventa)
</dt> <dt>

[<span data-ttu-id="5152a-123">**CreateEventEx** 函式</span><span class="sxs-lookup"><span data-stu-id="5152a-123">**CreateEventEx** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createeventexa)
</dt> </dl>
