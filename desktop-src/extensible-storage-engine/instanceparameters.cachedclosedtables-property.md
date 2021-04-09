---
description: 深入瞭解： InstanceParameters. CachedClosedTables 屬性
title: InstanceParameters. CachedClosedTables 屬性
TOCTitle: 'CachedClosedTables property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CachedClosedTables
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.cachedclosedtables(v=EXCHG.10)
ms:contentKeyID: 55103293
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CachedClosedTables
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CachedClosedTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.CachedClosedTables
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CachedClosedTables
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 8f2465de2df3d25293f5298d40700512b6a086d8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103691664"
---
# <a name="instanceparameterscachedclosedtables-property"></a><span data-ttu-id="31608-103">InstanceParameters. CachedClosedTables 屬性</span><span class="sxs-lookup"><span data-stu-id="31608-103">InstanceParameters.CachedClosedTables property</span></span>

<span data-ttu-id="31608-104">取得或設定值，這個值會在應用程式關閉實例所代表的資料表之後，提供實例快取的 B + 樹狀資源數目。</span><span class="sxs-lookup"><span data-stu-id="31608-104">Gets or sets a value giving the number of B+ Tree resources cached by the instance after the tables they represent have been closed by the application.</span></span> <span data-ttu-id="31608-105">此參數的大型值會導致資料庫引擎使用更多記憶體，但會增加應用程式隨機開啟大量資料表的速度。</span><span class="sxs-lookup"><span data-stu-id="31608-105">Large values for this parameter will cause the database engine to use more memory but will increase the speed with which a large number of tables can be opened randomly by the application.</span></span> <span data-ttu-id="31608-106">對於具有極大量資料表之架構的應用程式而言，這非常有用。</span><span class="sxs-lookup"><span data-stu-id="31608-106">This is useful for applications that have a schema with a very large number of tables.</span></span> <span data-ttu-id="31608-107">Windows Vista 和更新的支援。</span><span class="sxs-lookup"><span data-stu-id="31608-107">Supported on Windows Vista and up.</span></span> <span data-ttu-id="31608-108">在 Windows XP 和 Windows Server 2003 上略過。</span><span class="sxs-lookup"><span data-stu-id="31608-108">Ignored on Windows XP and Windows Server 2003.</span></span>

<span data-ttu-id="31608-109">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="31608-109">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="31608-110">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="31608-110">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="31608-111">Syntax</span><span class="sxs-lookup"><span data-stu-id="31608-111">Syntax</span></span>

``` vb
'Declaration
Public Property CachedClosedTables As Integer
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Integer

value = instance.CachedClosedTables

instance.CachedClosedTables = value
```

``` csharp
public int CachedClosedTables { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="31608-112">屬性值</span><span class="sxs-lookup"><span data-stu-id="31608-112">Property value</span></span>

<span data-ttu-id="31608-113">類型： [system.object](/dotnet/api/system.int32)</span><span class="sxs-lookup"><span data-stu-id="31608-113">Type: [System.Int32](/dotnet/api/system.int32)</span></span>  

## <a name="see-also"></a><span data-ttu-id="31608-114">另請參閱</span><span class="sxs-lookup"><span data-stu-id="31608-114">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="31608-115">參考</span><span class="sxs-lookup"><span data-stu-id="31608-115">Reference</span></span>

[<span data-ttu-id="31608-116">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="31608-116">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="31608-117">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="31608-117">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="31608-118">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="31608-118">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
