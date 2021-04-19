---
description: 加密函式、介面和物件會使用下列資料類型。
ms.assetid: 9d6a065d-c765-4d17-9f4c-38a984439278
title: 加密資料類型
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f84c6f21faa25e1ccc478c178a3f21458ff589ae
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106984165"
---
# <a name="cryptography-data-types"></a><span data-ttu-id="b35ff-103">加密資料類型</span><span class="sxs-lookup"><span data-stu-id="b35ff-103">Cryptography Data Types</span></span>

<span data-ttu-id="b35ff-104">加密函式、介面和物件會使用下列資料類型。</span><span class="sxs-lookup"><span data-stu-id="b35ff-104">The following data types are used by cryptography functions, interfaces, and objects.</span></span>



| <span data-ttu-id="b35ff-105">資料類型</span><span class="sxs-lookup"><span data-stu-id="b35ff-105">Data type</span></span>                                                                      | <span data-ttu-id="b35ff-106">描述</span><span class="sxs-lookup"><span data-stu-id="b35ff-106">Description</span></span>                                                                                                                                                                                      |
|--------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [<span data-ttu-id="b35ff-107">**ALG \_ 識別碼**</span><span class="sxs-lookup"><span data-stu-id="b35ff-107">**ALG\_ID**</span></span>](alg-id.md)                                                      | <span data-ttu-id="b35ff-108">指定演算法識別碼。</span><span class="sxs-lookup"><span data-stu-id="b35ff-108">Specifies algorithm identifiers.</span></span>                                                                                                                                                                 |
| [<span data-ttu-id="b35ff-109">**HCERT \_ SERVER \_ OCSP \_ 回應**</span><span class="sxs-lookup"><span data-stu-id="b35ff-109">**HCERT\_SERVER\_OCSP\_RESPONSE**</span></span>](hcert-server-ocsp-response.md)            | <span data-ttu-id="b35ff-110">表示與伺服器憑證鏈相關聯之 OCSP 回應的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b35ff-110">Represents a handle to an OCSP response associated with a server certificate chain.</span></span>                                                                                                              |
| [<span data-ttu-id="b35ff-111">**HCRYPTHASH**</span><span class="sxs-lookup"><span data-stu-id="b35ff-111">**HCRYPTHASH**</span></span>](hcrypthash.md)                                               | <span data-ttu-id="b35ff-112">指定 [*雜湊物件*](../secgloss/h-gly.md)的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b35ff-112">Specifies handles to a [*hash object*](../secgloss/h-gly.md).</span></span>                                                                                      |
| [<span data-ttu-id="b35ff-113">**HCRYPTKEY**</span><span class="sxs-lookup"><span data-stu-id="b35ff-113">**HCRYPTKEY**</span></span>](hcryptkey.md)                                                 | <span data-ttu-id="b35ff-114">指定密碼編譯金鑰的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b35ff-114">Specifies handles to cryptographic keys.</span></span>                                                                                                                                                         |
| [<span data-ttu-id="b35ff-115">**HCRYPTOIDFUNCADDR**</span><span class="sxs-lookup"><span data-stu-id="b35ff-115">**HCRYPTOIDFUNCADDR**</span></span>](hcryptoidfuncaddr.md)                                 | <span data-ttu-id="b35ff-116">表示函式的控制碼，這個控制碼可使用 (OID) 的 [*物件識別碼*](../secgloss/o-gly.md) 來安裝。</span><span class="sxs-lookup"><span data-stu-id="b35ff-116">Represents a handle to a function that can be installed by using an [*object identifier*](../secgloss/o-gly.md) (OID).</span></span>                 |
| [<span data-ttu-id="b35ff-117">**HCRYPTOIDFUNCSET**</span><span class="sxs-lookup"><span data-stu-id="b35ff-117">**HCRYPTOIDFUNCSET**</span></span>](hcryptoidfuncset.md)                                   | <span data-ttu-id="b35ff-118">表示可以使用 OID 安裝的一組函式的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b35ff-118">Represents a handle to a set of functions that can be installed by using an OID.</span></span>                                                                                                                 |
| [<span data-ttu-id="b35ff-119">**HCRYPTPROV \_ 舊版**</span><span class="sxs-lookup"><span data-stu-id="b35ff-119">**HCRYPTPROV\_LEGACY**</span></span>](hcryptprov-legacy.md)                                | <span data-ttu-id="b35ff-120">用來取代不再使用 **HCRYPTPROV** 資料類型的 [**HCRYPTPROV**](hcryptprov.md)資料類型。</span><span class="sxs-lookup"><span data-stu-id="b35ff-120">Used to replace the [**HCRYPTPROV**](hcryptprov.md) data type where the **HCRYPTPROV** data type is no longer used.</span></span>                                                                             |
| [<span data-ttu-id="b35ff-121">**HCRYPTPROV \_ 或 \_ NCRYPT \_ 金鑰 \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="b35ff-121">**HCRYPTPROV\_OR\_NCRYPT\_KEY\_HANDLE**</span></span>](hcryptprov-or-ncrypt-key-handle.md) | <span data-ttu-id="b35ff-122">指定 CryptoAPI [*密碼編譯服務提供者*](../secgloss/c-gly.md) (CSP) 或 CNG csp 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b35ff-122">Specifies a handle to a CryptoAPI [*cryptographic service provider*](../secgloss/c-gly.md) (CSP) or CNG CSP.</span></span> |
| [<span data-ttu-id="b35ff-123">**HCRYPTPROV**</span><span class="sxs-lookup"><span data-stu-id="b35ff-123">**HCRYPTPROV**</span></span>](hcryptprov.md)                                               | <span data-ttu-id="b35ff-124">指定 CryptoAPI CSP 的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b35ff-124">Specifies a handle to a CryptoAPI CSP.</span></span>                                                                                                                                                           |
| [<span data-ttu-id="b35ff-125">**KEYSVCC \_ 控制碼**</span><span class="sxs-lookup"><span data-stu-id="b35ff-125">**KEYSVCC\_HANDLE**</span></span>](keysvcc-handle.md)                                      | <span data-ttu-id="b35ff-126">指定金鑰服務的控制碼。</span><span class="sxs-lookup"><span data-stu-id="b35ff-126">Specifies handles to the key service.</span></span>                                                                                                                                                            |



 

 

 
