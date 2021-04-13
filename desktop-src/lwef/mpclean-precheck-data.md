---
title: 'MPCLEAN_PRECHECK_DATA 結構 (MpClient .h) '
description: 傳遞給清除前置檢查回呼函數的通知資料。
ms.assetid: 65B3B116-6E83-46F5-AE2B-92A41AE39480
keywords:
- MPCLEAN_PRECHECK_DATA 結構舊版 Windows 環境功能
- PMPCLEAN_PRECHECK_DATA 結構指標舊版 Windows 環境功能
topic_type:
- apiref
api_name:
- MPCLEAN_PRECHECK_DATA
api_location:
- MpClient.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bc3d67e0c71c95db49b633feeb3048cc9f104b2f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104464908"
---
# <a name="mpclean_precheck_data-structure"></a><span data-ttu-id="f25a8-105">MPCLEAN \_ 檢查 \_ 資料結構</span><span class="sxs-lookup"><span data-stu-id="f25a8-105">MPCLEAN\_PRECHECK\_DATA structure</span></span>

<span data-ttu-id="f25a8-106">傳遞給清除前置檢查回呼函數的通知資料。</span><span class="sxs-lookup"><span data-stu-id="f25a8-106">Notification data passed to clean precheck callback function.</span></span>

## <a name="syntax"></a><span data-ttu-id="f25a8-107">語法</span><span class="sxs-lookup"><span data-stu-id="f25a8-107">Syntax</span></span>


```C++
typedef struct tagMPCLEAN_PRECHECK_DATA {
  PMPRESOURCE_INFO     BlockedResourceInfo;
  BlockingResourceInfo PMPRESOURCE_INFO;
} MPCLEAN_PRECHECK_DATA, *PMPCLEAN_PRECHECK_DATA;
```



## <a name="members"></a><span data-ttu-id="f25a8-108">成員</span><span class="sxs-lookup"><span data-stu-id="f25a8-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="f25a8-109">**BlockedResourceInfo**</span><span class="sxs-lookup"><span data-stu-id="f25a8-109">**BlockedResourceInfo**</span></span>
</dt> <dd>

<span data-ttu-id="f25a8-110">類型： **PMPRESOURCE \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f25a8-110">Type: **PMPRESOURCE\_INFO**</span></span>

</dd> <dd>

<span data-ttu-id="f25a8-111">有關被封鎖之資源的資源資訊。</span><span class="sxs-lookup"><span data-stu-id="f25a8-111">Resource information about the resource being blocked.</span></span> <span data-ttu-id="f25a8-112">例如，當進度是封鎖 MPNOTIFY 的前置檢查 **\_ \_ 資源 \_** 時。</span><span class="sxs-lookup"><span data-stu-id="f25a8-112">For example, when progress is **MPNOTIFY\_PRECHECK\_RESOURCE\_BLOCKED**.</span></span> <span data-ttu-id="f25a8-113">請參閱 [**MPRESOURCE \_ 資訊**](mpresource-info.md)。</span><span class="sxs-lookup"><span data-stu-id="f25a8-113">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> <dt>

<span data-ttu-id="f25a8-114">**PMPRESOURCE \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f25a8-114">**PMPRESOURCE\_INFO**</span></span>
</dt> <dd>

<span data-ttu-id="f25a8-115">類型： **BlockingResourceInfo**</span><span class="sxs-lookup"><span data-stu-id="f25a8-115">Type: **BlockingResourceInfo**</span></span>

</dd> <dd>

<span data-ttu-id="f25a8-116">有關封鎖之資源的資源資訊。</span><span class="sxs-lookup"><span data-stu-id="f25a8-116">Resource information about the resource that is blocking.</span></span> <span data-ttu-id="f25a8-117">例如，當進度是封鎖 MPNOTIFY 的前置檢查 **\_ \_ 資源 \_** 時。</span><span class="sxs-lookup"><span data-stu-id="f25a8-117">For example, when progress is **MPNOTIFY\_PRECHECK\_RESOURCE\_BLOCKED**.</span></span> <span data-ttu-id="f25a8-118">請參閱 [**MPRESOURCE \_ 資訊**](mpresource-info.md)。</span><span class="sxs-lookup"><span data-stu-id="f25a8-118">See [**MPRESOURCE\_INFO**](mpresource-info.md).</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="f25a8-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="f25a8-119">Requirements</span></span>



| <span data-ttu-id="f25a8-120">需求</span><span class="sxs-lookup"><span data-stu-id="f25a8-120">Requirement</span></span> | <span data-ttu-id="f25a8-121">值</span><span class="sxs-lookup"><span data-stu-id="f25a8-121">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="f25a8-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f25a8-122">Minimum supported client</span></span><br/> | <span data-ttu-id="f25a8-123">\[僅 Windows 8 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f25a8-123">Windows 8 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="f25a8-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f25a8-124">Minimum supported server</span></span><br/> | <span data-ttu-id="f25a8-125">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f25a8-125">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="f25a8-126">標頭</span><span class="sxs-lookup"><span data-stu-id="f25a8-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="f25a8-127"><dt>MpClient。h</dt></span><span class="sxs-lookup"><span data-stu-id="f25a8-127"><dt>MpClient.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f25a8-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f25a8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f25a8-129">**MPRESOURCE \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="f25a8-129">**MPRESOURCE\_INFO**</span></span>](mpresource-info.md)
</dt> </dl>

 

 





