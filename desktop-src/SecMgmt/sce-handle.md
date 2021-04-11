---
description: SCE \_ 控制碼資料類型是由安全性設定工具集所提供的不透明控制碼。 PFSCE \_ 查詢 \_ 資訊和 PFSCE 設定資訊支援函式會使用它 \_ \_ 來傳遞附件和安全性資料庫之間的資訊。
ms.assetid: 8db91e6f-b31e-40c6-a158-b4b3b00ba0c0
title: 'SCE_HANDLE (Scesvc) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3fef21dbe03d97dfa14537d5df132ba3cb222643
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112657"
---
# <a name="sce_handle"></a><span data-ttu-id="cfe6f-104">SCE \_ 把手</span><span class="sxs-lookup"><span data-stu-id="cfe6f-104">SCE\_HANDLE</span></span>

<span data-ttu-id="cfe6f-105">**SCE \_ 控制碼** 資料類型是由安全性設定工具集所提供的不透明控制碼。</span><span class="sxs-lookup"><span data-stu-id="cfe6f-105">The **SCE\_HANDLE** data type is an opaque handle provided by the Security Configuration tool set.</span></span> <span data-ttu-id="cfe6f-106">[**PFSCE \_ 查詢 \_ 資訊**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)和 [**PFSCE \_ 設定 \_ 資訊**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)支援函式會使用它來傳遞附件和安全性資料庫之間的資訊。</span><span class="sxs-lookup"><span data-stu-id="cfe6f-106">It is used by [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) and [**PFSCE\_SET\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info) support functions to pass information between the attachment and the security database.</span></span>


```C++
typedef PVOID SCE_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="cfe6f-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="cfe6f-107">Requirements</span></span>



| <span data-ttu-id="cfe6f-108">需求</span><span class="sxs-lookup"><span data-stu-id="cfe6f-108">Requirement</span></span> | <span data-ttu-id="cfe6f-109">值</span><span class="sxs-lookup"><span data-stu-id="cfe6f-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="cfe6f-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="cfe6f-110">Minimum supported client</span></span><br/> | <span data-ttu-id="cfe6f-111">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cfe6f-111">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="cfe6f-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="cfe6f-112">Minimum supported server</span></span><br/> | <span data-ttu-id="cfe6f-113">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="cfe6f-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="cfe6f-114">標頭</span><span class="sxs-lookup"><span data-stu-id="cfe6f-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="cfe6f-115"><dt>Scesvc。h</dt></span><span class="sxs-lookup"><span data-stu-id="cfe6f-115"><dt>Scesvc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="cfe6f-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cfe6f-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cfe6f-117">**PFSCE \_ 查詢 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="cfe6f-117">**PFSCE\_QUERY\_INFO**</span></span>](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> <dt>

[<span data-ttu-id="cfe6f-118">**PFSCE \_ 設定 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="cfe6f-118">**PFSCE\_SET\_INFO**</span></span>](/windows/win32/api/scesvc/nc-scesvc-pfsce_set_info)
</dt> </dl>

 

