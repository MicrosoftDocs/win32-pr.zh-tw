---
description: 如果安裝程式寫入正在使用中的檔案，則會設定 ReplacedInUseFiles 屬性。
ms.assetid: cef7d36e-c721-4d47-beaa-53e6749334b6
title: ReplacedInUseFiles 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 43d6826f1db2ec1844234cf32f1137e43c89528c
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990715"
---
# <a name="replacedinusefiles-property"></a><span data-ttu-id="94feb-103">ReplacedInUseFiles 屬性</span><span class="sxs-lookup"><span data-stu-id="94feb-103">ReplacedInUseFiles property</span></span>

<span data-ttu-id="94feb-104">如果安裝程式寫入正在使用中的檔案，則會設定 **ReplacedInUseFiles** 屬性。</span><span class="sxs-lookup"><span data-stu-id="94feb-104">The **ReplacedInUseFiles** property is set if the installer writes over a file that is being held in use.</span></span> <span data-ttu-id="94feb-105">自訂動作會使用這個屬性來偵測需要重新開機才能完成安裝。</span><span class="sxs-lookup"><span data-stu-id="94feb-105">This property is used by custom actions to detect that a reboot is required to complete the installation.</span></span>

<span data-ttu-id="94feb-106">在 [InstallExecute](installexecute-action.md) 和 [InstallFinalize](installfinalize-action.md) 動作期間設定。</span><span class="sxs-lookup"><span data-stu-id="94feb-106">Set during the [InstallExecute](installexecute-action.md) and [InstallFinalize](installfinalize-action.md) actions.</span></span>

## <a name="requirements"></a><span data-ttu-id="94feb-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="94feb-107">Requirements</span></span>



| <span data-ttu-id="94feb-108">需求</span><span class="sxs-lookup"><span data-stu-id="94feb-108">Requirement</span></span> | <span data-ttu-id="94feb-109">值</span><span class="sxs-lookup"><span data-stu-id="94feb-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="94feb-110">版本</span><span class="sxs-lookup"><span data-stu-id="94feb-110">Version</span></span><br/> | <span data-ttu-id="94feb-111">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="94feb-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="94feb-112">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="94feb-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="94feb-113">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="94feb-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="94feb-114">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="94feb-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="94feb-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="94feb-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="94feb-116">屬性</span><span class="sxs-lookup"><span data-stu-id="94feb-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 




