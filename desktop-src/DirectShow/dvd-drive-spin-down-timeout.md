---
description: DVD 光碟機調低時間
ms.assetid: 2295253d-0199-41b4-95a8-cda049ca93c7
title: DVD 光碟機調低時間
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: acda6853830ee7289e529d029c78fe4e56e4a0e3
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846607"
---
# <a name="dvd-drive-spin-down-timeout"></a><span data-ttu-id="5bb7e-103">DVD 光碟機調低時間</span><span class="sxs-lookup"><span data-stu-id="5bb7e-103">DVD Drive Spin Down Timeout</span></span>

<span data-ttu-id="5bb7e-104">在膝上型電腦上，為了節省電池壽命，您可能會想要縮短 DVD 光碟機在使用者暫停播放後會繼續旋轉的時間長度。</span><span class="sxs-lookup"><span data-stu-id="5bb7e-104">On laptop computers, to conserve battery life it may be desirable to reduce the length of time that a DVD drive will continue to spin after the user has paused playback.</span></span> <span data-ttu-id="5bb7e-105">根據預設，DVD 導覽器會保留光碟旋轉兩分鐘。</span><span class="sxs-lookup"><span data-stu-id="5bb7e-105">By default, the DVD Navigator keeps the disc spinning for two minutes.</span></span> <span data-ttu-id="5bb7e-106">此值可以在 Windows 登錄的下列機碼底下修改：</span><span class="sxs-lookup"><span data-stu-id="5bb7e-106">This value can be modified in the Windows Registry under this key:</span></span>


```C++
DWORD HKLM\SOFTWARE\Microsoft\DVDNavigator\DriveSpindown 
[Sec]
```



<span data-ttu-id="5bb7e-107">其中</span><span class="sxs-lookup"><span data-stu-id="5bb7e-107">where</span></span>


```
Sec
```



<span data-ttu-id="5bb7e-108">這是微調時間（以秒為單位）。</span><span class="sxs-lookup"><span data-stu-id="5bb7e-108">is the spin down time in seconds.</span></span>

## <a name="related-topics"></a><span data-ttu-id="5bb7e-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="5bb7e-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="5bb7e-110">附錄</span><span class="sxs-lookup"><span data-stu-id="5bb7e-110">Appendixes</span></span>](appendixes.md)
</dt> </dl>

 

 



