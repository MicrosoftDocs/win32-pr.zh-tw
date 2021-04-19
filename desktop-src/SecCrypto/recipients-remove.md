---
description: 從收件者集合移除憑證物件。
ms.assetid: bb75f6d0-4bab-40dd-9d0c-f0431da9c5f3
title: 收件者. 移除方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Recipients.Remove
api_type:
- COM
api_location:
- Capicom.dll
ms.openlocfilehash: 06d276e2d8e75e8822cee3503a7e8342a94a6b0b
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106994227"
---
# <a name="recipientsremove-method"></a><span data-ttu-id="d877c-103">收件者. 移除方法</span><span class="sxs-lookup"><span data-stu-id="d877c-103">Recipients.Remove method</span></span>

<span data-ttu-id="d877c-104">\[**Remove** 方法可在 [需求] 區段中指定的作業系統中使用。</span><span class="sxs-lookup"><span data-stu-id="d877c-104">\[The **Remove** method is available for use in the operating systems specified in the Requirements section.</span></span> <span data-ttu-id="d877c-105">相反地，請使用 [**CmsRecipientCollection 類別**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true)，以使用 [**system.servicemodel 命名空間。**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true)\]</span><span class="sxs-lookup"><span data-stu-id="d877c-105">Instead, use the [**CmsRecipientCollection Class**](/dotnet/api/system.security.cryptography.pkcs.cmsrecipientcollection?view=dotnet-plat-ext-3.1&preserve-view=true) in the [**System.Security.Cryptography.Pkcs**](/dotnet/api/system.security.cryptography.pkcs?view=dotnet-plat-ext-3.1&preserve-view=true) namespace.\]</span></span>

<span data-ttu-id="d877c-106">**Remove** 方法會從收件 [**者集合中**](recipients.md)移除 [**憑證**](certificate.md)物件。</span><span class="sxs-lookup"><span data-stu-id="d877c-106">The **Remove** method removes a [**Certificate**](certificate.md) object from a [**Recipients**](recipients.md) collection.</span></span>

## <a name="syntax"></a><span data-ttu-id="d877c-107">語法</span><span class="sxs-lookup"><span data-stu-id="d877c-107">Syntax</span></span>


```VB
Recipients.Remove( _
  ByVal Index _
)
```



## <a name="parameters"></a><span data-ttu-id="d877c-108">參數</span><span class="sxs-lookup"><span data-stu-id="d877c-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="d877c-109">*索引* \[在\]</span><span class="sxs-lookup"><span data-stu-id="d877c-109">*Index* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="d877c-110">要從集合移除之 [**憑證**](certificate.md) 物件的索引。</span><span class="sxs-lookup"><span data-stu-id="d877c-110">Index of the [**Certificate**](certificate.md) object to be removed from the collection.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="d877c-111">傳回值</span><span class="sxs-lookup"><span data-stu-id="d877c-111">Return value</span></span>

<span data-ttu-id="d877c-112">這個方法不會傳回值。</span><span class="sxs-lookup"><span data-stu-id="d877c-112">This method does not return a value.</span></span>

## <a name="requirements"></a><span data-ttu-id="d877c-113">規格需求</span><span class="sxs-lookup"><span data-stu-id="d877c-113">Requirements</span></span>



| <span data-ttu-id="d877c-114">需求</span><span class="sxs-lookup"><span data-stu-id="d877c-114">Requirement</span></span> | <span data-ttu-id="d877c-115">值</span><span class="sxs-lookup"><span data-stu-id="d877c-115">Value</span></span> |
|----------------------------|----------------------------------------------------------------------------------------|
| <span data-ttu-id="d877c-116">可轉散發套件</span><span class="sxs-lookup"><span data-stu-id="d877c-116">Redistributable</span></span><br/> | <span data-ttu-id="d877c-117">Windows Server 2003 和 Windows XP 上的 CAPICOM 2.0 或更新版本</span><span class="sxs-lookup"><span data-stu-id="d877c-117">CAPICOM 2.0 or later on Windows Server 2003 and Windows XP</span></span><br/>                  |
| <span data-ttu-id="d877c-118">DLL</span><span class="sxs-lookup"><span data-stu-id="d877c-118">DLL</span></span><br/>             | <dl> <span data-ttu-id="d877c-119"><dt>Capicom.dll</dt></span><span class="sxs-lookup"><span data-stu-id="d877c-119"><dt>Capicom.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="d877c-120">另請參閱</span><span class="sxs-lookup"><span data-stu-id="d877c-120">See also</span></span>

<dl> <dt>

[<span data-ttu-id="d877c-121">**加密物件**</span><span class="sxs-lookup"><span data-stu-id="d877c-121">**Cryptography Objects**</span></span>](cryptography-objects.md)
</dt> <dt>

[<span data-ttu-id="d877c-122">**收件者**</span><span class="sxs-lookup"><span data-stu-id="d877c-122">**Recipients**</span></span>](recipients.md)
</dt> </dl>

 

 
