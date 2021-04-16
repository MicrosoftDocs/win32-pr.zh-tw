---
description: 磁片管理中使用的介面。
ms.assetid: c1f79e2e-834b-41dc-a15f-6dd1034d021b
title: 磁片管理介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c86881ff3bf6232da68c4cf1539dbbedf87c50f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194400"
---
# <a name="disk-management-interfaces"></a><span data-ttu-id="85f87-103">磁片管理介面</span><span class="sxs-lookup"><span data-stu-id="85f87-103">Disk Management Interfaces</span></span>

<span data-ttu-id="85f87-104">下列介面用於磁片管理。</span><span class="sxs-lookup"><span data-stu-id="85f87-104">The following interfaces are used in disk management.</span></span>

## <a name="in-this-section"></a><span data-ttu-id="85f87-105">本節內容</span><span class="sxs-lookup"><span data-stu-id="85f87-105">In this section</span></span>



| <span data-ttu-id="85f87-106">介面</span><span class="sxs-lookup"><span data-stu-id="85f87-106">Interface</span></span>                                                     | <span data-ttu-id="85f87-107">描述</span><span class="sxs-lookup"><span data-stu-id="85f87-107">Description</span></span>                                                                                                    |
|---------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="85f87-108">**IDiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="85f87-108">**IDiskQuotaControl**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)<br/>     | <span data-ttu-id="85f87-109">控制單一 NTFS 檔案系統磁片區的磁片配額工具。</span><span class="sxs-lookup"><span data-stu-id="85f87-109">Controls the disk quota facilities of a single NTFS file system volume.</span></span><br/>                             |
| [<span data-ttu-id="85f87-110">**IDiskQuotaEvents**</span><span class="sxs-lookup"><span data-stu-id="85f87-110">**IDiskQuotaEvents**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)<br/>       | <span data-ttu-id="85f87-111">接收與配額相關的事件通知。</span><span class="sxs-lookup"><span data-stu-id="85f87-111">Receives quota-related event notifications.</span></span><br/>                                                         |
| [<span data-ttu-id="85f87-112">**IDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="85f87-112">**IDiskQuotaUser**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)<br/>           | <span data-ttu-id="85f87-113">代表磁片區配額資訊檔案中的單一使用者配額專案。</span><span class="sxs-lookup"><span data-stu-id="85f87-113">Represents a single user quota entry in the volume quota information file.</span></span><br/>                          |
| [<span data-ttu-id="85f87-114">**IDiskQuotaUserBatch**</span><span class="sxs-lookup"><span data-stu-id="85f87-114">**IDiskQuotaUserBatch**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch)<br/> | <span data-ttu-id="85f87-115">新增多個配額使用者物件到容器，然後在單一呼叫中提交以進行更新。</span><span class="sxs-lookup"><span data-stu-id="85f87-115">Adds multiple quota user objects to a container that is then submitted for update in a single call.</span></span><br/> |
| [<span data-ttu-id="85f87-116">**IEnumDiskQuotaUsers**</span><span class="sxs-lookup"><span data-stu-id="85f87-116">**IEnumDiskQuotaUsers**</span></span>](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers)<br/> | <span data-ttu-id="85f87-117">列舉磁片區上的使用者配額專案。</span><span class="sxs-lookup"><span data-stu-id="85f87-117">Enumerates user quota entries on the volume.</span></span><br/>                                                        |



 

 

