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
# <a name="licenseagreement-dialog"></a>LicenseAgreement 對話方塊

這個強制回應對話方塊會顯示使用者的授權合約。 對話方塊通常會使用 [ScrollableText 控制項](scrollabletext-control.md) 和一組選項按鈕（讓使用者接受或拒絕合約）來顯示合約的文字。 基於法律考慮，建議您不要將任何按鈕呈現給使用者，因為預設已選取。 這會強制使用者進行有效的選擇。 作者通常會使用 [RadioButtonGroup 控制項](radiobuttongroup-control.md) 來達成此目的。 不過請注意，在選取群組中的其中一個按鈕之前，不會將焦點放在對話方塊中，而是移至 RadioButtonGroup 控制項。

 

 



