---
description: 在 Windows 2000 和更新版本的作業系統上，如果安裝程式是在 Windows Server 2003 的 web 版本上執行，安裝程式會將 MsiNTSuiteWebServer 屬性設定為1。
ms.assetid: de462ba2-4654-4f47-9dd7-3bc9c6f0af0e
title: MsiNTSuiteWebServer 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 082e3ae7f107bf3499f5a48473d53ebb530138a6
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995277"
---
# <a name="msintsuitewebserver-property"></a><span data-ttu-id="057bd-103">MsiNTSuiteWebServer 屬性</span><span class="sxs-lookup"><span data-stu-id="057bd-103">MsiNTSuiteWebServer property</span></span>

<span data-ttu-id="057bd-104">在 Windows 2000 和更新版本的作業系統上，如果安裝程式是在 Windows Server 2003 的 web 版本上執行，安裝程式會將 **MsiNTSuiteWebServer** 屬性設定為1。</span><span class="sxs-lookup"><span data-stu-id="057bd-104">On Windows 2000 and later operating systems, the installer sets the **MsiNTSuiteWebServer** property to 1 if the installer is running on a web edition of the Windows Server 2003.</span></span> <span data-ttu-id="057bd-105">只有當 VER \_ SUITE 分頁 \_ 旗標設定于 [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) 結構中時，安裝程式才會將這個屬性設定為1。</span><span class="sxs-lookup"><span data-stu-id="057bd-105">The installer sets this property to 1 only if the VER\_SUITE\_BLADE flag is set in the [**OSVERSIONINFOEX**](/windows/win32/api/winnt/ns-winnt-osversioninfoexa) structure.</span></span> <span data-ttu-id="057bd-106">否則，安裝程式不會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="057bd-106">Otherwise the installer does not set this property.</span></span>

## <a name="remarks"></a><span data-ttu-id="057bd-107">備註</span><span class="sxs-lookup"><span data-stu-id="057bd-107">Remarks</span></span>

<span data-ttu-id="057bd-108">這個屬性僅適用于 Windows Server 2003 版的安裝程式。</span><span class="sxs-lookup"><span data-stu-id="057bd-108">This property is available only with the Windows Server 2003 release of the installer.</span></span>

## <a name="requirements"></a><span data-ttu-id="057bd-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="057bd-109">Requirements</span></span>



| <span data-ttu-id="057bd-110">需求</span><span class="sxs-lookup"><span data-stu-id="057bd-110">Requirement</span></span> | <span data-ttu-id="057bd-111">值</span><span class="sxs-lookup"><span data-stu-id="057bd-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="057bd-112">版本</span><span class="sxs-lookup"><span data-stu-id="057bd-112">Version</span></span><br/> | <span data-ttu-id="057bd-113">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="057bd-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="057bd-114">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="057bd-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="057bd-115">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="057bd-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="057bd-116">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="057bd-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="057bd-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="057bd-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="057bd-118">屬性</span><span class="sxs-lookup"><span data-stu-id="057bd-118">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="057bd-119">Windows Installer 2.0 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="057bd-119">Not Supported in Windows Installer 2.0 and earlier</span></span>](not-supported-in-windows-installer-version-2-0.md)
</dt> </dl>

 

 
