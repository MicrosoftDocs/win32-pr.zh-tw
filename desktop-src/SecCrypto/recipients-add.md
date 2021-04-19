---
description: 將憑證物件加入至收件者集合。
ms.assetid: 2a1b9e0f-ccbf-4042-871b-397de6b6fc35
title: 收件者. 新增方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Add
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 255d17485e3423d50cd86b092c2120605f0f1106
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106989746"
---
# <a name="recipientsadd-method"></a><span data-ttu-id="62cd4-103">收件者. 新增方法</span><span class="sxs-lookup"><span data-stu-id="62cd4-103">Recipients.Add method</span></span>

<span data-ttu-id="62cd4-104">\[**Add** 方法可用於 [需求] 區段中指定的作業系統。</span><span class="sxs-lookup"><span data-stu-id="62cd4-104">\[The **Add** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="62cd4-105">相反地，請使用 [**CmsRecipientCollection 類別**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="62cd4-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="62cd4-106">**Add** 方法會將 [**憑證**](certificate.md)物件新增至收件 [**者集合。**](recipients.md)</span><span class="sxs-lookup"><span data-stu-id="62cd4-106">The **Add** method adds a [**Certificate**](certificate.md) object to a [**Recipients**](recipients.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="62cd4-107">語法</span><span class="sxs-lookup"><span data-stu-id="62cd4-107">Syntax</span></span>


```VB
Recipients.Add( _
  ByVal Certificate _
)
```



## <a name="parameters"></a><span data-ttu-id="62cd4-108">參數</span><span class="sxs-lookup"><span data-stu-id="62cd4-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="62cd4-109">*憑證* \[在\]</span><span class="sxs-lookup"><span data-stu-id="62cd4-109">*Certificate* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="62cd4-110">解析為要加入至集合之 [**憑證**](certificate.md) 物件的運算式。</span><span class="sxs-lookup"><span data-stu-id="62cd4-110">Expression that resolves to the [**Certificate**](certificate.md) object to be added to the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="62cd4-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="62cd4-111">Return value</span></span>

<span data-ttu-id="62cd4-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="62cd4-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="62cd4-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="62cd4-113">Requirements</span></span>



| <span data-ttu-id="62cd4-114">需求</span><span class="sxs-lookup"><span data-stu-id="62cd4-114">Requirement</span></span> | <span data-ttu-id="62cd4-115">值</span><span class="sxs-lookup"><span data-stu-id="62cd4-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="62cd4-116">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="62cd4-116">Redistributable</span></span><br/> | <span data-ttu-id="62cd4-117">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="62cd4-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="62cd4-118">DLL</span><span class="sxs-lookup"><span data-stu-id="62cd4-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="62cd4-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="62cd4-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="62cd4-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="62cd4-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="62cd4-121">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="62cd4-121">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="62cd4-122">**收件者**</span><span class="sxs-lookup"><span data-stu-id="62cd4-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
