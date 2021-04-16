---
description: 指定除了保護層級以外的視訊訊號相關資訊。
ms.assetid: ed78b7eb-bf15-4068-ab86-ae42a5e62096
title: 'OPM_SET_ACP_AND_CGMSA_SIGNALING (Opmapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 02247c48b89e61d49afe7f8f6f3821da68ff050b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104512577"
---
# <a name="opm_set_acp_and_cgmsa_signaling"></a>OPM \_ 設定 \_ ACP \_ 和 \_ CGMSA \_ 信號

指定除了保護層級以外的視訊訊號相關資訊。



| 需求 | 值 |
|--------------|---------------------------------------------------------------------------------------------------------------------|
| 命令 GUID | OPM \_ 設定 \_ ACP \_ 和 \_ CGMSA \_ 信號                                                                                |
| 輸入資料   | [**OPM \_ 設定 \_ ACP \_ 和 \_ CGMSA \_ 信號 \_ 參數**](/windows/desktop/api/opmapi/ns-opmapi-opm_set_acp_and_cgmsa_signaling_parameters)結構 |



 

## <a name="remarks"></a>備註

此命令相當於 \_ 經認證的輸出保護通訊協定 (COPP) 中所使用的 DXVA COPPSetSignaling 命令。

針對 CGMS-A，某些保護標準需要電視信號在與 CGMS-A 位相同的 VBI 波形封包中包含資訊。 除此之外，這項資訊也包含圖片外觀比例。 如果外觀比例資訊與影片串流不一致，則電視可能會顯示不良。 應用程式可以使用此命令來指定外觀比例，讓圖形驅動程式能夠產生正確的 VBI 封包。

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

 

 




