---
description: '深入瞭解： CimInstance. SetCimSessionComputerName 方法 (字串) '
title: CimInstance.SetCimSessionComputerName 方法 (Microsoft.Management.Infrastructure)
TOCTitle: CimInstance.SetCimSessionComputerName method (Microsoft.Management.Infrastructure)
ms:assetid: M:Microsoft.Management.Infrastructure.CimInstance.SetCimSessionComputerName(System.String)
ms.date: 11/12/2019
mtps_version: v=VS.85
f1_keywords:
- Microsoft.Management.Infrastructure.CimInstance.SetCimSessionComputerName
- Microsoft::Management::Infrastructure::CimInstance::SetCimSessionComputerName
dev_langs:
- CSharp
- C++
- VB
- FSharp
api_location:
- Microsoft.Management.Infrastructure.dll
api_name:
- Microsoft.Management.Infrastructure.CimInstance.SetCimSessionComputerName
api_type:
- Assembly
topic_type:
- apiref
product_family_name: VS
ms.topic: reference
ms.openlocfilehash: b9f4cd9d308617a2369eaa542705e4ad7f854fa4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319575"
---
# <a name="ciminstancesetcimsessioncomputername-method-string"></a><span data-ttu-id="74dd6-103">CimInstance. SetCimSessionComputerName 方法 (字串) </span><span class="sxs-lookup"><span data-stu-id="74dd6-103">CimInstance.SetCimSessionComputerName method (String)</span></span>

<span data-ttu-id="74dd6-104">設定用於 CIM 會話的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="74dd6-104">Sets the name of the computer used for the CIM session.</span></span>

<span data-ttu-id="74dd6-105">**命名空間：**   [Microsoft. 管理. 基礎結構](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958\(v=vs.85\))</span><span class="sxs-lookup"><span data-stu-id="74dd6-105">**Namespace:**   [Microsoft.Management.Infrastructure](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958\(v=vs.85\))</span></span>  
<span data-ttu-id="74dd6-106">**元件：**  Microsoft.Management.Infrastructure.dll) 中的 (基礎結構</span><span class="sxs-lookup"><span data-stu-id="74dd6-106">**Assembly:**  Microsoft.Management.Infrastructure (in Microsoft.Management.Infrastructure.dll)</span></span>  

## <a name="syntax"></a><span data-ttu-id="74dd6-107">語法</span><span class="sxs-lookup"><span data-stu-id="74dd6-107">Syntax</span></span>

``` csharp
public void SetCimSessionComputerName(
    string computerName
)
```

``` c++
public:
void SetCimSessionComputerName(
    String^ computerName
)
```

``` fsharp
member SetCimSessionComputerName : 
        computerName:string -> unit
```

``` vb
Public Sub SetCimSessionComputerName (
    computerName As String
)
```

#### <a name="parameters"></a><span data-ttu-id="74dd6-108">參數</span><span class="sxs-lookup"><span data-stu-id="74dd6-108">Parameters</span></span>

  - <span data-ttu-id="74dd6-109">computerName</span><span class="sxs-lookup"><span data-stu-id="74dd6-109">computerName</span></span>  
    <span data-ttu-id="74dd6-110">類型： [system.string](/dotnet/api/system.string?view=netframework-4.8)</span><span class="sxs-lookup"><span data-stu-id="74dd6-110">Type: [System.String](/dotnet/api/system.string?view=netframework-4.8)</span></span>
    
    <span data-ttu-id="74dd6-111">用於 CIM 會話的電腦名稱稱。</span><span class="sxs-lookup"><span data-stu-id="74dd6-111">The name of the computer used for the CIM session.</span></span> <span data-ttu-id="74dd6-112">如果目前的實例只是用戶端，或從 localhost 取出實例，則 **為 null** 。</span><span class="sxs-lookup"><span data-stu-id="74dd6-112">**null** if the current instance is client-side only, or if the instance was retrieved from localhost.</span></span>

## <a name="see-also"></a><span data-ttu-id="74dd6-113">另請參閱</span><span class="sxs-lookup"><span data-stu-id="74dd6-113">See also</span></span>

<span data-ttu-id="74dd6-114">[CimInstance 類別](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336\(v=vs.85\))</span><span class="sxs-lookup"><span data-stu-id="74dd6-114">[CimInstance Class](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832336\(v=vs.85\))</span></span>  
<span data-ttu-id="74dd6-115">[Microsoft. 基礎結構命名空間](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958\(v=vs.85\))</span><span class="sxs-lookup"><span data-stu-id="74dd6-115">[Microsoft.Management.Infrastructure namespace](/previous-versions/windows/desktop/wmi_v2/mi-managed-api/hh832958\(v=vs.85\))</span></span>
