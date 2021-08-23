---
title: 正在抓取裝置的相關資訊
description: 正在抓取裝置的相關資訊
ms.assetid: d038d3fb-43d0-4d9d-836c-205f6d8c98e3
keywords:
- MCI_GETDEVCAPS 命令
- MCI_STATUS 命令
- MCI_INFO 命令
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 412ccfb8819ac1c76cd3f0114fa114c877280de959f605535fd4bb83d224a91e
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119689088"
---
# <a name="retrieving-information-about-a-device"></a>正在抓取裝置的相關資訊

每部裝置都會回應 ([**mci \_ GETDEVCAPS**](mci-getdevcaps.md)) 、 [**status**](status.md) ([**Mci \_ status**](mci-status.md)) 和 [**info**](info.md) ([**mci \_ info**](mci-info.md)) 命令的 [**功能**](capability.md)。 這些命令會取得裝置的相關資訊。 例如，如果 **cdaudio** 裝置可以退出光碟，則下列命令會傳回 "true"：


```C++
mciSendString(
    "capability cdaudio can eject", 
    lpszReturnString, lstrlen(lpszReturnString), NULL);
```



針對 [必要] 和 [基本] 命令列出的旗標，可提供裝置最少的資訊數量。 許多裝置都會使用擴充旗標來補充必要和基本命令，以提供裝置的其他相關資訊。

 

 




