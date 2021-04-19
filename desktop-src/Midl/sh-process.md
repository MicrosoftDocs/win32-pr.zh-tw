---
title: sh_process 關鍵字
description: '\ Sh \_ process \ 關鍵字會指定系統物件是進程的控制碼。'
keywords:
- sh_process 關鍵字 MIDL
topic_type:
- apiref
api_name:
- sh_process
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 3652c6889c687173bbf7b397cddff4659c0329f1
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "106981720"
---
# <a name="sh_process-keyword"></a><span data-ttu-id="54acd-104">sh \_ process 關鍵字</span><span class="sxs-lookup"><span data-stu-id="54acd-104">sh\_process keyword</span></span>

<span data-ttu-id="54acd-105">**Sh \_ process** 關鍵字會指定 `system_handle` 保留進程的控制碼。</span><span class="sxs-lookup"><span data-stu-id="54acd-105">The **sh\_process** keyword specifies that a `system_handle` holds a handle to a process.</span></span>

``` syntax
[system_handle(sh_process)]

[system_handle(sh_process, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="54acd-106">參數</span><span class="sxs-lookup"><span data-stu-id="54acd-106">Parameters</span></span>

<span data-ttu-id="54acd-107">這個關鍵字是 [**system_handle**](system-handle.md)的參數。</span><span class="sxs-lookup"><span data-stu-id="54acd-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="54acd-108">[**System_handle**](system-handle.md)檔也包含選擇性使用 *存取權限* 參數的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="54acd-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="54acd-109">預設行為是 `DUPLICATE_SAME_ACCESS` 根據 [ **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)函式規格。</span><span class="sxs-lookup"><span data-stu-id="54acd-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="54acd-110">備註</span><span class="sxs-lookup"><span data-stu-id="54acd-110">Remarks</span></span>

<span data-ttu-id="54acd-111">若要使用這個關鍵字搭配 `system_handle` 屬性，在執行 `-target` midl.exe 時，旗標必須設定為 `NT100` (或更高的) 。</span><span class="sxs-lookup"><span data-stu-id="54acd-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="54acd-112">範例</span><span class="sxs-lookup"><span data-stu-id="54acd-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetStubProcess([out, system_handle(sh_process)] HANDLE* processHandle);

    HRESULT WatchProcess([in, system_handle(sh_process, PROCESS_QUERY_INFORMATION | PROCESS_QUERY_LIMITED_INFORMATION)] HANDLE processHandle);
}
```

## <a name="requirements"></a><span data-ttu-id="54acd-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="54acd-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="54acd-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="54acd-114">Minimum supported client</span></span> | <span data-ttu-id="54acd-115">Windows 10 年度更新版 (1607 版、組建 14393) </span><span class="sxs-lookup"><span data-stu-id="54acd-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="54acd-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="54acd-116">Minimum supported server</span></span> | <span data-ttu-id="54acd-117">Windows Server 2016 (build 14393) </span><span class="sxs-lookup"><span data-stu-id="54acd-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="54acd-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="54acd-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="54acd-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="54acd-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="54acd-120">關於處理序和執行緒</span><span class="sxs-lookup"><span data-stu-id="54acd-120">About Processes and Threads</span></span>](../procthread/about-processes-and-threads.md)
</dt> <dt>

[<span data-ttu-id="54acd-121">流程安全性和存取權限</span><span class="sxs-lookup"><span data-stu-id="54acd-121">Process Security and Access Rights</span></span>](../procthread/process-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="54acd-122">**CreateProcess** 函數</span><span class="sxs-lookup"><span data-stu-id="54acd-122">**CreateProcess** function</span></span>](/windows/win32/api/processthreadsapi/nf-processthreadsapi-createprocessa)
</dt> <dt>

[<span data-ttu-id="54acd-123">**OpenProcess** 函式</span><span class="sxs-lookup"><span data-stu-id="54acd-123">**OpenProcess** function</span></span>](/win32/api/processthreadsapi/nf-processthreadsapi-openprocess)
</dt> </dl>