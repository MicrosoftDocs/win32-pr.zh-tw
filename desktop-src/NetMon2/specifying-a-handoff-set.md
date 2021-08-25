---
description: 遞交集會指定遵循通訊協定的通訊協定。 只有當剖析器可以從通訊協定實例中的資料識別下一個通訊協定時，剖析器才會使用一組遞交集。
ms.assetid: d1f44646-98ee-4e3a-a81a-83d6c87c23f4
title: 指定遞交集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3c2f3f7d559c83e3c56bc6ea202b3a0e339dbc1b76d93fc2af1b73f5a2c60c4e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119778348"
---
# <a name="specifying-a-handoff-set"></a>指定遞交集

遞交集會指定遵循通訊協定的通訊協定。 只有當剖析器可以從通訊協定實例中的資料識別下一個通訊協定時，剖析器才會使用一組遞交集。

例如，TCP 通訊協定具有埠屬性，可識別 TCP 通訊協定後面的通訊協定。 屬性值為20表示下一個通訊協定是 FTP。 屬性值53表示下一個通訊協定是 DNS。 因為 port 屬性會識別接下來的通訊協定，所以 TCP 剖析器可以使用下列的遞交集來取得埠屬性指定之通訊協定的控制碼。

``` syntax
[TCP_HandoffSet]
  20    = FTP
  21    = FTP
  23    = TELNET
  25    = SMTP
  53    = DNS
  79    = FINGER
  80    = HTTP
  102   = ISO
  111   = RPC
  119   = NNTP
  137   = NBT, 1000
  138   = NBT, 1002
  139   = NBT, 1001
  389   = LDAP
  445   = NBT, 1001
  515   = LPR
  612   = HMMP
  613   = HMMP
  1024  = NBT, 1001
  1047  = NBT, 1001
  1362  = TDS
  1433  = TDS
  1723  = PPTP
  3020  = NBT, 1001
  3268  = LDAP
  5678  = PPTP
```

遞交集會儲存在剖析器 INI 檔案中。 例如，先前的 TCP 遞交集位於 tcpip.ini 檔案中。 請注意，如果剖析器 DLL 支援多個通訊協定，則每個使用遞交集的剖析器在 INI 檔案中都有自己的位置。

在 [**ParserAutoInstallInfo**](parserautoinstallinfo.md) 函數的執行期間，會指定遞交集資訊。 剖析器可以指定剖析器通訊協定之前的通訊協定，以及遵循剖析器通訊協定的通訊協定。 網路監視器會採用之前的所有通訊協定，並將剖析器通訊協定新增至剖析器 INI 檔案中的下列設定區段—適用于上述每個通訊協定。 網路監視器會在剖析器 INI 檔案的 [遞交集] 區段中儲存遵循的通訊協定清單。

網路監視器會將遞交集資訊儲存在剖析器 INI 檔案中，但剖析器不會直接存取 INI 檔案。 若要使用遞交集中的資訊，剖析器會呼叫 [**CreateHandoffTable**](createhandofftable.md) 函數來建立遞交資料表。 通常，當剖析器註冊通訊協定時，就會建立遞交資料表。 註冊通訊協定之後，網路監視器會建立剖析器可以使用的一個遞交集資料表。

剖析器會在辨識資料時使用其交付集。 首先，剖析器會讀取識別下一個通訊協定的屬性值。 然後，剖析器會呼叫 [**GetProtocolFromTable**](getprotocolfromtable.md) 來取得下一個通訊協定的控制碼。 最後，剖析器會將指標傳回至 [**RecognizeFrame**](recognizeframe.md)的 *phNextProtocol* 參數中的控制碼。

 

 



