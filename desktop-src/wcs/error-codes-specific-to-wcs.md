---
title: WCS 特定的錯誤碼
description: 以下是與使用 WCS 1.0 特別相關的錯誤碼清單。
ms.assetid: c6a0cacc-f83e-4f5c-9002-7718bb2ffb6c
ms.localizationpriority: high
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 46127e27b0f0890e305fee65534b0cce743c086e9e89934797bf2b16b15e9f9d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119814598"
---
# <a name="error-codes-specific-to-wcs"></a>WCS 特定的錯誤碼

以下是與使用 WCS 1.0 特別相關的錯誤碼清單。 這並不表示 WCS 函數只會傳回這些錯誤碼。 這表示，下表中的程式碼只會由 WCS 函數傳回。 它們也可能會傳回其他 Win32 錯誤碼，該錯誤碼記載于平臺 SDK 的 WIN32 API 中的其他位置。

<dl> <dt>

<span id="ERROR_DELETING_ICM_XFORM"></span><span id="error_deleting_icm_xform"></span>\_刪除 \_ ICM \_ XFORM 時發生錯誤
</dt> <dd>

無法刪除指定的色彩轉換。

</dd> <dt>

<span id="ERROR_DUPLICATE_TAG"></span><span id="error_duplicate_tag"></span>錯誤 \_ 重複 \_ 標記
</dt> <dd>

色彩設定檔中已經有指定的色彩設定檔元素標記。

</dd> <dt>

<span id="ERROR_ICM_NOT_ENABLED"></span><span id="error_icm_not_enabled"></span>\_ \_ 未啟用 ICM \_ 錯誤
</dt> <dd>

影像色彩管理目前未啟用。

</dd> <dt>

<span id="ERROR_INVALID_CMM"></span><span id="error_invalid_cmm"></span>錯誤 \_ 不正確 \_ CMM
</dt> <dd>

指定的檔案名未參考有效的色彩管理模組。

</dd> <dt>

<span id="ERROR_INVALID_COLORSPACE"></span><span id="error_invalid_colorspace"></span>錯誤 \_ 無效 \_ COLORSPACE
</dt> <dd>

指定的色彩空間無效。

</dd> <dt>

<span id="ERROR_INVALID_PROFILE"></span><span id="error_invalid_profile"></span>錯誤 \_ 不正確 \_ 設定檔
</dt> <dd>

指定的檔案名未參考有效的色彩設定檔。

</dd> <dt>

<span id="ERROR_INVALID_TRANSFORM_"></span><span id="error_invalid_transform_"></span>錯誤 \_ 不正確 \_ 轉換 
</dt> <dd>

指定的色彩轉換不是有效的色彩轉換。

</dd> <dt>

<span id="ERROR_PROFILE_NOT_ASSOCIATED_WITH_DEVICE"></span><span id="error_profile_not_associated_with_device"></span>錯誤 \_ 配置 \_ 檔 \_ 未 \_ 與 \_ 裝置相關聯
</dt> <dd>

指定的色彩設定檔未與任何裝置建立關聯。

</dd> <dt>

<span id="ERROR_PROFILE_NOT_FOUND_"></span><span id="error_profile_not_found_"></span>\_ \_ 找不到錯誤設定檔 \_ 
</dt> <dd>

找不到指定的色彩設定檔名稱。 檔案名或路徑不正確。

</dd> <dt>

<span id="ERROR_TAG_NOT_FOUND"></span><span id="error_tag_not_found"></span>\_ \_ 找不到錯誤標記 \_
</dt> <dd>

在色彩設定檔中找不到指定的色彩設定檔元素標記。

</dd> <dt>

<span id="ERROR_TAG_NOT_PRESENT"></span><span id="error_tag_not_present"></span>錯誤 \_ 標記 \_ 不 \_ 存在
</dt> <dd>

函數成功所需的色彩設定檔元素標記未傳遞至函式。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[基本色彩管理概念](basic-color-management-concepts.md)
</dt> <dt>

[WCS 常數](wcs-constants.md)
</dt> </dl>

 

 




