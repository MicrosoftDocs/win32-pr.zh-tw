---
description: 當目前使用者的系統已升級為使用隨選安裝時，安裝程式會將 OLEAdvtSupport 屬性設定為 true。
ms.assetid: 274d7658-3d33-4c3a-987c-878cbd5bf821
title: OLEAdvtSupport 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 72c9bd8f5ecaaa2690654211a2dd7ecdc5e9ef2f
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995242"
---
# <a name="oleadvtsupport-property"></a><span data-ttu-id="92dbf-103">OLEAdvtSupport 屬性</span><span class="sxs-lookup"><span data-stu-id="92dbf-103">OLEAdvtSupport property</span></span>

<span data-ttu-id="92dbf-104">當目前使用者的系統已升級為使用隨選安裝時，安裝程式會將 **OLEAdvtSupport** 屬性設定為 true。</span><span class="sxs-lookup"><span data-stu-id="92dbf-104">The installer sets the **OLEAdvtSupport** property to true when the current user's system has been upgraded to work with installation-on-demand through COM.</span></span> <span data-ttu-id="92dbf-105">請注意，若要讓安裝程式註冊 COM 類別並啟用隨選安裝，類別必須列在 [類別](class-table.md) 和 [ProgId](progid-table.md) 資料表中。</span><span class="sxs-lookup"><span data-stu-id="92dbf-105">Note that for the installer to register a COM class and enable installation-on-demand, the class must be listed in the [Class](class-table.md) and [ProgId](progid-table.md) tables.</span></span>

## <a name="requirements"></a><span data-ttu-id="92dbf-106">規格需求</span><span class="sxs-lookup"><span data-stu-id="92dbf-106">Requirements</span></span>



| <span data-ttu-id="92dbf-107">需求</span><span class="sxs-lookup"><span data-stu-id="92dbf-107">Requirement</span></span> | <span data-ttu-id="92dbf-108">值</span><span class="sxs-lookup"><span data-stu-id="92dbf-108">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="92dbf-109">版本</span><span class="sxs-lookup"><span data-stu-id="92dbf-109">Version</span></span><br/> | <span data-ttu-id="92dbf-110">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="92dbf-110">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="92dbf-111">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="92dbf-111">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="92dbf-112">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="92dbf-112">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="92dbf-113">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="92dbf-113">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="92dbf-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="92dbf-114">See also</span></span>

<dl> <dt>

[<span data-ttu-id="92dbf-115">屬性</span><span class="sxs-lookup"><span data-stu-id="92dbf-115">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="92dbf-116">**ShellAdvtSupport 屬性**</span><span class="sxs-lookup"><span data-stu-id="92dbf-116">**ShellAdvtSupport Property**</span></span>](shelladvtsupport.md)
</dt> <dt>

[<span data-ttu-id="92dbf-117">廣告的平臺支援</span><span class="sxs-lookup"><span data-stu-id="92dbf-117">Platform Support of Advertisement</span></span>](platform-support-of-advertisement.md)
</dt> </dl>

 

 




