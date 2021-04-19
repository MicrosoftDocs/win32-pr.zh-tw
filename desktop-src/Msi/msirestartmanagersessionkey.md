---
description: 安裝程式會將 MsiRestartManagerSessionKey 屬性的值設定為重新啟動管理員會話的工作階段金鑰。
ms.assetid: efbf11f2-38ab-4509-aa01-23fa8cfdaa60
title: MsiRestartManagerSessionKey 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 489095e0af617c7ae403811f0eab800c5502e3bd
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995996"
---
# <a name="msirestartmanagersessionkey-property"></a><span data-ttu-id="75da0-103">MsiRestartManagerSessionKey 屬性</span><span class="sxs-lookup"><span data-stu-id="75da0-103">MsiRestartManagerSessionKey property</span></span>

<span data-ttu-id="75da0-104">安裝程式會將 **MsiRestartManagerSessionKey** 屬性的值設定為 [重新開機管理員](../rstmgr/restart-manager-portal.md) 會話的工作階段金鑰。</span><span class="sxs-lookup"><span data-stu-id="75da0-104">The installer sets the value of the **MsiRestartManagerSessionKey** property to the session key for the [Restart Manager](../rstmgr/restart-manager-portal.md) session.</span></span> <span data-ttu-id="75da0-105">自訂動作可以使用工作階段金鑰加入 [重新開機管理員](../rstmgr/restart-manager-portal.md) 會話。</span><span class="sxs-lookup"><span data-stu-id="75da0-105">Custom actions can use the session key to join the [Restart Manager](../rstmgr/restart-manager-portal.md) session.</span></span>

## <a name="remarks"></a><span data-ttu-id="75da0-106">備註</span><span class="sxs-lookup"><span data-stu-id="75da0-106">Remarks</span></span>

<span data-ttu-id="75da0-107">安裝程式會在初始化時設定 **MsiRestartManagerSessionKey** 屬性的值，然後在 [InstallValidate](installvalidate-action.md) 動作期間清除此值。</span><span class="sxs-lookup"><span data-stu-id="75da0-107">The installer sets the value of the **MsiRestartManagerSessionKey** property at initialization, and then clears the value during the [InstallValidate](installvalidate-action.md) action.</span></span> <span data-ttu-id="75da0-108">需要 **MsiRestartManagerSessionKey** 屬性值的自訂動作必須位於動作順序中的 InstallValidate 動作之前。</span><span class="sxs-lookup"><span data-stu-id="75da0-108">Custom actions that need the value of the **MsiRestartManagerSessionKey** property must be come before the InstallValidate action in the action sequence.</span></span>

## <a name="requirements"></a><span data-ttu-id="75da0-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="75da0-109">Requirements</span></span>



| <span data-ttu-id="75da0-110">需求</span><span class="sxs-lookup"><span data-stu-id="75da0-110">Requirement</span></span> | <span data-ttu-id="75da0-111">值</span><span class="sxs-lookup"><span data-stu-id="75da0-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="75da0-112">版本</span><span class="sxs-lookup"><span data-stu-id="75da0-112">Version</span></span><br/> | <span data-ttu-id="75da0-113">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="75da0-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="75da0-114">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="75da0-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="75da0-115">如需 Windows Installer 版本所需的最低 service pack 資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="75da0-115">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum service pack required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="75da0-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="75da0-116">See also</span></span>

<dl> <dt>

[<span data-ttu-id="75da0-117">屬性</span><span class="sxs-lookup"><span data-stu-id="75da0-117">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="75da0-118">Windows Installer 3.1 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="75da0-118">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
