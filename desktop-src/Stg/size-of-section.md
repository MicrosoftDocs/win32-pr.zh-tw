---
title: 區段的大小
description: 區段大小資料類型表示區段的大小（以位元組為單位）。
ms.assetid: 6438fbce-42b9-4b16-a6b0-80c80246e546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 479edbfbf32c0e75e44ccef1ff7946b65a44f7482fb4078e51fe2abf575fed64
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "117960317"
---
# <a name="size-of-section"></a>區段的大小

區段大小資料類型表示區段的大小（以位元組為單位）。 由於區段大小是前4個位元組，因此可以將區段複製為位元組陣列。 區段大小應一律為四的倍數。

例如，空的區段，也就是其中有零屬性的區段，會有八個 (**DWORD** 位元組計數的位元組計數，以及) 屬性的 **dword** 計數。 區段本身會包含8個位元組： **08 00 00 00 00 00 00 00**。

 

 




