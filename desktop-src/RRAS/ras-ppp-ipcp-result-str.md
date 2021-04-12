---
title: 'RAS_PPP_IPCP_RESULT 結構 (Rassapi .h) '
description: RAS \_ ppp \_ IPCP \_ 結果結構是用來報告埠的 PPP 網際網路通訊協定 (IP) 投影作業的結果。
ms.assetid: edbdc8f2-ba56-4d34-8908-f7eccc2ebf61
keywords:
- RAS_PPP_IPCP_RESULT 結構 RAS
topic_type:
- apiref
api_name:
- RAS_PPP_IPCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: eedcd7c7390e01849371eee2cbb24ffa2593900d
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104508643"
---
# <a name="ras_ppp_ipcp_result-structure"></a><span data-ttu-id="9d171-104">RAS \_ PPP \_ IPCP \_ 結果結構</span><span class="sxs-lookup"><span data-stu-id="9d171-104">RAS\_PPP\_IPCP\_RESULT structure</span></span>

<span data-ttu-id="9d171-105">\[Windows Vista 不支援 **RAS \_ PPP \_ IPCP \_ 結果** 結構。\]</span><span class="sxs-lookup"><span data-stu-id="9d171-105">\[The **RAS\_PPP\_IPCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="9d171-106">**RAS \_ ppp \_ IPCP \_ 結果** 結構是用來報告埠的 PPP 網際網路通訊協定 (IP) 投影作業的結果。</span><span class="sxs-lookup"><span data-stu-id="9d171-106">The **RAS\_PPP\_IPCP\_RESULT** structure is used to report the result of a PPP Internet Protocol (IP) projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="9d171-107">語法</span><span class="sxs-lookup"><span data-stu-id="9d171-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_IPCP_RESULT {
  DWORD dwError;
  WCHAR wszAddress[RAS_IPADDRESSLEN + 1];
} RAS_PPP_IPCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="9d171-108">成員</span><span class="sxs-lookup"><span data-stu-id="9d171-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="9d171-109">**dwError**</span><span class="sxs-lookup"><span data-stu-id="9d171-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="9d171-110">表示 IP 投射作業的結果。</span><span class="sxs-lookup"><span data-stu-id="9d171-110">Indicates the results of the IP projection operation.</span></span> <span data-ttu-id="9d171-111">沒有錯誤的值 \_ 表示成功，在這種情況下， **wszAddress** 成員是有效的。</span><span class="sxs-lookup"><span data-stu-id="9d171-111">A value of NO\_ERROR indicates success, in which case, the **wszAddress** member is valid.</span></span> <span data-ttu-id="9d171-112">如果投射作業不成功，則 **dwError** 是 winerror.h .H 或 Raserror 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="9d171-112">If the projection operation was not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="9d171-113">**wszAddress**</span><span class="sxs-lookup"><span data-stu-id="9d171-113">**wszAddress**</span></span>
</dt> <dd>

<span data-ttu-id="9d171-114">以 null 終止的 Unicode 字串，指定指派給遠端用戶端的 IP 位址。</span><span class="sxs-lookup"><span data-stu-id="9d171-114">A null-terminated Unicode string that specifies the IP address assigned to the remote client.</span></span> <span data-ttu-id="9d171-115">這個字串的格式 \*為 \***。**_b_*_._*\*  c. \*_d._</span><span class="sxs-lookup"><span data-stu-id="9d171-115">This string has the form *a\***.**_b_*_._*_c_*_._\*_d_.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="9d171-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="9d171-116">Requirements</span></span>



| <span data-ttu-id="9d171-117">需求</span><span class="sxs-lookup"><span data-stu-id="9d171-117">Requirement</span></span> | <span data-ttu-id="9d171-118">值</span><span class="sxs-lookup"><span data-stu-id="9d171-118">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="9d171-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="9d171-119">Minimum supported client</span></span><br/> | <span data-ttu-id="9d171-120">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d171-120">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="9d171-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="9d171-121">Minimum supported server</span></span><br/> | <span data-ttu-id="9d171-122">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="9d171-122">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="9d171-123">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="9d171-123">End of client support</span></span><br/>    | <span data-ttu-id="9d171-124">Windows XP</span><span class="sxs-lookup"><span data-stu-id="9d171-124">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="9d171-125">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="9d171-125">End of server support</span></span><br/>    | <span data-ttu-id="9d171-126">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="9d171-126">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="9d171-127">標頭</span><span class="sxs-lookup"><span data-stu-id="9d171-127">Header</span></span><br/>                   | <dl> <span data-ttu-id="9d171-128"><dt>Rassapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="9d171-128"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="9d171-129">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9d171-129">See also</span></span>

<dl> <dt>

[<span data-ttu-id="9d171-130">遠端存取服務 (RAS) 總覽</span><span class="sxs-lookup"><span data-stu-id="9d171-130">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="9d171-131">RAS 伺服器管理結構</span><span class="sxs-lookup"><span data-stu-id="9d171-131">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="9d171-132">**RAS \_ 埠 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="9d171-132">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="9d171-133">**RAS \_ PPP \_ 投射 \_ 結果**</span><span class="sxs-lookup"><span data-stu-id="9d171-133">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="9d171-134">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="9d171-134">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





