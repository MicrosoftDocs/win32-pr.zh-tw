---
description: 當系統的變更開始進行此安裝時，安裝程式會設定 UpdateStarted 屬性，包括繼續暫止的安裝。UI 條件陳述式使用此值來選取對話方塊。
ms.assetid: aebc4a20-22b9-4a81-abed-1fed61b880da
title: UpdateStarted 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 99561d17bf6fcb251f1acd7ac0d30ed5c1682997
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106990792"
---
# <a name="updatestarted-property"></a><span data-ttu-id="13c80-103">UpdateStarted 屬性</span><span class="sxs-lookup"><span data-stu-id="13c80-103">UpdateStarted property</span></span>

<span data-ttu-id="13c80-104">當系統的變更開始進行此安裝時，安裝程式會設定 **UpdateStarted** 屬性，包括繼續暫止的安裝。</span><span class="sxs-lookup"><span data-stu-id="13c80-104">The installer sets the **UpdateStarted** property when changes to the system have begun for this installation, including resuming a suspended installation.</span></span>

<span data-ttu-id="13c80-105">UI 條件陳述式使用此值來選取對話方塊。</span><span class="sxs-lookup"><span data-stu-id="13c80-105">UI condition statements use this value to select a dialog box.</span></span> <span data-ttu-id="13c80-106">如果設定此屬性，則會在發生錯誤時詢問使用者，並取消是否要還原或稍後再繼續。</span><span class="sxs-lookup"><span data-stu-id="13c80-106">If this property is set, the user is asked after an error and cancellation whether to restore or to continue later.</span></span>

## <a name="requirements"></a><span data-ttu-id="13c80-107">規格需求</span><span class="sxs-lookup"><span data-stu-id="13c80-107">Requirements</span></span>



| <span data-ttu-id="13c80-108">需求</span><span class="sxs-lookup"><span data-stu-id="13c80-108">Requirement</span></span> | <span data-ttu-id="13c80-109">值</span><span class="sxs-lookup"><span data-stu-id="13c80-109">Value</span></span> |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="13c80-110">版本</span><span class="sxs-lookup"><span data-stu-id="13c80-110">Version</span></span><br/> | <span data-ttu-id="13c80-111">Windows Server 2012、Windows 8、Windows Server 2008 R2 或 Windows 7 上的 Windows Installer 5.0。</span><span class="sxs-lookup"><span data-stu-id="13c80-111">Windows Installer 5.0 on Windows Server 2012, Windows 8, Windows Server 2008 R2 or Windows 7.</span></span> <span data-ttu-id="13c80-112">Windows Server 2008 或 Windows Vista 上的 Windows Installer 4.0 或 Windows Installer 4.5。</span><span class="sxs-lookup"><span data-stu-id="13c80-112">Windows Installer 4.0 or Windows Installer 4.5 on Windows Server 2008 or Windows Vista.</span></span> <span data-ttu-id="13c80-113">Windows Server 2003 或 Windows XP 上的 Windows Installer。</span><span class="sxs-lookup"><span data-stu-id="13c80-113">Windows Installer on Windows Server 2003 or Windows XP.</span></span> <span data-ttu-id="13c80-114">如需 Windows Installer 版本所需的最小 Windows service pack 相關資訊，請參閱 [Windows Installer Run-Time 需求](windows-installer-portal.md) 。</span><span class="sxs-lookup"><span data-stu-id="13c80-114">See the [Windows Installer Run-Time Requirements](windows-installer-portal.md) for information about the minimum Windows service pack that is required by a Windows Installer version.</span></span><br/> |



## <a name="see-also"></a><span data-ttu-id="13c80-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="13c80-115">See also</span></span>

<dl> <dt>

[<span data-ttu-id="13c80-116">屬性</span><span class="sxs-lookup"><span data-stu-id="13c80-116">Properties</span></span>](properties.md)
</dt> </dl>

 

 




