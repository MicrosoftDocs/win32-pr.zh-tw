---
description: 取得設定檔中的屬性識別碼數目。
ms.assetid: fa587c8a-8d09-4dfc-938a-5ec8cc9265f5
title: 'IScanProfile：： GetNumPropIDS 方法 (Scanprofile .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfile.GetNumPropIDS
api_type:
- COM
api_location:
- Scanprofile.h
ms.openlocfilehash: 13d8d276ca4b849fc1a2ae108369f84354d44361
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113913"
---
# <a name="iscanprofilegetnumpropids-method"></a><span data-ttu-id="ab1b8-103">IScanProfile：： GetNumPropIDS 方法</span><span class="sxs-lookup"><span data-stu-id="ab1b8-103">IScanProfile::GetNumPropIDS method</span></span>

<span data-ttu-id="ab1b8-104">取得設定檔中的屬性識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="ab1b8-104">Gets the number of property IDs in a profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="ab1b8-105">語法</span><span class="sxs-lookup"><span data-stu-id="ab1b8-105">Syntax</span></span>


```C++
HRESULT GetNumPropIDS(
  [out] ULONG *num
);
```



## <a name="parameters"></a><span data-ttu-id="ab1b8-106">參數</span><span class="sxs-lookup"><span data-stu-id="ab1b8-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="ab1b8-107">*num* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="ab1b8-107">*num* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="ab1b8-108">類型： \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="ab1b8-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="ab1b8-109">設定檔中的屬性識別碼數目。</span><span class="sxs-lookup"><span data-stu-id="ab1b8-109">The number of property IDs in the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="ab1b8-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="ab1b8-110">Return value</span></span>

<span data-ttu-id="ab1b8-111">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="ab1b8-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="ab1b8-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="ab1b8-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="ab1b8-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="ab1b8-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="ab1b8-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="ab1b8-114">Requirements</span></span>



| <span data-ttu-id="ab1b8-115">需求</span><span class="sxs-lookup"><span data-stu-id="ab1b8-115">Requirement</span></span> | <span data-ttu-id="ab1b8-116">值</span><span class="sxs-lookup"><span data-stu-id="ab1b8-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="ab1b8-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="ab1b8-117">Minimum supported client</span></span><br/> | <span data-ttu-id="ab1b8-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab1b8-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="ab1b8-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="ab1b8-119">Minimum supported server</span></span><br/> | <span data-ttu-id="ab1b8-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="ab1b8-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="ab1b8-121">標頭</span><span class="sxs-lookup"><span data-stu-id="ab1b8-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="ab1b8-122"><dt>Scanprofile。h</dt></span><span class="sxs-lookup"><span data-stu-id="ab1b8-122"><dt>Scanprofile.h</dt></span></span> </dl>    |
| <span data-ttu-id="ab1b8-123">Idl</span><span class="sxs-lookup"><span data-stu-id="ab1b8-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="ab1b8-124"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="ab1b8-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="ab1b8-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="ab1b8-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="ab1b8-126">**IScanProfile**</span><span class="sxs-lookup"><span data-stu-id="ab1b8-126">**IScanProfile**</span></span>](-wia-iscanprofile.md)
</dt> <dt>

[<span data-ttu-id="ab1b8-127">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="ab1b8-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




