---
description: 將指定的掃描設定檔設定為預設設定檔。
ms.assetid: c680be8b-88f0-4f7f-b1a3-e12711dba870
title: 'IScanProfileMgr：： SetDefault 方法 (Scanprofilemgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IScanProfileMgr.SetDefault
api_type:
- COM
api_location:
- Scanprofilemgr.h
ms.openlocfilehash: 3a7c32f246bcafc8ff7ce55e8c6f34ea45553a95
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106982437"
---
# <a name="iscanprofilemgrsetdefault-method"></a><span data-ttu-id="3ad92-103">IScanProfileMgr：： SetDefault 方法</span><span class="sxs-lookup"><span data-stu-id="3ad92-103">IScanProfileMgr::SetDefault method</span></span>

<span data-ttu-id="3ad92-104">將指定的掃描設定檔設定為預設設定檔。</span><span class="sxs-lookup"><span data-stu-id="3ad92-104">Sets the specified scan profile as the default profile.</span></span>

## <a name="syntax"></a><span data-ttu-id="3ad92-105">語法</span><span class="sxs-lookup"><span data-stu-id="3ad92-105">Syntax</span></span>


```C++
HRESULT SetDefault(
  [in] IScanProfile *pScanProfile
);
```



## <a name="parameters"></a><span data-ttu-id="3ad92-106">參數</span><span class="sxs-lookup"><span data-stu-id="3ad92-106">Parameters</span></span>

<dl> <dt>

<span data-ttu-id="3ad92-107">*pScanProfile* \[在\]</span><span class="sxs-lookup"><span data-stu-id="3ad92-107">*pScanProfile* \[in\]</span></span>
</dt> <dd>

<span data-ttu-id="3ad92-108">類型： \**[**IScanProfile**](-wia-iscanprofile.md) \** _</span><span class="sxs-lookup"><span data-stu-id="3ad92-108">Type: \**[**IScanProfile**](-wia-iscanprofile.md)\** _</span></span>

<span data-ttu-id="3ad92-109">設定檔的指標。</span><span class="sxs-lookup"><span data-stu-id="3ad92-109">A pointer to the profile.</span></span>

</dd> </dl>

## <a name="return-value"></a><span data-ttu-id="3ad92-110">傳回值</span><span class="sxs-lookup"><span data-stu-id="3ad92-110">Return value</span></span>

<span data-ttu-id="3ad92-111">類型： _ *HRESULT*\*</span><span class="sxs-lookup"><span data-stu-id="3ad92-111">Type: _ *HRESULT*\*</span></span>

<span data-ttu-id="3ad92-112">如果這個方法成功，它會傳回 **S \_ OK**。</span><span class="sxs-lookup"><span data-stu-id="3ad92-112">If this method succeeds, it returns **S\_OK**.</span></span> <span data-ttu-id="3ad92-113">否則，它會傳回 **HRESULT** 錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="3ad92-113">Otherwise, it returns an **HRESULT** error code.</span></span>

## <a name="remarks"></a><span data-ttu-id="3ad92-114">備註</span><span class="sxs-lookup"><span data-stu-id="3ad92-114">Remarks</span></span>

<span data-ttu-id="3ad92-115">使用 **IScanProfileMgr：： SetDefault** 方法，將專案新增 `<Default>` 至設定檔，或從裝置的先前預設設定檔中移除該元素。</span><span class="sxs-lookup"><span data-stu-id="3ad92-115">Use the **IScanProfileMgr::SetDefault** method to add a `<Default>` element to the profile or to remove that element from the device's previous default profile.</span></span>

<span data-ttu-id="3ad92-116">使用 [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) 方法來變更預設設定檔。</span><span class="sxs-lookup"><span data-stu-id="3ad92-116">Use the [**ScanProfileDialog**](-wia-iscanprofileui-scanprofiledialog.md) method to change the default profile.</span></span>

## <a name="requirements"></a><span data-ttu-id="3ad92-117">規格需求</span><span class="sxs-lookup"><span data-stu-id="3ad92-117">Requirements</span></span>



| <span data-ttu-id="3ad92-118">需求</span><span class="sxs-lookup"><span data-stu-id="3ad92-118">Requirement</span></span> | <span data-ttu-id="3ad92-119">值</span><span class="sxs-lookup"><span data-stu-id="3ad92-119">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------|
| <span data-ttu-id="3ad92-120">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="3ad92-120">Minimum supported client</span></span><br/> | <span data-ttu-id="3ad92-121">\[僅限 Windows Vista 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ad92-121">Windows Vista \[desktop apps only\]</span></span><br/>                                              |
| <span data-ttu-id="3ad92-122">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="3ad92-122">Minimum supported server</span></span><br/> | <span data-ttu-id="3ad92-123">僅限 Windows Server 2008 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="3ad92-123">Windows Server 2008 \[desktop apps only\]</span></span><br/>                                        |
| <span data-ttu-id="3ad92-124">標頭</span><span class="sxs-lookup"><span data-stu-id="3ad92-124">Header</span></span><br/>                   | <dl> <span data-ttu-id="3ad92-125"><dt>Scanprofilemgr。h</dt></span><span class="sxs-lookup"><span data-stu-id="3ad92-125"><dt>Scanprofilemgr.h</dt></span></span> </dl> |
| <span data-ttu-id="3ad92-126">Idl</span><span class="sxs-lookup"><span data-stu-id="3ad92-126">IDL</span></span><br/>                      | <dl> <span data-ttu-id="3ad92-127"><dt>Scanprofiles .idl</dt></span><span class="sxs-lookup"><span data-stu-id="3ad92-127"><dt>Scanprofiles.idl</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="3ad92-128">另請參閱</span><span class="sxs-lookup"><span data-stu-id="3ad92-128">See also</span></span>

<dl> <dt>

[<span data-ttu-id="3ad92-129">**IScanProfileMgr**</span><span class="sxs-lookup"><span data-stu-id="3ad92-129">**IScanProfileMgr**</span></span>](-wia-iscanprofilemgr.md)
</dt> <dt>

[<span data-ttu-id="3ad92-130">掃描設定檔架構</span><span class="sxs-lookup"><span data-stu-id="3ad92-130">Scan Profile Schema</span></span>](-wia-scan-profile-schema.md)
</dt> </dl>

 

 




