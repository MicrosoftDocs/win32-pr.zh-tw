---
description: ACTION 屬性可以設定為下列值。
ms.assetid: f2c436b6-ebd9-4ac4-8609-f54129023ca7
title: ACTION 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 901061f953ffaed030ff6d3a94f440eada25fc59
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984123"
---
# <a name="action-property"></a><span data-ttu-id="ca4ed-103">ACTION 屬性</span><span class="sxs-lookup"><span data-stu-id="ca4ed-103">ACTION property</span></span>

<span data-ttu-id="ca4ed-104">**ACTION** 屬性可以設定為下列值。</span><span class="sxs-lookup"><span data-stu-id="ca4ed-104">The **ACTION** property can be set to the following values.</span></span>

## <a name="value"></a><span data-ttu-id="ca4ed-105">值</span><span class="sxs-lookup"><span data-stu-id="ca4ed-105">Value</span></span>



| <span data-ttu-id="ca4ed-106">值</span><span class="sxs-lookup"><span data-stu-id="ca4ed-106">Value</span></span>                                                                                                                                            | <span data-ttu-id="ca4ed-107">意義</span><span class="sxs-lookup"><span data-stu-id="ca4ed-107">Meaning</span></span>                                             |
|--------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <span id="INSTALL"></span><span id="install"></span><dl> <span data-ttu-id="ca4ed-108"><dt>**安裝**</dt></span><span class="sxs-lookup"><span data-stu-id="ca4ed-108"><dt>**INSTALL**</dt></span></span> </dl>       | [<span data-ttu-id="ca4ed-109">安裝動作</span><span class="sxs-lookup"><span data-stu-id="ca4ed-109">INSTALL Action</span></span>](install-action.md)<br/>     |
| <span id="ADVERTISE"></span><span id="advertise"></span><dl> <span data-ttu-id="ca4ed-110"><dt>**做廣告**</dt></span><span class="sxs-lookup"><span data-stu-id="ca4ed-110"><dt>**ADVERTISE**</dt></span></span> </dl> | [<span data-ttu-id="ca4ed-111">通告動作</span><span class="sxs-lookup"><span data-stu-id="ca4ed-111">ADVERTISE Action</span></span>](advertise-action.md)<br/> |
| <span id="ADMIN"></span><span id="admin"></span><dl> <span data-ttu-id="ca4ed-112"><dt>**管理**</dt></span><span class="sxs-lookup"><span data-stu-id="ca4ed-112"><dt>**ADMIN**</dt></span></span> </dl>             | [<span data-ttu-id="ca4ed-113">管理動作</span><span class="sxs-lookup"><span data-stu-id="ca4ed-113">ADMIN Action</span></span>](admin-action.md)<br/>         |



 

<span data-ttu-id="ca4ed-114">如果將 Null 動作名稱提供給 [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona)或 [**dataadapter.doaction 方法**](session-doaction.md)，則 [**動作**] 屬性會決定要執行的動作。</span><span class="sxs-lookup"><span data-stu-id="ca4ed-114">The **ACTION** property determines which action to perform if a Null action name is supplied to [**MsiDoAction**](/windows/desktop/api/Msiquery/nf-msiquery-msidoactiona) or the [**DoAction Method**](session-doaction.md).</span></span> <span data-ttu-id="ca4ed-115">如果未針對 **ACTION** 屬性定義任何值，則安裝程式會呼叫 [安裝動作](install-action.md)。</span><span class="sxs-lookup"><span data-stu-id="ca4ed-115">If no value is defined for the **ACTION** property, the installer calls the [INSTALL Action](install-action.md).</span></span>

## <a name="requirements"></a><span data-ttu-id="ca4ed-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="ca4ed-116">Requirements</span></span>



| <span data-ttu-id="ca4ed-117">需求</span><span class="sxs-lookup"><span data-stu-id="ca4ed-117">Requirement</span></span> | <span data-ttu-id="ca4ed-118">值</span><span class="sxs-lookup"><span data-stu-id="ca4ed-118">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="ca4ed-119">版本</span><span class="sxs-lookup"><span data-stu-id="ca4ed-119">Version</span></span><br/> | <span data-ttu-id="ca4ed-120">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="ca4ed-120">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="ca4ed-121">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="ca4ed-121">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="ca4ed-122">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="ca4ed-122">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="ca4ed-123">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="ca4ed-123">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="ca4ed-124">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ca4ed-124">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ca4ed-125">屬性</span><span class="sxs-lookup"><span data-stu-id="ca4ed-125">Properties</span></span>](properties.md)
</dt> </dl>

 

 




