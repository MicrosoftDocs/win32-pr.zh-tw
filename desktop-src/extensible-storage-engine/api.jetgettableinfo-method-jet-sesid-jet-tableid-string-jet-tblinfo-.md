---
description: '深入瞭解： JetGetTableInfo 方法 (JET_SESID、JET_TABLEID、字串 JET_TblInfo) '
title: 'JetGetTableInfo 方法 (JET_SESID、JET_TABLEID、字串、JET_TblInfo) '
TOCTitle: JetGetTableInfo method (JET_SESID, JET_TABLEID, String, JET_TblInfo)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,System.String@,Microsoft.Isam.Esent.Interop.JET_TblInfo)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgettableinfo(v=EXCHG.10)
ms:contentKeyID: 55100745
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetTableInfo
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 01431c018e633a5851f8ca88eb2f2e6f0e9065a5
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106989058"
---
# <a name="apijetgettableinfo-method-jet_sesid-jet_tableid-string-jet_tblinfo"></a><span data-ttu-id="9a011-103">JetGetTableInfo 方法 (JET_SESID、JET_TABLEID、字串、JET_TblInfo) </span><span class="sxs-lookup"><span data-stu-id="9a011-103">Api.JetGetTableInfo method (JET_SESID, JET_TABLEID, String, JET_TblInfo)</span></span>

<span data-ttu-id="9a011-104">抓取資料庫中資料表的各種資訊。</span><span class="sxs-lookup"><span data-stu-id="9a011-104">Retrieves various pieces of information about a table in a database.</span></span>

<span data-ttu-id="9a011-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9a011-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9a011-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="9a011-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9a011-107">語法</span><span class="sxs-lookup"><span data-stu-id="9a011-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetGetTableInfo ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    <OutAttribute> ByRef result As String, _
    infoLevel As JET_TblInfo _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim result As String
Dim infoLevel As JET_TblInfoApi.JetGetTableInfo(sesid, tableid, _
    result, infoLevel)
```

``` csharp
public static void JetGetTableInfo(
    JET_SESID sesid,
    JET_TABLEID tableid,
    out string result,
    JET_TblInfo infoLevel
)
```

#### <a name="parameters"></a><span data-ttu-id="9a011-108">參數</span><span class="sxs-lookup"><span data-stu-id="9a011-108">Parameters</span></span>

  - <span data-ttu-id="9a011-109">sesid</span><span class="sxs-lookup"><span data-stu-id="9a011-109">sesid</span></span>  
    <span data-ttu-id="9a011-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9a011-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9a011-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="9a011-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9a011-112">tableid</span><span class="sxs-lookup"><span data-stu-id="9a011-112">tableid</span></span>  
    <span data-ttu-id="9a011-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9a011-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="9a011-114">要取得相關資訊的資料表。</span><span class="sxs-lookup"><span data-stu-id="9a011-114">The table to retrieve information about.</span></span>

<!-- end list -->

  - <span data-ttu-id="9a011-115">result</span><span class="sxs-lookup"><span data-stu-id="9a011-115">result</span></span>  
    <span data-ttu-id="9a011-116">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="9a011-116">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="9a011-117">取出的資訊。</span><span class="sxs-lookup"><span data-stu-id="9a011-117">Retrieved information.</span></span>

<!-- end list -->

  - <span data-ttu-id="9a011-118">infoLevel</span><span class="sxs-lookup"><span data-stu-id="9a011-118">infoLevel</span></span>  
    <span data-ttu-id="9a011-119">類型： [Microsoft.Isam.Esent.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="9a011-119">Type: [Microsoft.Isam.Esent.Interop.JET_TblInfo](./jet-tblinfo-enumeration.md)</span></span>  
    
    <span data-ttu-id="9a011-120">要取出的資訊類型。</span><span class="sxs-lookup"><span data-stu-id="9a011-120">The type of information to retrieve.</span></span>

## <a name="remarks"></a><span data-ttu-id="9a011-121">備註</span><span class="sxs-lookup"><span data-stu-id="9a011-121">Remarks</span></span>

<span data-ttu-id="9a011-122">這個多載會搭配 [Name](./jet-tblinfo-enumeration.md) 和 [TemplateTableName](./jet-tblinfo-enumeration.md)使用。</span><span class="sxs-lookup"><span data-stu-id="9a011-122">This overload is used with [Name](./jet-tblinfo-enumeration.md) and [TemplateTableName](./jet-tblinfo-enumeration.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="9a011-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a011-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9a011-124">參考</span><span class="sxs-lookup"><span data-stu-id="9a011-124">Reference</span></span>

[<span data-ttu-id="9a011-125">Api 類別</span><span class="sxs-lookup"><span data-stu-id="9a011-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9a011-126">Api 成員</span><span class="sxs-lookup"><span data-stu-id="9a011-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9a011-127">JetGetTableInfo 多載</span><span class="sxs-lookup"><span data-stu-id="9a011-127">JetGetTableInfo overload</span></span>](./api.jetgettableinfo-method.md)

[<span data-ttu-id="9a011-128">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="9a011-128">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
