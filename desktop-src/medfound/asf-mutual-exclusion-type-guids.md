---
description: 下列 Guid 會定義 Advanced 系統格式的相互排除物件 (ASF) 資料流程的類型。
ms.assetid: 3db8eebd-2e26-4c77-8f66-7d08436c9e42
title: 'ASF 相互排除類型 Guid (Wmcontainer .h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2a6fedc766e26c35bb967054a704b732ca03e8a8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191089"
---
# <a name="asf-mutual-exclusion-type-guids"></a>ASF 相互排除類型 Guid

下列 Guid 會定義 Advanced 系統格式的相互排除物件 (ASF) 資料流程的類型。



| 常數                                                                                                                                                                                                                                              | 描述                                                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
|:------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="MFASFMutexType_Language"></span><span id="mfasfmutextype_language"></span><span id="MFASFMUTEXTYPE_LANGUAGE"></span><dl> <dt>**MFASFMutexType \_ 語言**</dt> </dl>                 | 資料流程是依語言相互排斥。 這種相互排除類型類似于 DVD 上的音訊曲目。<br/>                                                                                                                                                                                                                                                                                                                                                                 |
| <span id="MFASFMutexType_Bitrate"></span><span id="mfasfmutextype_bitrate"></span><span id="MFASFMUTEXTYPE_BITRATE"></span><dl> <dt>**MFASFMutexType \_ 位元速率**</dt> </dl>                     | 資料流程會以位元速率互斥。 這種相互排除也稱為「多位元率」（ (MBR) 排除）。<br/>                                                                                                                                                                                                                                                                                                                                                        |
| <span id="MFASFMutexType_Presentation"></span><span id="mfasfmutextype_presentation"></span><span id="MFASFMUTEXTYPE_PRESENTATION"></span><dl> <dt>**MFASFMutexType \_ 簡報**</dt> </dl> | 這些資料流程在簡報時是互斥的。 這種類型可以用於許多案例，但應該只在內容相同但採用不同的表單時使用。 例如，兩個包含相同影片的串流，其中一個格式化為填滿螢幕，另一個則維持原始寬螢幕外觀比例，則應該使用此類型來互斥。 另一個範例是包含不同角度之相同場景拍攝影片的串流。<br/> |
| <span id="MFASFMutexType_Unknown"></span><span id="mfasfmutextype_unknown"></span><span id="MFASFMUTEXTYPE_UNKNOWN"></span><dl> <dt>**MFASFMutexType \_ 不明**</dt> </dl>                     | 資料流程會根據自訂準則相互排斥。<br/>                                                                                                                                                                                                                                                                                                                                                                                                                           |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                           |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                                     |
| 標頭<br/>                   | <dl> <dt>Wmcontainer。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMFASFMutualExclusion：： GetType**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-gettype)
</dt> <dt>

[**IMFASFMutualExclusion：： >advanced.field.settype**](/windows/desktop/api/wmcontainer/nf-wmcontainer-imfasfmutualexclusion-settype)
</dt> <dt>

[媒體基礎常數](media-foundation-constants.md)
</dt> </dl>

 

 




