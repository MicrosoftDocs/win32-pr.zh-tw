---
description: 當您的函式中有一個以上的本機變數頁面時，由編譯器呼叫。
ms.assetid: 154dd992-88b5-44a4-9594-5d13afb71c28
title: _chkstk 常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b129b73801c6c18b63b10ac61898ee13a9c5d4f1f0422678bbfe5af82d5b44f8
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119538830"
---
# <a name="_chkstk-routine"></a>\_chkstk 常式

當您的函式中有一個以上的本機變數頁面時，由編譯器呼叫。

## <a name="remarks"></a>備註

\_chkstk 常式是 C 編譯器的 helper 常式。 For x86 compilers, \_chkstk Routine is called when the local variables exceed 4K bytes; for x64 compilers it is 8K.

 

 



