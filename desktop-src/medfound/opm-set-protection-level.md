---
description: 設定輸出保護機制的保護層級。
ms.assetid: f4e63bf5-0749-4054-9f86-7fd88f2881ad
title: 'OPM_SET_PROTECTION_LEVEL (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 17a80fb674c9347dafc3bcf1a62dc4bc909f0471
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974165"
---
# <a name="opm_set_protection_level"></a>OPM \_ SET \_ 保護 \_ 等級

設定輸出保護機制的保護層級。



| 需求 | 值 |
|--------------|-----------------------------------------------------------------------------------------------------|
| 命令 GUID | OPM \_ SET \_ 保護 \_ 等級                                                                         |
| 輸入資料   | [**OPM \_ SET \_ 保護 \_ 層級 \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_protection_level_parameters)結構 |



 

## <a name="remarks"></a>備註

某些連接器可支援多重保護機制。 使用該類型的連接器，您可以將數個保護機制套用至相同的連接器，每個都有不同的設定。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Opmapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IOPMVideoOutput：： Configure**](/windows/desktop/api/opmapi/nf-opmapi-iopmvideooutput-configure)
</dt> <dt>

[OPM 命令](opm-commands.md)
</dt> </dl>

 

 




