---
description: 指定複製產生管理系統的保護層級&\# 8212;類比 (CGMS-) 。
ms.assetid: 739e2f9e-b8f1-4ee1-8706-9a069773a3de
title: 'CGMS-保護旗標 (Opmapi .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 3329ae13741490f2783d548baeead65ba59bc5ec
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104386048"
---
# <a name="cgms-a-protection-flags"></a>CGMS-保護旗標

下表中的常數指定複製產生管理系統類比 (CGMS-A) 的保護層級。



| 常數/值                                                                                                                                                                                                                                                                                                 | Description                                                                                                                       |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------|
| <span id="OPM_CGMSA_OFF"></span><span id="opm_cgmsa_off"></span><dl> <dt>**OPM \_CGMSA \_ OFF**</dt> <dt>0x00</dt> </dl>                                                                                       | CGMS-A 已停用。 <br/>                                                                                                   |
| <span id="OPM_CGMSA_COPY_FREELY"></span><span id="opm_cgmsa_copy_freely"></span><dl> <dt>**OPM \_CGMSA \_ \_ 免費複製**</dt> <dt>0x01</dt> </dl>                                                              | 保護層級會自由複製。<br/>                                                                                   |
| <span id="OPM_CGMSA_COPY_NO_MORE"></span><span id="opm_cgmsa_copy_no_more"></span><dl> <dt>**OPM \_CGMSA \_ 複製 \_ 不再 \_**</dt>有 <dt>0x02</dt> </dl>                                                          | 保護層級將不再複製。 <br/>                                                                                 |
| <span id="OPM_CGMSA_COPY_ONE_GENERATION"></span><span id="opm_cgmsa_copy_one_generation"></span><dl> <dt>**OPM \_CGMSA \_ 複製 \_ 一 \_ 代**</dt> <dt>0x03</dt> </dl>                                     | 保護層級會複製1代。 <br/>                                                                          |
| <span id="OPM_CGMSA_COPY_NEVER"></span><span id="opm_cgmsa_copy_never"></span><dl> <dt>**OPM \_CGMSA \_ 複製 \_ 永不**</dt> <dt>0x04</dt> </dl>                                                                 | 保護層級為 [永遠複製]。<br/>                                                                                    |
| <span id="OPM_CGMSA_REDISTRIBUTION_CONTROL_REQUIRED"></span><span id="opm_cgmsa_redistribution_control_required"></span><dl> <dt>**OPM \_\_ \_ \_ 需要 CGMSA**</dt>重新發佈控制項 <dt>0x08</dt> </dl> | 轉散發控制 (也稱為「 *廣播旗* 標」，) 是必要的。 此旗標可以與其他旗標合併。<br/> |



## <a name="remarks"></a>備註

這些旗標相當於認證輸出保護通訊協定中使用的 **COPP \_ CGMSA \_ 保護 \_ 層級** 列舉常數 (COPP) 。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                      |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                |
| 標頭<br/>                   | <dl> <dt>Opmapi。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[媒體基礎常數](media-foundation-constants.md)
</dt> </dl>

 

 




