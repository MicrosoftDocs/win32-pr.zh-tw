---
description: 取得布林值，指出憑證是否為憑證授權單位單位 (CA) 。
ms.assetid: 3ca43475-fe97-4eb4-875d-dbc15a0b953c
title: BasicConstraints. IsCertificateAuthority 屬性
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- BasicConstraints.IsCertificateAuthority
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 5d4878a8cb21f89f3abeeb9e4b530948ef12e9aa
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001924"
---
# <a name="basicconstraintsiscertificateauthority-property"></a><span data-ttu-id="d4932-103">BasicConstraints. IsCertificateAuthority 屬性</span><span class="sxs-lookup"><span data-stu-id="d4932-103">BasicConstraints.IsCertificateAuthority property</span></span>

<span data-ttu-id="d4932-104">\[CAPICOM 是僅限32位的元件，可用於下列作業系統： Windows Server 2008、Windows Vista、Windows XP。</span><span class="sxs-lookup"><span data-stu-id="d4932-104">\[CAPICOM is a 32-bit only component that is available for use in the following operating systems: Windows Server 2008, Windows Vista, Windows XP.</span></span> <span data-ttu-id="d4932-105">請改為使用 [**system.security.cryptography.x509certificates.x509certificate2**](/previous-versions/windows/)命名空間中的 [**X509BasicConstraintsExtension 類別**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1)。\]</span><span class="sxs-lookup"><span data-stu-id="d4932-105">Instead, use the [**X509BasicConstraintsExtension Class**](/dotnet/api/system.security.cryptography.x509certificates.x509basicconstraintsextension?view=netcore-3.1) in the [**System.Security.Cryptography.X509Certificates**](/previous-versions/windows/) namespace.\]</span></span>

<span data-ttu-id="d4932-106">**IsCertificateAuthority** 屬性會取得布林值，指出憑證是否為證書 [*頒發機構*](../secgloss/c-gly.md)單位 (CA) 。</span><span class="sxs-lookup"><span data-stu-id="d4932-106">The **IsCertificateAuthority** property retrieves a Boolean value that indicates whether the certificate is for a [*certification authority*](../secgloss/c-gly.md) (CA).</span></span>

<span data-ttu-id="d4932-107">這個屬性是唯讀的。</span><span class="sxs-lookup"><span data-stu-id="d4932-107">This property is read-only.</span></span>

## <a name="syntax"></a><span data-ttu-id="d4932-108">語法</span><span class="sxs-lookup"><span data-stu-id="d4932-108">Syntax</span></span>


```VB
BasicConstraints.IsCertificateAuthority As Boolean
```



## <a name="property-value"></a><span data-ttu-id="d4932-109">屬性值</span><span class="sxs-lookup"><span data-stu-id="d4932-109">Property value</span></span>

<span data-ttu-id="d4932-110">若 **為 True**，則憑證只能由 CA 使用。</span><span class="sxs-lookup"><span data-stu-id="d4932-110">If **True**, the certificate is to be used only by a CA.</span></span>

## <a name="requirements"></a><span data-ttu-id="d4932-111">規格需求</span><span class="sxs-lookup"><span data-stu-id="d4932-111">Requirements</span></span>



| <span data-ttu-id="d4932-112">需求</span><span class="sxs-lookup"><span data-stu-id="d4932-112">Requirement</span></span> | <span data-ttu-id="d4932-113">值</span><span class="sxs-lookup"><span data-stu-id="d4932-113">Value</span></span> |
|----------------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d4932-114">用戶端支援結束</span><span class="sxs-lookup"><span data-stu-id="d4932-114">End of client support</span></span><br/> | <span data-ttu-id="d4932-115">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="d4932-115">Windows Vista</span></span><br/>                                                               |
| <span data-ttu-id="d4932-116">伺服器支援結束</span><span class="sxs-lookup"><span data-stu-id="d4932-116">End of server support</span></span><br/> | <span data-ttu-id="d4932-117">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="d4932-117">Windows Server 2008</span></span><br/>                                                         |
| <span data-ttu-id="d4932-118">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="d4932-118">Redistributable</span></span><br/>       | <span data-ttu-id="d4932-119">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="d4932-119">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d4932-120">DLL</span><span class="sxs-lookup"><span data-stu-id="d4932-120">DLL</span></span><br/>                   | <dl> <span data-ttu-id="d4932-121"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d4932-121"><dt>Capicom.dll</dt></span></span> </dl> |



 

 
