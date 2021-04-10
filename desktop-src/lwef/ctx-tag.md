---
title: Ctx 標記
description: Ctx 標記
ms.assetid: 96ceaa98-869d-4c51-a419-882cc9d40ae2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f16beae0fd4ccc062969d9aafb4d8747e4c5afe9
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021688"
---
# <a name="ctx-tag"></a>Ctx 標記

\[Microsoft Agent 已于 Windows 7 淘汰，在後續的 Windows 版本中可能無法使用。\]

<dl> <dt>

<span id="Description"></span><span id="description"></span><span id="DESCRIPTION"></span>**描述**
</dt> <dd>

設定輸出文字的內容。

</dd> <dt>

<span id="Syntax"></span><span id="syntax"></span><span id="SYNTAX"></span>**語法**
</dt> <dd>

\\**Ctx** =*字串*\\



| 部分     | 描述                                                                                                                                                                                                                                                                                      |
|----------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| *string* | 字串，指定下文字的內容，以決定如何說出符號或縮寫。<br/> **"Address"**    位址和/或電話號碼。<br/> 「**電子郵件**」   電子郵件。<br/> 「**未知**」 (預設) 內容不明。<br/> |



 

</dd> </dl>

### <a name="remarks"></a>備註

只有 TTS 產生的輸出才支援此標記。 參數的值範圍可能會根據已安裝的 TTS 引擎而有所不同。

 

 





