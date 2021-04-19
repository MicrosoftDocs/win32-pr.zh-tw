---
description: GetRequestId 方法會傳回要求 (GUID) 值的全域唯一識別碼。 GUID 是唯一的128位數位。
ms.assetid: c8df15cf-ab48-491f-ac18-1dad567bbc0b
ms.tgt_platform: multiple
title: 'IWbemCausalityAccess：： GetRequestId 方法 (Wbemint .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IWbemCausalityAccess.GetRequestId
api_type:
- COM
api_location:
- Fastprox.dll
ms.openlocfilehash: 075be627b26d99a8b4f03c5a4a962b41f153c8a0
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106988312"
---
# <a name="iwbemcausalityaccessgetrequestid-method"></a><span data-ttu-id="3d4f2-104">IWbemCausalityAccess：： GetRequestId 方法</span><span class="sxs-lookup"><span data-stu-id="3d4f2-104">IWbemCausalityAccess::GetRequestId method</span></span>

<span data-ttu-id="3d4f2-105">**GetRequestId** 方法會傳回要求 (GUID) 值的全域唯一識別碼。</span><span class="sxs-lookup"><span data-stu-id="3d4f2-105">The **GetRequestId** method returns a Globally Unique Identifier (GUID) value for a request.</span></span> <span data-ttu-id="3d4f2-106">GUID 是唯一的128位數位。</span><span class="sxs-lookup"><span data-stu-id="3d4f2-106">A GUID is a unique 128-bit number.</span></span>

## <a name="syntax"></a><span data-ttu-id="3d4f2-107">語法</span><span class="sxs-lookup"><span data-stu-id="3d4f2-107">Syntax</span></span>


```C++
HRESULT GetRequestId(
  [out] REQUESTID *pId
);
```



## <a name="parameters"></a><span data-ttu-id="3d4f2-108">參數</span><span class="sxs-lookup"><span data-stu-id="3d4f2-108">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3d4f2-109">*pId* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="3d4f2-109">*pId* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="3d4f2-110">可唯一識別要求的 GUID 值。</span><span class="sxs-lookup"><span data-stu-id="3d4f2-110">The GUID value that uniquely identifies a request.</span></span> <span data-ttu-id="3d4f2-111">例如，5b2fc63a-8af4-44cb-960c-aefdced908d6。</span><span class="sxs-lookup"><span data-stu-id="3d4f2-111">For example, 5b2fc63a-8af4-44cb-960c-aefdced908d6.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3d4f2-112">傳回值</span><span class="sxs-lookup"><span data-stu-id="3d4f2-112">Return value</span></span>

<span data-ttu-id="3d4f2-113">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="3d4f2-113">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3d4f2-114">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3d4f2-114">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3d4f2-115">規格需求</span><span class="sxs-lookup"><span data-stu-id="3d4f2-115">Requirements</span></span>



| <span data-ttu-id="3d4f2-116">需求</span><span class="sxs-lookup"><span data-stu-id="3d4f2-116">Requirement</span></span> | <span data-ttu-id="3d4f2-117">值</span><span class="sxs-lookup"><span data-stu-id="3d4f2-117">Value</span></span> |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| <span data-ttu-id="3d4f2-118">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3d4f2-118">Minimum supported client</span></span><br/> | <span data-ttu-id="3d4f2-119">Windows Vista</span><span class="sxs-lookup"><span data-stu-id="3d4f2-119">Windows Vista</span></span><br/>                                                                |
| <span data-ttu-id="3d4f2-120">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3d4f2-120">Minimum supported server</span></span><br/> | <span data-ttu-id="3d4f2-121">Windows Server 2008</span><span class="sxs-lookup"><span data-stu-id="3d4f2-121">Windows Server 2008</span></span><br/>                                                          |
| <span data-ttu-id="3d4f2-122">標頭</span><span class="sxs-lookup"><span data-stu-id="3d4f2-122">Header</span></span><br/>                   | <dl> <span data-ttu-id="3d4f2-123"><dt>Wbemint。h</dt></span><span class="sxs-lookup"><span data-stu-id="3d4f2-123"><dt>Wbemint.h</dt></span></span> </dl>    |
| <span data-ttu-id="3d4f2-124">DLL</span><span class="sxs-lookup"><span data-stu-id="3d4f2-124">DLL</span></span><br/>                      | <dl> <span data-ttu-id="3d4f2-125"><dt>Fastprox.dll</dt></span><span class="sxs-lookup"><span data-stu-id="3d4f2-125"><dt>Fastprox.dll</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3d4f2-126">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3d4f2-126">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3d4f2-127">**IWbemCausalityAccess**</span><span class="sxs-lookup"><span data-stu-id="3d4f2-127">**IWbemCausalityAccess**</span></span>](iwbemcausalityaccess.md)
</dt> </dl>

 

 




