---
description: '深入瞭解： JetGetDatabaseFileInfo 方法 (字串、Int64、JET_DbInfo) '
title: 'JetGetDatabaseFileInfo 方法 (字串、Int64、JET_DbInfo) '
TOCTitle: JetGetDatabaseFileInfo method (String, Int64, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo(System.String,System.Int64@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabasefileinfo(v=EXCHG.10)
ms:contentKeyID: 55100700
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: cc036a1c1eceedd39fd265bcf85a2dbaf779a432
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112584"
---
# <a name="apijetgetdatabasefileinfo-method-string-int64-jet_dbinfo"></a><span data-ttu-id="fed1e-103">JetGetDatabaseFileInfo 方法 (字串、Int64、JET_DbInfo) </span><span class="sxs-lookup"><span data-stu-id="fed1e-103">Api.JetGetDatabaseFileInfo method (String, Int64, JET_DbInfo)</span></span>

<span data-ttu-id="fed1e-104">抓取特定資料庫的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="fed1e-104">Retrieves certain information about the given database.</span></span>

<span data-ttu-id="fed1e-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="fed1e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="fed1e-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="fed1e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="fed1e-107">語法</span><span class="sxs-lookup"><span data-stu-id="fed1e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetDatabaseFileInfo ( _
    databaseName As String, _
    <OutAttribute> ByRef value As Long, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim databaseName As String
Dim value As Long
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseFileInfo(databaseName, _
    value, infoLevel)
```

``` csharp
public static void JetGetDatabaseFileInfo(
    string databaseName,
    out long value,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="fed1e-108">參數</span><span class="sxs-lookup"><span data-stu-id="fed1e-108">Parameters</span></span>

  - <span data-ttu-id="fed1e-109">databaseName</span><span class="sxs-lookup"><span data-stu-id="fed1e-109">databaseName</span></span>  
    <span data-ttu-id="fed1e-110">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="fed1e-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="fed1e-111">資料庫的檔案名。</span><span class="sxs-lookup"><span data-stu-id="fed1e-111">The file name of the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="fed1e-112">value</span><span class="sxs-lookup"><span data-stu-id="fed1e-112">value</span></span>  
    <span data-ttu-id="fed1e-113">類型： [Int64](/dotnet/api/system.int64)</span><span class="sxs-lookup"><span data-stu-id="fed1e-113">Type: [System.Int64](/dotnet/api/system.int64)</span></span>  
    
    <span data-ttu-id="fed1e-114">要擷取的值。</span><span class="sxs-lookup"><span data-stu-id="fed1e-114">The value to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="fed1e-115">infoLevel</span><span class="sxs-lookup"><span data-stu-id="fed1e-115">infoLevel</span></span>  
    <span data-ttu-id="fed1e-116">類型： [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="fed1e-116">Type: [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="fed1e-117">要取出的特定資料。</span><span class="sxs-lookup"><span data-stu-id="fed1e-117">The specific data to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="fed1e-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fed1e-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="fed1e-119">參考</span><span class="sxs-lookup"><span data-stu-id="fed1e-119">Reference</span></span>

[<span data-ttu-id="fed1e-120">Api 類別</span><span class="sxs-lookup"><span data-stu-id="fed1e-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="fed1e-121">Api 成員</span><span class="sxs-lookup"><span data-stu-id="fed1e-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="fed1e-122">JetGetDatabaseFileInfo 多載</span><span class="sxs-lookup"><span data-stu-id="fed1e-122">JetGetDatabaseFileInfo overload</span></span>](./api.jetgetdatabasefileinfo-method.md)

[<span data-ttu-id="fed1e-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="fed1e-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
