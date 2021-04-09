---
description: PlayChapterInTitle 方法會在指定的標題中播放指定的章節。
ms.assetid: 784b0612-133b-465c-b1da-d9dac26e1b20
title: PlayChapterInTitle 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 381a63c36c61a8853dcba6a587adb1f078b8cfaa
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103845676"
---
# <a name="playchapterintitle-method"></a>PlayChapterInTitle 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

`PlayChapterInTitle`方法會在指定的標題中播放指定的章節。

``` syntax
MSWebDVD.PlayChapterInTitle(iTitle, iChapter)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

將標題指定為整數值。

</dd> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*
</dt> <dd>

將章節指定為整數值。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

這個方法會在指定的章節開始播放，然後繼續無限期地播放。 如果您只想要播放特定的章節，請使用 [**PlayChaptersAutoStop**](playchaptersautostop-method.md)。

 

 



