---
description: 深入瞭解： JetCloseFileInstance 方法
title: JetCloseFileInstance 方法
TOCTitle: 'JetCloseFileInstance method '
ms:assetid: M:Microsoft.Isam.Esent.Interop.Api.JetCloseFileInstance(Microsoft.Isam.Esent.Interop.JET_INSTANCE,Microsoft.Isam.Esent.Interop.JET_HANDLE)
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.api.jetclosefileinstance(v=EXCHG.10)
ms:contentKeyID: 55100663
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.Api.JetCloseFileInstance
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.Api.JetCloseFileInstance
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8ac29dec4032d83197a57746789afc770d84ec30
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106967075"
---
# <a name="apijetclosefileinstance-method"></a><span data-ttu-id="2bbc3-103">JetCloseFileInstance 方法</span><span class="sxs-lookup"><span data-stu-id="2bbc3-103">Api.JetCloseFileInstance method</span></span>

<span data-ttu-id="2bbc3-104">當使用 JetReadFileInstance 解壓縮該檔案中的資料之後，關閉以 JetOpenFileInstance 開啟的檔案。</span><span class="sxs-lookup"><span data-stu-id="2bbc3-104">Closes a file that was opened with JetOpenFileInstance after the data from that file has been extracted using JetReadFileInstance.</span></span>

<span data-ttu-id="2bbc3-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="2bbc3-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="2bbc3-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="2bbc3-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="2bbc3-107">語法</span><span class="sxs-lookup"><span data-stu-id="2bbc3-107">Syntax</span></span>

``` vb
'Declaration
Public Shared Sub JetCloseFileInstance ( _
    instance As JET_INSTANCE, _
    handle As JET_HANDLE _
)
'Usage
Dim instance As JET_INSTANCE
Dim handle As JET_HANDLEApi.JetCloseFileInstance(instance, _
    handle)
```

``` csharp
public static void JetCloseFileInstance(
    JET_INSTANCE instance,
    JET_HANDLE handle
)
```

#### <a name="parameters"></a><span data-ttu-id="2bbc3-108">參數</span><span class="sxs-lookup"><span data-stu-id="2bbc3-108">Parameters</span></span>

  - <span data-ttu-id="2bbc3-109">instance</span><span class="sxs-lookup"><span data-stu-id="2bbc3-109">instance</span></span>  
    <span data-ttu-id="2bbc3-110">類型： [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2bbc3-110">Type: [Microsoft.Isam.Esent.Interop.JET_INSTANCE](./jet-instance-structure.md)</span></span>  
    
    <span data-ttu-id="2bbc3-111">要使用的實例。</span><span class="sxs-lookup"><span data-stu-id="2bbc3-111">The instance to use.</span></span>

<!-- end list -->

  - <span data-ttu-id="2bbc3-112">處理</span><span class="sxs-lookup"><span data-stu-id="2bbc3-112">handle</span></span>  
    <span data-ttu-id="2bbc3-113">類型： [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span><span class="sxs-lookup"><span data-stu-id="2bbc3-113">Type: [Microsoft.Isam.Esent.Interop.JET_HANDLE](./jet-handle-structure.md)</span></span>  
    
    <span data-ttu-id="2bbc3-114">要關閉的控制碼。</span><span class="sxs-lookup"><span data-stu-id="2bbc3-114">The handle to close.</span></span>

## <a name="see-also"></a><span data-ttu-id="2bbc3-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="2bbc3-115">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="2bbc3-116">參考</span><span class="sxs-lookup"><span data-stu-id="2bbc3-116">Reference</span></span>

[<span data-ttu-id="2bbc3-117">Api 類別</span><span class="sxs-lookup"><span data-stu-id="2bbc3-117">Api class</span></span>](./api-class.md)

[<span data-ttu-id="2bbc3-118">Api 成員</span><span class="sxs-lookup"><span data-stu-id="2bbc3-118">Api members</span></span>](./api-members.md)

[<span data-ttu-id="2bbc3-119">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="2bbc3-119">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
