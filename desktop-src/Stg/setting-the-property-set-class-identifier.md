---
title: 設定屬性集類別識別碼
description: IPropertyStorage SetClass 方法會設定儲存物件的 CLSID 和儲存在 COM 屬性集中的類別標記值。 當在儲存于結構化儲存物件中的簡單屬性儲存體上叫用時，就會發生這種情況。
ms.assetid: 3f542a66-5e04-43c1-a386-7d709c615972
keywords:
- 設定屬性集類別識別碼
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4f9ec6e038ef6bc5f4f12228581946a4051c532b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021889"
---
# <a name="setting-the-property-set-class-identifier"></a><span data-ttu-id="b31de-105">設定屬性集類別識別碼</span><span class="sxs-lookup"><span data-stu-id="b31de-105">Setting the Property Set Class Identifier</span></span>

<span data-ttu-id="b31de-106">[**IPropertyStorage：： SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass)方法會設定儲存物件的 CLSID 和儲存在 COM 屬性集中的類別標記值。</span><span class="sxs-lookup"><span data-stu-id="b31de-106">The [**IPropertyStorage::SetClass**](/windows/desktop/api/Propidl/nf-propidl-ipropertystorage-setclass) method sets both the CLSID of the storage object and the class tag value stored in the COM property set.</span></span> <span data-ttu-id="b31de-107">當在儲存于結構化儲存物件中的簡單屬性儲存體上叫用時，就會發生這種情況。</span><span class="sxs-lookup"><span data-stu-id="b31de-107">This occurs when invoked on a nonsimple property storage stored in a structured storage object.</span></span>

<span data-ttu-id="b31de-108">這可提供一致性和一致性，進而與某些工具產生更佳的互動。</span><span class="sxs-lookup"><span data-stu-id="b31de-108">This provides consistency and uniformity which creates better interaction with some tools.</span></span> <span data-ttu-id="b31de-109">如果屬性儲存物件是藉由呼叫 [**IPropertySetStorage：： Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) 並設定 **PROPSETFLAG \_ 簡單** 旗標所建立，就會簡單。</span><span class="sxs-lookup"><span data-stu-id="b31de-109">A property storage object is nonsimple if it is created by calling [**IPropertySetStorage::Create**](/windows/desktop/api/Propidl/nf-propidl-ipropertysetstorage-create) with the **PROPSETFLAG\_NONSIMPLE** flag set.</span></span>

<span data-ttu-id="b31de-110">儲存物件的 CLSID 是透過呼叫 [**IStorage：： SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass)來設定。</span><span class="sxs-lookup"><span data-stu-id="b31de-110">The CLSID of the storage object is set with a call to [**IStorage::SetClass**](/windows/desktop/api/Objidl/nf-objidl-istorage-setclass).</span></span>

 

 




