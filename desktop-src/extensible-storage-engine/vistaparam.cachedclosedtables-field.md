---
description: 深入瞭解： VistaParam. CachedClosedTables 欄位
title: VistaParam. CachedClosedTables 欄位)  (的欄位
TOCTitle: CachedClosedTables field
ms:assetid: F:Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.vista.vistaparam.cachedclosedtables(v=EXCHG.10)
ms:contentKeyID: 55104337
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Vista.VistaParam.CachedClosedTables
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: ff72925e34c731e57d11170753ecff13f4b96a39
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112033"
---
# <a name="vistaparamcachedclosedtables-field"></a><span data-ttu-id="d0e4d-103">VistaParam. CachedClosedTables 欄位</span><span class="sxs-lookup"><span data-stu-id="d0e4d-103">VistaParam.CachedClosedTables field</span></span>

<span data-ttu-id="d0e4d-104">此參數會控制應用程式已關閉實例所代表的資料表之後，該實例所快取的 B + 樹系資源數目。</span><span class="sxs-lookup"><span data-stu-id="d0e4d-104">This parameter controls the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="d0e4d-105">此參數的大型值會導致資料庫引擎使用更多記憶體，但會增加應用程式隨機開啟大量資料表的速度。</span><span class="sxs-lookup"><span data-stu-id="d0e4d-105">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="d0e4d-106">對於具有極大量資料表之架構的應用程式而言，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="d0e4d-106">This is useful for applications that have a schema with a very large number of tables.</span></span>

<span data-ttu-id="d0e4d-107">**命名空間：**[Microsoft. Isam](./microsoft.isam.esent.interop.vista-namespace.md) 。  </span><span class="sxs-lookup"><span data-stu-id="d0e4d-107">**Namespace:**  [Microsoft.Isam.Esent.Interop.Vista](./microsoft.isam.esent.interop.vista-namespace.md)</span></span>  
<span data-ttu-id="d0e4d-108">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="d0e4d-108">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="d0e4d-109">語法</span><span class="sxs-lookup"><span data-stu-id="d0e4d-109">Syntax</span></span>

``` vb
'Declaration
Public Const CachedClosedTables As JET_param
'Usage
Dim value As JET_param

value = VistaParam.CachedClosedTables
```

``` csharp
public const JET_param CachedClosedTables
```

## <a name="see-also"></a><span data-ttu-id="d0e4d-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d0e4d-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="d0e4d-111">參考</span><span class="sxs-lookup"><span data-stu-id="d0e4d-111">Reference</span></span>

[<span data-ttu-id="d0e4d-112">VistaParam 類別</span><span class="sxs-lookup"><span data-stu-id="d0e4d-112">VistaParam class</span></span>](./vistaparam-class.md)

[<span data-ttu-id="d0e4d-113">VistaParam 成員</span><span class="sxs-lookup"><span data-stu-id="d0e4d-113">VistaParam members</span></span>](./vistaparam-members.md)

[<span data-ttu-id="d0e4d-114">Microsoft.Isam.Esent.Interop.Vista namespace</span><span class="sxs-lookup"><span data-stu-id="d0e4d-114">Microsoft.Isam.Esent.Interop.Vista namespace</span></span>](./microsoft.isam.esent.interop.vista-namespace.md)
