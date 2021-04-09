---
description: '深入瞭解： JetGetSystemParameter 方法 (JET_INSTANCE、JET_SESID、JET_param、IntPtr、String、Int32) '
title: 'JetGetSystemParameter 方法 (JET_INSTANCE、JET_SESID、JET_param、IntPtr、String、Int32) '
TOCTitle: JetGetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String, Int32)
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_param,System.IntPtr@,System.String@,System.Int32)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetgetsystemparameter(v=EXCHG.10)
ms:contentKeyID: 55100731
ms.date: 07/30/2014
ms.topic: reference
dev_langs:
- vb
- csharp
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetGetSystemParameter
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 25e8430931cbf45c84d65fb68ae877ed96e7cea8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103847845"
---
# <a name="apijetgetsystemparameter-method-jet_instance-jet_sesid-jet_param-intptr-string-int32"></a><span data-ttu-id="7c3ed-103">JetGetSystemParameter 方法 (JET_INSTANCE、JET_SESID、JET_param、IntPtr、String、Int32) </span><span class="sxs-lookup"><span data-stu-id="7c3ed-103">Api.JetGetSystemParameter method (JET_INSTANCE, JET_SESID, JET_param, IntPtr, String, Int32)</span></span>

<span data-ttu-id="7c3ed-104">取得資料庫設定選項。</span><span class="sxs-lookup"><span data-stu-id="7c3ed-104">Gets database configuration options.</span></span>

<span data-ttu-id="7c3ed-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="7c3ed-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="7c3ed-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="7c3ed-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="7c3ed-107">語法</span><span class="sxs-lookup"><span data-stu-id="7c3ed-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Function JetGetSystemParameter ( _
    instance As JET_INSTANCE, _
    sesid As JET_SESID, _
    paramid As JET_param, _
    ByRef paramValue As IntPtr, _
    <OutAttribute> ByRef paramString As String, _
    maxParam As Integer _
) As JET_wrn
'Usage
Dim instance As JET_INSTANCE
Dim sesid As JET_SESID
Dim paramid As JET_param
Dim paramValue As IntPtr
Dim paramString As String
Dim maxParam As Integer
Dim returnValue As JET_wrn

returnValue = Api.JetGetSystemParameter(instance, _
    sesid, paramid, paramValue, paramString, _
    maxParam)
```

``` csharp
public static JET_wrn JetGetSystemParameter(
    JET_INSTANCE instance,
    JET_SESID sesid,
    JET_param paramid,
    ref IntPtr paramValue,
    out string paramString,
    int maxParam
)
```

#### <a name="parameters"></a><span data-ttu-id="7c3ed-108">參數</span><span class="sxs-lookup"><span data-stu-id="7c3ed-108">Parameters</span></span>

  - <span data-ttu-id="7c3ed-109">instance</span><span class="sxs-lookup"><span data-stu-id="7c3ed-109">instance</span></span>  
    <span data-ttu-id="7c3ed-110">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7c3ed-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="7c3ed-111">要從中取出選項的實例。</span><span class="sxs-lookup"><span data-stu-id="7c3ed-111">The instance to retrieve the options from.</span></span>

<!-- end list -->

  - <span data-ttu-id="7c3ed-112">sesid</span><span class="sxs-lookup"><span data-stu-id="7c3ed-112">sesid</span></span>  
    <span data-ttu-id="7c3ed-113">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="7c3ed-113">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="7c3ed-114">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="7c3ed-114">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="7c3ed-115">paramid</span><span class="sxs-lookup"><span data-stu-id="7c3ed-115">paramid</span></span>  
    <span data-ttu-id="7c3ed-116">類型： [Microsoft.Isam.Esent.Interop.JET_param](./jet-param-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7c3ed-116">Type: [Microsoft.Isam.Esent.Interop.JET_param](./jet-param-enumeration.md)</span></span>  
    
    <span data-ttu-id="7c3ed-117">要取得的參數。</span><span class="sxs-lookup"><span data-stu-id="7c3ed-117">The parameter to get.</span></span>

<!-- end list -->

  - <span data-ttu-id="7c3ed-118">paramValue</span><span class="sxs-lookup"><span data-stu-id="7c3ed-118">paramValue</span></span>  
    <span data-ttu-id="7c3ed-119">類型： [system.object](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="7c3ed-119">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="7c3ed-120">如果值是整數，則傳回參數的值。</span><span class="sxs-lookup"><span data-stu-id="7c3ed-120">Returns the value of the parameter, if the value is an integer.</span></span>

<!-- end list -->

  - <span data-ttu-id="7c3ed-121">paramString</span><span class="sxs-lookup"><span data-stu-id="7c3ed-121">paramString</span></span>  
    <span data-ttu-id="7c3ed-122">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="7c3ed-122">Type: [System.String](/dotnet/api/system.string)</span></span>  
    
    <span data-ttu-id="7c3ed-123">如果值為字串，則傳回參數的值。</span><span class="sxs-lookup"><span data-stu-id="7c3ed-123">Returns the value of the parameter, if the value is a string.</span></span>

<!-- end list -->

  - <span data-ttu-id="7c3ed-124">maxParam</span><span class="sxs-lookup"><span data-stu-id="7c3ed-124">maxParam</span></span>  
    <span data-ttu-id="7c3ed-125">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="7c3ed-125">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  
    
    <span data-ttu-id="7c3ed-126">參數字串的大小上限。</span><span class="sxs-lookup"><span data-stu-id="7c3ed-126">The maximum size of the parameter string.</span></span>

#### <a name="return-value"></a><span data-ttu-id="7c3ed-127">傳回值</span><span class="sxs-lookup"><span data-stu-id="7c3ed-127">Return value</span></span>

<span data-ttu-id="7c3ed-128">類型： [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="7c3ed-128">Type: [Microsoft.Isam.Esent.Interop.JET_wrn](./jet-wrn-enumeration.md)</span></span>  
<span data-ttu-id="7c3ed-129">ESENT 警告碼。</span><span class="sxs-lookup"><span data-stu-id="7c3ed-129">An ESENT warning code.</span></span>  

## <a name="remarks"></a><span data-ttu-id="7c3ed-130">備註</span><span class="sxs-lookup"><span data-stu-id="7c3ed-130">Remarks</span></span>

<span data-ttu-id="7c3ed-131">[ErrorToString](./jet-param-enumeration.md) 會傳入 paramValue 中的錯誤號碼，這就是為什麼它是 ref 參數，而不是 out 參數。</span><span class="sxs-lookup"><span data-stu-id="7c3ed-131">[ErrorToString](./jet-param-enumeration.md) passes in the error number in the paramValue, which is why it is a ref parameter and not an out parameter.</span></span>

## <a name="see-also"></a><span data-ttu-id="7c3ed-132">另請參閱</span><span class="sxs-lookup"><span data-stu-id="7c3ed-132">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="7c3ed-133">參考</span><span class="sxs-lookup"><span data-stu-id="7c3ed-133">Reference</span></span>

[<span data-ttu-id="7c3ed-134">Api 類別</span><span class="sxs-lookup"><span data-stu-id="7c3ed-134">Api class</span></span>](./api-class.md)

[<span data-ttu-id="7c3ed-135">Api 成員</span><span class="sxs-lookup"><span data-stu-id="7c3ed-135">Api members</span></span>](./api-members.md)

[<span data-ttu-id="7c3ed-136">JetGetSystemParameter 多載</span><span class="sxs-lookup"><span data-stu-id="7c3ed-136">JetGetSystemParameter overload</span></span>](./api.jetgetsystemparameter-method.md)

[<span data-ttu-id="7c3ed-137">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="7c3ed-137">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
