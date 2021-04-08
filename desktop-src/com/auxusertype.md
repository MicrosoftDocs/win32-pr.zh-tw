---
title: AuxUserType
description: 指定應用程式的簡短顯示名稱和應用程式名稱。
ms.assetid: 3367eb68-01f4-4cb9-b1d0-27554c28b68d
keywords:
- AuxUserType 登錄機碼 COM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c66fcfbcdc2886e93d08040659b39c42d47c291
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103670888"
---
# <a name="auxusertype"></a><span data-ttu-id="42670-104">AuxUserType</span><span class="sxs-lookup"><span data-stu-id="42670-104">AuxUserType</span></span>

<span data-ttu-id="42670-105">指定應用程式的簡短顯示名稱和應用程式名稱。</span><span class="sxs-lookup"><span data-stu-id="42670-105">Specifies an application's short display name and application names.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="42670-106">登錄項目</span><span class="sxs-lookup"><span data-stu-id="42670-106">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\SOFTWARE\Classes\CLSID
   {CLSID}
      AuxUserType
         2 = ShortDisplayName
         3 = ApplicationName
```

## <a name="remarks"></a><span data-ttu-id="42670-107">備註</span><span class="sxs-lookup"><span data-stu-id="42670-107">Remarks</span></span>

<span data-ttu-id="42670-108">建議的 *ShortDisplayName* 長度上限為15個字元。</span><span class="sxs-lookup"><span data-stu-id="42670-108">The recommended maximum length for *ShortDisplayName* is 15 characters.</span></span> <span data-ttu-id="42670-109">這個名稱會在功能表中使用，包括快顯功能表。</span><span class="sxs-lookup"><span data-stu-id="42670-109">This name is used in menus, including pop-up menus.</span></span>

<span data-ttu-id="42670-110">*ApplicationName* 應該包含應用程式的實際名稱 (例如「Acme Draw 2.0」 ) 。</span><span class="sxs-lookup"><span data-stu-id="42670-110">*ApplicationName* should contain the actual name of the application (such as "Acme Draw 2.0").</span></span> <span data-ttu-id="42670-111">這個名稱會用於 [**貼上特殊**] 對話方塊的 [**結果**] 欄位中。</span><span class="sxs-lookup"><span data-stu-id="42670-111">This name is used in the **Results** field of the **Paste Special** dialog box.</span></span>

## <a name="related-topics"></a><span data-ttu-id="42670-112">相關主題</span><span class="sxs-lookup"><span data-stu-id="42670-112">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="42670-113">**IOleObject::GetUserType**</span><span class="sxs-lookup"><span data-stu-id="42670-113">**IOleObject::GetUserType**</span></span>](/windows/desktop/api/OleIdl/nf-oleidl-ioleobject-getusertype)
</dt> </dl>

 

 




