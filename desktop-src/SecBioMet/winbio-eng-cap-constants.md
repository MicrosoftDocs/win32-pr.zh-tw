---
title: 'WINBIO_ENG_CAP 常數 (Winbio \_ 類型 .h) '
description: 指定一般引擎功能。
ms.assetid: 31C4E8AF-6EF8-43FF-A944-D7363A26BB1A
topic_type:
- apiref
api_name:
- WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT
- WINBIO_ENG_CAP_SPOOF_DETECTION
api_location:
- Winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: a5be1099b6ad555b0547dc975c1446740f43359792c1643d155322095ad26dd4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119867948"
---
# <a name="winbio_eng_cap-constants"></a>WINBIO \_ ENG \_ CAP 常數

下列常數是 **WINBIO 的 \_ 功能** 值，可用來指定連接到特定生物特徵辨識單位之引擎元件的一般功能。 您可以在 [**WINBIO \_ 擴充 \_ 引擎 \_ 資訊**](winbio-extended-engine-info.md)結構的 **GenericEngineCapabilities** 成員中指定這些功能。



| 常數/值                                                                                                                                                                                                                                                                                        | 描述                                                                  |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-----------------------------------------------------------------------------|
| <span id="WINBIO_ENG_CAP_ITERATIVE_IMPROVEMENT"></span><span id="winbio_eng_cap_iterative_improvement"></span><dl> <dt>**WINBIO \_ENG \_ 上限 \_ 反復 \_ 改進**</dt> <dt>0x00000001</dt> </dl> | 生物特徵辨識引擎元件可以執行反復的改進。<br/> |
| <span id="WINBIO_ENG_CAP_SPOOF_DETECTION"></span><span id="winbio_eng_cap_spoof_detection"></span><dl> <dt>**WINBIO \_ENG \_ 上限 \_ 詐騙 \_ 偵測**</dt>到 <dt>0x00000002</dt> </dl>                   | 生物識別引擎元件可以執行欺騙偵測。<br/>       |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                                   |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含 Winbio .h) </dt> </dl> |



 

 





