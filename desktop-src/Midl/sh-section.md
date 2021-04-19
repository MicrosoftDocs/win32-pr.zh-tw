---
title: sh_section 關鍵字
description: '\ Sh \_ 區段 \ 關鍵字指定系統物件是區段的控制碼。'
keywords:
- sh_section 關鍵字 MIDL
topic_type:
- apiref
api_name:
- sh_section keyword
api_type:
- NA
ms.topic: reference
ms.date: 02/05/2021
ms.openlocfilehash: 056112deb790e727206a5ac1a1a2a5043a68f5e1
ms.sourcegitcommit: af9983bab40fe0b042f177ce7ca79f2eb0f9d0e8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/06/2021
ms.locfileid: "106985511"
---
# <a name="sh_section-keyword"></a><span data-ttu-id="ad8b4-104">sh \_ 區段關鍵字</span><span class="sxs-lookup"><span data-stu-id="ad8b4-104">sh\_section keyword</span></span>

<span data-ttu-id="ad8b4-105">**Sh \_ 區段** 關鍵字指定將 `system_handle` 控制碼保存到區段。</span><span class="sxs-lookup"><span data-stu-id="ad8b4-105">The **sh\_section** keyword specifies that a `system_handle` holds a handle to a section.</span></span>

``` syntax
[system_handle(sh_section)]

[system_handle(sh_section, access-rights)]
```

## <a name="parameters"></a><span data-ttu-id="ad8b4-106">參數</span><span class="sxs-lookup"><span data-stu-id="ad8b4-106">Parameters</span></span>

<span data-ttu-id="ad8b4-107">這個關鍵字是 [**system_handle**](system-handle.md)的參數。</span><span class="sxs-lookup"><span data-stu-id="ad8b4-107">This keyword is a parameter for [**system_handle**](system-handle.md).</span></span>

<span data-ttu-id="ad8b4-108">[**System_handle**](system-handle.md)檔也包含選擇性使用 *存取權限* 參數的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="ad8b4-108">The [**system_handle**](system-handle.md) documentation also contains details on optional use of the *access-rights* parameter.</span></span> <span data-ttu-id="ad8b4-109">預設行為是 `DUPLICATE_SAME_ACCESS` 根據 [ **DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)函式規格。</span><span class="sxs-lookup"><span data-stu-id="ad8b4-109">The default behavior is `DUPLICATE_SAME_ACCESS` per [**DuplicateHandle** function](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle) specifications.</span></span>

## <a name="remarks"></a><span data-ttu-id="ad8b4-110">備註</span><span class="sxs-lookup"><span data-stu-id="ad8b4-110">Remarks</span></span>

<span data-ttu-id="ad8b4-111">若要使用這個關鍵字搭配 `system_handle` 屬性，在執行 `-target` midl.exe 時，旗標必須設定為 `NT100` (或更高的) 。</span><span class="sxs-lookup"><span data-stu-id="ad8b4-111">In order to use this keyword with the `system_handle` attribute, the `-target` flag must be set to `NT100` (or higher) when running midl.exe.</span></span>

## <a name="examples"></a><span data-ttu-id="ad8b4-112">範例</span><span class="sxs-lookup"><span data-stu-id="ad8b4-112">Examples</span></span>

``` syntax
interface MyInterface : IUnknown                         
{         
    HRESULT GiveSection([in, system_handle(sh_section)] HANDLE section);

    HRESULT GetSectionToWatch([out, system_handle(sh_section, SECTION_MAP_READ)] HANDLE* pSection);
}
```

## <a name="requirements"></a><span data-ttu-id="ad8b4-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="ad8b4-113">Requirements</span></span>

| &nbsp; | &nbsp; |
|-|-|
| <span data-ttu-id="ad8b4-114">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ad8b4-114">Minimum supported client</span></span> | <span data-ttu-id="ad8b4-115">Windows 10 年度更新版 (1607 版、組建 14393) </span><span class="sxs-lookup"><span data-stu-id="ad8b4-115">Windows 10 Anniversary Update (version 1607, build 14393)</span></span> |
| <span data-ttu-id="ad8b4-116">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ad8b4-116">Minimum supported server</span></span> | <span data-ttu-id="ad8b4-117">Windows Server 2016 (build 14393) </span><span class="sxs-lookup"><span data-stu-id="ad8b4-117">Windows Server 2016 (build 14393)</span></span> |

## <a name="see-also"></a><span data-ttu-id="ad8b4-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ad8b4-118">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ad8b4-119">**system_handle**</span><span class="sxs-lookup"><span data-stu-id="ad8b4-119">**system_handle**</span></span>](system-handle.md)
</dt> <dt>

[<span data-ttu-id="ad8b4-120">區段物件和視圖</span><span class="sxs-lookup"><span data-stu-id="ad8b4-120">Section Objects and Views</span></span>](/windows-hardware/drivers/kernel/section-objects-and-views)
</dt> <dt>

[<span data-ttu-id="ad8b4-121">**ZwCreateSection** 函式 (包括存取規格)</span><span class="sxs-lookup"><span data-stu-id="ad8b4-121">**ZwCreateSection** function (including access specifications)</span></span>](/windows-hardware/drivers/ddi/wdm/nf-wdm-zwcreatesection)
</dt> </dl>
