---
description: 深入瞭解： JetRegisterCallback 方法
title: JetRegisterCallback 方法
TOCTitle: 'JetRegisterCallback method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_cbtyp,Microsoft.Isam.Esent.Interop.JET_CALLBACK,System.IntPtr,Microsoft.Isam.Esent.Interop.JET_HANDLE@)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetregistercallback(v=EXCHG.10)
ms:contentKeyID: 55100784
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetRegisterCallback
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 97ba91d776575285d71e0ad4ec8d94eeb10a743a
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106997966"
---
# <a name="apijetregistercallback-method"></a><span data-ttu-id="a4b95-103">JetRegisterCallback 方法</span><span class="sxs-lookup"><span data-stu-id="a4b95-103">Api.JetRegisterCallback method</span></span>

<span data-ttu-id="a4b95-104">允許應用程式將資料庫引擎設定為對應用程式發出特定事件的通知。</span><span class="sxs-lookup"><span data-stu-id="a4b95-104">Allows the application to configure the database engine to issue notifications to the application for specific events.</span></span> <span data-ttu-id="a4b95-105">這些通知會與特定的資料表相關聯，而且只有在包含該資料表的實例使用 [JetTerm (JET_INSTANCE) ](./api.jetterm-method.md)關閉時，才會維持有效狀態。</span><span class="sxs-lookup"><span data-stu-id="a4b95-105">These notifications are associated with a specific table and remain in effect only until the instance containing the table is shut down using [JetTerm(JET_INSTANCE)](./api.jetterm-method.md).</span></span>

<span data-ttu-id="a4b95-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="a4b95-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="a4b95-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="a4b95-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="a4b95-108">語法</span><span class="sxs-lookup"><span data-stu-id="a4b95-108">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetRegisterCallback ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    cbtyp As JET_cbtyp, _
    callback As JET_CALLBACK, _
    context As IntPtr, _
    <OutAttribute> ByRef callbackId As JET_HANDLE _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim cbtyp As JET_cbtyp
Dim callback As JET_CALLBACK
Dim context As IntPtr
Dim callbackId As JET_HANDLEApi.JetRegisterCallback(sesid, _
    tableid, cbtyp, callback, context, _
    callbackId)
```

``` csharp
public static void JetRegisterCallback(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_cbtyp cbtyp,
    JET_CALLBACK callback,
    IntPtr context,
    out JET_HANDLE callbackId
)
```

#### <a name="parameters"></a><span data-ttu-id="a4b95-109">參數</span><span class="sxs-lookup"><span data-stu-id="a4b95-109">Parameters</span></span>

  - <span data-ttu-id="a4b95-110">sesid</span><span class="sxs-lookup"><span data-stu-id="a4b95-110">sesid</span></span>  
    <span data-ttu-id="a4b95-111">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a4b95-111">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="a4b95-112">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="a4b95-112">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="a4b95-113">tableid</span><span class="sxs-lookup"><span data-stu-id="a4b95-113">tableid</span></span>  
    <span data-ttu-id="a4b95-114">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a4b95-114">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="a4b95-115">在資料表上開啟回呼應該註冊的資料指標。</span><span class="sxs-lookup"><span data-stu-id="a4b95-115">A cursor opened on the table that the callback should be registered on.</span></span>

<!-- end list -->

  - <span data-ttu-id="a4b95-116">cbtyp</span><span class="sxs-lookup"><span data-stu-id="a4b95-116">cbtyp</span></span>  
    <span data-ttu-id="a4b95-117">類型： [Microsoft.Isam.Esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="a4b95-117">Type: [Microsoft.Isam.Esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span></span>  
    
    <span data-ttu-id="a4b95-118">應用程式希望接收通知的回呼原因。</span><span class="sxs-lookup"><span data-stu-id="a4b95-118">The callback reasons for which the application wishes to receive notifications.</span></span>

<!-- end list -->

  - <span data-ttu-id="a4b95-119">回撥</span><span class="sxs-lookup"><span data-stu-id="a4b95-119">callback</span></span>  
    <span data-ttu-id="a4b95-120">類型： [Microsoft.Isam.Esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span><span class="sxs-lookup"><span data-stu-id="a4b95-120">Type: [Microsoft.Isam.Esent.Interop.JET_CALLBACK](./jet-callback-delegate.md)</span></span>  
    
    <span data-ttu-id="a4b95-121">回呼函式。</span><span class="sxs-lookup"><span data-stu-id="a4b95-121">The callback function.</span></span>

<!-- end list -->

  - <span data-ttu-id="a4b95-122">內容</span><span class="sxs-lookup"><span data-stu-id="a4b95-122">context</span></span>  
    <span data-ttu-id="a4b95-123">類型： [system.object](/dotnet/api/system.intptr)</span><span class="sxs-lookup"><span data-stu-id="a4b95-123">Type: [System.IntPtr](/dotnet/api/system.intptr)</span></span>  
    
    <span data-ttu-id="a4b95-124">將提供給回呼的內容。</span><span class="sxs-lookup"><span data-stu-id="a4b95-124">A context that will be given to the callback.</span></span>

<!-- end list -->

  - <span data-ttu-id="a4b95-125">callbackId</span><span class="sxs-lookup"><span data-stu-id="a4b95-125">callbackId</span></span>  
    <span data-ttu-id="a4b95-126">類型： [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="a4b95-126">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="a4b95-127">使用 [JetUnregisterCallback (JET_SESID、JET_TABLEID、JET_cbtyp JET_HANDLE) ](./api.jetunregistercallback-method.md)，稍後可用來取消註冊指定回呼函數的控制碼。</span><span class="sxs-lookup"><span data-stu-id="a4b95-127">A handle that can later be used to cancel the registration of the given callback function using [JetUnregisterCallback(JET_SESID, JET_TABLEID, JET_cbtyp, JET_HANDLE)](./api.jetunregistercallback-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="a4b95-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a4b95-128">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="a4b95-129">參考</span><span class="sxs-lookup"><span data-stu-id="a4b95-129">Reference</span></span>

[<span data-ttu-id="a4b95-130">Api 類別</span><span class="sxs-lookup"><span data-stu-id="a4b95-130">Api class</span></span>](./api-class.md)

[<span data-ttu-id="a4b95-131">Api 成員</span><span class="sxs-lookup"><span data-stu-id="a4b95-131">Api members</span></span>](./api-members.md)

[<span data-ttu-id="a4b95-132">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="a4b95-132">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
