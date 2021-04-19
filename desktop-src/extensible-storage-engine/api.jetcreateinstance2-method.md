---
description: 深入瞭解： JetCreateInstance2 方法
title: JetCreateInstance2 方法
TOCTitle: 'JetCreateInstance2 method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2(Microsoft.Isam.Esent.Interop.JET_INSTANCE@,System.String,System.String,Microsoft.Isam.Esent.Interop.CreateInstanceGrbit)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetcreateinstance2(v=EXCHG.10)
ms:contentKeyID: 55100675
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCreateInstance2
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 4d21974d5c3bd5ca6dfbab2ac493d19b202ca6ef
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973435"
---
# <a name="apijetcreateinstance2-method"></a><span data-ttu-id="8885e-103">JetCreateInstance2 方法</span><span class="sxs-lookup"><span data-stu-id="8885e-103">Api.JetCreateInstance2 method</span></span>

<span data-ttu-id="8885e-104">配置 database engine 的新實例，以在單一進程中使用，並指定顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="8885e-104">Allocate a new instance of the database engine for use in a single process, with a display name specified.</span></span>

<span data-ttu-id="8885e-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="8885e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="8885e-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="8885e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="8885e-107">語法</span><span class="sxs-lookup"><span data-stu-id="8885e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCreateInstance2 ( _
    <OutAttribute> ByRef instance As JET_INSTANCE, _
    name As String, _
    displayName As String, _
    grbit As CreateInstanceGrbit _
)
'Usage
Dim instance As JET_INSTANCE
Dim name As String
Dim displayName As String
Dim grbit As CreateInstanceGrbitApi.JetCreateInstance2(instance, _
    name, displayName, grbit)
```

``` csharp
public static void JetCreateInstance2(
    out JET_INSTANCE instance,
    string name,
    string displayName,
    CreateInstanceGrbit grbit
)
```

#### <a name="parameters"></a><span data-ttu-id="8885e-108">參數</span><span class="sxs-lookup"><span data-stu-id="8885e-108">Parameters</span></span>

  - <span data-ttu-id="8885e-109">instance</span><span class="sxs-lookup"><span data-stu-id="8885e-109">instance</span></span>  
    <span data-ttu-id="8885e-110">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="8885e-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="8885e-111">傳回新建立的實例。</span><span class="sxs-lookup"><span data-stu-id="8885e-111">Returns the newly create instance.</span></span>

<!-- end list -->

  - <span data-ttu-id="8885e-112">NAME</span><span class="sxs-lookup"><span data-stu-id="8885e-112">name</span></span>  
    <span data-ttu-id="8885e-113">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="8885e-113">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="8885e-114">指定要建立之實例的唯一字串識別碼。</span><span class="sxs-lookup"><span data-stu-id="8885e-114">Specifies a unique string identifier for the instance to be created.</span></span> <span data-ttu-id="8885e-115">這個字串在主控資料庫引擎的指定進程內必須是唯一的。</span><span class="sxs-lookup"><span data-stu-id="8885e-115">This string must be unique within a given process hosting the database engine.</span></span>

<!-- end list -->

  - <span data-ttu-id="8885e-116">displayName</span><span class="sxs-lookup"><span data-stu-id="8885e-116">displayName</span></span>  
    <span data-ttu-id="8885e-117">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="8885e-117">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="8885e-118">要建立之實例的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="8885e-118">A display name for the instance to be created.</span></span> <span data-ttu-id="8885e-119">這將用於 eventlog 專案中。</span><span class="sxs-lookup"><span data-stu-id="8885e-119">This will be used in eventlog entries.</span></span>

<!-- end list -->

  - <span data-ttu-id="8885e-120">grbit</span><span class="sxs-lookup"><span data-stu-id="8885e-120">grbit</span></span>  
    <span data-ttu-id="8885e-121">型別： [CreateInstanceGrbit](./createinstancegrbit-enumeration.md) 。</span><span class="sxs-lookup"><span data-stu-id="8885e-121">Type: [Microsoft.Isam.Esent.Interop.CreateInstanceGrbit](./createinstancegrbit-enumeration.md)</span></span>  
    
    <span data-ttu-id="8885e-122">建立時的選項。</span><span class="sxs-lookup"><span data-stu-id="8885e-122">Creation options.</span></span>

## <a name="see-also"></a><span data-ttu-id="8885e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="8885e-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="8885e-124">參考</span><span class="sxs-lookup"><span data-stu-id="8885e-124">Reference</span></span>

[<span data-ttu-id="8885e-125">Api 類別</span><span class="sxs-lookup"><span data-stu-id="8885e-125">Api class</span></span>](./api-class.md)

[<span data-ttu-id="8885e-126">Api 成員</span><span class="sxs-lookup"><span data-stu-id="8885e-126">Api members</span></span>](./api-members.md)

[<span data-ttu-id="8885e-127">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="8885e-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
