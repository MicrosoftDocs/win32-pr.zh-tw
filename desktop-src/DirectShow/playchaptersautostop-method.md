---
description: PlayChaptersAutoStop 方法會在指定的章節中開始播放指定的標題，並針對指定的章節數開始播放。
ms.assetid: ede19f02-6eda-42da-a108-06d78dc2e8a9
title: PlayChaptersAutoStop 方法
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 00f542f890a54c755c9ea041c46f7cef3b4b7fd9
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104187455"
---
# <a name="playchaptersautostop-method"></a>PlayChaptersAutoStop 方法

> [!Note]  
> 此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。 它在後續版本中可能會變更或無法使用。

 

方法會在指定的 `PlayChaptersAutoStop` 章節中開始播放指定的標題，並針對指定的章節數開始播放。

``` syntax
MSWebDVD.PlayChaptersAutoStop(iTitle, iChapter, iChapterCount)
```

## <a name="parameters"></a>參數

<dl> <dt>

<span id="iTitle"></span><span id="ititle"></span><span id="ITITLE"></span>*iTitle*
</dt> <dd>

將標題指定為整數值。

</dd> <dt>

<span id="iChapter"></span><span id="ichapter"></span><span id="ICHAPTER"></span>*iChapter*
</dt> <dd>

將開始章節指定為整數值。

</dd> <dt>

<span id="iChapterCount"></span><span id="ichaptercount"></span><span id="ICHAPTERCOUNT"></span>*iChapterCount*
</dt> <dd>

指定要當作整數值播放的章節數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

播放最後一章之後，這個方法會讓 [**EC \_ DVD \_ 章節 \_ AUTOSTOP**](ec-dvd-chapter-autostop.md) 事件通知傳送至應用程式。

 

 



