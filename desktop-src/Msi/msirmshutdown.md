---
description: MSIRMSHUTDOWN 屬性會決定如何關閉目前使用受更新影響之檔案的應用程式或服務，以啟用更新的安裝。
ms.assetid: 6763a490-8d1a-42d2-a8cb-0743b7ba6866
title: MSIRMSHUTDOWN 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4011e4fad980913271012dd86de44eec8c514f7a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106983143"
---
# <a name="msirmshutdown-property"></a><span data-ttu-id="62629-103">MSIRMSHUTDOWN 屬性</span><span class="sxs-lookup"><span data-stu-id="62629-103">MSIRMSHUTDOWN property</span></span>

<span data-ttu-id="62629-104">**MSIRMSHUTDOWN** 屬性會決定如何關閉目前使用受更新影響之檔案的應用程式或服務，以啟用更新的安裝。</span><span class="sxs-lookup"><span data-stu-id="62629-104">The **MSIRMSHUTDOWN** property determines how applications or services that are currently using files affected by an update should be shut down to enable the installation of the update.</span></span>

## <a name="value"></a><span data-ttu-id="62629-105">值</span><span class="sxs-lookup"><span data-stu-id="62629-105">Value</span></span>



| <span data-ttu-id="62629-106">值</span><span class="sxs-lookup"><span data-stu-id="62629-106">Value</span></span>                                                                        | <span data-ttu-id="62629-107">意義</span><span class="sxs-lookup"><span data-stu-id="62629-107">Meaning</span></span>                                                                                                                                                                                                                                                                 |
|------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="62629-108"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="62629-108"><dt>0</dt></span></span> </dl> | <span data-ttu-id="62629-109">目前使用受更新影響之檔案的處理常式或服務會關閉。</span><span class="sxs-lookup"><span data-stu-id="62629-109">Processes or services that are currently using files affected by the update are shut down.</span></span><br/>                                                                                                                                                                   |
| <dl> <span data-ttu-id="62629-110"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="62629-110"><dt>1</dt></span></span> </dl> | <span data-ttu-id="62629-111">如果處理常式或服務目前使用受更新影響的檔案，而且沒有回應 [重新開機管理員](../rstmgr/restart-manager-portal.md)，則會強制關閉。</span><span class="sxs-lookup"><span data-stu-id="62629-111">Processes or services that are currently using files affected by the update, and that do not respond to the [Restart Manager](../rstmgr/restart-manager-portal.md), are forced to shut down.</span></span><br/>                                                                                       |
| <dl> <span data-ttu-id="62629-112"><dt>2</dt></span><span class="sxs-lookup"><span data-stu-id="62629-112"><dt>2</dt></span></span> </dl> | <span data-ttu-id="62629-113">目前使用受更新影響之檔案的處理常式或服務，只有在已註冊重新開機時才會關閉。</span><span class="sxs-lookup"><span data-stu-id="62629-113">Processes or services that are currently using files affected by the update are shut down only if they have all been registered for a restart.</span></span> <span data-ttu-id="62629-114">如果有任何進程或服務尚未註冊進行重新開機，則不會關閉任何進程或服務。</span><span class="sxs-lookup"><span data-stu-id="62629-114">If any process or service has not been registered for a restart, then no processes or services are shut down.</span></span><br/> |



 

## <a name="remarks"></a><span data-ttu-id="62629-115">備註</span><span class="sxs-lookup"><span data-stu-id="62629-115">Remarks</span></span>

<span data-ttu-id="62629-116">如果 [重新開機管理員](../rstmgr/restart-manager-portal.md)無法使用或停用，則會忽略 **MSIRMSHUTDOWN** 屬性。</span><span class="sxs-lookup"><span data-stu-id="62629-116">The **MSIRMSHUTDOWN** property is ignored if the [Restart Manager](../rstmgr/restart-manager-portal.md) is unavailable or disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="62629-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="62629-117">Requirements</span></span>



| <span data-ttu-id="62629-118">需求</span><span class="sxs-lookup"><span data-stu-id="62629-118">Requirement</span></span> | <span data-ttu-id="62629-119">值</span><span class="sxs-lookup"><span data-stu-id="62629-119">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="62629-120">版本</span><span class="sxs-lookup"><span data-stu-id="62629-120">Version</span></span><br/> | <span data-ttu-id="62629-121">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="62629-121">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="62629-122">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="62629-122">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="62629-123">如需 Windows Installer 版本所需的最低 service pack 資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="62629-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="62629-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62629-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62629-125">屬性</span><span class="sxs-lookup"><span data-stu-id="62629-125">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="62629-126">Windows Installer 3.1 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="62629-126">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
