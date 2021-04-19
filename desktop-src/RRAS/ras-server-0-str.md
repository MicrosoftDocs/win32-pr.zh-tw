---
title: 'RAS_SERVER_0 結構 (Rassapi .h) '
description: RasAdminServerGetInfo 函 \_ 式 \_ 會使用 ras 伺服器0結構來傳回在 RAS 伺服器上設定之埠的相關資訊。
ms.assetid: 8818ad68-b528-45fe-9ff4-eea194259f25
keywords:
- RAS_SERVER_0 結構 RAS
- PRAS_SERVER_0 結構指標 RAS
topic_type:
- apiref
api_name:
- RAS_SERVER_0
api_location:
- Rassapi.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 16f910fdfe53221daf8227d9f3e594133548fee9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969611"
---
# <a name="ras_server_0-structure"></a><span data-ttu-id="72db6-105">RAS \_ 伺服器 \_ 0 結構</span><span class="sxs-lookup"><span data-stu-id="72db6-105">RAS\_SERVER\_0 structure</span></span>

<span data-ttu-id="72db6-106">\[Windows Vista 不支援 **RAS \_ 伺服器 \_ 0** 結構。\]</span><span class="sxs-lookup"><span data-stu-id="72db6-106">\[The **RAS\_SERVER\_0** structure is not supported as of Windows Vista.\]</span></span>

<span data-ttu-id="72db6-107">[**RasAdminServerGetInfo**](rasadminservergetinfo.md)函式會使用 **ras \_ 伺服器 \_ 0** 結構來傳回在 RAS 伺服器上設定之埠的相關資訊。</span><span class="sxs-lookup"><span data-stu-id="72db6-107">The **RAS\_SERVER\_0** structure is used by the [**RasAdminServerGetInfo**](rasadminservergetinfo.md) function to return information about the ports configured on a RAS server.</span></span>

## <a name="syntax"></a><span data-ttu-id="72db6-108">語法</span><span class="sxs-lookup"><span data-stu-id="72db6-108">Syntax</span></span>


```C++
typedef struct _RAS_SERVER_0 {
  WORD  TotalPorts;
  WORD  PortsInUse;
  DWORD RasVersion;
} RAS_SERVER_0, *PRAS_SERVER_0;
```



## <a name="members"></a><span data-ttu-id="72db6-109">成員</span><span class="sxs-lookup"><span data-stu-id="72db6-109">Members</span></span>

<dl> <dt>

<span data-ttu-id="72db6-110">**TotalPorts**</span><span class="sxs-lookup"><span data-stu-id="72db6-110">**TotalPorts**</span></span>
</dt> <dd>

<span data-ttu-id="72db6-111">指定可供遠端用戶端連接的 RAS 伺服器上設定的埠總數。</span><span class="sxs-lookup"><span data-stu-id="72db6-111">Specifies the total number of ports configured on the RAS server that are available for remote clients to connect to.</span></span> <span data-ttu-id="72db6-112">例如，如果設定用來撥入伺服器的埠總數為四個，但其中一個埠目前用於撥出，則 **TotalPorts** 為三個。</span><span class="sxs-lookup"><span data-stu-id="72db6-112">For example, if the total number of ports configured for dialing in to a server is four, but one of the ports is currently in use for dialing out, **TotalPorts** is three.</span></span>

</dd> <dt>

<span data-ttu-id="72db6-113">**PortsInUse**</span><span class="sxs-lookup"><span data-stu-id="72db6-113">**PortsInUse**</span></span>
</dt> <dd>

<span data-ttu-id="72db6-114">指定遠端用戶端目前正在使用的埠數目。</span><span class="sxs-lookup"><span data-stu-id="72db6-114">Specifies the number of ports currently in use by remote clients.</span></span>

</dd> <dt>

<span data-ttu-id="72db6-115">**RasVersion**</span><span class="sxs-lookup"><span data-stu-id="72db6-115">**RasVersion**</span></span>
</dt> <dd>

<span data-ttu-id="72db6-116">指定 RAS 伺服器的版本。</span><span class="sxs-lookup"><span data-stu-id="72db6-116">Specifies the version of the RAS server.</span></span> <span data-ttu-id="72db6-117">使用此資訊來取得版本特定的動作。</span><span class="sxs-lookup"><span data-stu-id="72db6-117">Use this information to take version-specific action.</span></span> <span data-ttu-id="72db6-118">這個成員是下列其中一個值。</span><span class="sxs-lookup"><span data-stu-id="72db6-118">This member is one of the following values.</span></span>



| <span data-ttu-id="72db6-119">值</span><span class="sxs-lookup"><span data-stu-id="72db6-119">Value</span></span>                                                                                                                                                                  | <span data-ttu-id="72db6-120">意義</span><span class="sxs-lookup"><span data-stu-id="72db6-120">Meaning</span></span>                                                                         |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------|
| <span id="RASDOWNLEVEL"></span><span id="rasdownlevel"></span><dl> <span data-ttu-id="72db6-121"><dt>**RASDOWNLEVEL**</dt></span><span class="sxs-lookup"><span data-stu-id="72db6-121"><dt>**RASDOWNLEVEL**</dt></span></span> </dl>              | <span data-ttu-id="72db6-122">表示 LAN Manager 1.0 版 RAS 伺服器。</span><span class="sxs-lookup"><span data-stu-id="72db6-122">Indicates a LAN Manager version 1.0 RAS server.</span></span><br/>                      |
| <span id="RASADMIN_35"></span><span id="rasadmin_35"></span><dl> <span data-ttu-id="72db6-123"><dt>**RASADMIN \_ 35**</dt></span><span class="sxs-lookup"><span data-stu-id="72db6-123"><dt>**RASADMIN\_35**</dt></span></span> </dl>                | <span data-ttu-id="72db6-124">指出 Windows NT Server 3.51 及較早的 RAS 伺服器或用戶端。</span><span class="sxs-lookup"><span data-stu-id="72db6-124">Indicates a Windows NT Server 3.51 and earlier RAS server or client.</span></span><br/> |
| <span id="RASADMIN_CURRENT"></span><span id="rasadmin_current"></span><dl> <span data-ttu-id="72db6-125"><dt>**RASADMIN \_ 目前**</dt></span><span class="sxs-lookup"><span data-stu-id="72db6-125"><dt>**RASADMIN\_CURRENT**</dt></span></span> </dl> | <span data-ttu-id="72db6-126">指出 Windows NT 4.0 RAS 伺服器或用戶端。</span><span class="sxs-lookup"><span data-stu-id="72db6-126">Indicates a Windows NT 4.0 RAS server or client.</span></span><br/>                     |



 

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="72db6-127">規格需求</span><span class="sxs-lookup"><span data-stu-id="72db6-127">Requirements</span></span>



| <span data-ttu-id="72db6-128">需求</span><span class="sxs-lookup"><span data-stu-id="72db6-128">Requirement</span></span> | <span data-ttu-id="72db6-129">值</span><span class="sxs-lookup"><span data-stu-id="72db6-129">Value</span></span> |
|-------------------------------------|--------------------------------------------------------------------------------------|
| <span data-ttu-id="72db6-130">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="72db6-130">Minimum supported client</span></span><br/> | <span data-ttu-id="72db6-131">Windows 2000 Professional \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72db6-131">Windows 2000 Professional \[desktop apps only\]</span></span><br/>                           |
| <span data-ttu-id="72db6-132">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="72db6-132">Minimum supported server</span></span><br/> | <span data-ttu-id="72db6-133">Windows 2000 Server \[僅限傳統型應用程式\]</span><span class="sxs-lookup"><span data-stu-id="72db6-133">Windows 2000 Server \[desktop apps only\]</span></span><br/>                                 |
| <span data-ttu-id="72db6-134">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="72db6-134">End of client support</span></span><br/>    | <span data-ttu-id="72db6-135">Windows XP</span><span class="sxs-lookup"><span data-stu-id="72db6-135">Windows XP</span></span><br/>                                                                |
| <span data-ttu-id="72db6-136">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="72db6-136">End of server support</span></span><br/>    | <span data-ttu-id="72db6-137">Windows Server 2003</span><span class="sxs-lookup"><span data-stu-id="72db6-137">Windows Server 2003</span></span><br/>                                                       |
| <span data-ttu-id="72db6-138">標頭</span><span class="sxs-lookup"><span data-stu-id="72db6-138">Header</span></span><br/>                   | <dl> <span data-ttu-id="72db6-139"><dt>Rassapi。h</dt></span><span class="sxs-lookup"><span data-stu-id="72db6-139"><dt>Rassapi.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="72db6-140">另請參閱</span><span class="sxs-lookup"><span data-stu-id="72db6-140">See also</span></span>

<dl> <dt>

[<span data-ttu-id="72db6-141">遠端存取服務 (RAS) 總覽</span><span class="sxs-lookup"><span data-stu-id="72db6-141">Remote Access Service (RAS) Overview</span></span>](about-remote-access-service.md)
</dt> <dt>

[<span data-ttu-id="72db6-142">RAS 伺服器管理結構</span><span class="sxs-lookup"><span data-stu-id="72db6-142">RAS Server Administration Structures</span></span>](ras-server-administration-structures.md)
</dt> <dt>

[<span data-ttu-id="72db6-143">**RasAdminServerGetInfo**</span><span class="sxs-lookup"><span data-stu-id="72db6-143">**RasAdminServerGetInfo**</span></span>](rasadminservergetinfo.md)
</dt> </dl>

 

 





