---
description: 取得設定檔中的所有可用屬性識別碼。
ms.assetid: 9ef2abdd-0b33-4be3-a124-7795f42d5e55
title: 'IScanProfile：： GetAllPropIDs 方法 (Scanprofile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetAllPropIDs
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 34cd00f626bea3b8f1350950f0d2012ce019068e
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106966758"
---
# <a name="iscanprofilegetallpropids-method"></a><span data-ttu-id="5a1c8-103">IScanProfile：： GetAllPropIDs 方法</span><span class="sxs-lookup"><span data-stu-id="5a1c8-103">IScanProfile::GetAllPropIDs method</span></span>

<span data-ttu-id="5a1c8-104">取得設定檔中的所有可用屬性識別碼。</span><span class="sxs-lookup"><span data-stu-id="5a1c8-104">Gets all available property IDs in a profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="5a1c8-105">語法</span><span class="sxs-lookup"><span data-stu-id="5a1c8-105">Syntax</span></span>


```C++
HRESULT GetAllPropIDs(
  [in, out] ULONG  *num,
  [out]     PROPID *ppid
);
```



## <a name="parameters"></a><span data-ttu-id="5a1c8-106">參數</span><span class="sxs-lookup"><span data-stu-id="5a1c8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="5a1c8-107">*num* \[in、out\]</span><span class="sxs-lookup"><span data-stu-id="5a1c8-107">*num* \[in, out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a1c8-108">類型： \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="5a1c8-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="5a1c8-109">要求或傳回的屬性識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="5a1c8-109">The number of property IDs requested or returned.</span></span>

</dd> <dt>

<span data-ttu-id="5a1c8-110">_ppid \* \[ out\]</span><span class="sxs-lookup"><span data-stu-id="5a1c8-110">_ppid\* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="5a1c8-111">類型： \**PROPID \** _</span><span class="sxs-lookup"><span data-stu-id="5a1c8-111">Type: \**PROPID\** _</span></span>

<span data-ttu-id="5a1c8-112">屬性識別碼陣列的指標。</span><span class="sxs-lookup"><span data-stu-id="5a1c8-112">A pointer to an array of property IDs.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="5a1c8-113">傳回值</span><span class="sxs-lookup"><span data-stu-id="5a1c8-113">Return value</span></span>

<span data-ttu-id="5a1c8-114">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="5a1c8-114">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="5a1c8-115">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="5a1c8-115">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="5a1c8-116">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="5a1c8-116">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="5a1c8-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="5a1c8-117">Requirements</span></span>



| <span data-ttu-id="5a1c8-118">需求</span><span class="sxs-lookup"><span data-stu-id="5a1c8-118">Requirement</span></span> | <span data-ttu-id="5a1c8-119">值</span><span class="sxs-lookup"><span data-stu-id="5a1c8-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="5a1c8-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="5a1c8-120">Minimum supported client</span></span><br/> | <span data-ttu-id="5a1c8-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a1c8-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="5a1c8-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="5a1c8-122">Minimum supported server</span></span><br/> | <span data-ttu-id="5a1c8-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="5a1c8-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="5a1c8-124">標頭</span><span class="sxs-lookup"><span data-stu-id="5a1c8-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="5a1c8-125"><dt>Scanprofile。h</dt></span><span class="sxs-lookup"><span data-stu-id="5a1c8-125"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="5a1c8-126">Idl</span><span class="sxs-lookup"><span data-stu-id="5a1c8-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="5a1c8-127"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="5a1c8-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="5a1c8-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="5a1c8-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="5a1c8-129">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="5a1c8-129">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="5a1c8-130">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="5a1c8-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




