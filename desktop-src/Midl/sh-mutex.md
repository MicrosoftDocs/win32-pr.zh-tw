---
title: sh_mutex 關鍵字
description: '\ Sh \_ mutex \ 關鍵字會指定系統物件是 mutex 的控制碼。'
keywords:
- sh_mutex 關鍵字 MIDL
topic_type:
- apiref
api_name:
- sh_mutex
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 8616ded29d1d8c106af21e6cd1252535f4da8457
ms.sourcegitcommit: de72a1294df274b0a71dc0fdc42d757e5f6df0f3
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/05/2021
ms.locfileid: "106989134"
---
# <a name="sh_mutex-keyword"></a><span data-ttu-id="21bd8-104">sh \_ mutex 關鍵字</span><span class="sxs-lookup"><span data-stu-id="21bd8-104">sh\_mutex keyword</span></span>

<span data-ttu-id="21bd8-105">**Sh \_ mutex** 關鍵字會指定 `system_handle` 保留 mutex 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="21bd8-105">The **sh\_mutex** keyword specifies that a `system_handle` holds a handle to a mutex.</span></span>

``` syntax
[system_handle(sh_mutex)]

[system_handle(sh_mutex, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="21bd8-106">參數</span><span class="sxs-lookup"><span data-stu-id="21bd8-106">Parameters</span></span>

<span data-ttu-id="21bd8-107">這個關鍵字是 [**system_handle**](system-handle.md)的參數。</span><span class="sxs-lookup"><span data-stu-id="21bd8-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="21bd8-108">[**System_handle**](system-handle.md)檔也包含選擇性使用 *存取權限* 參數的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="21bd8-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="21bd8-109">預設行為是 `DUPLICATE_SAME_ACCESS` 根據 [ **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)函式規格。</span><span class="sxs-lookup"><span data-stu-id="21bd8-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="21bd8-110">備註</span><span class="sxs-lookup"><span data-stu-id="21bd8-110">Remarks</span></span>

<span data-ttu-id="21bd8-111">若要使用這個關鍵字搭配 `system_handle` 屬性，在執行 `-target` midl.exe 時，旗標必須設定為 `NT100` (或更高的) 。</span><span class="sxs-lookup"><span data-stu-id="21bd8-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="21bd8-112">範例</span><span class="sxs-lookup"><span data-stu-id="21bd8-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT WaitOnThisMutex([in, system_handle(sh_mutex)] HANDLE mutex);
}
```

## <a name="requirements"></a><span data-ttu-id="21bd8-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="21bd8-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="21bd8-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="21bd8-114">Minimum supported client</span></span> | <span data-ttu-id="21bd8-115">Windows 10 年度更新版 (1607 版、組建 14393) </span><span class="sxs-lookup"><span data-stu-id="21bd8-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="21bd8-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="21bd8-116">Minimum supported server</span></span> | <span data-ttu-id="21bd8-117">Windows Server 2016 (build 14393) </span><span class="sxs-lookup"><span data-stu-id="21bd8-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="21bd8-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="21bd8-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="21bd8-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="21bd8-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="21bd8-120">Mutex 物件</span><span class="sxs-lookup"><span data-stu-id="21bd8-120">Mutex Objects</span></span>](../sync/mutex-objects.md)
</dt> <dt>

[<span data-ttu-id="21bd8-121">同步處理物件安全性和存取權限</span><span class="sxs-lookup"><span data-stu-id="21bd8-121">Synchronization Object Security and Access Rights</span></span>](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="21bd8-122">**CreateMutex** 函式</span><span class="sxs-lookup"><span data-stu-id="21bd8-122">**CreateMutex** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createmutexa)
</dt> <dt>

[<span data-ttu-id="21bd8-123">**CreateMutexEx** 函式</span><span class="sxs-lookup"><span data-stu-id="21bd8-123">**CreateMutexEx** function</span></span>](/windows/win32/api/synchapi/nf-synchapi-createmutexexa)
</dt> </dl>