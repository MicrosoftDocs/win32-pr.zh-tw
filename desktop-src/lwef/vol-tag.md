---
title: 音量標記
description: 音量標記
ms.assetid: a6444eb2-79c2-4c86-8474-846d908479df
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 097d03b7bb536ada8dc783e1506ba4bedfd54c6b5698e1aa68dfe55fd1f939d3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119035976"
---
# <a name="vol-tag"></a>音量標記

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

設定語音輸出的基準說話量。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

**\\ 音量 =**_數位_*_\\_*



| 部分     | 描述                                                         |
|----------|---------------------------------------------------------------------|
| *number* | 基準朗讀磁片區：0是無回應，而65535是最大音量。 |



 

</dd> </dl>

### <a name="remarks"></a>備註

[磁片區] 設定會影響左右通道。 您無法分別設定每個通道的音量。 只有 TTS 產生的輸出才支援此標記。

 

 




