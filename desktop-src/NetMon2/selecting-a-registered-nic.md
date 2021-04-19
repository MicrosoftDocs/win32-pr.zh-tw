---
description: 若要選取在本機電腦上註冊的其中一個 Nic，請呼叫 GetNPPBlobFromUI 函數。
ms.assetid: ca1fb07f-7eee-419f-b25d-49718d02fc7d
title: 選取已註冊的 NIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 29b7047d5bbb46797210e18782c672cfd81b9cf8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974393"
---
# <a name="selecting-a-registered-nic"></a>選取已註冊的 NIC

若要選取在本機電腦上註冊的其中一個 Nic，請呼叫 [**GetNPPBlobFromUI**](getnppblobfromui.md) 函數。 此函式會使用網路監視器 UI 來顯示已註冊的 Nic，並傳回代表您所選 NIC 的 NPP BLOB。 您可以顯示在本機電腦或一組較小的已篩選 Nic 上註冊的所有 Nic。 若要篩選顯示的 Nic，請在進行呼叫時提供 [*篩選 BLOB*](f.md) 。

> [!Note]  
> 呼叫 [**GetNPPBlobFromUI**](getnppblobfromui.md) 函數時， [*NPP FINDER*](n.md) 會與 NPP dll 通訊，以取得代表已註冊 nic 的 NPP BLOB 結構。 如需詳細資訊，以及如何直接使用網路監視器 UI 的程式，請參閱網路監視器線上說明中的「選取網路對話方塊」主題。

 

當您呼叫 [**GetNPPBlobFromUI**](getnppblobfromui.md) 函數時，會出現 [ **選取網路** ] 對話方塊。 您可以在此查看在本機電腦上註冊的 NPPs 詳細資料。 這項資訊包括本機 NPPs 和遠端 NPPs。 從對話方塊中，您可以選取特定的 NIC，並查看其相關聯 NPP BLOB 結構的詳細資料。

下圖顯示網路監視器所提供之 NDIS NPP 的一般設定。

![網路監視器所提供之 ndis npp 的一般設定](images/networkdb.png)

下表列出描述每個 NIC 選擇方法的主題。



| 如需下列資訊                                                                          | 請參閱                                                                                                  |
|------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| 如何指定篩選器來限制 [ **選取網路** ] 對話方塊中顯示的 nic。 | [指定篩選 BLOB](specifying-a-filter-blob.md)                                             |
| 如何藉由呼叫 [**GetNPPBlobFromUI**](getnppblobfromui.md) 函數來選取 NIC。      | [使用 GetNPPBlobFromUI 選取 NIC](getnppblobfromui.md)                                       |
| 如何從提供的 NPP BLOB 資料表中選取 NIC。                                            | [從提供的 NPP BLOB 資料表選取 NIC](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 



