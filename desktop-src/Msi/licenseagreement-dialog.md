---
description: 這個強制回應對話方塊會顯示使用者的授權合約。
ms.assetid: 367fe264-6e08-4b40-b61b-617bb92986b7
title: LicenseAgreement 對話方塊
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8876f315787671ee36de42e5b86167659611a77a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106991734"
---
# <a name="licenseagreement-dialog"></a><span data-ttu-id="a3735-103">LicenseAgreement 對話方塊</span><span class="sxs-lookup"><span data-stu-id="a3735-103">LicenseAgreement Dialog</span></span>

<span data-ttu-id="a3735-104">這個強制回應對話方塊會顯示使用者的授權合約。</span><span class="sxs-lookup"><span data-stu-id="a3735-104">This modal dialog box displays the license agreement to the user.</span></span> <span data-ttu-id="a3735-105">對話方塊通常會使用 [ScrollableText 控制項](scrollabletext-control.md) 和一組選項按鈕（讓使用者接受或拒絕合約）來顯示合約的文字。</span><span class="sxs-lookup"><span data-stu-id="a3735-105">Typically the dialog box displays the text of the agreement using a [ScrollableText control](scrollabletext-control.md) and a pair of option buttons that let the user accept or reject the agreement.</span></span> <span data-ttu-id="a3735-106">基於法律考慮，建議您不要將任何按鈕呈現給使用者，因為預設已選取。</span><span class="sxs-lookup"><span data-stu-id="a3735-106">For legal reasons it is advisable that neither button be presented to the user as already selected by default.</span></span> <span data-ttu-id="a3735-107">這會強制使用者進行有效的選擇。</span><span class="sxs-lookup"><span data-stu-id="a3735-107">This forces the user to make an active choice.</span></span> <span data-ttu-id="a3735-108">作者通常會使用 [RadioButtonGroup 控制項](radiobuttongroup-control.md) 來達成此目的。</span><span class="sxs-lookup"><span data-stu-id="a3735-108">Authors commonly use a [RadioButtonGroup control](radiobuttongroup-control.md) for this purpose.</span></span> <span data-ttu-id="a3735-109">不過請注意，在選取群組中的其中一個按鈕之前，不會將焦點放在對話方塊中，而是移至 RadioButtonGroup 控制項。</span><span class="sxs-lookup"><span data-stu-id="a3735-109">Note however that the focus on a dialog box does not move to a RadioButtonGroup control until one of the buttons in the group has been selected.</span></span>

 

 



