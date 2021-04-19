---
description: 深入瞭解： InstanceParameters. CreatePathIfNotExist 屬性
title: InstanceParameters. CreatePathIfNotExist 屬性
TOCTitle: 'CreatePathIfNotExist property '
ms:assetid: P:Microsoft.Isam.Esent.Interop.InstanceParameters.CreatePathIfNotExist
ms:mtpsurl: https://msdn.microsoft.com/library/microsoft.isam.esent.interop.instanceparameters.createpathifnotexist(v=EXCHG.10)
ms:contentKeyID: 55103321
ms.date: 07/30/2014
ms.topic: reference
f1_keywords:
- Microsoft.Isam.Esent.Interop.InstanceParameters.CreatePathIfNotExist
dev_langs:
- CSharp
- JScript
- VB
- other
api_name:
- Microsoft.Isam.Esent.Interop.InstanceParameters.set_CreatePathIfNotExist
- Microsoft.Isam.Esent.Interop.InstanceParameters.get_CreatePathIfNotExist
- Microsoft.Isam.Esent.Interop.InstanceParameters.CreatePathIfNotExist
topic_type:
- apiref
- kbSyntax
api_type:
- Managed
api_location:
- Microsoft.Isam.Esent.Interop.dll
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: d777c7bae3c375118488105e275edba59e57cd05
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106996637"
---
# <a name="instanceparameterscreatepathifnotexist-property"></a><span data-ttu-id="40aab-103">InstanceParameters. CreatePathIfNotExist 屬性</span><span class="sxs-lookup"><span data-stu-id="40aab-103">InstanceParameters.CreatePathIfNotExist property</span></span>

<span data-ttu-id="40aab-104">取得或設定值，這個值表示 ESENT 是否會以無訊息方式建立檔案系統路徑中遺失的資料夾。</span><span class="sxs-lookup"><span data-stu-id="40aab-104">Gets or sets a value indicating whether ESENT will silently create folders that are missing in its filesystem paths.</span></span>

<span data-ttu-id="40aab-105">**命名空間：**  [Microsoft. Isam. Interop](./microsoft.isam.esent.interop-namespace.md)</span><span class="sxs-lookup"><span data-stu-id="40aab-105">**Namespace:**  [Microsoft.Isam.Esent.Interop](./microsoft.isam.esent.interop-namespace.md)</span></span>  
<span data-ttu-id="40aab-106">**元件：**  (在 Microsoft.Isam.Esent.Interop.dll) 中的 Microsoft。</span><span class="sxs-lookup"><span data-stu-id="40aab-106">**Assembly:**  Microsoft.Isam.Esent.Interop (in Microsoft.Isam.Esent.Interop.dll)</span></span>

## <a name="syntax"></a><span data-ttu-id="40aab-107">Syntax</span><span class="sxs-lookup"><span data-stu-id="40aab-107">Syntax</span></span>

``` vb
'Declaration
Public Property CreatePathIfNotExist As Boolean
    Get
    Set
'Usage
Dim instance As InstanceParameters
Dim value As Boolean

value = instance.CreatePathIfNotExist

instance.CreatePathIfNotExist = value
```

``` csharp
public bool CreatePathIfNotExist { get; set; }
```

#### <a name="property-value"></a><span data-ttu-id="40aab-108">屬性值</span><span class="sxs-lookup"><span data-stu-id="40aab-108">Property value</span></span>

<span data-ttu-id="40aab-109">型別： [system.object](/dotnet/api/system.boolean)</span><span class="sxs-lookup"><span data-stu-id="40aab-109">Type: [System.Boolean](/dotnet/api/system.boolean)</span></span>  

## <a name="see-also"></a><span data-ttu-id="40aab-110">另請參閱</span><span class="sxs-lookup"><span data-stu-id="40aab-110">See also</span></span>

#### <a name="reference"></a><span data-ttu-id="40aab-111">參考</span><span class="sxs-lookup"><span data-stu-id="40aab-111">Reference</span></span>

[<span data-ttu-id="40aab-112">InstanceParameters 類別</span><span class="sxs-lookup"><span data-stu-id="40aab-112">InstanceParameters class</span></span>](./instanceparameters-class.md)

[<span data-ttu-id="40aab-113">InstanceParameters 成員</span><span class="sxs-lookup"><span data-stu-id="40aab-113">InstanceParameters members</span></span>](./instanceparameters-members.md)

[<span data-ttu-id="40aab-114">Microsoft. Esent 命名空間</span><span class="sxs-lookup"><span data-stu-id="40aab-114">Microsoft.Isam.Esent.Interop namespace</span></span>](./microsoft.isam.esent.interop-namespace.md)
