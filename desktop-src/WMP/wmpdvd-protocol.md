---
title: WMPDVD 通訊協定
description: WMPDVD 通訊協定
ms.assetid: 01f38c9a-3ce5-4cd4-91a7-248f542eed03
keywords:
- Windows Media Player，通訊協定
- Windows Media Player 物件模型，通訊協定
- 物件模型，通訊協定
- Windows Media Player ActiveX 控制項、物件模型的通訊協定
- ActiveX 控制項，物件模型的通訊協定
- Windows Media Player行動 ActiveX 控制項，物件模型的通訊協定
- Windows Media Player行動裝置，物件模型的通訊協定
- 通訊協定，Windows Media Player 物件模型
- 通訊協定，WMPDVD
- WMPDVD 通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8ca67f3cdee6f040aeb266e02493425ca76715ade2e3269f4377ba340af89cc9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119761288"
---
# <a name="wmpdvd-protocol"></a>WMPDVD 通訊協定

WMPDVD 通訊協定可讓您使用 URL 語法，指定 DVD 中的媒體。 這是通訊協定的一般形式：


```C++
wmpdvd://drive/title/chapter?contentdir=path
```



*磁片磁碟機* 區段是 DVD 光碟機的字母;它不包含通常搭配磁片磁碟機規範使用的冒號。 此區段一律為必要項。

*標題* 區段是要播放的標題編號。 除非您想要在特定標題或特定標題的特定章節上開始播放，否則不需要此專案。

*章節* 區段是要播放的章節編號。 除非您想要在特定標題的特定章節上開始播放，否則不需要此專案。

Contentdir 引數是影片 TS 的路徑 \_ 。IFO 檔案，可能位於本機儲存體或網路共用上。 如果您包含此區段，則會忽略 *磁片磁碟機* 區段，不過它仍然是必要的。 如果您也包含 *標題* 區段或 *標題* 和 *章節* 區段，則會相對於 contentdir 區段中指定的 DVD 內容，而不是 *磁片磁碟機* 區段。

下列範例會使用 WMPDVD 通訊協定，從頭開始播放 DVD，就像是自動啟動一樣。


```C++
player.url = "wmpdvd://F";
```



下列範例會使用 WMPDVD 通訊協定，從指定標題的開頭播放 DVD。


```C++
player.url = "wmpdvd://F/2";
```



下列範例會使用 WMPDVD 通訊協定，從指定的章節播放 DVD。


```C++
player.url = "wmpdvd://F/2/4";
```



下列範例會使用 WMPDVD 通訊協定，從本機儲存體播放 DVD 內容。 *路徑* 字串的結尾是包含影片 TS 的資料夾 \_ 。IFO 檔案;它不包含檔案名。 在此範例中， *磁片磁碟機* 區段的值不會有任何作用，雖然它是必要的，而且會從標題2的第4章開始播放。


```C++
player.url = "wmpdvd://Z/2/4?contentdir="d:\sample1\video_ts";
```



將 WMPDVD 字串指派給 **url** 屬性需要 Windows Media Player 9 系列或更新版本。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**支援的通訊協定和檔案類型**](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




