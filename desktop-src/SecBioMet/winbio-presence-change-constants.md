---
title: 'WINBIO_PRESENCE_CHANGE 常數 (Winbio \_ 類型 .h) '
description: 描述當 Windows 生物特徵辨識架構監視個人是否存在時可能發生的變更類型。
ms.assetid: 1E0B65D8-A38F-46BA-A99A-18666729FA30
topic_type:
- apiref
api_name:
- WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN
- WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL
- WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE
- WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE
- WINBIO_PRESENCE_CHANGE_TYPE_DEPART
- WINBIO_PRESENCE_CHANGE_TYPE_TRACK
api_location:
- winbio_types.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 08cce9cc74bafdba6cf8d1aa11abccdaf7315370223ff6edf47eaba167af84f0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118909716"
---
# <a name="winbio_presence_change-constants"></a>WINBIO \_ 狀態 \_ 變更常數

描述當 Windows 生物特徵辨識架構監視個人是否存在時可能發生的變更類型。



| 常數/值                                                                                                                                                                                                                                                                                      | Description                                                                                                                                               |
|:----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UNKNOWN"></span><span id="winbio_presence_change_type_unknown"></span><dl> <dt>**WINBIO \_狀態 \_ 變更 \_ 類型 \_ 未知**</dt> <dt>0</dt> </dl>           | 事件的類型未知。 此值用於未初始化的結構。<br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_UPDATE_ALL"></span><span id="winbio_presence_change_type_update_all"></span><dl> <dt>**WINBIO \_狀態 \_ 變更 \_ 類型 \_ \_ 全部更新**</dt> <dt>1</dt> </dl> | 提供相機框架中所有目前臉部的相關資訊。<br/>                                                                       |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_ARRIVE"></span><span id="winbio_presence_change_type_arrive"></span><dl> <dt>**WINBIO \_狀態 \_ 變更 \_ 類型 \_ 抵達**</dt> <dt>2</dt> </dl>              | 新臉部進入相機框架。<br/>                                                                                                           |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_RECOGNIZE"></span><span id="winbio_presence_change_type_recognize"></span><dl> <dt>**WINBIO \_狀態 \_ 變更 \_ 類型 \_ 辨識**</dt> <dt>3</dt> </dl>     | 臉部與已註冊的使用者相符。<br/>                                                                                                        |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_DEPART"></span><span id="winbio_presence_change_type_depart"></span><dl> <dt>**WINBIO \_狀態 \_ 變更 \_ 類型 \_**</dt>為 <dt>4</dt> </dl>              | 先前偵測到的臉部已離開相機框架一段時間。<br/>                                                              |
| <span id="WINBIO_PRESENCE_CHANGE_TYPE_TRACK"></span><span id="winbio_presence_change_type_track"></span><dl> <dt>**WINBIO \_狀態 \_ 變更 \_ 類型 \_ 追蹤**</dt> <dt>5</dt> </dl>                 | 提供有關周框方塊的更新資訊，以及目前在相機框架中的臉部子集的拒絕詳細資料值。<br/> |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                                                                                              |
| 最低支援的伺服器<br/> | Windows Server 2016 \[僅限桌面應用程式\]<br/>                                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Winbio \_ 類型 .h (包含適用于 Winbio 的用戶端應用程式或 Winbio 的 .h \_) </dt> </dl> |



 

 





