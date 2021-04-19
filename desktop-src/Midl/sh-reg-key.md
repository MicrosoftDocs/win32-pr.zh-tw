---
title: sh_reg_key 關鍵字
description: '\ Sh \_ reg \_ key \ 關鍵字會指定系統物件是登錄機碼的控制碼。'
keywords:
- sh_reg_key 關鍵字 MIDL
topic_type:
- apiref
api_name:
- sh_reg_key keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: cec526bed766534f82d5a1bc24c55050dea814ed
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "106986001"
---
# <a name="sh_reg_key-keyword"></a><span data-ttu-id="b8a66-104">sh \_ reg \_ key 關鍵字</span><span class="sxs-lookup"><span data-stu-id="b8a66-104">sh\_reg\_key keyword</span></span>

<span data-ttu-id="b8a66-105">**Sh \_ reg \_ key** 關鍵字會指定保留登錄機碼的 `system_handle` 控制碼。</span><span class="sxs-lookup"><span data-stu-id="b8a66-105">The **sh\_reg\_key** keyword specifies that a `system_handle` holds a handle to a registry key.</span></span>

``` syntax
[system_handle(sh_reg_key)]

[system_handle(sh_reg_key, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="b8a66-106">參數</span><span class="sxs-lookup"><span data-stu-id="b8a66-106">Parameters</span></span>

<span data-ttu-id="b8a66-107">這個關鍵字是 [**system_handle**](system-handle.md)的參數。</span><span class="sxs-lookup"><span data-stu-id="b8a66-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="b8a66-108">[**System_handle**](system-handle.md)檔也包含選擇性使用 *存取權限* 參數的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b8a66-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="b8a66-109">預設行為是 `DUPLICATE_SAME_ACCESS` 根據 [ **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)函式規格。</span><span class="sxs-lookup"><span data-stu-id="b8a66-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="b8a66-110">備註</span><span class="sxs-lookup"><span data-stu-id="b8a66-110">Remarks</span></span>

<span data-ttu-id="b8a66-111">若要使用這個關鍵字搭配 `system_handle` 屬性，在執行 `-target` midl.exe 時，旗標必須設定為 `NT100` (或更高的) 。</span><span class="sxs-lookup"><span data-stu-id="b8a66-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="b8a66-112">範例</span><span class="sxs-lookup"><span data-stu-id="b8a66-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GetConfigurationKey([out, system_handle(sh_reg_key)] HANDLE* key);

    HRESULT SetKeyForWatch([in, system_handle(sh_reg_key, KEY_READ)] HANDLE watchKey);
}
```

## <a name="requirements"></a><span data-ttu-id="b8a66-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="b8a66-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="b8a66-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="b8a66-114">Minimum supported client</span></span> | <span data-ttu-id="b8a66-115">Windows 10 年度更新版 (1607 版、組建 14393) </span><span class="sxs-lookup"><span data-stu-id="b8a66-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="b8a66-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="b8a66-116">Minimum supported server</span></span> | <span data-ttu-id="b8a66-117">Windows Server 2016 (build 14393) </span><span class="sxs-lookup"><span data-stu-id="b8a66-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="b8a66-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b8a66-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="b8a66-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="b8a66-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="b8a66-120">登錄</span><span class="sxs-lookup"><span data-stu-id="b8a66-120">Registry</span></span>](../sysinfo/registry.md)
</dt> <dt>

[<span data-ttu-id="b8a66-121">登錄機碼安全性與存取權限</span><span class="sxs-lookup"><span data-stu-id="b8a66-121">Registry Key Security and Access Rights</span></span>](../sysinfo/registry-key-security-and-access-rights.md)
</dt> <dt>

[<span data-ttu-id="b8a66-122">**RegOpenKeyEx** 函數</span><span class="sxs-lookup"><span data-stu-id="b8a66-122">**RegOpenKeyEx** function</span></span>](/windows/win32/api/winreg/nf-winreg-regopenkeyexa)
</dt> <dt>
