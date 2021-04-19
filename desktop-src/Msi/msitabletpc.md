---
description: 如果目前的作業系統是 Windows XP Tablet PC Edition，安裝程式會將 MsiTabletPC 屬性設定為非零值。
ms.assetid: b178a98e-b6f8-4ff8-b554-e47c3b39f892
title: MsiTabletPC 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 0bf2878dbaa895e0924a50900d331db0b879edc1
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984798"
---
# <a name="msitabletpc-property"></a><span data-ttu-id="d1a70-103">MsiTabletPC 屬性</span><span class="sxs-lookup"><span data-stu-id="d1a70-103">MsiTabletPC property</span></span>

<span data-ttu-id="d1a70-104">如果目前的作業系統是 Windows XP Tablet PC Edition，安裝程式會將 **MsiTabletPC** 屬性設定為非零值。</span><span class="sxs-lookup"><span data-stu-id="d1a70-104">The installer sets the **MsiTabletPC** property to a nonzero value if the current operating system is Windows XP Tablet PC Edition.</span></span> <span data-ttu-id="d1a70-105">安裝程式會將 [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) 函式與 **SM \_ 平板** 使用者搭配使用，而屬性則會接收此函式所傳回的非零值。</span><span class="sxs-lookup"><span data-stu-id="d1a70-105">The installer uses the [**GetSystemMetrics**](/windows/win32/api/winuser/nf-winuser-getsystemmetrics) function with **SM\_TABLETPC**, and the property receives the nonzero value returned by this function.</span></span> <span data-ttu-id="d1a70-106">如果目前的系統不是 Windows XP Tablet PC Edition， **GetSystemMetrics** 函式會傳回零，而且安裝程式不會設定這個屬性。</span><span class="sxs-lookup"><span data-stu-id="d1a70-106">If the current system is not Windows XP Tablet PC Edition, the **GetSystemMetrics** function returns zero and the installer does not set this property.</span></span>

## <a name="requirements"></a><span data-ttu-id="d1a70-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="d1a70-107">Requirements</span></span>



| <span data-ttu-id="d1a70-108">需求</span><span class="sxs-lookup"><span data-stu-id="d1a70-108">Requirement</span></span> | <span data-ttu-id="d1a70-109">值</span><span class="sxs-lookup"><span data-stu-id="d1a70-109">Value</span></span> |
|--------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="d1a70-110">版本</span><span class="sxs-lookup"><span data-stu-id="d1a70-110">Version</span></span><br/> | <span data-ttu-id="d1a70-111">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="d1a70-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="d1a70-112">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="d1a70-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="d1a70-113">Windows Server 2003 或 Windows XP 上的 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="d1a70-113">Windows Installer 4.5 on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="d1a70-114">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="d1a70-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="d1a70-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d1a70-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d1a70-116">屬性</span><span class="sxs-lookup"><span data-stu-id="d1a70-116">Properties</span></span>](properties.md)
</dt> <dt>

[<span data-ttu-id="d1a70-117">Windows Installer 3.1 及更早版本不支援</span><span class="sxs-lookup"><span data-stu-id="d1a70-117">Not Supported in Windows Installer 3.1 and earlier versions</span></span>](not-supported-in-windows-installer-version-3-1.md)
</dt> </dl>

 

 
