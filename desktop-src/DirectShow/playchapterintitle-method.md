---
description: PlayChapterInTitle 方法會在指定的標題中播放指定的章節。
ms.assetid: 784b0612-133b-465c-b1da-d9dac26e1b20
title: PlayChapterInTitle 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 407684ecf8db6053a4d166a4ed069f9cabf0b36f983dd04bfdf9cf85e6c8dc2a
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119830868"
---
# <a name="playchapterintitle-method"></a>PlayChapterInTitle 方法

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

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

 

 



