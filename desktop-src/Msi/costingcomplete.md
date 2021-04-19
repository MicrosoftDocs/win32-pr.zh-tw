---
description: CostingComplete 屬性會指出安裝程式是否已完成磁碟空間的成本。
ms.assetid: 23688f1e-3ae8-4cd9-824c-36077cc7838f
title: CostingComplete 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 817b4d38b71e377bbf9b51588efef33e4fd6e93e
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106995689"
---
# <a name="costingcomplete-property"></a><span data-ttu-id="cde26-103">CostingComplete 屬性</span><span class="sxs-lookup"><span data-stu-id="cde26-103">CostingComplete property</span></span>

<span data-ttu-id="cde26-104">**CostingComplete** 屬性會指出安裝程式是否已完成磁碟空間的成本。</span><span class="sxs-lookup"><span data-stu-id="cde26-104">The **CostingComplete** property indicates whether the installer has completed disk space costing.</span></span> <span data-ttu-id="cde26-105">如果尚未完成成本計算，這個屬性可用來撰寫觸發的對話方塊。</span><span class="sxs-lookup"><span data-stu-id="cde26-105">This property can be used to author a dialog box triggered if costing has not been completed.</span></span> <span data-ttu-id="cde26-106">此屬性會在磁碟空間成本設定期間動態設定，並在完成成本設定時立即設定為1。</span><span class="sxs-lookup"><span data-stu-id="cde26-106">The property is set dynamically during disk space costing and is set to 1 as soon as the costing is complete.</span></span> <span data-ttu-id="cde26-107">[CostFinalize 動作](costfinalize-action.md)會將這個屬性初始化為0。</span><span class="sxs-lookup"><span data-stu-id="cde26-107">This property is initialized to 0 by the [CostFinalize action](costfinalize-action.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="cde26-108">備註</span><span class="sxs-lookup"><span data-stu-id="cde26-108">Remarks</span></span>

<span data-ttu-id="cde26-109">如需如何撰寫「請稍候」的範例。</span><span class="sxs-lookup"><span data-stu-id="cde26-109">For an example of how to author a "Please wait .</span></span> <span data-ttu-id="cde26-110">.</span><span class="sxs-lookup"><span data-stu-id="cde26-110">.</span></span> <span data-ttu-id="cde26-111">.</span><span class="sxs-lookup"><span data-stu-id="cde26-111">.</span></span> <span data-ttu-id="cde26-112">"在磁碟空間成本中快顯的對話方塊中，請參閱 [撰寫條件式「請稍候 ...」一節。訊息方塊](authoring-a-conditional-please-wait-------message-box.md)。</span><span class="sxs-lookup"><span data-stu-id="cde26-112">" dialog box that pops up during disk space costing, see the section [Authoring a Conditional "Please wait . . ." Message Box](authoring-a-conditional-please-wait-------message-box.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="cde26-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="cde26-113">Requirements</span></span>



| <span data-ttu-id="cde26-114">需求</span><span class="sxs-lookup"><span data-stu-id="cde26-114">Requirement</span></span> | <span data-ttu-id="cde26-115">值</span><span class="sxs-lookup"><span data-stu-id="cde26-115">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="cde26-116">版本</span><span class="sxs-lookup"><span data-stu-id="cde26-116">Version</span></span><br/> | <span data-ttu-id="cde26-117">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="cde26-117">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="cde26-118">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="cde26-118">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="cde26-119">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="cde26-119">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="cde26-120">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="cde26-120">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="cde26-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cde26-121">See also</span></span>

<dl> <dt>

[<span data-ttu-id="cde26-122">屬性</span><span class="sxs-lookup"><span data-stu-id="cde26-122">Properties</span></span>](properties.md)
</dt> </dl>

 

 




