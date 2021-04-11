---
description: 用來描述交易式 NTFS (TxF) 的術語。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: 44cb060c-e6a6-48d6-bbcf-d8dc1ae8ceb2
title: TxF 詞彙
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ee17e9c53b804995e7ef3491b68e963e9311a37f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194756"
---
# <a name="txf-glossary"></a>TxF 詞彙

<dl> <dt>

<span id="fs.availability"></span><span id="FS.AVAILABILITY"></span>**可用 性**
</dt> <dd>

可用性意指資源管理員會中止交易，即使這會中斷一致性，讓系統可以繼續執行新的工作。 預設資源管理員會在系統磁碟區上強制執行可用性。 例如，如果交易記錄檔已滿，就無法加入新的交易記錄空間，而將中止的較舊交易必須從高階資源管理員傳遞結果，才能讓分散式交易完成，資源管理員將不會等待較佳的交易管理員，也會中止交易，即使這可能會中斷一致性。

</dd> <dt>

<span id="fs.consistency"></span><span id="FS.CONSISTENCY"></span>**一致性**
</dt> <dd>

一致性表示如果新交易無法進行前進進度，則資源管理員將會失敗。 例如，如果交易記錄檔已滿，就無法加入新的交易記錄空間，而將中止的較舊交易必須從高階資源管理員傳遞結果，才能讓分散式交易完成，資源管理員會等待該結果。

</dd> <dt>

<span id="fs.miniversion"></span><span id="FS.MINIVERSION"></span>**迷你**
</dt> <dd>

迷你版本是交易寫入器在交易期間所建立的檔案版本。 您稍後可以在具有唯讀存取權的交易中開啟迷你。

</dd> <dt>

<span id="fs.transacted_reader"></span><span id="FS.TRANSACTED_READER"></span>**交易讀取器**
</dt> <dd>

交易式讀取器是以任何許可權開啟的交易式檔案控制代碼，該許可權屬於泛型讀取權限的一部分，但不屬於一般寫入存取權。

</dd> <dt>

<span id="fs.transacted_writer"></span><span id="FS.TRANSACTED_WRITER"></span>**交易寫入器**
</dt> <dd>

交易寫入器是一種使用不屬於泛型讀取權限的任何許可權開啟的交易式檔案控制代碼，但屬於一般寫入存取權的一部分。

</dd> </dl>

 

 



