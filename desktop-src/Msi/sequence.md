---
description: SEQUENCE 屬性指定的資料表具有與 InstallExecuteSequence 資料表相同的架構，也就是 Action、Condition 和 Sequence 資料行。 順序動作會使用這個屬性。
ms.assetid: bd2dd544-eb1d-4b6c-862b-952c8edc7593
title: SEQUENCE 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 55ba3e95e5ca7008c5654ebeec5e307002eb8582
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106999122"
---
# <a name="sequence-property"></a><span data-ttu-id="bd2f8-104">SEQUENCE 屬性</span><span class="sxs-lookup"><span data-stu-id="bd2f8-104">SEQUENCE property</span></span>

<span data-ttu-id="bd2f8-105">**SEQUENCE** 屬性指定的資料表具有與 InstallExecuteSequence 資料表相同的架構，也就是 Action、Condition 和 SEQUENCE 資料行。</span><span class="sxs-lookup"><span data-stu-id="bd2f8-105">The **SEQUENCE** property specifies a table having the same schema as the InstallExecuteSequence table, that is Action, Condition, and Sequence columns.</span></span> <span data-ttu-id="bd2f8-106">[順序動作](sequence-action.md)會使用這個屬性。</span><span class="sxs-lookup"><span data-stu-id="bd2f8-106">This property is used by the [SEQUENCE action](sequence-action.md).</span></span>

## <a name="remarks"></a><span data-ttu-id="bd2f8-107">備註</span><span class="sxs-lookup"><span data-stu-id="bd2f8-107">Remarks</span></span>

<span data-ttu-id="bd2f8-108">順序動作會依資料表的 [順序] 資料行所指定的順序，執行資料表中的動作。</span><span class="sxs-lookup"><span data-stu-id="bd2f8-108">The SEQUENCE action runs the actions in the table in the order specified by the Sequence column of the table.</span></span>

## <a name="requirements"></a><span data-ttu-id="bd2f8-109">規格需求</span><span class="sxs-lookup"><span data-stu-id="bd2f8-109">Requirements</span></span>



| <span data-ttu-id="bd2f8-110">需求</span><span class="sxs-lookup"><span data-stu-id="bd2f8-110">Requirement</span></span> | <span data-ttu-id="bd2f8-111">值</span><span class="sxs-lookup"><span data-stu-id="bd2f8-111">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="bd2f8-112">版本</span><span class="sxs-lookup"><span data-stu-id="bd2f8-112">Version</span></span><br/> | <span data-ttu-id="bd2f8-113">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="bd2f8-113">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="bd2f8-114">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="bd2f8-114">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="bd2f8-115">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="bd2f8-115">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="bd2f8-116">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="bd2f8-116">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="bd2f8-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="bd2f8-117">See also</span></span>

<dl> <dt>

[<span data-ttu-id="bd2f8-118">屬性</span><span class="sxs-lookup"><span data-stu-id="bd2f8-118">Properties</span></span>](properties.md)
</dt> </dl>

 

 




