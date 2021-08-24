---
description: GetKaraokeChannelAssignment 方法會抓取一個值，指出如何將卡拉卡拉板通道指派給喇叭。
ms.assetid: 08e35fa6-fa1b-4f9f-8f56-d953c4422226
title: GetKaraokeChannelAssignment 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 010e8112ece9b3fc66831055995ebf46657d4216942ac3b9dee05b1b68d18761
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119812548"
---
# <a name="getkaraokechannelassignment-method"></a>GetKaraokeChannelAssignment 方法

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`GetKaraokeChannelAssignment`方法會抓取一個值，指出如何將卡拉卡拉板通道指派給喇叭。

``` syntax
[ iAssignment = ] MSWebDVD.GetKaraokeChannelAssignment(iStream)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

將音訊串流指定為整數。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回整數，表示指定之資料流程的喇叭指派。



| 傳回碼 | 描述                                                             |
|-------------|-------------------------------------------------------------------------|
| 2           | 資料流程會指派給左邊和右邊的喇叭。                  |
| 3           | 資料流程會指派給左、右和中間說話者。         |
| 4           | 資料流程會指派給左、右和 audio1 喇叭。         |
| 5           | 資料流程會指派給左、右、中間和 audio1 喇叭。 |
| 6           | 資料流程會指派給左、右和 audio2 喇叭。         |
| 7           | 資料流程會指派給左、右、中間和 audio2 喇叭。 |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md)
</dt> </dl>

 

 



