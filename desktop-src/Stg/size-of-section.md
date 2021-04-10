---
title: 區段的大小
description: 區段大小資料類型表示區段的大小（以位元組為單位）。
ms.assetid: 6438fbce-42b9-4b16-a6b0-80c80246e546
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d71b19df1c2f9a65f6952855a4ab325565c759af
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104184074"
---
# <a name="size-of-section"></a>區段的大小

區段大小資料類型表示區段的大小（以位元組為單位）。 由於區段大小是前4個位元組，因此可以將區段複製為位元組陣列。 區段大小應一律為四的倍數。

例如，空的區段，也就是其中有零屬性的區段，會有八個 (**DWORD** 位元組計數的位元組計數，以及) 屬性的 **dword** 計數。 區段本身會包含8個位元組： **08 00 00 00 00 00 00 00**。

 

 




