---
description: SCE \_ 列舉 \_ 內容資料類型是由安全性設定工具集所提供的不透明控制碼。 PFSCE \_ QUERY INFO 函數會使用它 \_ 來流覽安全性資料庫。
ms.assetid: 05629c49-e36b-4045-93d0-d0f4bc09b08a
title: 'SCE_ENUMERATION_CONTEXT (Scesvc) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e380f6f99d68ad63199c3b82f5aa1e5ace8ddf0d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318223"
---
# <a name="sce_enumeration_context"></a><span data-ttu-id="65ed4-104">SCE \_ 列舉 \_ 內容</span><span class="sxs-lookup"><span data-stu-id="65ed4-104">SCE\_ENUMERATION\_CONTEXT</span></span>

<span data-ttu-id="65ed4-105">**SCE \_ 列舉 \_ 內容** 資料類型是由安全性設定工具集所提供的不透明控制碼。</span><span class="sxs-lookup"><span data-stu-id="65ed4-105">The **SCE\_ENUMERATION\_CONTEXT** data type is an opaque handle provided by the Security Configuration tool set.</span></span> <span data-ttu-id="65ed4-106">[**PFSCE \_ QUERY \_ INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)函數會使用它來流覽安全性資料庫。</span><span class="sxs-lookup"><span data-stu-id="65ed4-106">It is used by the [**PFSCE\_QUERY\_INFO**](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info) function to navigate through the security database.</span></span>


```C++
typedef ULONG SCE_ENUMERATION_CONTEXT, *PSCE_ENUMERATION_CONTEXT;
```



## <a name="requirements"></a><span data-ttu-id="65ed4-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="65ed4-107">Requirements</span></span>



| <span data-ttu-id="65ed4-108">需求</span><span class="sxs-lookup"><span data-stu-id="65ed4-108">Requirement</span></span> | <span data-ttu-id="65ed4-109">值</span><span class="sxs-lookup"><span data-stu-id="65ed4-109">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="65ed4-110">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="65ed4-110">Minimum supported client</span></span><br/> | <span data-ttu-id="65ed4-111">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65ed4-111">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="65ed4-112">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="65ed4-112">Minimum supported server</span></span><br/> | <span data-ttu-id="65ed4-113">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="65ed4-113">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="65ed4-114">標頭</span><span class="sxs-lookup"><span data-stu-id="65ed4-114">Header</span></span><br/>                   | <dl> <span data-ttu-id="65ed4-115"><dt>Scesvc。h</dt></span><span class="sxs-lookup"><span data-stu-id="65ed4-115"><dt>Scesvc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="65ed4-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="65ed4-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="65ed4-117">**PFSCE \_ 查詢 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="65ed4-117">**PFSCE\_QUERY\_INFO**</span></span>](/windows/win32/api/scesvc/nc-scesvc-pfsce_query_info)
</dt> </dl>

 

