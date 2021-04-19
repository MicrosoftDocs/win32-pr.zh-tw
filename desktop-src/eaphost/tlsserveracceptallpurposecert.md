---
title: TlsServerAcceptAllPurposeCert
description: TlsServerAcceptAllPurposeCert 登錄機碼會判斷是否接受 EAP-TLS 驗證的所有用途憑證。
ms.assetid: F0881397-5D8C-4C8F-8EB5-6D59454C55B7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 1c6561418d8d9cb06fb9618e6b93189cbd28e408
ms.sourcegitcommit: c20a43b333f03175ac23823c55f3204bfe8cd243
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/26/2019
ms.locfileid: "106966228"
---
# <a name="tlsserveracceptallpurposecert"></a><span data-ttu-id="47e0b-103">TlsServerAcceptAllPurposeCert</span><span class="sxs-lookup"><span data-stu-id="47e0b-103">TlsServerAcceptAllPurposeCert</span></span>

<span data-ttu-id="47e0b-104">TlsServerAcceptAllPurposeCert 登錄機碼會判斷是否接受 EAP-TLS 驗證的所有用途憑證。</span><span class="sxs-lookup"><span data-stu-id="47e0b-104">The TlsServerAcceptAllPurposeCert registry key determines if all-purpose certificates are accepted for EAP-TLS authentication.</span></span>

## <a name="registry-entry"></a><span data-ttu-id="47e0b-105">登錄項目</span><span class="sxs-lookup"><span data-stu-id="47e0b-105">Registry Entry</span></span>

```
HKEY_LOCAL_MACHINE\System\CurrentControlSet\Services\Rasman\PPP\EAP\13
   TlsServerAcceptAllPurposeCert = value
```

## <a name="remarks"></a><span data-ttu-id="47e0b-106">備註</span><span class="sxs-lookup"><span data-stu-id="47e0b-106">Remarks</span></span>

<span data-ttu-id="47e0b-107">這是 **REG \_ DWORD** 值。</span><span class="sxs-lookup"><span data-stu-id="47e0b-107">This is a **REG\_DWORD** value.</span></span>



| <span data-ttu-id="47e0b-108">值</span><span class="sxs-lookup"><span data-stu-id="47e0b-108">Value</span></span>        | <span data-ttu-id="47e0b-109">描述</span><span class="sxs-lookup"><span data-stu-id="47e0b-109">Description</span></span>                                                                                                 |
|--------------|-------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="47e0b-110">1</span><span class="sxs-lookup"><span data-stu-id="47e0b-110">1</span></span>            | <span data-ttu-id="47e0b-111">伺服器和用戶端接受由另一方針對 EAP-TLS 驗證傳送的所有用途憑證。</span><span class="sxs-lookup"><span data-stu-id="47e0b-111">Server and client accept all-purpose certificates sent by the other party for EAP-TLS authentication.</span></span>       |
| <span data-ttu-id="47e0b-112">其他值</span><span class="sxs-lookup"><span data-stu-id="47e0b-112">Other values</span></span> | <span data-ttu-id="47e0b-113">伺服器和用戶端不接受由另一方針對 EAP-TLS 驗證傳送的所有用途憑證</span><span class="sxs-lookup"><span data-stu-id="47e0b-113">Server and client do not accept all-purpose certificates sent by the other party for EAP-TLS authentication</span></span> |



 

<span data-ttu-id="47e0b-114">如果此登錄值不存在，伺服器和用戶端會接受由另一方針對 EAP-TLS 驗證傳送的所有用途憑證。</span><span class="sxs-lookup"><span data-stu-id="47e0b-114">If this registry value is not present, the server and client accept all-purpose certificates sent by the other party for EAP-TLS authentication.</span></span>

## <a name="related-topics"></a><span data-ttu-id="47e0b-115">相關主題</span><span class="sxs-lookup"><span data-stu-id="47e0b-115">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="47e0b-116">EAPHost 登錄設定</span><span class="sxs-lookup"><span data-stu-id="47e0b-116">EAPHost Registry Settings</span></span>](eaphost-registry-settings.md)
</dt> </dl>

 

 




