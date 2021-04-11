---
description: '深入瞭解： JetGetDatabaseFileInfo 方法 (字串、JET_DBINFOMISC JET_DbInfo) '
title: 'JetGetDatabaseFileInfo 方法 (字串、JET_DBINFOMISC JET_DbInfo) '
TOCTitle: JetGetDatabaseFileInfo method (String, JET_DBINFOMISC, JET_DbInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo(System.String,Microsoft.Isam.Esent.Interop.JET_DBINFOMISC@,Microsoft.Isam.Esent.Interop.JET_DbInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetdatabasefileinfo(v=EXCHG.10)
ms:contentKeyID: 55100709
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetDatabaseFileInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d72711314312c843d9e456a5194cb6133b4f491f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104112581"
---
# <a name="apijetgetdatabasefileinfo-method-string-jet_dbinfomisc-jet_dbinfo"></a><span data-ttu-id="70e99-103">JetGetDatabaseFileInfo 方法 (字串、JET_DBINFOMISC JET_DbInfo) </span><span class="sxs-lookup"><span data-stu-id="70e99-103">Api.JetGetDatabaseFileInfo method (String, JET_DBINFOMISC, JET_DbInfo)</span></span>

<span data-ttu-id="70e99-104">抓取特定資料庫的特定資訊。</span><span class="sxs-lookup"><span data-stu-id="70e99-104">Retrieves certain information about the given database.</span></span>

<span data-ttu-id="70e99-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="70e99-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="70e99-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="70e99-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="70e99-107">語法</span><span class="sxs-lookup"><span data-stu-id="70e99-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetDatabaseFileInfo ( _
    databaseName As String, _
    <OutAttribute> ByRef dbinfomisc As JET_DBINFOMISC, _
    infoLevel As JET_DbInfo _
)
'Usage
Dim databaseName As String
Dim dbinfomisc As JET_DBINFOMISC
Dim infoLevel As JET_DbInfoApi.JetGetDatabaseFileInfo(databaseName, _
    dbinfomisc, infoLevel)
```

``` csharp
public static void JetGetDatabaseFileInfo(
    string databaseName,
    out JET_DBINFOMISC dbinfomisc,
    JET_DbInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="70e99-108">參數</span><span class="sxs-lookup"><span data-stu-id="70e99-108">Parameters</span></span>

  - <span data-ttu-id="70e99-109">databaseName</span><span class="sxs-lookup"><span data-stu-id="70e99-109">databaseName</span></span>  
    <span data-ttu-id="70e99-110">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="70e99-110">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="70e99-111">資料庫的檔案名。</span><span class="sxs-lookup"><span data-stu-id="70e99-111">The file name of the database.</span></span>

<!-- end list -->

  - <span data-ttu-id="70e99-112">dbinfomisc</span><span class="sxs-lookup"><span data-stu-id="70e99-112">dbinfomisc</span></span>  
    <span data-ttu-id="70e99-113">類型： [Microsoft.Isam.Esent.Interop.JET_DBINFOMISC](./jet-dbinfomisc-class.md)</span><span class="sxs-lookup"><span data-stu-id="70e99-113">Type: [Microsoft.Isam.Esent.Interop.JET_DBINFOMISC](./jet-dbinfomisc-class.md)</span></span>  
    
    <span data-ttu-id="70e99-114">要擷取的值。</span><span class="sxs-lookup"><span data-stu-id="70e99-114">The value to be retrieved.</span></span>

<!-- end list -->

  - <span data-ttu-id="70e99-115">infoLevel</span><span class="sxs-lookup"><span data-stu-id="70e99-115">infoLevel</span></span>  
    <span data-ttu-id="70e99-116">類型： [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="70e99-116">Type: [Microsoft.Isam.Esent.Interop.JET_DbInfo](./jet-dbinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="70e99-117">要取出的特定資料。</span><span class="sxs-lookup"><span data-stu-id="70e99-117">The specific data to retrieve.</span></span>

## <a name="see-also"></a><span data-ttu-id="70e99-118">另請參閱</span><span class="sxs-lookup"><span data-stu-id="70e99-118">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="70e99-119">參考</span><span class="sxs-lookup"><span data-stu-id="70e99-119">Reference</span></span>

[<span data-ttu-id="70e99-120">Api 類別</span><span class="sxs-lookup"><span data-stu-id="70e99-120">Api class</span></span>](./api-class.md)

[<span data-ttu-id="70e99-121">Api 成員</span><span class="sxs-lookup"><span data-stu-id="70e99-121">Api members</span></span>](./api-members.md)

[<span data-ttu-id="70e99-122">JetGetDatabaseFileInfo 多載</span><span class="sxs-lookup"><span data-stu-id="70e99-122">JetGetDatabaseFileInfo overload</span></span>](./api.jetgetdatabasefileinfo-method.md)

[<span data-ttu-id="70e99-123">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="70e99-123">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
