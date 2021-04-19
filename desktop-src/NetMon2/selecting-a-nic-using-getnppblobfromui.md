---
description: 使用網路監視器，以程式設計方式選取 NIC 是兩個步驟的程式。 首先，藉由呼叫 CreateBlob 方法來建立篩選 BLOB。 然後，藉由呼叫 GetNPPBlobFromUI 方法來選取 NIC。
ms.assetid: 0556b20a-307e-4bc3-a986-cfee96a8655d
title: 使用 GetNPPBlobFromUI 選取 NIC
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bb429a87d284a5a6a03a20357728c8bbcb5acac4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106972442"
---
# <a name="selecting-a-nic-using-getnppblobfromui"></a>使用 GetNPPBlobFromUI 選取 NIC

使用網路監視器，以程式設計方式選取 NIC 是兩個步驟的程式。 首先，藉由呼叫 [**CreateBlob**](createblob.md) 方法來建立篩選 BLOB。 然後，藉由呼叫 [**GetNPPBlobFromUI**](getnppblobfromui.md) 方法來選取 NIC。

在此範例中，會使用篩選 BLOB 來選取所需的 NIC：


```C++
DWORD rc;

// Call CreateBlob to create a filter blob.
///////////////////////////////////////////
HBLOB hFilterBlob;
rc = CreateBlob(&hFilterBlob);
if (FAILED (rc));
{
  // Failed creating filter BLOB. Add appropriate error handling.
}


// Call GetNPPBlobFromUI to retrieve the NPP Blob.
//////////////////////////////////////////////////
rc = GetNPPBlobFromUI(hwnd,
                      hFilterBlob,
                      &hBlob);
if (FAILED (rc));
{
  // Failed retrieving NPP BLOB. Add appropriate error handling.
}
```



 

 



