---
description: GetKaraokeChannelContent 方法會抓取值，指出指定之資料流程中指定之卡拉別通道的內容類型。
ms.assetid: e36a88b8-7184-44a4-8e02-204440f651bc
title: GetKaraokeChannelContent 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bd35705f1fba65eaf5c6f7c67ea55078c68e5036
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106988051"
---
# <a name="getkaraokechannelcontent-method"></a>GetKaraokeChannelContent 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`GetKaraokeChannelContent`方法會抓取值，指出指定之資料流程中指定之卡拉別通道的內容類型。

``` syntax
[ iContent = ] MSWebDVD.GetKaraokeChannelContent(iStream, iChannel)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iStream"></span><span id="istream"></span><span id="ISTREAM"></span>*iStream*
</dt> <dd>

將音訊串流指定為整數。

</dd> <dt>

<span id="iChannel"></span><span id="ichannel"></span><span id="ICHANNEL"></span>*iChannel*
</dt> <dd>

將通道指定為整數。 每個通道的可能值為：



| 值  | 描述    |
|--------|----------------|
| 0x0001 | 指南關切這個領域1  |
| 0x0002 | 指南關切這個領域2  |
| 0x0004 | 指南旋律1 |
| 0x0008 | 指南旋律2 |
| 0x0010 | 指南旋律 |
| 0x0020 | 指南旋律 B |
| 0x0040 | 音效效果 A |
| 0x0080 | 音效效果 B |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回整數值，其個別位指定卡拉 ok 通道的內容。

## <a name="remarks"></a>備註

DVD-音訊頻道編號是以零為基礎，因此通道2、3和4是輔助的卡拉卡拉器通道。 在方法傳回之後，請在 *iContent* 上執行位 and 運算，以判斷每個通道的內容。 由於單一通道可能會在其上記錄一個以上的內容，因此您應該測試所有可能的值，即使在找到相符的之後也是一樣。

當使用者知道每個頻道的內容之後，他或她必須能夠視需要調整音量，或開啟或關閉個別頻道。 使用 [**KaraokeAudioPresentationMode**](karaokeaudiopresentationmode-property.md) 屬性，在您的應用程式中執行這項功能。

> [!Note]  
> 若要播放卡拉卡拉5光碟，使用者系統上的音訊解碼器必須與 DirectShow 8 卡拉卡拉的執行相容。

 

 

 



