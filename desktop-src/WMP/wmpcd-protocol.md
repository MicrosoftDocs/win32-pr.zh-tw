---
title: WMPCD 通訊協定
description: WMPCD 通訊協定
ms.assetid: 385cfb03-88cc-400c-a2b9-174008ebd854
keywords:
- Windows Media Player，通訊協定
- Windows Media Player 物件模型，通訊協定
- 物件模型，通訊協定
- Windows Media Player ActiveX 控制項，物件模型的通訊協定
- ActiveX 控制項，物件模型的通訊協定
- Windows Media Player 的行動 ActiveX 控制項、物件模型的通訊協定
- Windows Media Player 行動裝置、物件模型的通訊協定
- 通訊協定，Windows Media Player 物件模型
- 通訊協定，WMPCD
- WMPCD 通訊協定
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: aa78c591d0ba9605f1f63e3e152b974d112548d6
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104183454"
---
# <a name="wmpcd-protocol"></a>WMPCD 通訊協定

WMPCD 通訊協定可讓您使用 URL 語法來指定光碟片上的軌跡。 這是通訊協定的一般語法：


```C++
wmpcd://drive/track
```



*磁片磁碟機* 區段是 CD 光碟機的索引。 *曲目* 區段是曲目的編號。下列範例將示範如何使用 WMPCD 通訊協定。


```C++
player.url = "wmpcd://0/4";
```



此範例會在第一個 CD 光碟機的光碟上播放第四個曲目， (其索引為 0) 的磁片磁碟機。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**支援的通訊協定和檔案類型**](supported-protocols-and-file-types.md)
</dt> </dl>

 

 




