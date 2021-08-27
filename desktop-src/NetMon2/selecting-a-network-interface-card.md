---
description: 網路監視器提供三個功能來選取網路介面卡 (NIC) 。 這些函式提供三種方式來列舉一組 Nic，並選取您想要使用的一組。 下表列出這些函數。
ms.assetid: fbf319bb-4e24-46e3-81bc-d407b26220fb
title: 選取網路介面卡
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d1f93341bb169f2672579ac6764186925b7190f1ac52c698e2426e1c20d3e854
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074488"
---
# <a name="selecting-a-network-interface-card"></a>選取網路介面卡

網路監視器提供三個功能來選取網路介面卡 (NIC) 。 這些函式提供三種方式來列舉一組 Nic，並選取您想要使用的一組。 下表列出這些函數。



| 函式                                                 | 描述                                                                                                                                  |
|----------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------|
| [**GetNPPBlobFromUI**](getnppblobfromui.md)             | 使用網路監視器 UI 來顯示已註冊的 Nic，並傳回代表您感興趣之 NIC 的 NPP BLOB。           |
| [**GetNPPBlobTable**](getnppblobtable.md)               | 傳回 BLOB 資料表。 應用程式必須列舉資料表並選取 NPP BLOB。                                                       |
| [**SelectNPPBlobFromTable**](selectnppblobfromtable.md) | 使用網路監視器介面顯示提供的 NPP Blob，並傳回代表您感興趣之 NIC 的 NPP BLOB。 |



 

每個 NIC 都會以 NPP 二進位大型物件表示 (BLOB) 。 這些函式可以從電腦上註冊的 NPP BLOB、所提供之 NPP BLOB 資料表中的單一 NPP BLOB，或呼叫端必須用來選取特定 BLOB 的 NPP Blob 資料表傳回單一 BLOB。 在前兩個案例中，從已註冊的 Nic 或從提供的 NPP BLOB 資料表中選取時，網路監視器 UI 會顯示您可以選取的 Nic。

> [!Note]  
> 網路監視器使用稱為 NPP Finder 的功能來列舉在本機電腦上註冊的 Nic。 NPP Finder 是 Npptools.dll 的元件。

 



| 如需下列資訊                            | 請參閱                                                                                                  |
|--------------------------------------------------|------------------------------------------------------------------------------------------------------|
| 選取在本機電腦上註冊的 NIC | [選取已註冊的 NIC](selecting-a-registered-nic.md)                                         |
| 從提供的 NPP BLOB 資料表選取 NIC   | [從提供的 NPP BLOB 資料表選取 NIC](selecting-a-nic-from-a-supplied-npp-blob-table.md) |
| 正在抓取 NPP BLOB 資料表                     | [從傳回的 NPP BLOB 資料表選取 NIC](selecting-a-nic-from-a-returned-npp-blob-table.md) |



 

 

 



