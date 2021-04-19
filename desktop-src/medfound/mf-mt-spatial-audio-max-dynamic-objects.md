---
description: 指定音訊端點 simulataneously 可轉譯的動態音訊物件最大數目。
ms.assetid: 6B6D73C1-C2E6-4C23-BBAD-7B51E8441C71
title: 'MF_MT_SPATIAL_AUDIO_MAX_DYNAMIC_OBJECTS 屬性 (Mfapi) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 358045079fb9cf52ad1fd0c8969f54723c7f02d9
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977949"
---
# <a name="mf_mt_spatial_audio_max_dynamic_objects-attribute"></a>MF \_ MT \_ 空間 \_ 音訊 \_ 最大 \_ 動態 \_ 物件屬性

指定音訊端點 simulataneously 可轉譯的動態音訊物件最大數目。

## <a name="data-type"></a>資料類型

**UINT32**

## <a name="remarks"></a>備註

[**IMFSpatialAudioSample**](/windows/desktop/api/mfspatialaudio/nn-mfspatialaudio-imfspatialaudiosample)可能包含的樣本數比這個屬性所指定的數目少。 如果範例包含的音訊物件數目超過這個屬性所指定的數目，則行為會是未定義的。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10， \[ 僅限1703版桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Mfapi。h</dt> </dl> |



 

 




