---
title: Ctx 標記
description: Ctx 標記
ms.assetid: 96ceaa98-869d-4c51-a419-882cc9d40ae2
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7071994e741cb7dfd1147f163f0d7ef6299ec0dcb9d568ad068251d5a9436809
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119726097"
---
# <a name="ctx-tag"></a>Ctx 標記

\[Microsoft Agent 已于 Windows 7 淘汰，在後續版本的 Windows 中可能無法使用。\]

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

 

 





