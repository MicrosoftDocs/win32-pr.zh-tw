---
description: '深入瞭解： JetSetSystemParameter 方法 (JET_INSTANCE、JET_SESID、JET_param、IntPtr、String) '
title: 'JetSetSystemParameter 方法 (JET_INSTANCE、JET_SESID、JET_param、IntPtr、String) '
TOCTitle: JetSetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,System.IntPtr,System.String)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetsetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100822
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetSetSystemParameter
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 72a92ea3d6b6d4b828e409cd08b896f54c4aa053
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104194024"
---
# <a name="apijetsetsystemparameter-method-jet_instance-jet_sesid-jet_param-intptr-string"></a><span data-ttu-id="e3e1e-103">JetSetSystemParameter 方法 (JET_INSTANCE、JET_SESID、JET_param、IntPtr、String) </span><span class="sxs-lookup"><span data-stu-id="e3e1e-103">Api.JetSetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String)</span></span>

<span data-ttu-id="e3e1e-104">設定資料庫設定選項。</span><span class="sxs-lookup"><span data-stu-id="e3e1e-104">Sets database configuration options.</span></span>

<span data-ttu-id="e3e1e-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e3e1e-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e3e1e-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e3e1e-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e3e1e-107">語法</span><span class="sxs-lookup"><span data-stu-id="e3e1e-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetSetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    paramValue As IntPtr, _
    paramString As String _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As IntPtr
Dim paramString As String
Dim returnValue As JET_wrn

returnValue = Api.JetSetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString)
```

``` csharp
public static JET_wrn JetSetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    IntPtr paramValue,
    string paramString
)
```

#### <a name="parameters"></a><span data-ttu-id="e3e1e-108">參數</span><span class="sxs-lookup"><span data-stu-id="e3e1e-108">Parameters</span></span>

  - <span data-ttu-id="e3e1e-109">instance</span><span class="sxs-lookup"><span data-stu-id="e3e1e-109">instance</span></span>  
    <span data-ttu-id="e3e1e-110">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e3e1e-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="e3e1e-111">要在其上設定選項的實例，或設定 [Nil](./jet-instance.nil-property.md) 來設定所有實例的選項。</span><span class="sxs-lookup"><span data-stu-id="e3e1e-111">The instance to set the option on or [Nil](./jet-instance.nil-property.md) to set the option on all instances.</span></span>

<!-- end list -->

  - <span data-ttu-id="e3e1e-112">sesid</span><span class="sxs-lookup"><span data-stu-id="e3e1e-112">sesid</span></span>  
    <span data-ttu-id="e3e1e-113">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="e3e1e-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="e3e1e-114">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="e3e1e-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="e3e1e-115">paramid</span><span class="sxs-lookup"><span data-stu-id="e3e1e-115">paramid</span></span>  
    <span data-ttu-id="e3e1e-116">類型： [Microsoft.Isam.Esent.Interop.JET_param](./jet-param-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e3e1e-116">Type: [Microsoft.Isam.Esent.Interop.JET_param](./jet-param-enumeration.md)</span></span>  
    
    <span data-ttu-id="e3e1e-117">要設定的參數。</span><span class="sxs-lookup"><span data-stu-id="e3e1e-117">The parameter to set.</span></span>

<!-- end list -->

  - <span data-ttu-id="e3e1e-118">paramValue</span><span class="sxs-lookup"><span data-stu-id="e3e1e-118">paramValue</span></span>  
    <span data-ttu-id="e3e1e-119">類型： [system.object](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="e3e1e-119">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="e3e1e-120">如果參數是整數類型，則為要設定的參數值。</span><span class="sxs-lookup"><span data-stu-id="e3e1e-120">The value of the parameter to set, if the parameter is an integer type.</span></span>

<!-- end list -->

  - <span data-ttu-id="e3e1e-121">paramString</span><span class="sxs-lookup"><span data-stu-id="e3e1e-121">paramString</span></span>  
    <span data-ttu-id="e3e1e-122">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="e3e1e-122">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="e3e1e-123">如果參數是字串類型，則為要設定的參數值。</span><span class="sxs-lookup"><span data-stu-id="e3e1e-123">The value of the parameter to set, if the parameter is a string type.</span></span>

#### <a name="return-value"></a><span data-ttu-id="e3e1e-124">傳回值</span><span class="sxs-lookup"><span data-stu-id="e3e1e-124">Return value</span></span>

<span data-ttu-id="e3e1e-125">類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="e3e1e-125">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="e3e1e-126">ESENT 警告碼。</span><span class="sxs-lookup"><span data-stu-id="e3e1e-126">An ESENT warning code.</span></span>  

## <a name="see-also"></a><span data-ttu-id="e3e1e-127">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e3e1e-127">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e3e1e-128">參考</span><span class="sxs-lookup"><span data-stu-id="e3e1e-128">Reference</span></span>

[<span data-ttu-id="e3e1e-129">Api 類別</span><span class="sxs-lookup"><span data-stu-id="e3e1e-129">Api class</span></span>](./api-class.md)

[<span data-ttu-id="e3e1e-130">Api 成員</span><span class="sxs-lookup"><span data-stu-id="e3e1e-130">Api members</span></span>](./api-members.md)

[<span data-ttu-id="e3e1e-131">JetSetSystemParameter 多載</span><span class="sxs-lookup"><span data-stu-id="e3e1e-131">JetSetSystemParameter overload</span></span>](./api.jetsetsystemparameter-method.md)

[<span data-ttu-id="e3e1e-132">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e3e1e-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
