---
description: 深入瞭解： InstanceParameters. CleanupMismatchedLogFiles 屬性
title: InstanceParameters. CleanupMismatchedLogFiles 屬性
TOCTitle: 'CleanupMismatchedLogFiles property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.cleanupmismatchedlogfiles(v=EXCHG.10)
ms:contentKeyID: 55103296
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CleanupMismatchedLogFiles
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CleanupMismatchedLogFiles
- Microsoft.Isam.Esent.Interop.InstanceParameters.CleanupMismatchedLogFiles
topic_type:
- kbSyntax
- apiref
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 0e80bb8877335e26cb233a09b2fa3ec3a6f12615
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104114441"
---
# <a name="instanceparameterscleanupmismatchedlogfiles-property"></a><span data-ttu-id="adb7c-103">InstanceParameters. CleanupMismatchedLogFiles 屬性</span><span class="sxs-lookup"><span data-stu-id="adb7c-103">InstanceParameters.CleanupMismatchedLogFiles property</span></span>

<span data-ttu-id="adb7c-104">取得或設定值，這個值表示當資料庫引擎設定為開始使用磁片上的交易記錄檔時，如果磁片上的交易記錄檔的大小與所設定的不同，JetInit 是否會失敗。</span><span class="sxs-lookup"><span data-stu-id="adb7c-104">Gets or sets a value indicating whether JetInit fails when the database engine is configured to start using transaction log files on disk that are of a different size than what is configured.</span></span> <span data-ttu-id="adb7c-105">一般來說， [JetInit (JET_INSTANCE) ](./api.jetinit-method.md) 會成功復原資料庫，但會失敗並出現 [LogFileSizeMismatchDatabasesConsistent](./jet-err-enumeration.md) ，指出記錄檔的大小設定不正確。</span><span class="sxs-lookup"><span data-stu-id="adb7c-105">Normally, [JetInit(JET_INSTANCE)](./api.jetinit-method.md) will successfully recover the databases but will fail with [LogFileSizeMismatchDatabasesConsistent](./jet-err-enumeration.md) to indicate that the log file size is misconfigured.</span></span> <span data-ttu-id="adb7c-106">但是，當這個參數設定為 true 時，database engine 就會以無訊息模式刪除所有舊的記錄檔，並使用所設定的記錄檔大小來啟動一組新的交易記錄檔。</span><span class="sxs-lookup"><span data-stu-id="adb7c-106">However, when this parameter is set to true then the database engine will silently delete all the old log files, start a new set of transaction log files using the configured log file size.</span></span> <span data-ttu-id="adb7c-107">當應用程式希望以透明的方式變更其交易記錄檔大小，但在升級和還原案例中仍可正常運作時，此參數很有用。</span><span class="sxs-lookup"><span data-stu-id="adb7c-107">This parameter is useful when the application wishes to transparently change its transaction log file size yet still work transparently in upgrade and restore scenarios.</span></span>

<span data-ttu-id="adb7c-108">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="adb7c-108">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="adb7c-109">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="adb7c-109">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="adb7c-110">Syntax</span><span class="sxs-lookup"><span data-stu-id="adb7c-110">Syntax</span></span>

``` vb
'Declaration
Public Property CleanupMismatchedLogFiles As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.CleanupMismatchedLogFiles

instance.CleanupMismatchedLogFiles = value
```

``` csharp
public bool CleanupMismatchedLogFiles { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="adb7c-111">屬性值</span><span class="sxs-lookup"><span data-stu-id="adb7c-111">Property value</span></span>

<span data-ttu-id="adb7c-112">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="adb7c-112">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="adb7c-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="adb7c-113">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="adb7c-114">參考</span><span class="sxs-lookup"><span data-stu-id="adb7c-114">Reference</span></span>

[<span data-ttu-id="adb7c-115">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="adb7c-115">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="adb7c-116">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="adb7c-116">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="adb7c-117">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="adb7c-117">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
