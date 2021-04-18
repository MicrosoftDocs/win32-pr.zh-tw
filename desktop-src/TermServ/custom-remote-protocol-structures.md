---
title: 遠端桌面通訊協定提供者結構
description: 自訂遠端通訊協定 API 支援下列結構。
ms.assetid: 45d17758-4554-42aa-aeb9-c8d4e7fc6bb7
ms.tgt_platform: multiple
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a626db328ede3bac9422a9a47ebe55f05953a22d
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106964948"
---
# <a name="remote-desktop-protocol-provider-structures"></a>遠端桌面通訊協定提供者結構

自訂遠端通訊協定 API 支援下列結構。

## <a name="in-this-section"></a>本節內容

<dl> <dt>

[**TSMF \_ \_ \_ 中的支援資料**](tsmf-support-data-in.md)
</dt> <dd>

包含媒體格式的相關資訊。

</dd> <dt>

[**TSMF \_ 支援 \_ 資料 \_ 輸出**](tsmf-support-data-out.md)
</dt> <dd>

包含媒體格式的相關資訊。

</dd> <dt>

[**TSMF \_ 支援 \_ NODEDATA \_**](tsmf-support-nodedata-in.md)
</dt> <dd>

在 TSMF 中使用，可 [**\_ 支援結構 \_ \_ 中的資料**](tsmf-support-data-in.md) ，以包含支援之媒體格式的相關資訊。

</dd> <dt>

[**TSMF \_ 支援 \_ NODEDATA \_**](tsmf-support-nodedata-out.md)
</dt> <dd>

在 TSMF 內使用可 [**\_ 支援 \_ 資料 \_ 輸出**](tsmf-support-data-out.md) 結構，以包含支援之媒體格式的相關資訊。

</dd> <dt>

[**WRDS \_ 連接 \_ 設定**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings)
</dt> <dd>

包含遠端會話的連接設定資訊。

</dd> <dt>

[**WRDS \_ 連接 \_ 設定 \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_connection_settings_1)
</dt> <dd>

包含遠端會話的連接設定資訊。

</dd> <dt>

[**WRDS \_ 動態 \_ 時區 \_ \_ 資訊**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_dynamic_time_zone_information)
</dt> <dd>

包含動態時區資訊。

</dd> <dt>

[**WRDS 接聽程式 \_ \_ 設定**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings)
</dt> <dd>

包含遠端會話的接聽程式設定資訊。

</dd> <dt>

[**WRDS 接聽程式 \_ \_ 設定 \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_listener_settings_1)
</dt> <dd>

包含遠端會話的接聽程式設定。

</dd> <dt>

[**WRDS \_ 設定**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings)
</dt> <dd>

包含遠端會話的原則相關設定資訊。

</dd> <dt>

[**WRDS \_ 設定 \_ 1**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wrds_settings_1)
</dt> <dd>

包含遠端會話的原則相關設定。

</dd> <dt>

[**WTS 快取 \_ \_ 統計資料**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_cache_stats)
</dt> <dd>

包含通訊協定快取統計資料。

</dd> <dt>

[**WTS \_ 顯示 \_ IOCTL**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_display_ioctl)
</dt> <dd>

包含用戶端顯示的相關資訊。

</dd> <dt>

[**WTS \_ 用戶端 \_ 資料**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_client_data)
</dt> <dd>

包含用戶端連接的相關資訊。

</dd> <dt>

[**WTS \_ 授權 \_ 功能**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_license_capabilities)
</dt> <dd>

包含用戶端授權功能的相關資訊。

</dd> <dt>

[**WTS \_ 原則 \_ 資料**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_policy_data)
</dt> <dd>

包含由遠端桌面服務服務傳遞至通訊協定的原則資訊。

</dd> <dt>

[**WTS \_ 屬性 \_ 值**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_property_value)
</dt> <dd>

包含要從通訊協定取得之屬性值的相關資訊。

</dd> <dt>

[**WTS \_ 通訊協定快取 \_**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_cache)
</dt> <dd>

包含快取讀取和快取點擊的數目。

</dd> <dt>

[**WTS \_ 通訊協定 \_ 計數器**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_counters)
</dt> <dd>

包含通訊協定效能計數器。

</dd> <dt>

[**WTS \_ 通訊協定 \_ 狀態**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_protocol_status)
</dt> <dd>

包含通訊協定狀態的相關資訊。

</dd> <dt>

[**WTS \_ 服務 \_ 狀態**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_service_state)
</dt> <dd>

包含遠端桌面服務服務狀態變更的相關資訊。

</dd> <dt>

[**WTS \_ 會話 \_ 識別碼**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_session_id)
</dt> <dd>

包含可唯一識別會話的 **GUID** 。

</dd> <dt>

[**WTS \_ SMALL \_ RECT**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_small_rect)
</dt> <dd>

包含用戶端視窗座標。

</dd> <dt>

[**WTS \_ SOCKADDR**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_sockaddr)
</dt> <dd>

包含通訊端位址。

</dd> <dt>

[**WTS \_ SYSTEMTIME**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_systemtime)
</dt> <dd>

指定標準時間和日光節約時間之間轉換的日期和時間資訊。

</dd> <dt>

[**WTS \_ 時區 \_ \_ 資訊**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_time_zone_information)
</dt> <dd>

包含用戶端時區資訊。

</dd> <dt>

[**WTS \_ 使用者 \_ 認證**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_credential)
</dt> <dd>

包含使用者的認證資訊。

</dd> <dt>

[**WTS \_ 使用者 \_ 資料**](/windows/desktop/api/Wtsdefs/ns-wtsdefs-wts_user_data)
</dt> <dd>

包含選取的用戶端屬性值。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[遠端桌面通訊協定提供者參考](custom-remote-protocol-reference.md)
</dt> <dt>

[遠端桌面通訊協定提供者列舉](custom-remote-protocol-enumerations.md)
</dt> <dt>

[遠端桌面通訊協定提供者介面](custom-remote-protocol-interfaces.md)
</dt> <dt>

[遠端桌面通訊協定提供者聯集](custom-remote-protocol-unions.md)
</dt> </dl>

 

 




