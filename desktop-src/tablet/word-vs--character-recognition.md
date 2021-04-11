---
description: 藉由將 [模擬] 屬性設定為 [無]，字元辨識器會以字元為單位來辨識手寫。
ms.assetid: 4dacceab-032e-4b9b-858f-67961fd587b5
title: 單字與字元識別的比較
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f521b8abf1064ef87c5c79c3293e725c44190ce3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112873"
---
# <a name="word-vs-character-recognition"></a>單字與字元識別的比較

藉由將 [ [模擬](/previous-versions/ms835848(v=msdn.10)) ] 屬性設定為 [ **無**]，字元辨識器會以字元為單位來辨識手寫。

[RecoTimeout](/previous-versions/ms835852(v=msdn.10)) ([**RecoTimeout**](/windows/desktop/api/inked/nf-inked-iinkedit-get_recognitiontimeout) in Automation) 屬性會指定最後一個 [筆劃](/previous-versions/ms552692(v=vs.100))和手寫輸入結尾之間的延遲毫秒數。 您可以增加此值，以在寫入整個單字或句子之前辨識文字。 您也可以使用「辨識」方法，立即強制 [辨識](/previous-versions/ms836275(v=msdn.10)) 筆墨。

 

 
