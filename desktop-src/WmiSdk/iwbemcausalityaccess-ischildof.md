---
description: IsChildOf 方法會判斷要求是否為指定要求 (pId) 的子系。
ms.assetid: 7be52496-7dcf-41c0-853a-859810a57d21
ms.tgt_platform: multiple
title: 'IWbemCausalityAccess：： IsChildOf 方法 (Wbemint .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.IsChildOf
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 6deec7521ceb58a76db3dbf8064ccc444019cb9d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104193863"
---
# <a name="iwbemcausalityaccessischildof-method"></a><span data-ttu-id="27f7c-103">IWbemCausalityAccess：： IsChildOf 方法</span><span class="sxs-lookup"><span data-stu-id="27f7c-103">IWbemCausalityAccess::IsChildOf method</span></span>

<span data-ttu-id="27f7c-104">**IsChildOf** 方法會判斷要求是否為指定要求 (pId) 的子系。</span><span class="sxs-lookup"><span data-stu-id="27f7c-104">The **IsChildOf** method determines if a request is a child of a specified request (pId).</span></span> <span data-ttu-id="27f7c-105">父要求可以有多個子要求。</span><span class="sxs-lookup"><span data-stu-id="27f7c-105">A parent request can have multiple child requests.</span></span> <span data-ttu-id="27f7c-106">每個要求都是由全域唯一識別碼 (GUID) 來識別，而且可以有父要求或可能是最上層要求。</span><span class="sxs-lookup"><span data-stu-id="27f7c-106">Each request is identified by a Globally Unique Identifier (GUID) and can have a parent request or can be a top request.</span></span> <span data-ttu-id="27f7c-107">GUID 是唯一的128位數位。</span><span class="sxs-lookup"><span data-stu-id="27f7c-107">A GUID is a unique 128-bit number.</span></span>

## <a name="syntax"></a><span data-ttu-id="27f7c-108">語法</span><span class="sxs-lookup"><span data-stu-id="27f7c-108">Syntax</span></span>


```C++
HRESULT IsChildOf(
  [in] REQUESTID pId
);
```



## <a name="parameters"></a><span data-ttu-id="27f7c-109">參數</span><span class="sxs-lookup"><span data-stu-id="27f7c-109">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="27f7c-110">*pId* \[在\]</span><span class="sxs-lookup"><span data-stu-id="27f7c-110">*pId* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="27f7c-111">可唯一識別要求的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="27f7c-111">The GUID value that uniquely identifies a request.</span></span> <span data-ttu-id="27f7c-112">例如，5b2fc63a-8af4-44cb-960c-aefdced908d6。</span><span class="sxs-lookup"><span data-stu-id="27f7c-112">For example, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="27f7c-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="27f7c-113">Return value</span></span>

<span data-ttu-id="27f7c-114">如果指定的要求是呼叫 **IsChildOf** 方法之要求的子系，則會傳回成功。</span><span class="sxs-lookup"><span data-stu-id="27f7c-114">Returns successful if the specified request is a child of the request calling the **IsChildOf** method.</span></span>

## <a name="requirements"></a><span data-ttu-id="27f7c-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="27f7c-115">Requirements</span></span>



| <span data-ttu-id="27f7c-116">需求</span><span class="sxs-lookup"><span data-stu-id="27f7c-116">Requirement</span></span> | <span data-ttu-id="27f7c-117">值</span><span class="sxs-lookup"><span data-stu-id="27f7c-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="27f7c-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="27f7c-118">Minimum supported client</span></span><br/> | <span data-ttu-id="27f7c-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="27f7c-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="27f7c-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="27f7c-120">Minimum supported server</span></span><br/> | <span data-ttu-id="27f7c-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="27f7c-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="27f7c-122">標頭</span><span class="sxs-lookup"><span data-stu-id="27f7c-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="27f7c-123"><dt>Wbemint。h</dt></span><span class="sxs-lookup"><span data-stu-id="27f7c-123"><dt>Wbemint.h</dt></span></span> </dl>    |
| <span data-ttu-id="27f7c-124">DLL</span><span class="sxs-lookup"><span data-stu-id="27f7c-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="27f7c-125"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="27f7c-125"><dt>Fastprox.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="27f7c-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="27f7c-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="27f7c-127">**IWbemCausalityAccess**</span><span class="sxs-lookup"><span data-stu-id="27f7c-127">**IWbemCausalityAccess**</span></span>](iwbemcausalityaccess.md)
</dt> </dl>

 

 




