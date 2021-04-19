---
title: OP_CERT_PFX_STORE
description: OP_CERT_PFX_STORE IDL 定義
ms.assetid: 10773feb-623c-4256-a973-f006ed66d936
ms.topic: reference
ms.date: 10/12/2020
ms.reviewer: jsimmons
ms.openlocfilehash: b07d0b8e5572763cc42fe2f5b19a4dde2cfe2157
ms.sourcegitcommit: 1e64562147b11f90de802c2431173582d066fae6
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/14/2020
ms.locfileid: "106968123"
---
# <a name="op_cert_pfx_store-structure"></a><span data-ttu-id="fb26c-103">OP_CERT_PFX_STORE 結構</span><span class="sxs-lookup"><span data-stu-id="fb26c-103">OP_CERT_PFX_STORE structure</span></span>

<span data-ttu-id="fb26c-104">包含序列化的 PFX 結構。</span><span class="sxs-lookup"><span data-stu-id="fb26c-104">Contains a serialized PFX structure.</span></span>

## <a name="syntax"></a><span data-ttu-id="fb26c-105">語法</span><span class="sxs-lookup"><span data-stu-id="fb26c-105">Syntax</span></span>

```C++
typedef struct _OP_CERT_PFX_STORE
{
    [string] wchar_t            *pTemplateName;
    ULONG                       ulPrivateKeyExportPolicy;
    [string] wchar_t            *pPolicyServerUrl;
    ULONG                       ulPolicyServerUrlFlags;
    [string] wchar_t            *pPolicyServerId;
    ULONG                       cbPfx;
    [size_is(cbPfx)]    PBYTE   pPfx;
} OP_CERT_PFX_STORE, *POP_CERT_PFX_STORE;
```

## <a name="members"></a><span data-ttu-id="fb26c-106">成員</span><span class="sxs-lookup"><span data-stu-id="fb26c-106">Members</span></span>

### <a name="ptemplatename"></a><span data-ttu-id="fb26c-107">pTemplateName</span><span class="sxs-lookup"><span data-stu-id="fb26c-107">pTemplateName</span></span>

<span data-ttu-id="fb26c-108">必須設定為用來建立憑證的憑證範本名稱。</span><span class="sxs-lookup"><span data-stu-id="fb26c-108">Must be set to the name of the certificate template used to create the certificate.</span></span>

### <a name="ulprivatekeyexportpolicy"></a><span data-ttu-id="fb26c-109">ulPrivateKeyExportPolicy</span><span class="sxs-lookup"><span data-stu-id="fb26c-109">ulPrivateKeyExportPolicy</span></span>

<span data-ttu-id="fb26c-110">包含 [**X509PrivateKeyExportFlags**](/windows/win32/api/certenroll/ne-certenroll-x509privatekeyexportflags) 列舉中的一個值。</span><span class="sxs-lookup"><span data-stu-id="fb26c-110">Contains one value from the [**X509PrivateKeyExportFlags**](/windows/win32/api/certenroll/ne-certenroll-x509privatekeyexportflags) enumeration.</span></span>

### <a name="ppolicyserverurl"></a><span data-ttu-id="fb26c-111">pPolicyServerUrl</span><span class="sxs-lookup"><span data-stu-id="fb26c-111">pPolicyServerUrl</span></span>

<span data-ttu-id="fb26c-112">必須設定原則伺服器的 URL。</span><span class="sxs-lookup"><span data-stu-id="fb26c-112">Must be set the URL of the policy server.</span></span>

### <a name="ulpolicyserverurlflags"></a><span data-ttu-id="fb26c-113">ulPolicyServerUrlFlags</span><span class="sxs-lookup"><span data-stu-id="fb26c-113">ulPolicyServerUrlFlags</span></span>

<span data-ttu-id="fb26c-114">包含 [**PolicyServerUrlFlags**](/windows/win32/api/certenroll/ne-certenroll-policyserverurlflags) 列舉中的一個值。</span><span class="sxs-lookup"><span data-stu-id="fb26c-114">Contains one value from the [**PolicyServerUrlFlags**](/windows/win32/api/certenroll/ne-certenroll-policyserverurlflags) enumeration.</span></span>

### <a name="ppolicyserverid"></a><span data-ttu-id="fb26c-115">pPolicyServerId</span><span class="sxs-lookup"><span data-stu-id="fb26c-115">pPolicyServerId</span></span>

<span data-ttu-id="fb26c-116">包含可唯一識別原則伺服器的字串</span><span class="sxs-lookup"><span data-stu-id="fb26c-116">Contains a string that uniquely identifies the policy server</span></span>

### <a name="cbpfx"></a><span data-ttu-id="fb26c-117">cbPfx</span><span class="sxs-lookup"><span data-stu-id="fb26c-117">cbPfx</span></span>

<span data-ttu-id="fb26c-118">包含 pPfx 的大小（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="fb26c-118">Contains the size of pPfx in bytes.</span></span>

### <a name="ppfx"></a><span data-ttu-id="fb26c-119">pPfx</span><span class="sxs-lookup"><span data-stu-id="fb26c-119">pPfx</span></span>

<span data-ttu-id="fb26c-120">包含序列化的 PFX 結構 (請參閱 [**RFC 7292**](https://tools.ietf.org/html/rfc7292)) 。</span><span class="sxs-lookup"><span data-stu-id="fb26c-120">Contains a serialized PFX structure (see [**RFC 7292**](https://tools.ietf.org/html/rfc7292)).</span></span>

## <a name="see-also"></a><span data-ttu-id="fb26c-121">另請參閱</span><span class="sxs-lookup"><span data-stu-id="fb26c-121">See also</span></span>

[<span data-ttu-id="fb26c-122">**離線網域加入 IDL 定義**</span><span class="sxs-lookup"><span data-stu-id="fb26c-122">**Offline Domain Join IDL Definitions**</span></span>](odj-idl.md)
