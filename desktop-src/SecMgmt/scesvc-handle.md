---
description: SCESVC \_ 控制碼資料類型是由安全性設定工具集所提供的不透明控制碼。
ms.assetid: 478d7d4b-7983-4247-b8be-2e2cd3327533
title: 'SCESVC_HANDLE (Scesvc) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 09fbc115326361e4cbfe1152361a70a36007a302
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104511166"
---
# <a name="scesvc_handle"></a><span data-ttu-id="f62a1-103">SCESVC \_ 控制碼</span><span class="sxs-lookup"><span data-stu-id="f62a1-103">SCESVC\_HANDLE</span></span>

<span data-ttu-id="f62a1-104">**SCESVC \_ 控制碼** 資料類型是由安全性設定工具集所提供的不透明控制碼。</span><span class="sxs-lookup"><span data-stu-id="f62a1-104">The **SCESVC\_HANDLE** data type is an opaque handle provided by the Security Configuration tool set.</span></span> <span data-ttu-id="f62a1-105">[**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)和 [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo)介面的方法會使用它，在 [安全性設定] 嵌入式管理單元和嵌入式管理單元擴充功能之間傳遞資訊。</span><span class="sxs-lookup"><span data-stu-id="f62a1-105">It is used by methods of the [**ISceSvcAttachmentData**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata) and [**ISceSvcAttachmentPersistInfo**](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo) interfaces to pass information between the Security Configuration snap-in and the snap-in extension.</span></span>


```C++
typedef PVOID SCESVC_HANDLE;
```



## <a name="requirements"></a><span data-ttu-id="f62a1-106">規格需求</span><span class="sxs-lookup"><span data-stu-id="f62a1-106">Requirements</span></span>



| <span data-ttu-id="f62a1-107">需求</span><span class="sxs-lookup"><span data-stu-id="f62a1-107">Requirement</span></span> | <span data-ttu-id="f62a1-108">值</span><span class="sxs-lookup"><span data-stu-id="f62a1-108">Value</span></span> |
|-------------------------------------|-------------------------------------------------------------------------------------|
| <span data-ttu-id="f62a1-109">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f62a1-109">Minimum supported client</span></span><br/> | <span data-ttu-id="f62a1-110">\[僅限 WINDOWS XP desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f62a1-110">Windows XP \[desktop apps only\]</span></span><br/>                                         |
| <span data-ttu-id="f62a1-111">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f62a1-111">Minimum supported server</span></span><br/> | <span data-ttu-id="f62a1-112">僅限 Windows Server 2003 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f62a1-112">Windows Server 2003 \[desktop apps only\]</span></span><br/>                                |
| <span data-ttu-id="f62a1-113">標頭</span><span class="sxs-lookup"><span data-stu-id="f62a1-113">Header</span></span><br/>                   | <dl> <span data-ttu-id="f62a1-114"><dt>Scesvc。h</dt></span><span class="sxs-lookup"><span data-stu-id="f62a1-114"><dt>Scesvc.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f62a1-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f62a1-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f62a1-116">**ISceSvcAttachmentData**</span><span class="sxs-lookup"><span data-stu-id="f62a1-116">**ISceSvcAttachmentData**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentdata)
</dt> <dt>

[<span data-ttu-id="f62a1-117">**ISceSvcAttachmentPersistInfo**</span><span class="sxs-lookup"><span data-stu-id="f62a1-117">**ISceSvcAttachmentPersistInfo**</span></span>](/windows/desktop/api/Scesvc/nn-scesvc-iscesvcattachmentpersistinfo)
</dt> </dl>

 

 




