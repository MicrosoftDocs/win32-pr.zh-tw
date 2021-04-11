---
title: 'RAS_PPP_ATCP_RESULT 結構 (Rassapi .h) '
description: RAS \_ PPP 的 \_ ATCP \_ 結果結構是用來報告埠之 AppleTalk 通訊協定投影作業的結果。
ms.assetid: ac9df618-f79c-4066-a37e-f92e64e951dd
keywords:
- RAS_PPP_ATCP_RESULT 結構 RAS
topic_type:
- apiref
api_name:
- RAS_PPP_ATCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 66f3f950af9d5bdde8feef085457a895212ad04b
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934482"
---
# <a name="ras_ppp_atcp_result-structure"></a><span data-ttu-id="e23af-104">RAS \_ PPP \_ ATCP \_ 結果結構</span><span class="sxs-lookup"><span data-stu-id="e23af-104">RAS\_PPP\_ATCP\_RESULT structure</span></span>

<span data-ttu-id="e23af-105">\[Windows Vista 不支援 **RAS \_ PPP \_ ATCP \_ 結果** 結構。\]</span><span class="sxs-lookup"><span data-stu-id="e23af-105">\[The **RAS\_PPP\_ATCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="e23af-106">**RAS \_ PPP 的 \_ ATCP \_ 結果** 結構是用來報告埠之 AppleTalk 通訊協定投影作業的結果。</span><span class="sxs-lookup"><span data-stu-id="e23af-106">The **RAS\_PPP\_ATCP\_RESULT** structure is used to report the result of an AppleTalk protocol projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="e23af-107">語法</span><span class="sxs-lookup"><span data-stu-id="e23af-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_ATCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_ATADDRESSLEN + 1];
} RAS_PPP_ATCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="e23af-108">成員</span><span class="sxs-lookup"><span data-stu-id="e23af-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="e23af-109">**dwError**</span><span class="sxs-lookup"><span data-stu-id="e23af-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="e23af-110">指定值，指出 AppleTalk 投射作業的結果。</span><span class="sxs-lookup"><span data-stu-id="e23af-110">Specifies a value that indicates the results of the AppleTalk projection operation.</span></span> <span data-ttu-id="e23af-111">沒有錯誤的值 \_ 表示成功，在這種情況下， **wszAddress** 成員是有效的。</span><span class="sxs-lookup"><span data-stu-id="e23af-111">A value of NO\_ERROR indicates success, in which case, the **wszAddress** member is valid.</span></span> <span data-ttu-id="e23af-112">如果投射作業不成功，則 **dwError** 是 winerror.h .H 或 Raserror 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="e23af-112">If the projection operation is not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="e23af-113">**wszAddress**</span><span class="sxs-lookup"><span data-stu-id="e23af-113">**wszAddress**</span></span>
</dt> <dd>

<span data-ttu-id="e23af-114">指定以 null 終止的 Unicode 字串，指定指派給遠端用戶端的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="e23af-114">Specifies a null-terminated Unicode string that specifies the IP address assigned to the remote client.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="e23af-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="e23af-115">Requirements</span></span>



| <span data-ttu-id="e23af-116">需求</span><span class="sxs-lookup"><span data-stu-id="e23af-116">Requirement</span></span> | <span data-ttu-id="e23af-117">值</span><span class="sxs-lookup"><span data-stu-id="e23af-117">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="e23af-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="e23af-118">Minimum supported client</span></span><br/> | <span data-ttu-id="e23af-119">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e23af-119">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="e23af-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="e23af-120">Minimum supported server</span></span><br/> | <span data-ttu-id="e23af-121">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="e23af-121">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="e23af-122">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="e23af-122">End of client support</span></span><br/>    | <span data-ttu-id="e23af-123">Windows XP</span><span class="sxs-lookup"><span data-stu-id="e23af-123">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="e23af-124">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="e23af-124">End of server support</span></span><br/>    | <span data-ttu-id="e23af-125">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="e23af-125">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="e23af-126">標頭</span><span class="sxs-lookup"><span data-stu-id="e23af-126">Header</span></span><br/>                   | <dl> <span data-ttu-id="e23af-127"><dt>Rassapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="e23af-127"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="e23af-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e23af-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="e23af-129">遠端存取服務 (RAS) 總覽</span><span class="sxs-lookup"><span data-stu-id="e23af-129">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="e23af-130">RAS 伺服器管理結構</span><span class="sxs-lookup"><span data-stu-id="e23af-130">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="e23af-131">**RAS \_ PPP \_ 投射 \_ 結果**</span><span class="sxs-lookup"><span data-stu-id="e23af-131">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> </dl>

 

 





