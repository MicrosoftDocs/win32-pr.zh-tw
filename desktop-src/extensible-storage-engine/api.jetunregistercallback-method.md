---
description: 深入瞭解： JetUnregisterCallback 方法
title: JetUnregisterCallback 方法
TOCTitle: 'JetUnregisterCallback method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetUnregisterCallback(Microsoft.Isam.Esent.Interop.JET_SESID,Microsoft.Isam.Esent.Interop.JET_TABLEID,Microsoft.Isam.Esent.Interop.JET_cbtyp,Microsoft.Isam.Esent.Interop.JET_HANDLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetunregistercallback(v=EXCHG.10)
ms:contentKeyID: 55100812
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetUnregisterCallback
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetUnregisterCallback
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: db3f4a26803242f4ac9d3cb1de09805f9dd57012
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974099"
---
# <a name="apijetunregistercallback-method"></a><span data-ttu-id="1b26d-103">JetUnregisterCallback 方法</span><span class="sxs-lookup"><span data-stu-id="1b26d-103">Api.JetUnregisterCallback method</span></span>

<span data-ttu-id="1b26d-104">設定 database engine，以停止在先前透過 [JetRegisterCallback (JET_SESID、JET_TABLEID、JET_cbtyp、JET_CALLBACK、IntPtr、JET_HANDLE) ](./api.jetregistercallback-method.md)要求的情況下發出通知至應用程式。</span><span class="sxs-lookup"><span data-stu-id="1b26d-104">Configures the database engine to stop issuing notifications to the application as previously requested through [JetRegisterCallback(JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)](./api.jetregistercallback-method.md).</span></span>

<span data-ttu-id="1b26d-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="1b26d-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="1b26d-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="1b26d-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="1b26d-107">語法</span><span class="sxs-lookup"><span data-stu-id="1b26d-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetUnregisterCallback ( _
    sesid As JET_SESID, _
    tableid As JET_TABLEID, _
    cbtyp As JET_cbtyp, _
    callbackId As JET_HANDLE _
)
'Usage
Dim sesid As JET_SESID
Dim tableid As JET_TABLEID
Dim cbtyp As JET_cbtyp
Dim callbackId As JET_HANDLEApi.JetUnregisterCallback(sesid, _
    tableid, cbtyp, callbackId)
```

``` csharp
public static void JetUnregisterCallback(
    JET_SESID sesid,
    JET_TABLEID tableid,
    JET_cbtyp cbtyp,
    JET_HANDLE callbackId
)
```

#### <a name="parameters"></a><span data-ttu-id="1b26d-108">參數</span><span class="sxs-lookup"><span data-stu-id="1b26d-108">Parameters</span></span>

  - <span data-ttu-id="1b26d-109">sesid</span><span class="sxs-lookup"><span data-stu-id="1b26d-109">sesid</span></span>  
    <span data-ttu-id="1b26d-110">類型： [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1b26d-110">Type: [Microsoft.Isam.Esent.Interop.JET_SESID](./jet-sesid-structure.md)</span></span>  
    
    <span data-ttu-id="1b26d-111">要使用的會話。</span><span class="sxs-lookup"><span data-stu-id="1b26d-111">The session to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="1b26d-112">tableid</span><span class="sxs-lookup"><span data-stu-id="1b26d-112">tableid</span></span>  
    <span data-ttu-id="1b26d-113">類型： [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1b26d-113">Type: [Microsoft.Isam.Esent.Interop.JET_TABLEID](./jet-tableid-structure.md)</span></span>  
    
    <span data-ttu-id="1b26d-114">在資料表上開啟回呼應該註冊的資料指標。</span><span class="sxs-lookup"><span data-stu-id="1b26d-114">A cursor opened on the table that the callback should be registered on.</span></span>

<!-- end list -->

  - <span data-ttu-id="1b26d-115">cbtyp</span><span class="sxs-lookup"><span data-stu-id="1b26d-115">cbtyp</span></span>  
    <span data-ttu-id="1b26d-116">類型： [Microsoft.Isam.Esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span><span class="sxs-lookup"><span data-stu-id="1b26d-116">Type: [Microsoft.Isam.Esent.Interop.JET_cbtyp](./jet-cbtyp-enumeration.md)</span></span>  
    
    <span data-ttu-id="1b26d-117">應用程式不再希望接收通知的回呼原因。</span><span class="sxs-lookup"><span data-stu-id="1b26d-117">The callback reasons for which the application no longer wishes to receive notifications.</span></span>

<!-- end list -->

  - <span data-ttu-id="1b26d-118">callbackId</span><span class="sxs-lookup"><span data-stu-id="1b26d-118">callbackId</span></span>  
    <span data-ttu-id="1b26d-119">類型： [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="1b26d-119">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="1b26d-120">[JetRegisterCallback (JET_SESID、JET_TABLEID、JET_cbtyp、JET_CALLBACK、IntPtr、JET_HANDLE) ](./api.jetregistercallback-method.md)所傳回之已註冊回呼的控制碼。</span><span class="sxs-lookup"><span data-stu-id="1b26d-120">The handle of the registered callback that was returned by [JetRegisterCallback(JET_SESID, JET_TABLEID, JET_cbtyp, JET_CALLBACK, IntPtr, JET_HANDLE)](./api.jetregistercallback-method.md).</span></span>

## <a name="see-also"></a><span data-ttu-id="1b26d-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="1b26d-121">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="1b26d-122">參考</span><span class="sxs-lookup"><span data-stu-id="1b26d-122">Reference</span></span>

[<span data-ttu-id="1b26d-123">Api 類別</span><span class="sxs-lookup"><span data-stu-id="1b26d-123">Api class</span></span>](./api-class.md)

[<span data-ttu-id="1b26d-124">Api 成員</span><span class="sxs-lookup"><span data-stu-id="1b26d-124">Api members</span></span>](./api-members.md)

[<span data-ttu-id="1b26d-125">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="1b26d-125">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
