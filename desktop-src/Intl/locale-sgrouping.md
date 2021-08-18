---
description: 地區設定 \_ SGROUPING
ms.assetid: 3f07ecae-38f4-477b-8b23-a9cd87613c24
title: LOCALE_SGROUPING
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 476fa80a22e55791ca7b5636237540c457480ff0bd9c808b99ef3c6e46a17dce
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106208"
---
# <a name="locale_sgrouping"></a>地區設定 \_ SGROUPING

小數點左邊每個位數群組的大小。 此字串允許的最大字元數為十個字元，包括結束的 null 字元。 每個群組都需要明確的大小，且大小會以分號分隔。 如果最後一個值為0，則會重複上述值。 例如，若要將數以千計分組，請指定 3; 0。 印度地區設定群組的前一千個群組，然後分組為數百。 例如，12、34、56789是以3表示，2; 0。

其他範例：



| 規格 | 產生的字串   |
|---------------|--------------------|
| 3; 0           | 3000000000000  |
| 3; 2; 0         | 30、00、00、00、00000 |
| 3             | 3000000000000     |
| 3; 2           | 30000000、00000    |



 

 

 



