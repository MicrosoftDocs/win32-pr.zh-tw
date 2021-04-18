---
description: 深入瞭解： InstanceParameters. LogFileSize 屬性
title: InstanceParameters. LogFileSize 屬性
TOCTitle: 'LogFileSize property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileSize
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.logfilesize(v=EXCHG.10)
ms:contentKeyID: 55103312
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileSize
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.LogFileSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_LogFileSize
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_LogFileSize
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: c141c76a92f49b4b5000cad65e302a7cf15d780f
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106978050"
---
# <a name="instanceparameterslogfilesize-property"></a><span data-ttu-id="f87f2-103">InstanceParameters. LogFileSize 屬性</span><span class="sxs-lookup"><span data-stu-id="f87f2-103">InstanceParameters.LogFileSize property</span></span>

<span data-ttu-id="f87f2-104">取得或設定交易記錄檔的大小。</span><span class="sxs-lookup"><span data-stu-id="f87f2-104">Gets or sets the size of the transaction log files.</span></span> <span data-ttu-id="f87f2-105">此參數應以1024個位元組的單位來設定 (例如，2048的設定會提供2MB 的記錄檔) 。</span><span class="sxs-lookup"><span data-stu-id="f87f2-105">This parameter should be set in units of 1024 bytes (e.g. a setting of 2048 will give 2MB logfiles).</span></span>

<span data-ttu-id="f87f2-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="f87f2-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="f87f2-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="f87f2-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="f87f2-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="f87f2-108">Syntax</span></span>

``` vb
'Declaration
Public Property LogFileSize As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.LogFileSize

instance.LogFileSize = value
```

``` csharp
public int LogFileSize { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="f87f2-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="f87f2-109">Property value</span></span>

<span data-ttu-id="f87f2-110">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="f87f2-110">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="f87f2-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f87f2-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="f87f2-112">參考</span><span class="sxs-lookup"><span data-stu-id="f87f2-112">Reference</span></span>

[<span data-ttu-id="f87f2-113">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="f87f2-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="f87f2-114">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="f87f2-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="f87f2-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="f87f2-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
