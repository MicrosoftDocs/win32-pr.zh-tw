---
description: 若要從網路監視器所傳回的 NPP BLOB 資料表中選取 NIC，請呼叫 GetNPPBlobTable 函數。 此函式會傳回 NPP BLOB 資料表，然後您的應用程式會加以列舉，以選取您感興趣的 NIC。
ms.assetid: 51428cc9-0b48-4da6-bbf6-b22798e01263
title: 從傳回的 NPP BLOB 資料表選取 NIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7f5555e68e04886b390a6b6bd1f9f8372202fe970a4784ffa2652a3fc991c4da
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120074468"
---
# <a name="selecting-a-nic-from-a-returned-npp-blob-table"></a>從傳回的 NPP BLOB 資料表選取 NIC

若要從網路監視器所傳回的 NPP BLOB 資料表中選取 NIC，請呼叫 [**GetNPPBlobTable**](getnppblobtable.md) 函數。 此函式會傳回 NPP BLOB 資料表，然後您的應用程式會加以列舉，以選取您感興趣的 NIC。

當您呼叫此函式時，您可以傳回在本機電腦上註冊之所有 Nic 的 BLOB 資料表，或是一組較小的篩選 Nic。 若要篩選傳回的 Nic，您可以在進行呼叫時提供 [*篩選 BLOB*](f.md) 。



| 如需下列資訊                                                       | 請參閱                                                                                                  |
|-----------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------|
| 如何指定篩選器來限制 NPP BLOB 資料表中傳回的 Nic。 | [指定篩選 BLOB](specifying-a-filter-blob.md)                                             |
| 如何選取在本機電腦上註冊的 NIC。                         | [選取已註冊的 NIC](selecting-a-registered-nic.md)                                         |
| 如何從提供的 NPP BLOB 資料表選取 NIC                          | [從提供的 NPP BLOB 資料表選取 NIC](selecting-a-nic-from-a-supplied-npp-blob-table.md) |



 

 

 



