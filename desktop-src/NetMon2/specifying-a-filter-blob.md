---
description: 當您選取已註冊的網路介面卡 (NIC) 列在本機電腦上時，可以使用篩選 BLOB 來忽略您不感興趣的 Nic。
ms.assetid: fa87bb7d-c481-4eb1-b116-b22643a7c9da
title: 指定篩選 BLOB
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 486a5dfe318da50a921560c92b82a3a3bf05a9434a4ac609b7f135afd7bf5a34
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119555348"
---
# <a name="specifying-a-filter-blob"></a>指定篩選 BLOB

當您選取已註冊的網路介面卡 (NIC) 列在本機電腦上時，可以使用 [*篩選 BLOB*](f.md) 來忽略您不感興趣的 nic。 例如，您可以限制搜尋特定類型的卡片 (例如 ETHERNET) 或特定 MAC 位址。

在搜尋 NIC 期間，篩選 BLOB 中的每個專案都必須符合代表 NIC 的 NPP BLOB 中的對等專案。 篩選 Blob 也可以是 [*特殊的 blob*](s.md)。

呼叫 [**GetNPPBlobFromUI**](getnppblobfromui.md) 函數時，篩選 BLOB 會限制 [ **選取網路** ] 對話方塊中顯示的 nic。 呼叫 [**GetNPPBlobTable**](getnppblobtable.md) 函數時，篩選 blob 會限制在 BLOB 資料表中傳回的 nic。

若要使用篩選準則，您必須建立篩選 BLOB、設定您想要篩選的屬性值 (包括) 的任何特殊 BLOB 專案，然後指定 BLOB 篩選器和 [**GetNPPBlobTable**](getnppblobtable.md) 或 [**GetNPPBlobFromUI**](getnppblobfromui.md) 函數的呼叫。



| 如需相關資訊                                 | 請參閱                                                                                                  |
|----------------------------------------------------|------------------------------------------------------------------------------------------------------|
| 如何選取在本機電腦上註冊的 NIC | [選取已註冊的 NIC](selecting-a-registered-nic.md)                                         |
| 正在抓取 NPP BLOB 資料表                       | [從傳回的 NPP BLOB 資料表選取 NIC](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



