---
description: 深入瞭解： JetGetVersion 方法
title: JetGetVersion 方法
TOCTitle: 'JetGetVersion method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetVersion(Microsoft.Isam.Esent.Interop.JET_SESID,System.UInt32@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetversion(v=EXCHG.10)
ms:contentKeyID: 55100744
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetGetVersion
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetVersion
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8860b21ec2b5db3841b866aa9c1c2cc7cff300aa
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512380"
---
# <a name="apijetgetversion-method"></a><span data-ttu-id="9a2cb-103">JetGetVersion 方法</span><span class="sxs-lookup"><span data-stu-id="9a2cb-103">Api.JetGetVersion method</span></span>

<span data-ttu-id="9a2cb-104">抓取資料庫引擎的版本。</span><span class="sxs-lookup"><span data-stu-id="9a2cb-104">Retrieves the version of the database engine.</span></span>

<span data-ttu-id="9a2cb-105">此 API 不符合 CLS 規範。</span><span class="sxs-lookup"><span data-stu-id="9a2cb-105">This API is not CLS-compliant.</span></span> 

<span data-ttu-id="9a2cb-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="9a2cb-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="9a2cb-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="9a2cb-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="9a2cb-108">語法</span><span class="sxs-lookup"><span data-stu-id="9a2cb-108">Syntax</span></span>

``` vb
'Declaration
<CLSCompliantAttribute(False)> _
Public Shared Sub JetGetVersion ( _
    sesid As JET_SESID, _
    <OutAttribute> ByRef version As UInteger _
)
'Usage
Dim sesid As JET_SESID
Dim version As UIntegerApi.JetGetVersion(sesid, version)
```

``` csharp
[CLSCompliantAttribute(false)]
public static void JetGetVersion(
    JET_SESID sesid,
    out uint version
)
```

#### <a name="parameters"></a><span data-ttu-id="9a2cb-109">參數</span><span class="sxs-lookup"><span data-stu-id="9a2cb-109">Parameters</span></span>

  - <span data-ttu-id="9a2cb-110">sesid</span><span class="sxs-lookup"><span data-stu-id="9a2cb-110">sesid</span></span>  
    <span data-ttu-id="9a2cb-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="9a2cb-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="9a2cb-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="9a2cb-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="9a2cb-113">version</span><span class="sxs-lookup"><span data-stu-id="9a2cb-113">version</span></span>  
    <span data-ttu-id="9a2cb-114">類型： [system.object](/dotnet/api/system.uint32)</span><span class="sxs-lookup"><span data-stu-id="9a2cb-114">Type: [System.UInt32](/dotnet/api/system.uint32)</span></span>  
    
    <span data-ttu-id="9a2cb-115">傳回資料庫引擎的版本號碼。</span><span class="sxs-lookup"><span data-stu-id="9a2cb-115">Returns the version number of the database engine.</span></span>

## <a name="see-also"></a><span data-ttu-id="9a2cb-116">另請參閱</span><span class="sxs-lookup"><span data-stu-id="9a2cb-116">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="9a2cb-117">參考</span><span class="sxs-lookup"><span data-stu-id="9a2cb-117">Reference</span></span>

[<span data-ttu-id="9a2cb-118">Api 類別</span><span class="sxs-lookup"><span data-stu-id="9a2cb-118">Api class</span></span>](./api-class.md)

[<span data-ttu-id="9a2cb-119">Api 成員</span><span class="sxs-lookup"><span data-stu-id="9a2cb-119">Api members</span></span>](./api-members.md)

[<span data-ttu-id="9a2cb-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="9a2cb-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
