---
description: 深入瞭解： InstanceParameters. AlternateDatabaseRecoveryDirectory 屬性
title: InstanceParameters. AlternateDatabaseRecoveryDirectory 屬性
TOCTitle: 'AlternateDatabaseRecoveryDirectory property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.alternatedatabaserecoverydirectory(v=EXCHG.10)
ms:contentKeyID: 55107440
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.AlternateDatabaseRecoveryDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_AlternateDatabaseRecoveryDirectory
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_AlternateDatabaseRecoveryDirectory
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 70e08c65027806990ab511ef8561b41551f0ac2c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974956"
---
# <a name="instanceparametersalternatedatabaserecoverydirectory-property"></a><span data-ttu-id="e4b34-103">InstanceParameters. AlternateDatabaseRecoveryDirectory 屬性</span><span class="sxs-lookup"><span data-stu-id="e4b34-103">InstanceParameters.AlternateDatabaseRecoveryDirectory property</span></span>

<span data-ttu-id="e4b34-104">取得或設定資料夾的相對或絕對檔案系統路徑，其中損毀復原或還原作業可以在指定資料夾的交易記錄中找到參考的資料庫。</span><span class="sxs-lookup"><span data-stu-id="e4b34-104">Gets or sets the relative or absolute file system path of the a folder where crash recovery or a restore operation can find the databases referenced in the transaction log in the specified folder.</span></span>

<span data-ttu-id="e4b34-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="e4b34-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="e4b34-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="e4b34-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="e4b34-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="e4b34-107">Syntax</span></span>

``` vb
'Declaration
Public Property AlternateDatabaseRecoveryDirectory As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.AlternateDatabaseRecoveryDirectory

instance.AlternateDatabaseRecoveryDirectory = value
```

``` csharp
public string AlternateDatabaseRecoveryDirectory { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="e4b34-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="e4b34-108">Property value</span></span>

<span data-ttu-id="e4b34-109">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="e4b34-109">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="remarks"></a><span data-ttu-id="e4b34-110">備註</span><span class="sxs-lookup"><span data-stu-id="e4b34-110">Remarks</span></span>

<span data-ttu-id="e4b34-111">在 Windows XP 上，會忽略這個參數。</span><span class="sxs-lookup"><span data-stu-id="e4b34-111">This parameter is ignored on Windows XP.</span></span>

## <a name="see-also"></a><span data-ttu-id="e4b34-112">另請參閱</span><span class="sxs-lookup"><span data-stu-id="e4b34-112">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="e4b34-113">參考</span><span class="sxs-lookup"><span data-stu-id="e4b34-113">Reference</span></span>

[<span data-ttu-id="e4b34-114">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="e4b34-114">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="e4b34-115">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="e4b34-115">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="e4b34-116">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="e4b34-116">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
