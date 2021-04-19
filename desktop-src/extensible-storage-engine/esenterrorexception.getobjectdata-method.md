---
description: 深入瞭解： EsentErrorException. GetObjectData 方法
title: EsentErrorException. GetObjectData 方法
TOCTitle: 'GetObjectData method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData(System.Runtime.Serialization.SerializationInfo,System.Runtime.Serialization.StreamingContext)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esenterrorexception.getobjectdata(v=EXCHG.10)
ms:contentKeyID: 55101432
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentErrorException.GetObjectData
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 86d951828da0f8bb8eb3ada13bb67b02e801709e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106981221"
---
# <a name="esenterrorexceptiongetobjectdata-method"></a><span data-ttu-id="cf7dc-103">EsentErrorException. GetObjectData 方法</span><span class="sxs-lookup"><span data-stu-id="cf7dc-103">EsentErrorException.GetObjectData method</span></span>

<span data-ttu-id="cf7dc-104">在衍生類別中覆寫時，使用例外狀況的相關資訊設定 [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) 。</span><span class="sxs-lookup"><span data-stu-id="cf7dc-104">When overridden in a derived class, sets the [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) with information about the exception.</span></span>

<span data-ttu-id="cf7dc-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cf7dc-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cf7dc-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="cf7dc-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cf7dc-107">語法</span><span class="sxs-lookup"><span data-stu-id="cf7dc-107">Syntax</span></span>

``` vb
'Declaration
Public Overrides Sub GetObjectData ( _
    info As SerializationInfo, _
    context As StreamingContext _
)
'Usage
Dim instance As EsentErrorException
Dim info As SerializationInfo
Dim context As StreamingContext

instance.GetObjectData(info, context)
```

``` csharp
public override void GetObjectData(
    SerializationInfo info,
    StreamingContext context
)
```

#### <a name="parameters"></a><span data-ttu-id="cf7dc-108">參數</span><span class="sxs-lookup"><span data-stu-id="cf7dc-108">Parameters</span></span>

  - <span data-ttu-id="cf7dc-109">info</span><span class="sxs-lookup"><span data-stu-id="cf7dc-109">info</span></span>  
    <span data-ttu-id="cf7dc-110">類型： [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) 。</span><span class="sxs-lookup"><span data-stu-id="cf7dc-110">Type: [System.Runtime.Serialization.SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo)</span></span>  
    
    <span data-ttu-id="cf7dc-111">[SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) ，其中保存所擲回之例外狀況的相關序列化物件資料。</span><span class="sxs-lookup"><span data-stu-id="cf7dc-111">The [SerializationInfo](/dotnet/api/system.runtime.serialization.serializationinfo) that holds the serialized object data about the exception being thrown.</span></span>

<!-- end list -->

  - <span data-ttu-id="cf7dc-112">內容</span><span class="sxs-lookup"><span data-stu-id="cf7dc-112">context</span></span>  
    <span data-ttu-id="cf7dc-113">類型： [StreamingCoNtext](/dotnet/api/system.runtime.serialization.streamingcontext) 。</span><span class="sxs-lookup"><span data-stu-id="cf7dc-113">Type: [System.Runtime.Serialization.StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext)</span></span>  
    
    <span data-ttu-id="cf7dc-114">[StreamingCoNtext](/dotnet/api/system.runtime.serialization.streamingcontext) ，其中包含來源或目的地的相關內容資訊。</span><span class="sxs-lookup"><span data-stu-id="cf7dc-114">The [StreamingContext](/dotnet/api/system.runtime.serialization.streamingcontext) that contains contextual information about the source or destination.</span></span>

#### <a name="implements"></a><span data-ttu-id="cf7dc-115">實作</span><span class="sxs-lookup"><span data-stu-id="cf7dc-115">Implements</span></span>

[<span data-ttu-id="cf7dc-116">ISerializable GetObjectData (SerializationInfo、StreamingCoNtext) </span><span class="sxs-lookup"><span data-stu-id="cf7dc-116">ISerializable.GetObjectData(SerializationInfo, StreamingContext)</span></span>](/dotnet/api/system.runtime.serialization.iserializable.getobjectdata#System_Runtime_Serialization_ISerializable_GetObjectData_System_Runtime_Serialization_SerializationInfo_System_Runtime_Serialization_StreamingContext_)  
[<span data-ttu-id="cf7dc-117">_Exception 的 GetObjectData (SerializationInfo、StreamingCoNtext) </span><span class="sxs-lookup"><span data-stu-id="cf7dc-117">_Exception.GetObjectData(SerializationInfo, StreamingContext)</span></span>](/dotnet/api/system.runtime.interopservices._exception.getobjectdata#System_Runtime_InteropServices__Exception_GetObjectData_System_Runtime_Serialization_SerializationInfo_System_Runtime_Serialization_StreamingContext_)  

## <a name="exceptions"></a><span data-ttu-id="cf7dc-118">例外狀況</span><span class="sxs-lookup"><span data-stu-id="cf7dc-118">Exceptions</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf7dc-119">例外狀況</span><span class="sxs-lookup"><span data-stu-id="cf7dc-119">Exception</span></span></th>
<th><span data-ttu-id="cf7dc-120">條件</span><span class="sxs-lookup"><span data-stu-id="cf7dc-120">Condition</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf7dc-121"><a href="/dotnet/api/system.argumentnullexception">ArgumentNullException</a></span><span class="sxs-lookup"><span data-stu-id="cf7dc-121"><a href="/dotnet/api/system.argumentnullexception">ArgumentNullException</a></span></span></td>
<td><p><span data-ttu-id="cf7dc-122">info 參數是 null 參考 (在 Visual Basic 中為 Nothing)。</span><span class="sxs-lookup"><span data-stu-id="cf7dc-122">The info parameter is a null reference (Nothing in Visual Basic).</span></span></p></td>
</tr>
</tbody>
</table>


## <a name="see-also"></a><span data-ttu-id="cf7dc-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf7dc-123">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cf7dc-124">參考</span><span class="sxs-lookup"><span data-stu-id="cf7dc-124">Reference</span></span>

[<span data-ttu-id="cf7dc-125">EsentErrorException 類別</span><span class="sxs-lookup"><span data-stu-id="cf7dc-125">EsentErrorException class</span></span>](./esenterrorexception-class.md)

[<span data-ttu-id="cf7dc-126">EsentErrorException 成員</span><span class="sxs-lookup"><span data-stu-id="cf7dc-126">EsentErrorException members</span></span>](./esenterrorexception-members.md)

[<span data-ttu-id="cf7dc-127">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="cf7dc-127">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
