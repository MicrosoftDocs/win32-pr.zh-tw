---
description: 當安裝使用位於媒體上的來源（如 CD-ROM）時，安裝程式會將 MediaSourceDir 屬性設定為1。
ms.assetid: 79c7c5eb-b212-4dbf-943a-00ebd6037ce1
title: MediaSourceDir 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4ae8ec79d11f8aaf5027ae0e68003532449c52ba
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999210"
---
# <a name="mediasourcedir-property"></a><span data-ttu-id="7abfa-103">MediaSourceDir 屬性</span><span class="sxs-lookup"><span data-stu-id="7abfa-103">MediaSourceDir property</span></span>

<span data-ttu-id="7abfa-104">當安裝使用位於媒體上的來源（如 CD-ROM）時，安裝程式會將 **MediaSourceDir** 屬性設定為1。</span><span class="sxs-lookup"><span data-stu-id="7abfa-104">The installer sets the **MediaSourceDir** property to 1 when the installation uses a source located on media, such as a CD-ROM.</span></span> <span data-ttu-id="7abfa-105">當安裝使用位於網路位置的來源時，不會設定此屬性。</span><span class="sxs-lookup"><span data-stu-id="7abfa-105">This property is not set when the installation uses a source located at a network location.</span></span> <span data-ttu-id="7abfa-106">例如， [SelectionTree 控制項](selectiontree-control.md) 會使用 **MediaSourceDir** 來判斷是否正在從來源執行安裝，或從網路位置執行安裝。</span><span class="sxs-lookup"><span data-stu-id="7abfa-106">For example, the [SelectionTree Control](selectiontree-control.md) uses **MediaSourceDir** to determine whether the installation is being run from source or run from a network location.</span></span>

## <a name="requirements"></a><span data-ttu-id="7abfa-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="7abfa-107">Requirements</span></span>



| <span data-ttu-id="7abfa-108">需求</span><span class="sxs-lookup"><span data-stu-id="7abfa-108">Requirement</span></span> | <span data-ttu-id="7abfa-109">值</span><span class="sxs-lookup"><span data-stu-id="7abfa-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="7abfa-110">版本</span><span class="sxs-lookup"><span data-stu-id="7abfa-110">Version</span></span><br/> | <span data-ttu-id="7abfa-111">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="7abfa-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="7abfa-112">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="7abfa-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="7abfa-113">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="7abfa-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="7abfa-114">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="7abfa-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="7abfa-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7abfa-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="7abfa-116">屬性</span><span class="sxs-lookup"><span data-stu-id="7abfa-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 




