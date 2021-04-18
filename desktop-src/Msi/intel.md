---
description: Intel 屬性是在 Intel 處理器上執行時，由 Windows Installer 設定為數值處理器等級。
ms.assetid: c1190df2-0440-4dd1-bce5-61d899f71437
title: Intel 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ab73f35b371d3bf8323fe2a3f3de1608666bc181
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106976137"
---
# <a name="intel-property"></a><span data-ttu-id="8416f-103">Intel 屬性</span><span class="sxs-lookup"><span data-stu-id="8416f-103">Intel property</span></span>

<span data-ttu-id="8416f-104">**Intel** 屬性是在 intel 處理器上執行時，由 Windows Installer 設定為數值處理器等級。</span><span class="sxs-lookup"><span data-stu-id="8416f-104">The **Intel** property is set by the Windows Installer to the numeric processor level when running on an Intel processor.</span></span> <span data-ttu-id="8416f-105">這些值與 [**系統 \_ 資訊**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info)結構的 [ *wProcessorLevel* ] 欄位相同。</span><span class="sxs-lookup"><span data-stu-id="8416f-105">The values are the same as the *wProcessorLevel* field of the [**SYSTEM\_INFO**](/windows/win32/api/sysinfoapi/ns-sysinfoapi-system_info) structure.</span></span> <span data-ttu-id="8416f-106">在 x64 處理器上執行時，Windows Installer 會設定 **Intel** 屬性，以反映由作業系統所報告的 x64 電腦所模擬的 x86 處理器。</span><span class="sxs-lookup"><span data-stu-id="8416f-106">When running on a x64 processor, the Windows Installer sets the **Intel** property to reflect the x86 processor emulated by the x64 computer as reported by the operating system.</span></span>

## <a name="requirements"></a><span data-ttu-id="8416f-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="8416f-107">Requirements</span></span>



| <span data-ttu-id="8416f-108">需求</span><span class="sxs-lookup"><span data-stu-id="8416f-108">Requirement</span></span> | <span data-ttu-id="8416f-109">值</span><span class="sxs-lookup"><span data-stu-id="8416f-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="8416f-110">版本</span><span class="sxs-lookup"><span data-stu-id="8416f-110">Version</span></span><br/> | <span data-ttu-id="8416f-111">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="8416f-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="8416f-112">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="8416f-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="8416f-113">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="8416f-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="8416f-114">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="8416f-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="8416f-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8416f-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="8416f-116">屬性</span><span class="sxs-lookup"><span data-stu-id="8416f-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 
