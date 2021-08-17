---
description: 設定 DVD 播放的 HDCP 保護層級，並遵循 DVD 內容管理系統 (CSS) 規則。
ms.assetid: 8d9ecb9b-8528-4b23-ab2f-234ba2cb7ed0
title: 'OPM_SET_PROTECTION_LEVEL_ACCORDING_TO_CSS_DVD (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2290f8d0dd17e01d482c197a54448a3317b11f80840579c2ddd05f01b6103840
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119101899"
---
# <a name="opm_set_protection_level_according_to_css_dvd"></a>\_ \_ \_ \_ 根據 \_ \_ CSS \_ DVD OPM 設定保護等級

設定 DVD 播放的 HDCP 保護層級，並遵循 DVD 內容管理系統 (CSS) 規則。



| 需求 | 值 |
|--------------|-----------------------------------------------------------------------------------------------------|
| 命令 GUID | \_ \_ \_ \_ 根據 \_ \_ CSS \_ DVD OPM 設定保護等級                                                |
| 輸入資料   | [**OPM \_ SET \_ 保護 \_ 層級 \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)結構 |



 

## <a name="remarks"></a>備註

此命令是用來在播放標準 Dvd 時，設定 High-Bandwidth 數位內容保護 (HDCP) 。 不同于 [**OPM \_ SET \_ PROTECTION \_ LEVEL**](opm-set-protection-level.md) 命令，如果因為某些原因而無法設定 HDCP，此命令不會停止播放。  (DVD CSS 規則包含適用于玩家的「最大努力」布建 ) 。否則，此命令與 **OPM \_ SET \_ PROTECTION \_ LEVEL** 命令相同。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Opmapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IOPMVideoOutput：： Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[OPM 命令](opm-commands.md)
</dt> </dl>

 

 




