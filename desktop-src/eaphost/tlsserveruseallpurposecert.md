---
title: TlsServerUseAllPurposeCert
description: TlsServerUseAllPurposeCert 登錄機碼會判斷是否使用所有用途的憑證來進行 EAP-TLS 驗證。
ms.assetid: a672cecb-6bba-4ba6-b362-f6d5a220184b
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b7cb767a8f6c8f40b377cca84d948b384170486
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "104313814"
---
# <a name="tlsserveruseallpurposecert"></a><span data-ttu-id="06b68-103">TlsServerUseAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="06b68-103">TlsServerUseAllPurposeCert</span></span>

<span data-ttu-id="06b68-104">TlsServerUseAllPurposeCert 登錄機碼會判斷是否使用所有用途的憑證來進行 EAP-TLS 驗證。</span><span class="sxs-lookup"><span data-stu-id="06b68-104">The TlsServerUseAllPurposeCert registry key determines if all-purpose certificates are used for EAP-TLS authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="06b68-105">登錄項目</span><span class="sxs-lookup"><span data-stu-id="06b68-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerUseAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="06b68-106">備註</span><span class="sxs-lookup"><span data-stu-id="06b68-106">Remarks</span></span>

<span data-ttu-id="06b68-107">這是 **REG \_ DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="06b68-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="06b68-108">值</span><span class="sxs-lookup"><span data-stu-id="06b68-108">Value</span></span>        | <span data-ttu-id="06b68-109">描述</span><span class="sxs-lookup"><span data-stu-id="06b68-109">Description</span></span>                                                                                                      |
|--------------|------------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="06b68-110">1</span><span class="sxs-lookup"><span data-stu-id="06b68-110">1</span></span>            | <span data-ttu-id="06b68-111">用戶端或伺服器憑證存儲中的所有用途憑證都是針對 PEAP 驗證所選取。</span><span class="sxs-lookup"><span data-stu-id="06b68-111">All-purpose certificates in the client's or server's certificate store are selected for PEAP authentication.</span></span>     |
| <span data-ttu-id="06b68-112">其他值</span><span class="sxs-lookup"><span data-stu-id="06b68-112">Other values</span></span> | <span data-ttu-id="06b68-113">用戶端或伺服器憑證存儲中的所有用途憑證都不會針對 PEAP 驗證進行選取。</span><span class="sxs-lookup"><span data-stu-id="06b68-113">All-purpose certificates in the client's or server's certificate store are not selected for PEAP authentication.</span></span> |



 

<span data-ttu-id="06b68-114">如果此登錄值不存在，則會選取用戶端或伺服器憑證存儲中的所有用途憑證以進行 EAP-TLS 驗證。</span><span class="sxs-lookup"><span data-stu-id="06b68-114">If this registry value is not present, all-purpose certificates in the client's or server's certificate store are selected for EAP-TLS authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="06b68-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="06b68-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="06b68-116">EAPHost 登錄設定</span><span class="sxs-lookup"><span data-stu-id="06b68-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




