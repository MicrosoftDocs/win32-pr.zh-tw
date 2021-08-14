---
description: 下列旗標指定轉譯時要使用的動態重新連接層級。
ms.assetid: 5e9d5f11-6716-4539-96fd-a0b37036555b
title: '動態重新連接旗標 (Qedit .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CONNECTF_DYNAMIC_NONE
- CONNECTF_DYNAMIC_SOURCES
- CONNECTF_DYNAMIC_EFFECTS
api_type:
- HeaderDef
api_location:
- Qedit.h
ms.openlocfilehash: f7bd2ff28c0928c59c632df501e6545b50707cfd948dd57e4ff1bd1cf01d1721
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119966238"
---
# <a name="dynamic-reconnection-flags"></a>動態重新連接旗標

\[廢棄。 此 API 可能會從 Windows 的未來版本中移除。\]

下列旗標指定轉譯時要使用的動態重新連接層級。



| 常數/值                                                                                                                                                                                                                                            | Description                                                                       |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------|
| <span id="CONNECTF_DYNAMIC_NONE"></span><span id="connectf_dynamic_none"></span><dl> <dt>**CONNECTF \_DYNAMIC \_ NONE**</dt> <dt>0x00</dt> </dl>          | 無動態重新連接。 先載入所有專案，然後再呈現專案。<br/> |
| <span id="CONNECTF_DYNAMIC_SOURCES"></span><span id="connectf_dynamic_sources"></span><dl> <dt>**CONNECTF \_動態 \_ 來源**</dt> <dt>0x01</dt> </dl> | 只在需要時才載入來源。<br/>                                           |
| <span id="CONNECTF_DYNAMIC_EFFECTS"></span><span id="connectf_dynamic_effects"></span><dl> <dt>**CONNECTF \_動態 \_ 效果**</dt> <dt>0x02</dt> </dl> | 保留的。 請勿使用。<br/>                                                  |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Qedit。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IRenderEngine::SetDynamicReconnectLevel**](irenderengine-setdynamicreconnectlevel.md)
</dt> </dl>

 

 




