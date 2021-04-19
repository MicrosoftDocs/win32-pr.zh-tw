---
title: PeapServerAcceptAllPurposeCert
description: PeapServerAcceptAllPurposeCert 登錄機碼會判斷是否接受 PEAP 驗證的所有用途憑證。
ms.assetid: 59C58459-7735-4733-9F95-646864802D70
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: b291696c6bee90b4f980d8f96ad96faf40fe3376
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "106969089"
---
# <a name="peapserveracceptallpurposecert"></a><span data-ttu-id="97cd6-103">PeapServerAcceptAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="97cd6-103">PeapServerAcceptAllPurposeCert</span></span>

<span data-ttu-id="97cd6-104">PeapServerAcceptAllPurposeCert 登錄機碼會判斷是否接受 PEAP 驗證的所有用途憑證。</span><span class="sxs-lookup"><span data-stu-id="97cd6-104">The PeapServerAcceptAllPurposeCert registry key determines if all-purpose certificates are accepted for PEAP authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="97cd6-105">登錄項目</span><span class="sxs-lookup"><span data-stu-id="97cd6-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\25
   PeapServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="97cd6-106">備註</span><span class="sxs-lookup"><span data-stu-id="97cd6-106">Remarks</span></span>

<span data-ttu-id="97cd6-107">這是 **REG \_ DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="97cd6-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="97cd6-108">值</span><span class="sxs-lookup"><span data-stu-id="97cd6-108">Value</span></span>        | <span data-ttu-id="97cd6-109">描述</span><span class="sxs-lookup"><span data-stu-id="97cd6-109">Description</span></span>                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="97cd6-110">1</span><span class="sxs-lookup"><span data-stu-id="97cd6-110">1</span></span>            | <span data-ttu-id="97cd6-111">伺服器和用戶端接受由另一方針對 EAP-TLS 驗證傳送的所有用途憑證。</span><span class="sxs-lookup"><span data-stu-id="97cd6-111">Server and client accept all-purpose certificates sent by the other party for EAP-TLS authentication.</span></span>       |
| <span data-ttu-id="97cd6-112">其他值</span><span class="sxs-lookup"><span data-stu-id="97cd6-112">Other values</span></span> | <span data-ttu-id="97cd6-113">伺服器和用戶端不接受由另一方針對 EAP-TLS 驗證傳送的所有用途憑證</span><span class="sxs-lookup"><span data-stu-id="97cd6-113">Server and client do not accept all-purpose certificates sent by the other party for EAP-TLS authentication</span></span> |



 

<span data-ttu-id="97cd6-114">如果此登錄值不存在，伺服器和用戶端會接受由另一方針對 PEAP 驗證傳送的所有用途憑證。</span><span class="sxs-lookup"><span data-stu-id="97cd6-114">If this registry value is not present, the server and client accept all-purpose certificates sent by the other party for PEAP authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="97cd6-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="97cd6-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="97cd6-116">EAPHost 登錄設定</span><span class="sxs-lookup"><span data-stu-id="97cd6-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




