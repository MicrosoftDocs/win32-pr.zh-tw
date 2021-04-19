---
title: sh_semaphore 關鍵字
description: '\ Sh \_ 信號 \ 關鍵字指定系統物件是信號的控制碼。'
keywords:
- sh_semaphore 關鍵字 MIDL
topic_type:
- apiref
api_name:
- sh_semaphore
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 2a5c33e4c44b67e3106a48cde244abaf13f41ad5
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "106991383"
---
# <a name="sh_semaphore-keyword"></a><span data-ttu-id="0d974-104">sh \_ 信號關鍵字</span><span class="sxs-lookup"><span data-stu-id="0d974-104">sh\_semaphore keyword</span></span>

<span data-ttu-id="0d974-105">**Sh \_ 信號** 關鍵字會指定 `system_handle` 保留信號的控制碼。</span><span class="sxs-lookup"><span data-stu-id="0d974-105">The **sh\_semaphore** keyword specifies that a `system_handle` holds a handle to a semaphore.</span></span>

``` syntax
[system_handle(sh_semaphore)]

[system_handle(sh_semaphore, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="0d974-106">參數</span><span class="sxs-lookup"><span data-stu-id="0d974-106">Parameters</span></span>

<span data-ttu-id="0d974-107">這個關鍵字是 [**system_handle**](system-handle.md)的參數。</span><span class="sxs-lookup"><span data-stu-id="0d974-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="0d974-108">[**System_handle**](system-handle.md)檔也包含選擇性使用 *存取權限* 參數的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="0d974-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="0d974-109">預設行為是 `DUPLICATE_SAME_ACCESS` 根據 [ **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)函式規格。</span><span class="sxs-lookup"><span data-stu-id="0d974-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="0d974-110">備註</span><span class="sxs-lookup"><span data-stu-id="0d974-110">Remarks</span></span>

<span data-ttu-id="0d974-111">若要使用這個關鍵字搭配 `system_handle` 屬性，在執行 `-target` midl.exe 時，旗標必須設定為 `NT100` (或更高的) 。</span><span class="sxs-lookup"><span data-stu-id="0d974-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="0d974-112">範例</span><span class="sxs-lookup"><span data-stu-id="0d974-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT SignalThisSemaphore([in, system_handle(sh_semaphore)] HANDLE semaphore);
}
```

## <a name="requirements"></a><span data-ttu-id="0d974-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="0d974-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="0d974-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="0d974-114">Minimum supported client</span></span> | <span data-ttu-id="0d974-115">Windows 10 年度更新版 (1607 版、組建 14393) </span><span class="sxs-lookup"><span data-stu-id="0d974-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="0d974-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="0d974-116">Minimum supported server</span></span> | <span data-ttu-id="0d974-117">Windows Server 2016 (build 14393) </span><span class="sxs-lookup"><span data-stu-id="0d974-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="0d974-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="0d974-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="0d974-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="0d974-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="0d974-120">信號物件</span><span class="sxs-lookup"><span data-stu-id="0d974-120">Semaphore Objects</span></span>](../sync/semaphore-objects.md)
</dt> <dt>

[<span data-ttu-id="0d974-121">同步處理物件安全性和存取權限</span><span class="sxs-lookup"><span data-stu-id="0d974-121">Synchronization Object Security and Access Rights</span></span>](../sync/synchronization-object-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="0d974-122">**CreateSemaphore** 函式</span><span class="sxs-lookup"><span data-stu-id="0d974-122">**CreateSemaphore** function</span></span>](/windows/win32/api/winbase/nf-winbase-createsemaphorea)
</dt> <dt>

[<span data-ttu-id="0d974-123">**CreateSemaphoreEx** 函式</span><span class="sxs-lookup"><span data-stu-id="0d974-123">**CreateSemaphoreEx** function</span></span>](/windows/win32/api/winbase/nf-winbase-createsemaphoreexa)
</dt> </dl>
