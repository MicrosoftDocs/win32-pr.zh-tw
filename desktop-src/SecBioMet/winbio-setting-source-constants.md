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
# <a name="winbio_setting_source-constants"></a>WINBIO \_ 設定 \_ 來源常數

[**WinBioGetEnabledSetting**](/windows/desktop/api/Winbio/nf-winbio-winbiogetenabledsetting)函式會使用下列常數來判斷 Windows 生物特徵辨識架構目前是否已啟用。 常數會指定設定的來源位置。



| 常數                                                                                                                                                                                                        | 描述                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:------------------------------------------------------------------|
| <span id="WINBIO_SETTING_SOURCE_INVALID"></span><span id="winbio_setting_source_invalid"></span><dl> <dt>**WINBIO \_ 設定 \_ 來源 \_ 無效**</dt> </dl> | 設定無效。<br/>                              |
| <span id="WINBIO_SETTING_SOURCE_DEFAULT"></span><span id="winbio_setting_source_default"></span><dl> <dt>**WINBIO \_ 設定 \_ 來源 \_ 預設值**</dt> </dl> | 設定源自內建原則。<br/>           |
| <span id="WINBIO_SETTING_SOURCE_POLICY"></span><span id="winbio_setting_source_policy"></span><dl> <dt>**WINBIO \_ 設定 \_ 來源 \_ 原則**</dt> </dl>    | 這項設定源自本機電腦登錄中。<br/> |
| <span id="WINBIO_SETTING_SOURCE_LOCAL"></span><span id="winbio_setting_source_local"></span><dl> <dt>**WINBIO \_ 設定 \_ 來源 \_ 本機**</dt> </dl>       | 設定由群組原則建立<br/>                |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                                    |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 R2 \[ desktop 應用程式\]<br/>                                                       |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[用戶端應用程式常數](client-application-constants.md)
</dt> </dl>

 

 





