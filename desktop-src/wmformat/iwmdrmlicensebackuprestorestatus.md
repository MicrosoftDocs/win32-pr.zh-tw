---
title: IWMDRMLicenseBackupRestoreStatus 介面
description: IWMDRMLicenseBackupRestoreStatus 介面會提供方法，以取得有關授權備份或還原作業的詳細狀態資訊。此介面會隨授權備份和還原作業期間產生的進度事件一起傳遞。
ms.assetid: fbcd059f-13d9-4edb-8946-b55c9da6dca4
keywords:
- IWMDRMLicenseBackupRestoreStatus 介面 windows 媒體格式
- IWMDRMLicenseBackupRestoreStatus 介面 windows 媒體格式，描述
topic_type:
- apiref
api_name:
- IWMDRMLicenseBackupRestoreStatus
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
api_location: ''
ms.openlocfilehash: a9db5d95daab78a506a3cc994fb9dd22153d0907
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104315994"
---
# <a name="iwmdrmlicensebackuprestorestatus-interface"></a><span data-ttu-id="93307-105">IWMDRMLicenseBackupRestoreStatus 介面</span><span class="sxs-lookup"><span data-stu-id="93307-105">IWMDRMLicenseBackupRestoreStatus interface</span></span>

<span data-ttu-id="93307-106">**IWMDRMLicenseBackupRestoreStatus** 介面會提供方法，以取得有關授權備份或還原作業的詳細狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="93307-106">The **IWMDRMLicenseBackupRestoreStatus** interface provides a method to retrieve detailed status information about a license backup or restore operation.</span></span>

<span data-ttu-id="93307-107">此介面會隨授權備份和還原作業期間產生的進度事件一起傳遞。</span><span class="sxs-lookup"><span data-stu-id="93307-107">This interface is delivered with progress events generated during license backup and restore operations.</span></span> <span data-ttu-id="93307-108">在授權備份期間會產生數個 **MEWMDRMLicenseBackupProgress** 事件，每個事件都有伴隨此介面的實例。</span><span class="sxs-lookup"><span data-stu-id="93307-108">Several **MEWMDRMLicenseBackupProgress** events are generated during license backup, each of which has an accompanying instance of this interface.</span></span> <span data-ttu-id="93307-109">在授權還原期間產生的 **MEWMDRMLicenseRestoreProgress** 事件也是如此。</span><span class="sxs-lookup"><span data-stu-id="93307-109">The same is true of **MEWMDRMLicenseRestoreProgress** events, which are generated during license restoration.</span></span>

<span data-ttu-id="93307-110">若要取出 **IWMDRMLicenseBackupRestoreStatus** 介面實例的指標，您必須先呼叫進度事件的 **IMFMediaEvent：： GetValue** 方法。</span><span class="sxs-lookup"><span data-stu-id="93307-110">To retrieve a pointer to an instance of the **IWMDRMLicenseBackupRestoreStatus** interface, you must first call the **IMFMediaEvent::GetValue** method of the progress event.</span></span> <span data-ttu-id="93307-111">您從事件中取出的值是實 **IWMDRMLicenseBackupRestoreStatus** 介面之物件的 **IUnknown** 介面指標。</span><span class="sxs-lookup"><span data-stu-id="93307-111">The value you retrieve from the event is a pointer to the **IUnknown** interface of the object that implements the **IWMDRMLicenseBackupRestoreStatus** interface.</span></span>

## <a name="members"></a><span data-ttu-id="93307-112">成員</span><span class="sxs-lookup"><span data-stu-id="93307-112">Members</span></span>

<span data-ttu-id="93307-113">**IWMDRMLicenseBackupRestoreStatus** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。</span><span class="sxs-lookup"><span data-stu-id="93307-113">The **IWMDRMLicenseBackupRestoreStatus** interface inherits from the [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.</span></span> <span data-ttu-id="93307-114">**IWMDRMLicenseBackupRestoreStatus** 也有下列類型的成員：</span><span class="sxs-lookup"><span data-stu-id="93307-114">**IWMDRMLicenseBackupRestoreStatus** also has these types of members:</span></span>

-   [<span data-ttu-id="93307-115">方法</span><span class="sxs-lookup"><span data-stu-id="93307-115">Methods</span></span>](#methods)

### <a name="methods"></a><span data-ttu-id="93307-116">方法</span><span class="sxs-lookup"><span data-stu-id="93307-116">Methods</span></span>

<span data-ttu-id="93307-117">**IWMDRMLicenseBackupRestoreStatus** 介面具有這些方法。</span><span class="sxs-lookup"><span data-stu-id="93307-117">The **IWMDRMLicenseBackupRestoreStatus** interface has these methods.</span></span>



| <span data-ttu-id="93307-118">方法</span><span class="sxs-lookup"><span data-stu-id="93307-118">Method</span></span>                                                          | <span data-ttu-id="93307-119">描述</span><span class="sxs-lookup"><span data-stu-id="93307-119">Description</span></span>                                                                                   |
|:----------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| [<span data-ttu-id="93307-120">**GetStatus**</span><span class="sxs-lookup"><span data-stu-id="93307-120">**GetStatus**</span></span>](iwmdrmlicensebackuprestorestatus-getstatus.md) | <span data-ttu-id="93307-121">捕獲有關授權備份或還原作業的詳細狀態資訊。</span><span class="sxs-lookup"><span data-stu-id="93307-121">Retrieves detailed status information about a license backup or restore operation.</span></span><br/> |



 

## <a name="see-also"></a><span data-ttu-id="93307-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="93307-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="93307-123">**介面**</span><span class="sxs-lookup"><span data-stu-id="93307-123">**Interfaces**</span></span>](drm-interfaces.md)
</dt> </dl>

 

