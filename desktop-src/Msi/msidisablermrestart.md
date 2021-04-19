---
description: MSIDISABLERMRESTART 屬性會決定目前使用受更新影響之檔案的應用程式或服務如何關閉並重新啟動，以啟用更新的安裝。
ms.assetid: 45c804bf-6d15-416a-b106-d8bb3f4c547d
title: MSIDISABLERMRESTART 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: e1215822b26bb9bd48fa52ee46806bc288a2986b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106998868"
---
# <a name="msidisablermrestart-property"></a><span data-ttu-id="71051-103">MSIDISABLERMRESTART 屬性</span><span class="sxs-lookup"><span data-stu-id="71051-103">MSIDISABLERMRESTART property</span></span>

<span data-ttu-id="71051-104">**MSIDISABLERMRESTART** 屬性會決定目前使用受更新影響之檔案的應用程式或服務如何關閉並重新啟動，以啟用更新的安裝。</span><span class="sxs-lookup"><span data-stu-id="71051-104">The **MSIDISABLERMRESTART** property determines how applications or services that are currently using files affected by an update should be shut down and restarted to enable the installation of the update.</span></span>

## <a name="value"></a><span data-ttu-id="71051-105">值</span><span class="sxs-lookup"><span data-stu-id="71051-105">Value</span></span>



| <span data-ttu-id="71051-106">值</span><span class="sxs-lookup"><span data-stu-id="71051-106">Value</span></span>                                                                        | <span data-ttu-id="71051-107">意義</span><span class="sxs-lookup"><span data-stu-id="71051-107">Meaning</span></span>                                                                                                                                                                                      |
|------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <span data-ttu-id="71051-108"><dt>0</dt></span><span class="sxs-lookup"><span data-stu-id="71051-108"><dt>0</dt></span></span> </dl> | <span data-ttu-id="71051-109">已關閉以安裝更新的所有系統服務都會重新開機。</span><span class="sxs-lookup"><span data-stu-id="71051-109">All system services that were shut down to install the update are restarted.</span></span> <span data-ttu-id="71051-110">使用 [重新開機管理員](../rstmgr/restart-manager-portal.md) 註冊本身的所有應用程式都會重新開機。</span><span class="sxs-lookup"><span data-stu-id="71051-110">All applications that registered themselves with the [Restart Manager](../rstmgr/restart-manager-portal.md) are restarted.</span></span><br/> |
| <dl> <span data-ttu-id="71051-111"><dt>1</dt></span><span class="sxs-lookup"><span data-stu-id="71051-111"><dt>1</dt></span></span> </dl> | <span data-ttu-id="71051-112">在安裝更新之後，使用 [重新開機管理員](../rstmgr/restart-manager-portal.md) 關閉的進程不會在套用更新之後重新開機。</span><span class="sxs-lookup"><span data-stu-id="71051-112">Processes that were shut down using the [Restart Manager](../rstmgr/restart-manager-portal.md) while installing the update will not be restarted after the update is applied.</span></span><br/>                           |



 

## <a name="remarks"></a><span data-ttu-id="71051-113">備註</span><span class="sxs-lookup"><span data-stu-id="71051-113">Remarks</span></span>

<span data-ttu-id="71051-114">如果 [重新開機管理員](../rstmgr/restart-manager-portal.md)無法使用或停用，則會忽略 **MSIDISABLERMRESTART** 屬性。</span><span class="sxs-lookup"><span data-stu-id="71051-114">The **MSIDISABLERMRESTART** Property is ignored if the [Restart Manager](../rstmgr/restart-manager-portal.md) is unavailable or disabled.</span></span>

## <a name="requirements"></a><span data-ttu-id="71051-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="71051-115">Requirements</span></span>



| <span data-ttu-id="71051-116">需求</span><span class="sxs-lookup"><span data-stu-id="71051-116">Requirement</span></span> | <span data-ttu-id="71051-117">值</span><span class="sxs-lookup"><span data-stu-id="71051-117">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="71051-118">版本</span><span class="sxs-lookup"><span data-stu-id="71051-118">Version</span></span><br/> | <span data-ttu-id="71051-119">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="71051-119">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="71051-120">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="71051-120">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="71051-121">如需 Windows Installer 版本所需的最低 service pack 資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="71051-121">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="71051-122">另請參閱</span><span class="sxs-lookup"><span data-stu-id="71051-122">See also</span></span>

<dl> <dt>

[<span data-ttu-id="71051-123">屬性</span><span class="sxs-lookup"><span data-stu-id="71051-123">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="71051-124">Windows Installer 3.1 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="71051-124">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
