---
description: 如果系統的 IShellLink 介面支援安裝程式描述項解析，則 ShellAdvtSupport 屬性是由安裝程式設定。
ms.assetid: 8c3503c5-2a9c-43ad-8cc5-ea10df39b24d
title: ShellAdvtSupport 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: df0040aef3b53352a9da8a31bf97f14e8df3791e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977391"
---
# <a name="shelladvtsupport-property"></a><span data-ttu-id="23894-103">ShellAdvtSupport 屬性</span><span class="sxs-lookup"><span data-stu-id="23894-103">ShellAdvtSupport property</span></span>

<span data-ttu-id="23894-104">如果系統的 [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka)介面支援安裝程式描述項解析，則 **ShellAdvtSupport** 屬性是由安裝程式設定。</span><span class="sxs-lookup"><span data-stu-id="23894-104">The **ShellAdvtSupport** property is set by the installer if the system's [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) interface supports installer descriptor resolution.</span></span>

## <a name="remarks"></a><span data-ttu-id="23894-105">備註</span><span class="sxs-lookup"><span data-stu-id="23894-105">Remarks</span></span>

<span data-ttu-id="23894-106">如果設定此屬性，則系統的 [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) 介面支援安裝程式描述項解析。</span><span class="sxs-lookup"><span data-stu-id="23894-106">If this property is set, the system's [**IShellLink**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ishelllinka) interface supports installer descriptor resolution.</span></span> <span data-ttu-id="23894-107">Windows 2000 和執行 Internet Explorer 4.01 的系統都支援此功能。</span><span class="sxs-lookup"><span data-stu-id="23894-107">This is supported by Windows 2000 and systems running Internet Explorer 4.01.</span></span> <span data-ttu-id="23894-108">如果未設定此屬性，安裝程式會在安裝期間建立非公告功能的預設行為，不論是在本機或從來源執行。</span><span class="sxs-lookup"><span data-stu-id="23894-108">If this property is not set, the installer has the default behavior of creating non-advertised features during installation, either locally or run from source.</span></span>

## <a name="requirements"></a><span data-ttu-id="23894-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="23894-109">Requirements</span></span>



| <span data-ttu-id="23894-110">需求</span><span class="sxs-lookup"><span data-stu-id="23894-110">Requirement</span></span> | <span data-ttu-id="23894-111">值</span><span class="sxs-lookup"><span data-stu-id="23894-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="23894-112">版本</span><span class="sxs-lookup"><span data-stu-id="23894-112">Version</span></span><br/> | <span data-ttu-id="23894-113">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="23894-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="23894-114">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="23894-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="23894-115">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="23894-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="23894-116">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="23894-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="23894-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="23894-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="23894-118">屬性</span><span class="sxs-lookup"><span data-stu-id="23894-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="23894-119">廣告的平臺支援</span><span class="sxs-lookup"><span data-stu-id="23894-119">Platform Support of Advertisement</span></span>](platform-support-of-advertisement.md)
</dt> </dl>

 

 
