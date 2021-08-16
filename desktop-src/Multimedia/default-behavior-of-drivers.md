---
title: 驅動程式的預設行為
description: 驅動程式的預設行為
ms.assetid: ed6905eb-67ad-421d-be00-4a5585dff7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 61312010759ddd1bf152f0e51f7605bda1954329096913b61dac14a671908f0f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119144521"
---
# <a name="default-behavior-of-drivers"></a>驅動程式的預設行為

在許多情況下，MCI 命令規格會定義特定裝置類型之驅動程式的預設值和行為。 由於多媒體裝置可以有各式各樣的功能 (和限制) ，因此可能會有未定義的行為範圍。 此外，驅動程式可能會根據裝置的功能，以不同的方式處理例外狀況。

例如，請考慮使用 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 函式將下列命令傳送到波形音訊驅動程式：


```C++
mciSendString("open sound.wav alias sound", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("play sound notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("record sound from 0 notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



[**Record**](record.md)命令會傳回「參數超出範圍」值，並停止先前的 [**play**](play.md)命令啟動的播放。 其中一個可能會預期驅動程式先驗證記錄命令才能停止播放，但是驅動程式會先停止播放。

 

 