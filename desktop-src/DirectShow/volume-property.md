---
description: '[磁片區] 屬性會設定或抓取音訊串流輸出的喇叭音量。'
ms.assetid: b6e22d07-525b-4af2-898c-ce3ed16ea9c1
title: Volume 屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: cc3c7ebd89b971e8a8f934608ff38dc741c0db91ac2d25f717d7354b3d6294b0
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119632878"
---
# <a name="volume-property"></a>Volume 屬性

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`Volume`屬性會設定或抓取音訊串流輸出的喇叭音量。

``` syntax
[ iVolume = ] MSWebDVD.Volume
```

## <a name="return-value"></a>傳回值

將磁片區層級傳回為分貝（以分貝為單位），以做為整數。

## <a name="remarks"></a>備註

這個屬性是讀取/寫入，預設值是0。 完整磁片區為0，而10000為無回應;尺規為對數。 將所需的分貝層級乘以 100 (例如 10000 = 100 dB) 。

 

 



