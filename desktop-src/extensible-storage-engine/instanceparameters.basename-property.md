---
description: 深入瞭解： InstanceParameters. BaseName 屬性
title: InstanceParameters. BaseName 屬性
TOCTitle: 'BaseName property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.BaseName
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.basename(v=EXCHG.10)
ms:contentKeyID: 55103315
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.BaseName
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.BaseName
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_BaseName
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_BaseName
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 2d7e36363a73dc19c324e1852f58346e0ad95b40
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106983694"
---
# <a name="instanceparametersbasename-property"></a><span data-ttu-id="cf35b-103">InstanceParameters. BaseName 屬性</span><span class="sxs-lookup"><span data-stu-id="cf35b-103">InstanceParameters.BaseName property</span></span>

<span data-ttu-id="cf35b-104">取得或設定用於資料庫引擎所使用之許多檔案的三個字母前置詞。</span><span class="sxs-lookup"><span data-stu-id="cf35b-104">Gets or sets the three letter prefix used for many of the files used by the database engine.</span></span> <span data-ttu-id="cf35b-105">例如，檢查點檔案稱為「EDB」。因為 EDB 是預設的基底名稱，所以預設為使用 .CHK。</span><span class="sxs-lookup"><span data-stu-id="cf35b-105">For example, the checkpoint file is called EDB.CHK by default because EDB is the default base name.</span></span>

<span data-ttu-id="cf35b-106">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="cf35b-106">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="cf35b-107">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="cf35b-107">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="cf35b-108">Syntax</span><span class="sxs-lookup"><span data-stu-id="cf35b-108">Syntax</span></span>

``` vb
'Declaration
Public Property BaseName As String
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As String

value = instance.BaseName

instance.BaseName = value
```

``` csharp
public string BaseName { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="cf35b-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="cf35b-109">Property value</span></span>

<span data-ttu-id="cf35b-110">類型： [system.string](/dotnet/api/system.string)</span><span class="sxs-lookup"><span data-stu-id="cf35b-110">Type: [System.String](/dotnet/api/system.string)</span></span>  

## <a name="see-also"></a><span data-ttu-id="cf35b-111">另請參閱</span><span class="sxs-lookup"><span data-stu-id="cf35b-111">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="cf35b-112">參考</span><span class="sxs-lookup"><span data-stu-id="cf35b-112">Reference</span></span>

[<span data-ttu-id="cf35b-113">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="cf35b-113">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="cf35b-114">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="cf35b-114">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="cf35b-115">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="cf35b-115">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
