---
title: COM)  (介面
description: 選擇性專案，指定相關聯類別 (Iid) 所支援的所有介面識別碼。
ms.assetid: 212a6500-14ce-4a9b-9e6a-38d83a5630c8
keywords:
- 介面登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 990c06285d60067c9a26faffabffc70cbdd283d1
ms.sourcegitcommit: 8fa6614b715bddf14648cce36d2df22e5232801a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/10/2020
ms.locfileid: "106965268"
---
# <a name="interface-com"></a><span data-ttu-id="ce742-104">COM)  (介面</span><span class="sxs-lookup"><span data-stu-id="ce742-104">Interface (COM)</span></span>

<span data-ttu-id="ce742-105">選擇性專案，指定相關聯類別 (Iid) 所支援的所有介面識別碼。</span><span class="sxs-lookup"><span data-stu-id="ce742-105">An optional entry that specifies all interface IDs (IIDs) supported by the associated class.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="ce742-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="ce742-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      Interface
         {IID1} = name1
         {IID2} = name2
         ...
```

## <a name="remarks"></a><span data-ttu-id="ce742-107">備註</span><span class="sxs-lookup"><span data-stu-id="ce742-107">Remarks</span></span>

<span data-ttu-id="ce742-108">如果此清單中沒有介面名稱，此類別的實例永遠不會支援此介面。</span><span class="sxs-lookup"><span data-stu-id="ce742-108">If an interface name is not present in this list, the interface can never be supported by an instance of this class.</span></span>

## <a name="related-topics"></a><span data-ttu-id="ce742-109">相關主題</span><span class="sxs-lookup"><span data-stu-id="ce742-109">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="ce742-110">介面金鑰</span><span class="sxs-lookup"><span data-stu-id="ce742-110">Interface Key</span></span>](interface-key.md)
</dt> </dl>

 

 




