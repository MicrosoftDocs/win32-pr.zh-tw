---
description: 這個屬性會測量進度指標列的填滿程度。
ms.assetid: d2b64cdf-e0b4-4c92-9cce-7f50753b875f
title: 進度控制項屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ff8854106ebacc8af2bdc0acfb58c5afc5d700df
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106979398"
---
# <a name="progress-control-attribute"></a>進度控制項屬性

這個屬性會測量進度指標列的填滿程度。 記錄包含兩個整數和一個字串。 第一個數位是進度，第二個數字是 (進度) 最大可能數目的範圍。 設定時，可以輸入整數位段或字串（包含整數）的整數。 如果遺漏第二個數字，則會假設為預設的 (1024) 。 如果進度大於範圍，則會將它變更為範圍。 第三個欄位是字串，即顯示其進度的動作名稱。

如需相關資訊，請參閱 [撰寫 ProgressBar 控制項](authoring-a-progressbar-control.md)，以及 [將自訂動作新增至 ProgressBar](adding-custom-actions-to-the-progressbar.md)。

## <a name="valid-controls"></a>有效的控制項

[進度列](progressbar-control.md)

## <a name="associated-bit-flags"></a>相關聯的位旗標

這個屬性不會使用位旗標。

## <a name="remarks"></a>備註

請參閱 [控制項屬性](control-attributes.md) 和您需要在 [控制項](controls.md)下建立的控制項。

 

 



