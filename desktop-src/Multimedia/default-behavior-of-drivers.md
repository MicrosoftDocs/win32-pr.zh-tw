---
title: 驅動程式的預設行為
description: 驅動程式的預設行為
ms.assetid: ed6905eb-67ad-421d-be00-4a5585dff7fb
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 53e5a4294ffc117041d3aca4273cd1f4b8378814
ms.sourcegitcommit: ebd3ce6908ff865f1ef66f2fc96769be0aad82e1
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2020
ms.locfileid: "103682173"
---
# <a name="default-behavior-of-drivers"></a><span data-ttu-id="85874-103">驅動程式的預設行為</span><span class="sxs-lookup"><span data-stu-id="85874-103">Default Behavior of Drivers</span></span>

<span data-ttu-id="85874-104">在許多情況下，MCI 命令規格會定義特定裝置類型之驅動程式的預設值和行為。</span><span class="sxs-lookup"><span data-stu-id="85874-104">In many situations, the MCI command specifications define the default values and behavior for drivers of a particular device type.</span></span> <span data-ttu-id="85874-105">由於多媒體裝置可以有各式各樣的功能 (和限制) ，因此可能會有未定義的行為範圍。</span><span class="sxs-lookup"><span data-stu-id="85874-105">Since multimedia devices can have a wide range of features (and limitations), there can be undefined areas of behavior.</span></span> <span data-ttu-id="85874-106">此外，驅動程式可能會根據裝置的功能，以不同的方式處理例外狀況。</span><span class="sxs-lookup"><span data-stu-id="85874-106">Also, drivers might handle exceptions differently, based on the capabilities of the device.</span></span>

<span data-ttu-id="85874-107">例如，請考慮使用 [**mciSendString**](/previous-versions//dd757161(v=vs.85)) 函式將下列命令傳送到波形音訊驅動程式：</span><span class="sxs-lookup"><span data-stu-id="85874-107">For example, consider the following commands sent to a waveform-audio driver using the [**mciSendString**](/previous-versions//dd757161(v=vs.85)) function:</span></span>


```C++
mciSendString("open sound.wav alias sound", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("play sound notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
mciSendString("record sound from 0 notify", lpszReturnString,
    lstrlen(lpszReturnString), NULL);
```



<span data-ttu-id="85874-108">[**Record**](record.md)命令會傳回「參數超出範圍」值，並停止先前的 [**play**](play.md)命令啟動的播放。</span><span class="sxs-lookup"><span data-stu-id="85874-108">The [**record**](record.md) command returns a "Parameter out of range" value and stops the playback started by the previous [**play**](play.md) command.</span></span> <span data-ttu-id="85874-109">其中一個可能會預期驅動程式先驗證記錄命令才能停止播放，但是驅動程式會先停止播放。</span><span class="sxs-lookup"><span data-stu-id="85874-109">One might expect the driver to validate the record command before stopping playback, but the driver stops the playback first.</span></span>

 

 