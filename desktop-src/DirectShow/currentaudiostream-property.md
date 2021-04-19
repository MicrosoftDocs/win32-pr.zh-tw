---
description: CurrentAudioStream 屬性會設定或抓取已啟用之音訊串流的數目。
ms.assetid: 9efaae3f-1fb8-41ab-b7a9-889cc3cc39c3
title: CurrentAudioStream 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2b8b67d81eeec21aec164f3ca865ee3f2de4cd3f
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106973746"
---
# <a name="currentaudiostream-property"></a>CurrentAudioStream 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`CurrentAudioStream`屬性會設定或抓取已啟用的音訊資料流程數目。

``` syntax
[ iStream = ] MSWebDVD.CurrentAudioStream
```

## <a name="return-value"></a>傳回值

傳回從0到7的整數值，表示目前的音訊資料流程。

## <a name="remarks"></a>備註

此屬性是讀取/寫入，沒有預設值。 嘗試設定新的音訊串流之前，請先呼叫 [**IsAudioStreamEnabled**](isaudiostreamenabled-method.md) 來確認資料流程是否可用。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AudioStreamsAvailable**](audiostreamsavailable-property.md)
</dt> </dl>

 

 



