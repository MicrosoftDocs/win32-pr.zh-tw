---
description: 具有特殊許可權的屬性會指出是否在較高許可權的內容中執行安裝。
ms.assetid: 483ab73a-3ff7-4111-a6b5-eac990d85bd7
title: 具有特殊許可權的屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: f5d28a7079e7ab12b9832447172f1b3b2c8650a8
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106991224"
---
# <a name="privileged-property"></a><span data-ttu-id="4cfc5-103">具有特殊許可權的屬性</span><span class="sxs-lookup"><span data-stu-id="4cfc5-103">Privileged property</span></span>

<span data-ttu-id="4cfc5-104">具有 **特殊許可權的屬性會** 指出是否在較高許可權的內容中執行安裝。</span><span class="sxs-lookup"><span data-stu-id="4cfc5-104">The **Privileged** property indicates whether the installation is performed in the context of elevated privileges.</span></span> <span data-ttu-id="4cfc5-105">如果使用者具有系統管理員許可權、系統管理員已指派應用程式，或使用者和電腦原則 AlwaysInstallElevated 都設定為 true，則安裝程式會設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="4cfc5-105">The installer sets this property if the user has administrator privileges, if the application has been assigned by a system administrator, or if both the user and machine policies AlwaysInstallElevated are set to true.</span></span>

## <a name="default-value"></a><span data-ttu-id="4cfc5-106">預設值</span><span class="sxs-lookup"><span data-stu-id="4cfc5-106">Default Value</span></span>

<span data-ttu-id="4cfc5-107">如果不允許使用者以較高的許可權安裝，安裝程式就不會設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="4cfc5-107">The installer does not set this property if the user is not allowed to install with elevated privileges.</span></span>

## <a name="remarks"></a><span data-ttu-id="4cfc5-108">備註</span><span class="sxs-lookup"><span data-stu-id="4cfc5-108">Remarks</span></span>

<span data-ttu-id="4cfc5-109">安裝程式套件的開發人員可以使用 [特殊 **許可權** ] 屬性，根據系統原則、使用者是系統管理員或系統管理員指派來進行安裝。</span><span class="sxs-lookup"><span data-stu-id="4cfc5-109">Developers of installer packages can use the **Privileged** property to make the installation conditional upon system policy, the user being an administrator, or assignment by an administrator.</span></span>

<span data-ttu-id="4cfc5-110">在 Windows Vista 上執行時，特殊 **許可權** 和 [**AdminUser**](adminuser.md) 相同。</span><span class="sxs-lookup"><span data-stu-id="4cfc5-110">When running on Windows Vista, the **Privileged** and [**AdminUser**](adminuser.md) are the same.</span></span>

## <a name="requirements"></a><span data-ttu-id="4cfc5-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="4cfc5-111">Requirements</span></span>



| <span data-ttu-id="4cfc5-112">需求</span><span class="sxs-lookup"><span data-stu-id="4cfc5-112">Requirement</span></span> | <span data-ttu-id="4cfc5-113">值</span><span class="sxs-lookup"><span data-stu-id="4cfc5-113">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="4cfc5-114">版本</span><span class="sxs-lookup"><span data-stu-id="4cfc5-114">Version</span></span><br/> | <span data-ttu-id="4cfc5-115">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="4cfc5-115">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="4cfc5-116">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="4cfc5-116">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="4cfc5-117">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="4cfc5-117">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="4cfc5-118">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="4cfc5-118">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="4cfc5-119">另請參閱</span><span class="sxs-lookup"><span data-stu-id="4cfc5-119">See also</span></span>

<dl> <dt>

[<span data-ttu-id="4cfc5-120">屬性</span><span class="sxs-lookup"><span data-stu-id="4cfc5-120">Properties</span></span>](properties.md)
</dt> </dl>

 

 




