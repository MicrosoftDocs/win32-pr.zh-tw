---
title: 'WINBIO_SETTING_SOURCE 常數 (Winbio \_ 類型 .h) '
description: 判斷 Windows 生物特徵辨識架構目前是否已啟用。
ms.assetid: d95aa6cc-ddff-40fb-ab82-eac78dc0cb6b
topic_type:
- apiref
api_name:
- WINBIO_SETTING_SOURCE_INVALID
- WINBIO_SETTING_SOURCE_DEFAULT
- WINBIO_SETTING_SOURCE_POLICY
- WINBIO_SETTING_SOURCE_LOCAL
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b54723612c7e0948e09baddf22ad4f4703ca5c38
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103935064"
---
# <a name="winbio_setting_source-constants"></a><span data-ttu-id="a99ef-103">WINBIO \_ 設定 \_ 來源常數</span><span class="sxs-lookup"><span data-stu-id="a99ef-103">WINBIO\_SETTING\_SOURCE Constants</span></span>

<span data-ttu-id="a99ef-104">[**WinBioGetEnabledSetting**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting)函式會使用下列常數來判斷 Windows 生物特徵辨識架構目前是否已啟用。</span><span class="sxs-lookup"><span data-stu-id="a99ef-104">The following constants are used by the [**WinBioGetEnabledSetting**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting) function to determine whether the Windows Biometric Framework is currently enabled.</span></span> <span data-ttu-id="a99ef-105">常數會指定設定的來源位置。</span><span class="sxs-lookup"><span data-stu-id="a99ef-105">The constants specify where the setting originated.</span></span>



| <span data-ttu-id="a99ef-106">常數</span><span class="sxs-lookup"><span data-stu-id="a99ef-106">Constant</span></span>                                                                                                                                                                                                        | <span data-ttu-id="a99ef-107">描述</span><span class="sxs-lookup"><span data-stu-id="a99ef-107">Description</span></span>                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| <span id="WINBIO_SETTING_SOURCE_INVALID"></span><span id="winbio_setting_source_invalid"></span><dl> <span data-ttu-id="a99ef-108"><dt>**WINBIO \_ 設定 \_ 來源 \_ 無效**</dt></span><span class="sxs-lookup"><span data-stu-id="a99ef-108"><dt>**WINBIO\_SETTING\_SOURCE\_INVALID**</dt></span></span> </dl> | <span data-ttu-id="a99ef-109">設定無效。</span><span class="sxs-lookup"><span data-stu-id="a99ef-109">The setting is not valid.</span></span><br/>                              |
| <span id="WINBIO_SETTING_SOURCE_DEFAULT"></span><span id="winbio_setting_source_default"></span><dl> <span data-ttu-id="a99ef-110"><dt>**WINBIO \_ 設定 \_ 來源 \_ 預設值**</dt></span><span class="sxs-lookup"><span data-stu-id="a99ef-110"><dt>**WINBIO\_SETTING\_SOURCE\_DEFAULT**</dt></span></span> </dl> | <span data-ttu-id="a99ef-111">設定源自內建原則。</span><span class="sxs-lookup"><span data-stu-id="a99ef-111">The setting originated from built-in policy.</span></span><br/>           |
| <span id="WINBIO_SETTING_SOURCE_POLICY"></span><span id="winbio_setting_source_policy"></span><dl> <span data-ttu-id="a99ef-112"><dt>**WINBIO \_ 設定 \_ 來源 \_ 原則**</dt></span><span class="sxs-lookup"><span data-stu-id="a99ef-112"><dt>**WINBIO\_SETTING\_SOURCE\_POLICY**</dt></span></span> </dl>    | <span data-ttu-id="a99ef-113">這項設定源自本機電腦登錄中。</span><span class="sxs-lookup"><span data-stu-id="a99ef-113">The setting originated in the local computer registry.</span></span><br/> |
| <span id="WINBIO_SETTING_SOURCE_LOCAL"></span><span id="winbio_setting_source_local"></span><dl> <span data-ttu-id="a99ef-114"><dt>**WINBIO \_ 設定 \_ 來源 \_ 本機**</dt></span><span class="sxs-lookup"><span data-stu-id="a99ef-114"><dt>**WINBIO\_SETTING\_SOURCE\_LOCAL**</dt></span></span> </dl>       | <span data-ttu-id="a99ef-115">設定由群組原則建立</span><span class="sxs-lookup"><span data-stu-id="a99ef-115">The setting was created by Group Policy</span></span><br/>                |



## <a name="requirements"></a><span data-ttu-id="a99ef-116">規格需求</span><span class="sxs-lookup"><span data-stu-id="a99ef-116">Requirements</span></span>



| <span data-ttu-id="a99ef-117">需求</span><span class="sxs-lookup"><span data-stu-id="a99ef-117">Requirement</span></span> | <span data-ttu-id="a99ef-118">值</span><span class="sxs-lookup"><span data-stu-id="a99ef-118">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| <span data-ttu-id="a99ef-119">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a99ef-119">Minimum supported client</span></span><br/> | <span data-ttu-id="a99ef-120">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a99ef-120">Windows 7 \[desktop apps only\]</span></span><br/>                                                                    |
| <span data-ttu-id="a99ef-121">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a99ef-121">Minimum supported server</span></span><br/> | <span data-ttu-id="a99ef-122">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a99ef-122">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                                                       |
| <span data-ttu-id="a99ef-123">標頭</span><span class="sxs-lookup"><span data-stu-id="a99ef-123">Header</span></span><br/>                   | <dl> <span data-ttu-id="a99ef-124"><dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt></span><span class="sxs-lookup"><span data-stu-id="a99ef-124"><dt>Winbio\_types.h (include Winbio.h)</dt></span></span> </dl> |



## <a name="see-also"></a><span data-ttu-id="a99ef-125">另請參閱</span><span class="sxs-lookup"><span data-stu-id="a99ef-125">See also</span></span>

<dl> <dt>

[<span data-ttu-id="a99ef-126">用戶端應用程式常數</span><span class="sxs-lookup"><span data-stu-id="a99ef-126">Client Application Constants</span></span>](client-application-constants.md)
</dt> </dl>

 

 





