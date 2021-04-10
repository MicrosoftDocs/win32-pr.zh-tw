---
title: 'RAS_PPP_NBFCP_RESULT 結構 (Rassapi .h) '
description: RAS \_ ppp \_ NBFCP \_ 結果結構是用來報告通訊埠的 PPP NETBEUI Framer (NBF) 投影作業的結果。
ms.assetid: 670bf125-cad5-481f-89e4-858e636316bd
keywords:
- RAS_PPP_NBFCP_RESULT 結構 RAS
topic_type:
- apiref
api_name:
- RAS_PPP_NBFCP_RESULT
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ddcb1cfe28a72e390cedbcc35fa299dddbfb8634
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104103998"
---
# <a name="ras_ppp_nbfcp_result-structure"></a><span data-ttu-id="61a5a-104">RAS \_ PPP \_ NBFCP \_ 結果結構</span><span class="sxs-lookup"><span data-stu-id="61a5a-104">RAS\_PPP\_NBFCP\_RESULT structure</span></span>

<span data-ttu-id="61a5a-105">\[Windows Vista 不支援 **RAS \_ PPP \_ NBFCP \_ 結果** 結構。\]</span><span class="sxs-lookup"><span data-stu-id="61a5a-105">\[The **RAS\_PPP\_NBFCP\_RESULT** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="61a5a-106">**RAS \_ ppp \_ NBFCP \_ 結果** 結構是用來報告通訊埠的 PPP NetBEUI Framer (NBF) 投影作業的結果。</span><span class="sxs-lookup"><span data-stu-id="61a5a-106">The **RAS\_PPP\_NBFCP\_RESULT** structure is used to report the result of a PPP NetBEUI Framer (NBF) projection operation for a port.</span></span>

## <a name="syntax"></a><span data-ttu-id="61a5a-107">語法</span><span class="sxs-lookup"><span data-stu-id="61a5a-107">Syntax</span></span>


```C++
typedef struct _RAS_PPP_NBFCP_RESULT {
  DWORD dwError;
  DWORD dwNetBiosError;
  CHAR  szName[NETBIOS_NAME_LEN + 1];
  WCHAR wszWksta[NETBIOS_NAME_LEN + 1];
} RAS_PPP_NBFCP_RESULT;
```



## <a name="members"></a><span data-ttu-id="61a5a-108">成員</span><span class="sxs-lookup"><span data-stu-id="61a5a-108">Members</span></span>

<dl> <dt>

<span data-ttu-id="61a5a-109">**dwError**</span><span class="sxs-lookup"><span data-stu-id="61a5a-109">**dwError**</span></span>
</dt> <dd>

<span data-ttu-id="61a5a-110">表示 NBF 投射作業的結果。</span><span class="sxs-lookup"><span data-stu-id="61a5a-110">Indicates the results of the NBF projection operation.</span></span> <span data-ttu-id="61a5a-111">沒有錯誤的值 \_ 表示成功，在這種情況下， **wszWksta** 成員會包含遠端電腦的名稱。</span><span class="sxs-lookup"><span data-stu-id="61a5a-111">A value of NO\_ERROR indicates success, in which case, the **wszWksta** member contains the name of the remote computer.</span></span> <span data-ttu-id="61a5a-112">如果投射作業不成功，則 **dwError** 是 winerror.h .H 或 Raserror 的錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="61a5a-112">If the projection operation was not successful, **dwError** is an error code from Winerror.h or Raserror.h.</span></span>

</dd> <dt>

<span data-ttu-id="61a5a-113">**dwNetBiosError**</span><span class="sxs-lookup"><span data-stu-id="61a5a-113">**dwNetBiosError**</span></span>
</dt> <dd>

<span data-ttu-id="61a5a-114">忽略伺服器上的這個成員;它只與用戶端相關。</span><span class="sxs-lookup"><span data-stu-id="61a5a-114">Ignore this member on the server; it is relevant only on the client.</span></span>

</dd> <dt>

<span data-ttu-id="61a5a-115">**szName**</span><span class="sxs-lookup"><span data-stu-id="61a5a-115">**szName**</span></span>
</dt> <dd>

<span data-ttu-id="61a5a-116">忽略伺服器上的這個成員;它只與用戶端相關。</span><span class="sxs-lookup"><span data-stu-id="61a5a-116">Ignore this member on the server; it is relevant only on the client.</span></span>

</dd> <dt>

<span data-ttu-id="61a5a-117">**wszWksta**</span><span class="sxs-lookup"><span data-stu-id="61a5a-117">**wszWksta**</span></span>
</dt> <dd>

<span data-ttu-id="61a5a-118">以 null 結束的 Unicode 字串，指定 RAS 用戶端工作站的 NetBIOS 名稱。</span><span class="sxs-lookup"><span data-stu-id="61a5a-118">A null-terminated Unicode string that specifies the NetBIOS name of the RAS client workstation.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="61a5a-119">規格需求</span><span class="sxs-lookup"><span data-stu-id="61a5a-119">Requirements</span></span>



| <span data-ttu-id="61a5a-120">需求</span><span class="sxs-lookup"><span data-stu-id="61a5a-120">Requirement</span></span> | <span data-ttu-id="61a5a-121">值</span><span class="sxs-lookup"><span data-stu-id="61a5a-121">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="61a5a-122">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="61a5a-122">Minimum supported client</span></span><br/> | <span data-ttu-id="61a5a-123">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61a5a-123">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="61a5a-124">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="61a5a-124">Minimum supported server</span></span><br/> | <span data-ttu-id="61a5a-125">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="61a5a-125">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="61a5a-126">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="61a5a-126">End of client support</span></span><br/>    | <span data-ttu-id="61a5a-127">Windows XP</span><span class="sxs-lookup"><span data-stu-id="61a5a-127">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="61a5a-128">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="61a5a-128">End of server support</span></span><br/>    | <span data-ttu-id="61a5a-129">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="61a5a-129">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="61a5a-130">標頭</span><span class="sxs-lookup"><span data-stu-id="61a5a-130">Header</span></span><br/>                   | <dl> <span data-ttu-id="61a5a-131"><dt>Rassapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="61a5a-131"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="61a5a-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="61a5a-132">See also</span></span>

<dl> <dt>

[<span data-ttu-id="61a5a-133">遠端存取服務 (RAS) 總覽</span><span class="sxs-lookup"><span data-stu-id="61a5a-133">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="61a5a-134">RAS 伺服器管理結構</span><span class="sxs-lookup"><span data-stu-id="61a5a-134">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="61a5a-135">**RAS \_ 埠 \_ 1**</span><span class="sxs-lookup"><span data-stu-id="61a5a-135">**RAS\_PORT\_1**</span></span>](ras-port-1-str.md)
</dt> <dt>

[<span data-ttu-id="61a5a-136">**RAS \_ PPP \_ 投射 \_ 結果**</span><span class="sxs-lookup"><span data-stu-id="61a5a-136">**RAS\_PPP\_PROJECTION\_RESULT**</span></span>](ras-ppp-projection-result-str.md)
</dt> <dt>

[<span data-ttu-id="61a5a-137">**RasAdminPortGetInfo**</span><span class="sxs-lookup"><span data-stu-id="61a5a-137">**RasAdminPortGetInfo**</span></span>](rasadminportgetinfo.md)
</dt> </dl>

 

 





