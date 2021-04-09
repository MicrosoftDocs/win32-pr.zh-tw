---
title: " (Windows 多媒體) 的裝置控制項"
description: 裝置控制
ms.assetid: b4479803-f1da-4646-909e-c4ef412ebdcd
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 9e0e0b59127d160cc44418fd4bce1f9f670d13de
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "104024473"
---
# <a name="device-control-windows-multimedia"></a> (Windows 多媒體) 的裝置控制項

若要控制 MCI 裝置，請開啟裝置，將必要的命令傳送給它，然後關閉裝置。 命令可能非常類似，即使是完全不同的 MCI 裝置也是一樣。 例如，下列一系列的 MCI 命令會使用 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 函式來播放音訊 CD 的第六個播放軌：


```C++
mciSendString("open cdaudio", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("set cdaudio time format tmsf", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("play cdaudio from 6 to 7", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close cdaudio", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



下一個範例會顯示一系列類似的 MCI 命令，這些命令會播放波形音訊檔案的前10000個範例：


```C++
mciSendString(
    "open c:\mmdata\purplefi.wav type waveaudio alias finch", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
mciSendString("set finch time format samples", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("play finch from 1 to 10000", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
mciSendString("close finch", lpszReturnString, 
    lstrlen(lpszReturnString), NULL);
```



這些範例說明一些有關 MCI 命令的有趣事實：

-   相同的基本命令 ([**開啟**](open.md)、 [**設定**](set.md)、 [**播放**](play.md)和 [**關閉**](close.md)) 用於 CD 音訊和波形音訊裝置。 相同的 MCI 命令會與所有 MCI 裝置搭配使用。
-   波形音訊裝置的 open 命令包含檔案名規格。 波形音訊裝置是一種 *複合裝置* ， (與資料檔案) 相關聯的裝置，而 CD 音訊裝置則是一個 *簡單的裝置* ， (不含相關聯資料檔案) 的裝置。
-   Set 命令會在每個案例中指定時間格式，但 CD 音訊裝置的時間格式旗標會指定曲目/分鐘/秒/畫面格 (TMSF) 格式，而波形音訊裝置所使用的時間格式則指定「範例」。
-   搭配 "from" 和 "to" 旗標使用的變數適用于各自的時間格式。 例如，針對 CD 音訊裝置，變數會指定一系列的曲目，但針對波形音訊裝置，變數會指定一系列的範例。

 

 
