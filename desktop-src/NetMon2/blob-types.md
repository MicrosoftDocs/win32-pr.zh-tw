---
description: 網路監視器使用三種類型的二進位大型物件 (Blob) 選取並連接網路介面卡 (Nic) 、捕捉資料和操作 NPP 資料。
ms.assetid: f7cbceb1-1a85-4a05-8420-90b32c9c9b61
title: BLOB 類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 029c375c446d53074cc0c9797dfa2992b2b2d933
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104195078"
---
# <a name="blob-types"></a>BLOB 類型

網路監視器使用三種類型的二進位大型物件 (Blob) 選取並連接網路介面卡 (Nic) 、捕捉資料和操作 NPP 資料。

## <a name="npp-blob"></a>NPP BLOB

應用程式會使用 NPP Blob 透過 NPP 連接到特定的 NIC。  (應用程式會對 NPP BLOB 中 **CreateNPPInterface** 和位置資料的呼叫進行連線。應用程式 ) 應用程式也可以將其設定資料儲存在 NPP BLOB 中，以設定 NPP。 此外，儲存其 NPP BLOB 的應用程式不需要經過搜尋工具即可重複使用該 BLOB。

## <a name="filter-blob"></a>篩選 BLOB

篩選 BLOB 包含應用程式定義的準則，您可以用來選取 NPP 和 NIC。 例如，應用程式可以要求特定的 NIC、只有乙太網路卡，或支援特定畫面格捕獲速率的卡片。

## <a name="special-blob"></a>特殊 BLOB

當 NPP 需要額外的資料才能將 NPP BLOB 傳回給應用程式時，NPP 會使用特殊的 BLOB。 最常見的情況是，應用程式不需要或使用特殊的 Blob，除非在一個函式呼叫中設定特定的旗標，否則不會將它們傳回給應用程式。 例如，遠端 NPP 會使用特殊的 BLOB，因為需要路徑名稱才能建立連接。 接收遠端 NPP 特殊 BLOB 的應用程式可以將字串加回搜尋工具，以取得 NPP BLOB 資料表。 如需詳細資訊，請參閱 [特殊 BLOB 專案](special-blob-entries.md)。

 

 



