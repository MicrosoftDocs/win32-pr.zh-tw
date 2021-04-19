---
title: WCS 特定的錯誤碼
description: 以下是與使用 WCS 1.0 特別相關的錯誤碼清單。
ms.assetid: c6a0cacc-f83e-4f5c-9002-7718bb2ffb6c
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3040f462ce226ebd3018070abc818884cee6ad6
ms.sourcegitcommit: 9bf844f41bd6451b8508d93e722e88a43e913b56
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/02/2021
ms.locfileid: "106985787"
---
# <a name="error-codes-specific-to-wcs"></a><span data-ttu-id="7eb3e-103">WCS 特定的錯誤碼</span><span class="sxs-lookup"><span data-stu-id="7eb3e-103">Error Codes Specific To WCS</span></span>

<span data-ttu-id="7eb3e-104">以下是與使用 WCS 1.0 特別相關的錯誤碼清單。</span><span class="sxs-lookup"><span data-stu-id="7eb3e-104">The following is a list of error codes that are specifically related to the use of WCS 1.0.</span></span> <span data-ttu-id="7eb3e-105">這並不表示 WCS 函數只會傳回這些錯誤碼。</span><span class="sxs-lookup"><span data-stu-id="7eb3e-105">This does not mean that WCS functions will return only these error codes.</span></span> <span data-ttu-id="7eb3e-106">這表示，下表中的程式碼只會由 WCS 函數傳回。</span><span class="sxs-lookup"><span data-stu-id="7eb3e-106">It means that the codes in the table below are returned only by WCS functions.</span></span> <span data-ttu-id="7eb3e-107">它們也可能會傳回其他 Win32 錯誤碼，該錯誤碼記載于平臺 SDK 的 WIN32 API 中的其他位置。</span><span class="sxs-lookup"><span data-stu-id="7eb3e-107">They may also return other Win32 error codes that are documented elsewhere in the Win32 API of the Platform SDK.</span></span>

<dl> <dt>

<span data-ttu-id="7eb3e-108"><span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>\_刪除 \_ ICM \_ XFORM 時發生錯誤</span><span class="sxs-lookup"><span data-stu-id="7eb3e-108"><span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>ERROR\_DELETING\_ICM\_XFORM</span></span>
</dt> <dd>

<span data-ttu-id="7eb3e-109">無法刪除指定的色彩轉換。</span><span class="sxs-lookup"><span data-stu-id="7eb3e-109">The specified color transform could not be deleted.</span></span>

</dd> <dt>

<span data-ttu-id="7eb3e-110"><span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>錯誤 \_ 重複 \_ 標記</span><span class="sxs-lookup"><span data-stu-id="7eb3e-110"><span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>ERROR\_DUPLICATE\_TAG</span></span>
</dt> <dd>

<span data-ttu-id="7eb3e-111">色彩設定檔中已經有指定的色彩設定檔元素標記。</span><span class="sxs-lookup"><span data-stu-id="7eb3e-111">The specified color profile element tag is already present in the color profile.</span></span>

</dd> <dt>

<span data-ttu-id="7eb3e-112"><span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>錯誤 \_ ICM \_ 未 \_ 啟用</span><span class="sxs-lookup"><span data-stu-id="7eb3e-112"><span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>ERROR\_ICM\_NOT\_ENABLED</span></span>
</dt> <dd>

<span data-ttu-id="7eb3e-113">影像色彩管理目前未啟用。</span><span class="sxs-lookup"><span data-stu-id="7eb3e-113">Image Color Management is not currently enabled.</span></span>

</dd> <dt>

<span data-ttu-id="7eb3e-114"><span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>錯誤 \_ 不正確 \_ CMM</span><span class="sxs-lookup"><span data-stu-id="7eb3e-114"><span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>ERROR\_INVALID\_CMM</span></span>
</dt> <dd>

<span data-ttu-id="7eb3e-115">指定的檔案名未參考有效的色彩管理模組。</span><span class="sxs-lookup"><span data-stu-id="7eb3e-115">The specified file name does not refer to a valid color management module.</span></span>

</dd> <dt>

<span data-ttu-id="7eb3e-116"><span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>錯誤 \_ 無效 \_ COLORSPACE</span><span class="sxs-lookup"><span data-stu-id="7eb3e-116"><span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>ERROR\_INVALID\_COLORSPACE</span></span>
</dt> <dd>

<span data-ttu-id="7eb3e-117">指定的色彩空間無效。</span><span class="sxs-lookup"><span data-stu-id="7eb3e-117">The specified color space is invalid.</span></span>

</dd> <dt>

<span data-ttu-id="7eb3e-118"><span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>錯誤 \_ 不正確 \_ 設定檔</span><span class="sxs-lookup"><span data-stu-id="7eb3e-118"><span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>ERROR\_INVALID\_PROFILE</span></span>
</dt> <dd>

<span data-ttu-id="7eb3e-119">指定的檔案名未參考有效的色彩設定檔。</span><span class="sxs-lookup"><span data-stu-id="7eb3e-119">The specified file name does not refer to a valid color profile.</span></span>

</dd> <dt>

<span data-ttu-id="7eb3e-120"><span id="ERROR_INVALID_TRANSFORM_"></span><span id="error_invalid_transform_"></span>錯誤 \_ 不正確 \_ 轉換</span><span class="sxs-lookup"><span data-stu-id="7eb3e-120"><span id="ERROR_INVALID_TRANSFORM_"></span><span id="error_invalid_transform_"></span>ERROR\_INVALID\_TRANSFORM</span></span> 
</dt> <dd>

<span data-ttu-id="7eb3e-121">指定的色彩轉換不是有效的色彩轉換。</span><span class="sxs-lookup"><span data-stu-id="7eb3e-121">The color transform that was specified is not a valid color transform.</span></span>

</dd> <dt>

<span data-ttu-id="7eb3e-122"><span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>錯誤 \_ 配置 \_ 檔 \_ 未 \_ 與 \_ 裝置相關聯</span><span class="sxs-lookup"><span data-stu-id="7eb3e-122"><span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>ERROR\_PROFILE\_NOT\_ASSOCIATED\_WITH\_DEVICE</span></span>
</dt> <dd>

<span data-ttu-id="7eb3e-123">指定的色彩設定檔未與任何裝置建立關聯。</span><span class="sxs-lookup"><span data-stu-id="7eb3e-123">The specified color profile is not associated with any device.</span></span>

</dd> <dt>

<span data-ttu-id="7eb3e-124"><span id="ERROR_PROFILE_NOT_FOUND_"></span><span id="error_profile_not_found_"></span>\_ \_ 找不到錯誤設定檔 \_</span><span class="sxs-lookup"><span data-stu-id="7eb3e-124"><span id="ERROR_PROFILE_NOT_FOUND_"></span><span id="error_profile_not_found_"></span>ERROR\_PROFILE\_NOT\_FOUND</span></span> 
</dt> <dd>

<span data-ttu-id="7eb3e-125">找不到指定的色彩設定檔名稱。</span><span class="sxs-lookup"><span data-stu-id="7eb3e-125">The specified color profile file name was not found.</span></span> <span data-ttu-id="7eb3e-126">檔案名或路徑不正確。</span><span class="sxs-lookup"><span data-stu-id="7eb3e-126">The file name or path is incorrect.</span></span>

</dd> <dt>

<span data-ttu-id="7eb3e-127"><span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>\_ \_ 找不到錯誤標記 \_</span><span class="sxs-lookup"><span data-stu-id="7eb3e-127"><span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>ERROR\_TAG\_NOT\_FOUND</span></span>
</dt> <dd>

<span data-ttu-id="7eb3e-128">在色彩設定檔中找不到指定的色彩設定檔元素標記。</span><span class="sxs-lookup"><span data-stu-id="7eb3e-128">The specified color profile element tag was not found in the color profile.</span></span>

</dd> <dt>

<span data-ttu-id="7eb3e-129"><span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>錯誤 \_ 標記 \_ 不 \_ 存在</span><span class="sxs-lookup"><span data-stu-id="7eb3e-129"><span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>ERROR\_TAG\_NOT\_PRESENT</span></span>
</dt> <dd>

<span data-ttu-id="7eb3e-130">函數成功所需的色彩設定檔元素標記未傳遞至函式。</span><span class="sxs-lookup"><span data-stu-id="7eb3e-130">A color profile element tag that is required for the function to succeed was not passed to the function.</span></span>

</dd> </dl>

## <a name="related-topics"></a><span data-ttu-id="7eb3e-131">相關主題</span><span class="sxs-lookup"><span data-stu-id="7eb3e-131">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="7eb3e-132">基本色彩管理概念</span><span class="sxs-lookup"><span data-stu-id="7eb3e-132">Basic color management concepts</span></span>](basic-color-management-concepts.md)
</dt> <dt>

[<span data-ttu-id="7eb3e-133">WCS 常數</span><span class="sxs-lookup"><span data-stu-id="7eb3e-133">WCS Constants</span></span>](wcs-constants.md)
</dt> </dl>

 

 




