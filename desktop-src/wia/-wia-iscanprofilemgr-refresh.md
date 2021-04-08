---
description: 重新列舉系統中的所有掃描設定檔。
ms.assetid: f5e49645-e81a-4750-8ea5-f0c698a61752
title: 'IScanProfileMgr：： Refresh 方法 (Scanprofilemgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.Refresh
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: e4af44e95889abf35fe13e1669411513458a16c6
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103943583"
---
# <a name="iscanprofilemgrrefresh-method"></a><span data-ttu-id="341d2-103">IScanProfileMgr：： Refresh 方法</span><span class="sxs-lookup"><span data-stu-id="341d2-103">IScanProfileMgr::Refresh method</span></span>

<span data-ttu-id="341d2-104">重新列舉系統中的所有掃描設定檔。</span><span class="sxs-lookup"><span data-stu-id="341d2-104">Re-enumerates all the scan profiles in the system.</span></span>

## <a name="syntax"></a><span data-ttu-id="341d2-105">語法</span><span class="sxs-lookup"><span data-stu-id="341d2-105">Syntax</span></span>


```C++
HRESULT Refresh();
```



## <a name="parameters"></a><span data-ttu-id="341d2-106">參數</span><span class="sxs-lookup"><span data-stu-id="341d2-106">Parameters</span></span>

<span data-ttu-id="341d2-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="341d2-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="341d2-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="341d2-108">Return value</span></span>

<span data-ttu-id="341d2-109">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="341d2-109">Type: **HRESULT**</span></span>

<span data-ttu-id="341d2-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="341d2-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="341d2-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="341d2-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="341d2-112">備註</span><span class="sxs-lookup"><span data-stu-id="341d2-112">Remarks</span></span>

<span data-ttu-id="341d2-113">當有一個以上的 [**IScanProfileMgr**](-wia-iscanprofilemgr.md) 物件可能同時建立或刪除設定檔時，請使用這個方法。</span><span class="sxs-lookup"><span data-stu-id="341d2-113">Use this method when more than one [**IScanProfileMgr**](-wia-iscanprofilemgr.md) object might be creating or deleting profiles at the same time.</span></span>

## <a name="requirements"></a><span data-ttu-id="341d2-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="341d2-114">Requirements</span></span>



| <span data-ttu-id="341d2-115">需求</span><span class="sxs-lookup"><span data-stu-id="341d2-115">Requirement</span></span> | <span data-ttu-id="341d2-116">值</span><span class="sxs-lookup"><span data-stu-id="341d2-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="341d2-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="341d2-117">Minimum supported client</span></span><br/> | <span data-ttu-id="341d2-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="341d2-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="341d2-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="341d2-119">Minimum supported server</span></span><br/> | <span data-ttu-id="341d2-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="341d2-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="341d2-121">標頭</span><span class="sxs-lookup"><span data-stu-id="341d2-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="341d2-122"><dt>Scanprofilemgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="341d2-122"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="341d2-123">Idl</span><span class="sxs-lookup"><span data-stu-id="341d2-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="341d2-124"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="341d2-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="341d2-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="341d2-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="341d2-126">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="341d2-126">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="341d2-127">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="341d2-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




