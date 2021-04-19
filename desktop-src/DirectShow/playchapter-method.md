---
description: PlayChapter 方法會從目前標題內的指定章節開始播放。
ms.assetid: d0318a0d-4ff4-42f2-b009-996b7ff0f632
title: PlayChapter 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: bab4600d8d4fc09c4b63fa423c66823e92e95a2a
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "106998422"
---
# <a name="playchapter-method"></a>PlayChapter 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

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

 

 



