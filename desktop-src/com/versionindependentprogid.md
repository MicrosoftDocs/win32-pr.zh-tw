---
title: VersionIndependentProgID
description: 將 ProgID 與 CLSID 產生關聯。 此值可用來判斷物件應用程式的最新版本。
ms.assetid: 5d188db9-ea4f-47fe-882f-a6caa7e86a25
keywords:
- VersionIndependentProgID 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a5774dfa5202521bb5055bab6a62aa7c6a60b3cc
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104022095"
---
# <a name="versionindependentprogid"></a><span data-ttu-id="b93a4-105">VersionIndependentProgID</span><span class="sxs-lookup"><span data-stu-id="b93a4-105">VersionIndependentProgID</span></span>

<span data-ttu-id="b93a4-106">將 ProgID 與 CLSID 產生關聯。</span><span class="sxs-lookup"><span data-stu-id="b93a4-106">Associates a ProgID with a CLSID.</span></span> <span data-ttu-id="b93a4-107">此值可用來判斷物件應用程式的最新版本。</span><span class="sxs-lookup"><span data-stu-id="b93a4-107">This value is used to determine the latest version of an object application.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="b93a4-108">登錄項目</span><span class="sxs-lookup"><span data-stu-id="b93a4-108">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      VersionIndependentProgID = Program.Component
```

## <a name="remarks"></a><span data-ttu-id="b93a4-109">備註</span><span class="sxs-lookup"><span data-stu-id="b93a4-109">Remarks</span></span>

<span data-ttu-id="b93a4-110">這是 **REG \_ SZ** 值，可指定最新版的物件應用程式。</span><span class="sxs-lookup"><span data-stu-id="b93a4-110">This is a **REG\_SZ** value that specifies the latest version of the object application.</span></span>

<span data-ttu-id="b93a4-111">與版本無關的 ProgID 只會由應用程式程式碼儲存和維護。</span><span class="sxs-lookup"><span data-stu-id="b93a4-111">The version-independent ProgID is stored and maintained solely by application code.</span></span> <span data-ttu-id="b93a4-112">當指定與版本無關的 ProgID 時， [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) 函數會傳回目前版本的 CLSID。</span><span class="sxs-lookup"><span data-stu-id="b93a4-112">When given the version-independent ProgID, the [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) function returns the CLSID of the current version.</span></span>

<span data-ttu-id="b93a4-113">您可以使用 [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) 和 [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) ，在這兩種標記法之間進行轉換。</span><span class="sxs-lookup"><span data-stu-id="b93a4-113">You can use [**CLSIDFromProgID**](/windows/desktop/api/combaseapi/nf-combaseapi-clsidfromprogid) and [**ProgIDFromCLSID**](/windows/desktop/api/combaseapi/nf-combaseapi-progidfromclsid) to convert between these two representations.</span></span>

 

 




