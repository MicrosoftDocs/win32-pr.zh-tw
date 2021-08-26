---
description: 深入瞭解：可擴充的儲存體引擎受控參考
title: 可擴充的儲存體引擎受控參考
TOCTitle: Extensible Storage Engine Managed Reference
ms:assetid: b6dc69d0-82be-478d-b47f-37d7569cd200
ms:mtpsurl: https://msdn.microsoft.com/library/Dn375980(v=EXCHG.10)
ms:contentKeyID: 56355772
ms.date: 09/02/2015
ms.topic: article
ms.openlocfilehash: 38f7f09d441fa6f4158594caa8eda0b15bbe07fe909a73cd194f0886bb29914d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120093678"
---
# <a name="extensible-storage-engine-managed-reference"></a>可擴充的儲存體引擎受控參考

尋找 ManagedESENT 程式庫的參考資訊。 ManagedESENT 程式庫提供對 ESENT 的 managed 存取，也就是 Windows 原生的可內嵌資料庫引擎。


_**適用于：** Windows |Windows伺服器_

**本文內容**  
ManagedESENT 程式庫與 ESENT 有何不同？  
規格需求  
本節內容  

## <a name="how-is-the-managedesent-library-different-than-esent"></a>ManagedESENT 程式庫與 ESENT 有何不同？

ESENT 是可內嵌的交易式資料庫引擎，可讓您建立需要可靠、高效能、低額外儲存資料的自訂應用程式。 ESENT 引擎可協助資料需要的範圍，從簡單到太大而無法儲存在記憶體中的雜湊表，到更複雜的資料，例如具有資料表、資料行和索引的應用程式。 若要建立具有 ESENT 的應用程式，您可以使用屬於 Windows 作業系統一部分的 esent.dll DLL，並使用 c/c + + 撰寫您的程式碼。 如需 ESENT 的詳細資訊，請參閱[可擴展的儲存體引擎參考](./extensible-storage-engine-reference.md)。

ManagedESENT 是以 esent.dll 為基礎，這是 Windows 的一部分，所以沒有額外的非受控二進位檔可供下載和安裝。 使用 ManagedESENT 程式庫，您可以使用 managed 語言（例如 C）來建立應用程式， \# 而不是使用 c/c + +。 程式庫會使用相同的類型和成員名稱來公開 ESE API，因此如果您已經熟悉此 API 的結構，就可以輕鬆地轉換至此 managed 程式庫。

## <a name="requirements"></a>規格需求

此 managed 程式庫需要下列各項：

  - 從 Windows Vista 開始執行版本 Windows 的電腦

  - Visual Studio 2012

  - .NET Framework 4.5

## <a name="in-this-section"></a>本節內容

  - [Microsoft. Esent](./microsoft.isam.esent-namespace.md)

  - [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)

  - [Server2003 （.）](./microsoft.isam.esent.interop.server2003-namespace.md)

  - [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)

  - [最為理想（.）](./microsoft.isam.esent.interop.windows7-namespace.md)

  - [Windows8 （.）](./microsoft.isam.esent.interop.windows8-namespace.md)
