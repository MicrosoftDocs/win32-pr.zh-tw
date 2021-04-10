---
description: AudioStreamsAvailable 屬性會抓取目前標題中可用的音訊資料流程數目。
ms.assetid: 4359ec30-920a-4b34-8e27-4cf1d9452aa8
title: AudioStreamsAvailable 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cb68020b30f4349fcbbb464150624d75250a0dbf
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103846180"
---
# <a name="audiostreamsavailable-property"></a>AudioStreamsAvailable 屬性

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

屬性會抓取 `AudioStreamsAvailable` 目前標題中可用的音訊資料流程數目。

``` syntax
[ iStreams = ] MSWebDVD.AudioStreamsAvailable
```

## <a name="return-value"></a>傳回值

傳回從1到8的整數值，代表目前標題中可用的音訊資料流程數目。

## <a name="remarks"></a>備註

這個屬性是唯讀的，沒有預設值。 多個音訊串流的主要用途是提供一種以上語言的電影 soundtracks。 一般而言，並非光碟上的每個標題都已啟用所有音訊串流。 例如，功能電影可能有三種不同語言的 soundtracks，但結尾可能只有英文的聲段。 在使用者可以選取資料流程之前，應用程式必須判斷目前的標題中有哪些可用的資料流程。 請注意，特定資料流程是由0到7的索引所識別。

光碟通常會顯示一個顯示可用 soundtracks 的功能表，讓使用者可以選取要啟用的音訊串流。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**GetAudioLanguage**](getaudiolanguage-method.md)
</dt> </dl>

 

 



