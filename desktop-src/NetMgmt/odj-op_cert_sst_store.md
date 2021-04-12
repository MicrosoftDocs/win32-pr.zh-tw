---
title: OP_CERT_SST_STORE
description: OP_CERT_SST_STORE IDL 定義
ms.assetid: 6c44756e-29f9-48fc-b678-d2b1f0fb90d4
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: 294d21d730e1cce478088cddb43686706217ec5b
ms.sourcegitcommit: db89157e3be911fdce2e543e99faa31fb2403bc8
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/18/2020
ms.locfileid: "104383434"
---
# <a name="op_cert_sst_store-structure"></a><span data-ttu-id="18ac9-103">OP_CERT_SST_STORE 結構</span><span class="sxs-lookup"><span data-stu-id="18ac9-103">OP_CERT_SST_STORE structure</span></span>

<span data-ttu-id="18ac9-104">包含序列化的憑證存放區。</span><span class="sxs-lookup"><span data-stu-id="18ac9-104">Contains a serialized certificate store.</span></span>

## <a name="syntax"></a><span data-ttu-id="18ac9-105">語法</span><span class="sxs-lookup"><span data-stu-id="18ac9-105">Syntax</span></span>

```C++
typedef struct _OP_CERT_SST_STORE
{
    ULONG                       StoreLocation;
    [string] wchar_t            *pStoreName;
    ULONG                       cbSst;
    [size_is(cbSst)]    PBYTE   pSst;
} OP_CERT_SST_STORE, *POP_CERT_SST_STORE;
```

## <a name="members"></a><span data-ttu-id="18ac9-106">成員</span><span class="sxs-lookup"><span data-stu-id="18ac9-106">Members</span></span>

### <a name="storelocation"></a><span data-ttu-id="18ac9-107">StoreLocation</span><span class="sxs-lookup"><span data-stu-id="18ac9-107">StoreLocation</span></span>

<span data-ttu-id="18ac9-108">包含 [**系統存放區位置**](../seccrypto/system-store-locations.md)中憑證存放區的識別碼。</span><span class="sxs-lookup"><span data-stu-id="18ac9-108">Contains an identifier for the certificate store from [**System Store Locations**](../seccrypto/system-store-locations.md).</span></span>

### <a name="pstorename"></a><span data-ttu-id="18ac9-109">pStoreName</span><span class="sxs-lookup"><span data-stu-id="18ac9-109">pStoreName</span></span>

<span data-ttu-id="18ac9-110">包含存放區的名稱。</span><span class="sxs-lookup"><span data-stu-id="18ac9-110">Contains the name of the store.</span></span>

### <a name="cbsst"></a><span data-ttu-id="18ac9-111">cbSst</span><span class="sxs-lookup"><span data-stu-id="18ac9-111">cbSst</span></span>

<span data-ttu-id="18ac9-112">包含 pSst 的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="18ac9-112">Contains the size of pSst in bytes.</span></span>

### <a name="psst"></a><span data-ttu-id="18ac9-113">pSst</span><span class="sxs-lookup"><span data-stu-id="18ac9-113">pSst</span></span>

<span data-ttu-id="18ac9-114">包含序列化的憑證存放區 (請參閱 [**RFC 7292**](https://tools.ietf.org/html/rfc7292)) 。</span><span class="sxs-lookup"><span data-stu-id="18ac9-114">Contains a serialized certificate store (see [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).</span></span>

## <a name="see-also"></a><span data-ttu-id="18ac9-115">另請參閱</span><span class="sxs-lookup"><span data-stu-id="18ac9-115">See also</span></span>

[<span data-ttu-id="18ac9-116">**離線網域加入 IDL 定義**</span><span class="sxs-lookup"><span data-stu-id="18ac9-116">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)