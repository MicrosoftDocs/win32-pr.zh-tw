---
description: SFVM \_ GETDETAILSOF 可能已變更或無法使用。
ms.assetid: 46a81a7b-527c-4d41-8d25-ce65fd87416e
title: 'SFVM_GETDETAILSOF 訊息 (Shlobj.h .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 6170c0fc8dc29435b2c6f2bb033f30706ccb7b33
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973481"
---
# <a name="sfvm_getdetailsof-message"></a><span data-ttu-id="d315d-103">SFVM \_ GETDETAILSOF 訊息</span><span class="sxs-lookup"><span data-stu-id="d315d-103">SFVM\_GETDETAILSOF message</span></span>

<span data-ttu-id="d315d-104">\[**SFVM \_GETDETAILSOF** 可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="d315d-104">\[**SFVM\_GETDETAILSOF** is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d315d-105">它在後續版本中可能會變更或無法使用。\]</span><span class="sxs-lookup"><span data-stu-id="d315d-105">It may be altered or unavailable in subsequent versions.\]</span></span>

<span data-ttu-id="d315d-106">允許回呼物件提供 Shell 資料夾中專案的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="d315d-106">Allows the callback object to provide the details for an item in a Shell folder.</span></span> <span data-ttu-id="d315d-107">只有在呼叫 [**IShellFolder2：： GetDetailsOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof) 失敗，而且沒有可供呼叫的 [**IShellDetails：： GetDetailsOf**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof) 方法時，才使用。</span><span class="sxs-lookup"><span data-stu-id="d315d-107">Use only if a call to [**IShellFolder2::GetDetailsOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder2-getdetailsof) fails and there is no [**IShellDetails::GetDetailsOf**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishelldetails-getdetailsof) method available to call.</span></span> <span data-ttu-id="d315d-108">由 [**IShellFolderViewCB：： MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb)使用。</span><span class="sxs-lookup"><span data-stu-id="d315d-108">Used by [**IShellFolderViewCB::MessageSFVCB**](/windows/win32/api/shlobj_core/nf-shlobj_core-ishellfolderviewcb-messagesfvcb).</span></span>


```C++
SFVM_GETDETAILSOF
    wParam = (WPARAM)(int) iColumn;
    lParam = (LPARAM)(DETAILSINFO*) pDi;
            
```



## <a name="parameters"></a><span data-ttu-id="d315d-109">參數</span><span class="sxs-lookup"><span data-stu-id="d315d-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d315d-110">*iColumn* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d315d-110">*iColumn* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d315d-111">以零為基底的資料行識別碼。</span><span class="sxs-lookup"><span data-stu-id="d315d-111">The zero-based ID of the column.</span></span>

</dd> <dt>

<span data-ttu-id="d315d-112">*pDi* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="d315d-112">*pDi* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="d315d-113">[**DETAILSINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo)結構的指標，該結構已填入要求的資訊。</span><span class="sxs-lookup"><span data-stu-id="d315d-113">A pointer to a [**DETAILSINFO**](/windows/desktop/api/shlobj_core/ns-shlobj_core-detailsinfo) structure filled with the requested information.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="d315d-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="d315d-114">Requirements</span></span>



| <span data-ttu-id="d315d-115">需求</span><span class="sxs-lookup"><span data-stu-id="d315d-115">Requirement</span></span> | <span data-ttu-id="d315d-116">值</span><span class="sxs-lookup"><span data-stu-id="d315d-116">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="d315d-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="d315d-117">Minimum supported client</span></span><br/> | <span data-ttu-id="d315d-118">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d315d-118">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="d315d-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="d315d-119">Minimum supported server</span></span><br/> | <span data-ttu-id="d315d-120">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="d315d-120">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="d315d-121">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d315d-121">End of client support</span></span><br/>    | <span data-ttu-id="d315d-122">Windows XP 含 SP2</span><span class="sxs-lookup"><span data-stu-id="d315d-122">Windows XP with SP2</span></span><br/>                                                      |
| <span data-ttu-id="d315d-123">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="d315d-123">End of server support</span></span><br/>    | <span data-ttu-id="d315d-124">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="d315d-124">Windows Server 2003</span></span><br/>                                                      |
| <span data-ttu-id="d315d-125">標頭</span><span class="sxs-lookup"><span data-stu-id="d315d-125">Header</span></span><br/>                   | <dl> <span data-ttu-id="d315d-126"><dt>Shlobj.h。h</dt></span><span class="sxs-lookup"><span data-stu-id="d315d-126"><dt>Shlobj.h</dt></span></span> </dl> |



 

 
