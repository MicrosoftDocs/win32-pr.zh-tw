---
description: 取得在您的應用程式執行所在系統中為使用者建立的掃描設定檔數目。
ms.assetid: 0667a885-d61f-4c44-b988-a42242c2678e
title: 'IScanProfileMgr：： GetNumProfiles 方法 (Scanprofilemgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.GetNumProfiles
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: a8c3167bd428054054a32d7823ce57e562501533
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999897"
---
# <a name="iscanprofilemgrgetnumprofiles-method"></a><span data-ttu-id="f843e-103">IScanProfileMgr：： GetNumProfiles 方法</span><span class="sxs-lookup"><span data-stu-id="f843e-103">IScanProfileMgr::GetNumProfiles method</span></span>

<span data-ttu-id="f843e-104">取得在您的應用程式執行所在系統中為使用者建立的掃描設定檔數目。</span><span class="sxs-lookup"><span data-stu-id="f843e-104">Gets the number of scan profiles created for the user in the system that your application is running under.</span></span>

## <a name="syntax"></a><span data-ttu-id="f843e-105">語法</span><span class="sxs-lookup"><span data-stu-id="f843e-105">Syntax</span></span>


```C++
HRESULT GetNumProfiles(
  [out] ULONG *pulNumProfiles
);
```



## <a name="parameters"></a><span data-ttu-id="f843e-106">參數</span><span class="sxs-lookup"><span data-stu-id="f843e-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="f843e-107">*pulNumProfiles* \[擴展\]</span><span class="sxs-lookup"><span data-stu-id="f843e-107">*pulNumProfiles* \[out\]</span></span>
</dt> <dd>

<span data-ttu-id="f843e-108">類型： \**ULONG \** _</span><span class="sxs-lookup"><span data-stu-id="f843e-108">Type: \**ULONG\** _</span></span>

<span data-ttu-id="f843e-109">為使用者建立的設定檔數目的指標。</span><span class="sxs-lookup"><span data-stu-id="f843e-109">A pointer to the number of profiles created for the user.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="f843e-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="f843e-110">Return value</span></span>

<span data-ttu-id="f843e-111">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="f843e-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="f843e-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="f843e-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="f843e-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="f843e-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="requirements"></a><span data-ttu-id="f843e-114">規格需求</span><span class="sxs-lookup"><span data-stu-id="f843e-114">Requirements</span></span>



| <span data-ttu-id="f843e-115">需求</span><span class="sxs-lookup"><span data-stu-id="f843e-115">Requirement</span></span> | <span data-ttu-id="f843e-116">值</span><span class="sxs-lookup"><span data-stu-id="f843e-116">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="f843e-117">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="f843e-117">Minimum supported client</span></span><br/> | <span data-ttu-id="f843e-118">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f843e-118">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="f843e-119">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="f843e-119">Minimum supported server</span></span><br/> | <span data-ttu-id="f843e-120">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="f843e-120">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="f843e-121">標頭</span><span class="sxs-lookup"><span data-stu-id="f843e-121">Header</span></span><br/>                   | <dl> <span data-ttu-id="f843e-122"><dt>Scanprofilemgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="f843e-122"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="f843e-123">Idl</span><span class="sxs-lookup"><span data-stu-id="f843e-123">IDL</span></span><br/>                      | <dl> <span data-ttu-id="f843e-124"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="f843e-124"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="f843e-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="f843e-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="f843e-126">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="f843e-126">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="f843e-127">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="f843e-127">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




