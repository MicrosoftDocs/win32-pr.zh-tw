---
description: '深入瞭解： JetGetDatabaseFileInfo 方法 (字串、Int32、JET_DbInfo) '
title: 'JetGetDatabaseFileInfo 方法 (字串、Int32、JET_DbInfo) '
TOCTitle: JetGetDatabaseFileInfo method (String, Int32, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo(System.String,System.Int32@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabasefileinfo(v=EXCHG.10)
ms:contentKeyID: 55100698
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
ms.openlocfilehash: 7a7d873d3688d6c18ff01a20c5e5c53809fbcdad
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966691"
---
# <a name="apijetgetdatabasefileinfo-method-string-int32-jet_dbinfo"></a><span data-ttu-id="6cf8a-103">JetGetDatabaseFileInfo 方法 (字串、Int32、JET_DbInfo) </span><span class="sxs-lookup"><span data-stu-id="6cf8a-103">Api.JetGetDatabaseFileInfo method (String, Int32, JET_DbInfo)</span></span>

<span data-ttu-id="6cf8a-104">抓取特定資料庫的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="6cf8a-104">Retrieves certain information about the given database.</span></span>

<span data-ttu-id="6cf8a-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="6cf8a-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="6cf8a-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="6cf8a-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="6cf8a-107">語法</span><span class="sxs-lookup"><span data-stu-id="6cf8a-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetDatabaseFileInfo ( _
    databaseName As String, _
    <OutAttribute> ByRef value As Integer, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim databaseName As String
Dim value As Integer
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseFileInfo(databaseName, _
    value, infoLevel)
```

``` csharp
public static void JetGetDatabaseFileInfo(
    string databaseName,
    out int value,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="6cf8a-108">參數</span><span class="sxs-lookup"><span data-stu-id="6cf8a-108">Parameters</span></span>

  - <span data-ttu-id="6cf8a-109">databaseName</span><span class="sxs-lookup"><span data-stu-id="6cf8a-109">databaseName</span></span>  
    <span data-ttu-id="6cf8a-110">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="6cf8a-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="6cf8a-111">資料庫的檔案名。</span><span class="sxs-lookup"><span data-stu-id="6cf8a-111">The file name of the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="6cf8a-112">value</span><span class="sxs-lookup"><span data-stu-id="6cf8a-112">value</span></span>  
    <span data-ttu-id="6cf8a-113">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="6cf8a-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="6cf8a-114">要擷取的值。</span><span class="sxs-lookup"><span data-stu-id="6cf8a-114">The value to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="6cf8a-115">infoLevel</span><span class="sxs-lookup"><span data-stu-id="6cf8a-115">infoLevel</span></span>  
    <span data-ttu-id="6cf8a-116">類型： [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="6cf8a-116">Type: [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="6cf8a-117">要取出的特定資料。</span><span class="sxs-lookup"><span data-stu-id="6cf8a-117">The specific data to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="6cf8a-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="6cf8a-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="6cf8a-119">參考</span><span class="sxs-lookup"><span data-stu-id="6cf8a-119">Reference</span></span>

[<span data-ttu-id="6cf8a-120">Api 類別</span><span class="sxs-lookup"><span data-stu-id="6cf8a-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="6cf8a-121">Api 成員</span><span class="sxs-lookup"><span data-stu-id="6cf8a-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="6cf8a-122">JetGetDatabaseFileInfo 多載</span><span class="sxs-lookup"><span data-stu-id="6cf8a-122">JetGetDatabaseFileInfo overload</span></span>](./api.jetgetdatabasefileinfo-method.md)

[<span data-ttu-id="6cf8a-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="6cf8a-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
