---
description: 深入瞭解： EsentOperationException 類別
title: EsentOperationException 類別
TOCTitle: EsentOperationException class
ms:assetid: T:Microsoft.Isam.Esent.Interop.EsentOperationException
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.esentoperationexception(v=EXCHG.10)
ms:contentKeyID: 55102414
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.EsentOperationException
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.EsentOperationException
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 314ae88a674f6bd59b0111d40ff3ca5a9eab8a2f
ms.sourcegitcommit: 3bdf30edb314e0fcd17dc4ddbc70e4ec7d3596e6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "106986005"
---
# <a name="esentoperationexception-class"></a><span data-ttu-id="b05dd-103">EsentOperationException 類別</span><span class="sxs-lookup"><span data-stu-id="b05dd-103">EsentOperationException class</span></span>

<span data-ttu-id="b05dd-104">作業例外狀況的基類。</span><span class="sxs-lookup"><span data-stu-id="b05dd-104">Base class for Operation exceptions.</span></span>

## <a name="inheritance-hierarchy"></a><span data-ttu-id="b05dd-105">繼承階層</span><span class="sxs-lookup"><span data-stu-id="b05dd-105">Inheritance hierarchy</span></span>

[<span data-ttu-id="b05dd-106">System.Object</span><span class="sxs-lookup"><span data-stu-id="b05dd-106">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b05dd-107">System.Exception</span><span class="sxs-lookup"><span data-stu-id="b05dd-107">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b05dd-108">EsentException。</span><span class="sxs-lookup"><span data-stu-id="b05dd-108">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b05dd-109">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="b05dd-109">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        <span data-ttu-id="b05dd-110">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="b05dd-110">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>  
          

<span data-ttu-id="b05dd-111">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="b05dd-111">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="b05dd-112">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="b05dd-112">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="b05dd-113">Syntax</span><span class="sxs-lookup"><span data-stu-id="b05dd-113">Syntax</span></span>

``` vb
'Declaration
<SerializableAttribute> _
Public MustInherit Class EsentOperationException _
    Inherits EsentErrorException
'Usage
Dim instance As EsentOperationException
```

``` csharp
[SerializableAttribute]
public abstract class EsentOperationException : EsentErrorException
```

## <a name="thread-safety"></a><span data-ttu-id="b05dd-114">執行緒安全</span><span class="sxs-lookup"><span data-stu-id="b05dd-114">Thread safety</span></span>

<span data-ttu-id="b05dd-115">這個類型的任何公用靜態 (Visual Basic 中的 Shared) 成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="b05dd-115">Any public static (Shared in Visual Basic) members of this type are thread safe.</span></span> <span data-ttu-id="b05dd-116">並非所有的執行個體成員都是安全執行緒。</span><span class="sxs-lookup"><span data-stu-id="b05dd-116">Any instance members are not guaranteed to be thread safe.</span></span>

## <a name="see-also"></a><span data-ttu-id="b05dd-117">另請參閱</span><span class="sxs-lookup"><span data-stu-id="b05dd-117">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="b05dd-118">參考</span><span class="sxs-lookup"><span data-stu-id="b05dd-118">Reference</span></span>

[<span data-ttu-id="b05dd-119">EsentOperationException 成員</span><span class="sxs-lookup"><span data-stu-id="b05dd-119">EsentOperationException members</span></span>](./esentoperationexception-members.md)

[<span data-ttu-id="b05dd-120">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="b05dd-120">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)

## <a name="derived-types"></a><span data-ttu-id="b05dd-121">衍生類型</span><span class="sxs-lookup"><span data-stu-id="b05dd-121">Derived types</span></span>

[<span data-ttu-id="b05dd-122">System.Object</span><span class="sxs-lookup"><span data-stu-id="b05dd-122">System.Object</span></span>](/dotnet/api/system.object)  
  [<span data-ttu-id="b05dd-123">System.Exception</span><span class="sxs-lookup"><span data-stu-id="b05dd-123">System.Exception</span></span>](/dotnet/api/system.exception)  
    [<span data-ttu-id="b05dd-124">EsentException。</span><span class="sxs-lookup"><span data-stu-id="b05dd-124">Microsoft.Isam.Esent.EsentException</span></span>](./esentexception-class.md)  
      [<span data-ttu-id="b05dd-125">EsentErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="b05dd-125">Microsoft.Isam.Esent.Interop.EsentErrorException</span></span>](./esenterrorexception-class.md)  
        <span data-ttu-id="b05dd-126">EsentOperationException （.）</span><span class="sxs-lookup"><span data-stu-id="b05dd-126">Microsoft.Isam.Esent.Interop.EsentOperationException</span></span>  
          [<span data-ttu-id="b05dd-127">EsentBackupAbortByServerException （.）</span><span class="sxs-lookup"><span data-stu-id="b05dd-127">Microsoft.Isam.Esent.Interop.EsentBackupAbortByServerException</span></span>](./esentbackupabortbyserverexception-class.md)  
          [<span data-ttu-id="b05dd-128">EsentCheckpointDepthTooDeepException （.）</span><span class="sxs-lookup"><span data-stu-id="b05dd-128">Microsoft.Isam.Esent.Interop.EsentCheckpointDepthTooDeepException</span></span>](./esentcheckpointdepthtoodeepexception-class.md)  
          [<span data-ttu-id="b05dd-129">EsentClientRequestToStopJetServiceException （.）</span><span class="sxs-lookup"><span data-stu-id="b05dd-129">Microsoft.Isam.Esent.Interop.EsentClientRequestToStopJetServiceException</span></span>](./esentclientrequesttostopjetserviceexception-class.md)  
          [<span data-ttu-id="b05dd-130">EsentFatalException （.）</span><span class="sxs-lookup"><span data-stu-id="b05dd-130">Microsoft.Isam.Esent.Interop.EsentFatalException</span></span>](./esentfatalexception-class.md)  
          [<span data-ttu-id="b05dd-131">EsentInitInProgressException （.）</span><span class="sxs-lookup"><span data-stu-id="b05dd-131">Microsoft.Isam.Esent.Interop.EsentInitInProgressException</span></span>](./esentinitinprogressexception-class.md)  
          [<span data-ttu-id="b05dd-132">EsentInternalErrorException （.）</span><span class="sxs-lookup"><span data-stu-id="b05dd-132">Microsoft.Isam.Esent.Interop.EsentInternalErrorException</span></span>](./esentinternalerrorexception-class.md)  
          [<span data-ttu-id="b05dd-133">EsentIOException （.）</span><span class="sxs-lookup"><span data-stu-id="b05dd-133">Microsoft.Isam.Esent.Interop.EsentIOException</span></span>](./esentioexception-class.md)  
          [<span data-ttu-id="b05dd-134">EsentNTSystemCallFailedException （.）</span><span class="sxs-lookup"><span data-stu-id="b05dd-134">Microsoft.Isam.Esent.Interop.EsentNTSystemCallFailedException</span></span>](./esentntsystemcallfailedexception-class.md)  
          [<span data-ttu-id="b05dd-135">EsentOSSnapshotTimeOutException （.）</span><span class="sxs-lookup"><span data-stu-id="b05dd-135">Microsoft.Isam.Esent.Interop.EsentOSSnapshotTimeOutException</span></span>](./esentossnapshottimeoutexception-class.md)  
          [<span data-ttu-id="b05dd-136">EsentRecordNotDeletedException （.）</span><span class="sxs-lookup"><span data-stu-id="b05dd-136">Microsoft.Isam.Esent.Interop.EsentRecordNotDeletedException</span></span>](./esentrecordnotdeletedexception-class.md)  
          [<span data-ttu-id="b05dd-137">EsentResourceException （.）</span><span class="sxs-lookup"><span data-stu-id="b05dd-137">Microsoft.Isam.Esent.Interop.EsentResourceException</span></span>](./esentresourceexception-class.md)  
          [<span data-ttu-id="b05dd-138">EsentTermInProgressException （.）</span><span class="sxs-lookup"><span data-stu-id="b05dd-138">Microsoft.Isam.Esent.Interop.EsentTermInProgressException</span></span>](./esentterminprogressexception-class.md)  
          [<span data-ttu-id="b05dd-139">EsentUnicodeLanguageValidationFailureException （.）</span><span class="sxs-lookup"><span data-stu-id="b05dd-139">Microsoft.Isam.Esent.Interop.EsentUnicodeLanguageValidationFailureException</span></span>](./esentunicodelanguagevalidationfailureexception-class.md)  
          [<span data-ttu-id="b05dd-140">EsentUnicodeTranslationFailException （.）</span><span class="sxs-lookup"><span data-stu-id="b05dd-140">Microsoft.Isam.Esent.Interop.EsentUnicodeTranslationFailException</span></span>](./esentunicodetranslationfailexception-class.md)