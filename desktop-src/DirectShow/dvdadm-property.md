---
description: DVDAdm 屬性可讓您存取 MSDVDAdm 物件，其中包含用來儲存應用程式和使用者資訊的方法和屬性。
ms.assetid: eb73a851-7118-42f3-be99-1cf356d2e37a
title: DVDAdm 屬性
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 4c3d81742fc6e643d6ee805a76c14d07d45d1924
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "104109224"
---
# <a name="dvdadm-property"></a><span data-ttu-id="f50f0-103">DVDAdm 屬性</span><span class="sxs-lookup"><span data-stu-id="f50f0-103">DVDAdm Property</span></span>

> [!Note]  
> <span data-ttu-id="f50f0-104">此元件可用於 Microsoft Windows 2000、Windows XP 及 Windows Server 2003 作業系統。</span><span class="sxs-lookup"><span data-stu-id="f50f0-104">This component is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.</span></span> <span data-ttu-id="f50f0-105">它在後續版本中可能會變更或無法使用。</span><span class="sxs-lookup"><span data-stu-id="f50f0-105">It may be altered or unavailable in subsequent versions.</span></span>

 

<span data-ttu-id="f50f0-106">`DVDAdm`屬性可讓您存取[MSDVDAdm](msdvdadm-object.md)物件，其中包含用來儲存應用程式和使用者資訊的方法和屬性。</span><span class="sxs-lookup"><span data-stu-id="f50f0-106">The `DVDAdm` property provides access to the [MSDVDAdm](msdvdadm-object.md) object that contains methods and properties for saving application and user information.</span></span>

``` syntax
        MSWebDVD.DVDAdm
```

## <a name="remarks"></a><span data-ttu-id="f50f0-107">備註</span><span class="sxs-lookup"><span data-stu-id="f50f0-107">Remarks</span></span>

<span data-ttu-id="f50f0-108">這個屬性是唯讀的，沒有預設值。</span><span class="sxs-lookup"><span data-stu-id="f50f0-108">This property is read-only with no default value.</span></span> <span data-ttu-id="f50f0-109">不需要建立 **MSDVDAdm** 物件的個別參考。</span><span class="sxs-lookup"><span data-stu-id="f50f0-109">There is no need to create a separate reference to the **MSDVDAdm** object.</span></span> <span data-ttu-id="f50f0-110">若要存取物件的方法和屬性，請使用 `DVDAdm` 屬性，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="f50f0-110">To access the methods and properties of the object, use the `DVDAdm` property as shown in the following example.</span></span>

## <a name="examples"></a><span data-ttu-id="f50f0-111">範例</span><span class="sxs-lookup"><span data-stu-id="f50f0-111">Examples</span></span>


```VB
DVD.DVDAdm.DisableScreenSaver = true
```



 

 



