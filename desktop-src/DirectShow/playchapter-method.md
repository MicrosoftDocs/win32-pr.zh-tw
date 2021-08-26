---
description: PlayChapter 方法會從目前標題內的指定章節開始播放。
ms.assetid: d0318a0d-4ff4-42f2-b009-996b7ff0f632
title: PlayChapter 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 832b1da6940b26a3cc3a4ab5bdba8653806966f8a399b74eb5adf50600e22293
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120102338"
---
# <a name="playchapter-method"></a>PlayChapter 方法

> [!Note]  
> 此元件可在 Microsoft Windows 2000、Windows XP 和 Windows Server 2003 作業系統中使用。 它在後續版本中可能會變更或無法使用。

 

`PlayChapter`方法會從目前標題內的指定章節開始播放。

``` syntax
MSWebDVD.PlayChapter(iChapter)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*
</dt> <dd>

將目前標題中的章節索引指定為整數。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

到達指定章節的結尾時，此方法會繼續播放後續章節（如果有的話）。 如果您只想要播放指定的章節，請使用 [**PlayChaptersAutoStop**](playchaptersautostop-method.md)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**PlayChapterInTitle**](playchapterintitle-method.md)
</dt> </dl>

 

 



