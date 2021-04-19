---
description: 代表磁碟分割管理員上針對屬於叢集一部分之磁片所維護的資訊。
ms.assetid: 9138F61A-E295-4F5B-AD65-361FCCB3C4B7
title: 'DISK_CLUSTER_INFO 結構 (Ntdddisk .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- DISK_CLUSTER_INFO
api_type:
- HeaderDef
api_location:
- Ntdddisk.h
ms.openlocfilehash: f18e8f47cd5b1b527c9d6d2d19a09775528602d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969373"
---
# <a name="disk_cluster_info-structure"></a><span data-ttu-id="41aea-103">磁片 \_ 群集 \_ 資訊結構</span><span class="sxs-lookup"><span data-stu-id="41aea-103">DISK\_CLUSTER\_INFO structure</span></span>

<span data-ttu-id="41aea-104">代表磁碟分割管理員上針對屬於叢集一部分之磁片所維護的資訊。</span><span class="sxs-lookup"><span data-stu-id="41aea-104">Represents information maintained on the partition manager about a disk that is part of a cluster.</span></span>

## <a name="syntax"></a><span data-ttu-id="41aea-105">語法</span><span class="sxs-lookup"><span data-stu-id="41aea-105">Syntax</span></span>


```C++
typedef struct _DISK_CLUSTER_INFO {
  ULONG     Version;
  ULONGLONG Flags;
  ULONGLONG FlagsMask;
  BOOLEAN   Notify;
} DISK_CLUSTER_INFO, *PDISK_CLUSTER_INFO;
```



## <a name="members"></a><span data-ttu-id="41aea-106">成員</span><span class="sxs-lookup"><span data-stu-id="41aea-106">Members</span></span>

<dl> <dt>

<span data-ttu-id="41aea-107">**版本**</span><span class="sxs-lookup"><span data-stu-id="41aea-107">**Version**</span></span>
</dt> <dd>

<span data-ttu-id="41aea-108">版本號碼。</span><span class="sxs-lookup"><span data-stu-id="41aea-108">The version number.</span></span> <span data-ttu-id="41aea-109">此值必須設定為此結構的大小。</span><span class="sxs-lookup"><span data-stu-id="41aea-109">This value must be set to the size of this structure.</span></span>

</dd> <dt>

<span data-ttu-id="41aea-110">**旗標**</span><span class="sxs-lookup"><span data-stu-id="41aea-110">**Flags**</span></span>
</dt> <dd>

<span data-ttu-id="41aea-111">與磁片和叢集相關的旗標組合。</span><span class="sxs-lookup"><span data-stu-id="41aea-111">A combination of flags related to disks and clusters.</span></span>



| <span data-ttu-id="41aea-112">值</span><span class="sxs-lookup"><span data-stu-id="41aea-112">Value</span></span>                                                                                                                                                                                                                                                                                               | <span data-ttu-id="41aea-113">意義</span><span class="sxs-lookup"><span data-stu-id="41aea-113">Meaning</span></span>                                                                                                                 |
|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------|
| <span id="DISK_CLUSTER_FLAG_ENABLED"></span><span id="disk_cluster_flag_enabled"></span><dl> <span data-ttu-id="41aea-114"><dt>**磁片 \_叢集 \_ 旗標 \_ 已啟用**</dt> <dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="41aea-114"><dt>**DISK\_CLUSTER\_FLAG\_ENABLED**</dt> <dt>1</dt></span></span> </dl>                                          | <span data-ttu-id="41aea-115">磁片會當做叢集服務的一部分使用。</span><span class="sxs-lookup"><span data-stu-id="41aea-115">The disk is used as part of the cluster service.</span></span><br/>                                                             |
| <span id="DISK_CLUSTER_FLAG_CSV"></span><span id="disk_cluster_flag_csv"></span><dl> <span data-ttu-id="41aea-116"><dt>**磁片 \_群集 \_ 旗標 \_ CSV**</dt> <dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="41aea-116"><dt>**DISK\_CLUSTER\_FLAG\_CSV**</dt> <dt>2</dt></span></span> </dl>                                                      | <span data-ttu-id="41aea-117">磁片上的磁片區是由所有叢集節點上的 CSVFS 所公開。</span><span class="sxs-lookup"><span data-stu-id="41aea-117">Volumes on the disk are exposed by CSVFS on all nodes of the cluster.</span></span><br/>                                        |
| <span id="DISK_CLUSTER_FLAG_IN_MAINTENANCE"></span><span id="disk_cluster_flag_in_maintenance"></span><dl> <span data-ttu-id="41aea-118"><dt>**磁片 \_\_維護 4 \_ 中 \_ 的群集旗**</dt>標 <dt></dt></span><span class="sxs-lookup"><span data-stu-id="41aea-118"><dt>**DISK\_CLUSTER\_FLAG\_IN\_MAINTENANCE**</dt> <dt>4</dt></span></span> </dl>                    | <span data-ttu-id="41aea-119">與此磁片相關聯的叢集資源處於維護模式。</span><span class="sxs-lookup"><span data-stu-id="41aea-119">The cluster resource associated with this disk is in maintenance mode.</span></span><br/>                                       |
| <span id="DISK_CLUSTER_FLAG_PNP_ARRIVAL_COMPLETE"></span><span id="disk_cluster_flag_pnp_arrival_complete"></span><dl> <span data-ttu-id="41aea-120"><dt>**磁片 \_叢集 \_ 旗標 \_ PNP \_ 抵達 \_ 完成**</dt> <dt>8</dt></span><span class="sxs-lookup"><span data-stu-id="41aea-120"><dt>**DISK\_CLUSTER\_FLAG\_PNP\_ARRIVAL\_COMPLETE**</dt> <dt>8</dt></span></span> </dl> | <span data-ttu-id="41aea-121">適用于核心模式的叢集磁片驅動程式 (clusdisk) 已收到磁片抵達的 PnP 通知。</span><span class="sxs-lookup"><span data-stu-id="41aea-121">The cluster disk driver for kernel mode (clusdisk) has received PnP notification of the arrival of the disk.</span></span><br/> |



 

</dd> <dt>

<span data-ttu-id="41aea-122">**FlagsMask**</span><span class="sxs-lookup"><span data-stu-id="41aea-122">**FlagsMask**</span></span>
</dt> <dd>

<span data-ttu-id="41aea-123">**旗** 標成員中正在修改的旗標。</span><span class="sxs-lookup"><span data-stu-id="41aea-123">The flags that are being modified in the **Flags** member.</span></span>

</dd> <dt>

<span data-ttu-id="41aea-124">**通知**</span><span class="sxs-lookup"><span data-stu-id="41aea-124">**Notify**</span></span>
</dt> <dd>

<span data-ttu-id="41aea-125">**TRUE** 表示傳送配置變更通知;否則 **為 FALSE**。</span><span class="sxs-lookup"><span data-stu-id="41aea-125">**TRUE** to send a layout change notification; otherwise, **FALSE**.</span></span>

</dd> </dl>

## <a name="requirements"></a><span data-ttu-id="41aea-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="41aea-126">Requirements</span></span>



| <span data-ttu-id="41aea-127">需求</span><span class="sxs-lookup"><span data-stu-id="41aea-127">Requirement</span></span> | <span data-ttu-id="41aea-128">值</span><span class="sxs-lookup"><span data-stu-id="41aea-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="41aea-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="41aea-129">Minimum supported client</span></span><br/> | <span data-ttu-id="41aea-130">都不支援</span><span class="sxs-lookup"><span data-stu-id="41aea-130">None supported</span></span><br/>                                                             |
| <span data-ttu-id="41aea-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="41aea-131">Minimum supported server</span></span><br/> | <span data-ttu-id="41aea-132">僅限 Windows Server 2012 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="41aea-132">Windows Server 2012 \[desktop apps only\]</span></span><br/>                                  |
| <span data-ttu-id="41aea-133">標頭</span><span class="sxs-lookup"><span data-stu-id="41aea-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="41aea-134"><dt>Ntdddisk。h</dt></span><span class="sxs-lookup"><span data-stu-id="41aea-134"><dt>Ntdddisk.h</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="41aea-135">另請參閱</span><span class="sxs-lookup"><span data-stu-id="41aea-135">See also</span></span>

<dl> <dt>

[<span data-ttu-id="41aea-136">磁片管理結構</span><span class="sxs-lookup"><span data-stu-id="41aea-136">Disk Management Structures</span></span>](disk-management-structures.md)
</dt> <dt>

[<span data-ttu-id="41aea-137">**IOCTL \_ 磁片 \_ 取得 \_ 叢集 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="41aea-137">**IOCTL\_DISK\_GET\_CLUSTER\_INFO**</span></span>](ioctl-disk-get-cluster-info.md)
</dt> <dt>

[<span data-ttu-id="41aea-138">**IOCTL \_ 磁片 \_ 集 \_ 叢集 \_ 資訊**</span><span class="sxs-lookup"><span data-stu-id="41aea-138">**IOCTL\_DISK\_SET\_CLUSTER\_INFO**</span></span>](ioctl-disk-set-cluster-info.md)
</dt> </dl>

 

 




