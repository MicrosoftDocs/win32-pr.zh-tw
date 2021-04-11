---
description: 刪除您的應用程式執行所在系統中使用者可用的所有掃描設定檔。
ms.assetid: 1a79fd0e-1309-4fc4-863f-6dfb20594d91
title: 'IScanProfileMgr：:D eleteAllProfilesForUser 方法 (Scanprofilemgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.DeleteAllProfilesForUser
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: c5d723379bb542346e3612f70c19a1629d325ebe
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104113908"
---
# <a name="iscanprofilemgrdeleteallprofilesforuser-method"></a><span data-ttu-id="3931e-103">IScanProfileMgr：:D eleteAllProfilesForUser 方法</span><span class="sxs-lookup"><span data-stu-id="3931e-103">IScanProfileMgr::DeleteAllProfilesForUser method</span></span>

<span data-ttu-id="3931e-104">刪除您的應用程式執行所在系統中使用者可用的所有掃描設定檔。</span><span class="sxs-lookup"><span data-stu-id="3931e-104">Deletes all the scan profiles available for the user in the system that your application is running under.</span></span>

## <a name="syntax"></a><span data-ttu-id="3931e-105">語法</span><span class="sxs-lookup"><span data-stu-id="3931e-105">Syntax</span></span>


```C++
HRESULT DeleteAllProfilesForUser();
```



## <a name="parameters"></a><span data-ttu-id="3931e-106">參數</span><span class="sxs-lookup"><span data-stu-id="3931e-106">Parameters</span></span>

<span data-ttu-id="3931e-107">這個方法沒有任何參數。</span><span class="sxs-lookup"><span data-stu-id="3931e-107">This method has no parameters.</span></span>

## <a name="return-value"></a><span data-ttu-id="3931e-108">傳回值</span><span class="sxs-lookup"><span data-stu-id="3931e-108">Return value</span></span>

<span data-ttu-id="3931e-109">類型： **HRESULT**</span><span class="sxs-lookup"><span data-stu-id="3931e-109">Type: **HRESULT**</span></span>

<span data-ttu-id="3931e-110">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="3931e-110">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3931e-111">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3931e-111">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="3931e-112">規格需求</span><span class="sxs-lookup"><span data-stu-id="3931e-112">Requirements</span></span>



| <span data-ttu-id="3931e-113">需求</span><span class="sxs-lookup"><span data-stu-id="3931e-113">Requirement</span></span> | <span data-ttu-id="3931e-114">值</span><span class="sxs-lookup"><span data-stu-id="3931e-114">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3931e-115">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3931e-115">Minimum supported client</span></span><br/> | <span data-ttu-id="3931e-116">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3931e-116">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="3931e-117">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3931e-117">Minimum supported server</span></span><br/> | <span data-ttu-id="3931e-118">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3931e-118">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3931e-119">標頭</span><span class="sxs-lookup"><span data-stu-id="3931e-119">Header</span></span><br/>                   | <dl> <span data-ttu-id="3931e-120"><dt>Scanprofilemgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="3931e-120"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="3931e-121">Idl</span><span class="sxs-lookup"><span data-stu-id="3931e-121">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3931e-122"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3931e-122"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3931e-123">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3931e-123">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3931e-124">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="3931e-124">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="3931e-125">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="3931e-125">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




