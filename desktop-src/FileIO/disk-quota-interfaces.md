---
description: 搭配磁片配額使用的介面。
ms.assetid: 422d93d9-f4aa-428d-94c1-fdf2dcf4c974
title: 磁片配額介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7bbcd4240a6a5910942aad71c7ea080da40918a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104469397"
---
# <a name="disk-quota-interfaces"></a><span data-ttu-id="cf979-103">磁片配額介面</span><span class="sxs-lookup"><span data-stu-id="cf979-103">Disk Quota Interfaces</span></span>

<span data-ttu-id="cf979-104">下列介面適用于磁片配額。</span><span class="sxs-lookup"><span data-stu-id="cf979-104">The following interfaces are used with disk quotas.</span></span>



| <span data-ttu-id="cf979-105">介面</span><span class="sxs-lookup"><span data-stu-id="cf979-105">Interface</span></span>                                          | <span data-ttu-id="cf979-106">描述</span><span class="sxs-lookup"><span data-stu-id="cf979-106">Description</span></span>                                                                                                    |
|----------------------------------------------------|----------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="cf979-107">**IDiskQuotaControl**</span><span class="sxs-lookup"><span data-stu-id="cf979-107">**IDiskQuotaControl**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotacontrol)     | <span data-ttu-id="cf979-108">控制單一 NTFS 檔案系統磁片區的磁片配額工具。</span><span class="sxs-lookup"><span data-stu-id="cf979-108">Controls the disk quota facilities of a single NTFS file system volume.</span></span><br/>                             |
| [<span data-ttu-id="cf979-109">**IDiskQuotaEvents**</span><span class="sxs-lookup"><span data-stu-id="cf979-109">**IDiskQuotaEvents**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotaevents)       | <span data-ttu-id="cf979-110">接收與配額相關的事件通知。</span><span class="sxs-lookup"><span data-stu-id="cf979-110">Receives quota-related event notifications.</span></span><br/>                                                         |
| [<span data-ttu-id="cf979-111">**IDiskQuotaUser**</span><span class="sxs-lookup"><span data-stu-id="cf979-111">**IDiskQuotaUser**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauser)           | <span data-ttu-id="cf979-112">代表磁片區配額資訊檔案中的單一使用者配額專案。</span><span class="sxs-lookup"><span data-stu-id="cf979-112">Represents a single user quota entry in the volume quota information file.</span></span><br/>                          |
| [<span data-ttu-id="cf979-113">**IDiskQuotaUserBatch**</span><span class="sxs-lookup"><span data-stu-id="cf979-113">**IDiskQuotaUserBatch**</span></span>](/windows/win32/api/dskquota/nn-dskquota-idiskquotauserbatch) | <span data-ttu-id="cf979-114">新增多個配額使用者物件到容器，然後在單一呼叫中提交以進行更新。</span><span class="sxs-lookup"><span data-stu-id="cf979-114">Adds multiple quota user objects to a container that is then submitted for update in a single call.</span></span><br/> |
| [<span data-ttu-id="cf979-115">**IEnumDiskQuotaUsers**</span><span class="sxs-lookup"><span data-stu-id="cf979-115">**IEnumDiskQuotaUsers**</span></span>](/windows/win32/api/dskquota/nn-dskquota-ienumdiskquotausers) | <span data-ttu-id="cf979-116">列舉磁片區上的使用者配額專案。</span><span class="sxs-lookup"><span data-stu-id="cf979-116">Enumerates user quota entries on the volume.</span></span><br/>                                                        |



 

 

