---
title: 音量標記
description: 音量標記
ms.assetid: a6444eb2-79c2-4c86-8474-846d908479df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7979278b2eb89c352b9e53f6141cb585fb0ed134
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021002"
---
# <a name="vol-tag"></a>音量標記

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

設定語音輸出的基準說話量。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

**\\音量 =***數位***\\**



| 部分     | 描述                                                         |
|----------|---------------------------------------------------------------------|
| *number* | 基準朗讀磁片區：0是無回應，而65535是最大音量。 |



 

</dd> </dl>

### <a name="remarks"></a>備註

[磁片區] 設定會影響左右通道。 您無法分別設定每個通道的音量。 只有 TTS 產生的輸出才支援此標記。

 

 




