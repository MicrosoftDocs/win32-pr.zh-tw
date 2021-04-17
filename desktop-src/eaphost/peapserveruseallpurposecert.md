---
title: PeapServerUseAllPurposeCert
description: PeapServerUseAllPurposeCert 登錄機碼會判斷是否使用所有用途的憑證進行 PEAP 驗證。
ms.assetid: e239fb88-4bf3-49b6-a95c-67a8c060a50d
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bc90f083f9020ad02960d7620a2ab54706df203e
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104313833"
---
# <a name="peapserveruseallpurposecert"></a><span data-ttu-id="17d92-103">PeapServerUseAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="17d92-103">PeapServerUseAllPurposeCert</span></span>

<span data-ttu-id="17d92-104">PeapServerUseAllPurposeCert 登錄機碼會判斷是否使用所有用途的憑證進行 PEAP 驗證。</span><span class="sxs-lookup"><span data-stu-id="17d92-104">The PeapServerUseAllPurposeCert registry key determines if all-purpose certificates are used for PEAP authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="17d92-105">登錄項目</span><span class="sxs-lookup"><span data-stu-id="17d92-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerUseAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="17d92-106">備註</span><span class="sxs-lookup"><span data-stu-id="17d92-106">Remarks</span></span>

<span data-ttu-id="17d92-107">這是 **REG \_ DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="17d92-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="17d92-108">值</span><span class="sxs-lookup"><span data-stu-id="17d92-108">Value</span></span>        | <span data-ttu-id="17d92-109">描述</span><span class="sxs-lookup"><span data-stu-id="17d92-109">Description</span></span>                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="17d92-110">1</span><span class="sxs-lookup"><span data-stu-id="17d92-110">1</span></span>            | <span data-ttu-id="17d92-111">用戶端或伺服器憑證存儲中的所有用途憑證都是針對 PEAP 驗證所選取。</span><span class="sxs-lookup"><span data-stu-id="17d92-111">All-purpose certificates in the client's or server's certificate store are selected for PEAP authentication.</span></span>     |
| <span data-ttu-id="17d92-112">其他值</span><span class="sxs-lookup"><span data-stu-id="17d92-112">Other values</span></span> | <span data-ttu-id="17d92-113">用戶端或伺服器憑證存儲中的所有用途憑證都不會針對 PEAP 驗證進行選取。</span><span class="sxs-lookup"><span data-stu-id="17d92-113">All-purpose certificates in the client's or server's certificate store are not selected for PEAP authentication.</span></span> |



 

<span data-ttu-id="17d92-114">如果此登錄值不存在，則會選取用戶端或伺服器憑證存儲中的所有用途憑證進行 PEAP 驗證。</span><span class="sxs-lookup"><span data-stu-id="17d92-114">If this registry value is not present, all-purpose certificates in the client's or server's certificate store are selected for PEAP authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="17d92-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="17d92-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="17d92-116">EAPHost 登錄設定</span><span class="sxs-lookup"><span data-stu-id="17d92-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




