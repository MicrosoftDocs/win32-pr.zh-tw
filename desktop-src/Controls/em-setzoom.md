---
title: 'EM_SETZOOM 訊息 (Richedit .h) '
description: 設定縮放比例。 比率必須是介於1/64 到64之間的值。 您可以將此訊息傳送至編輯控制項或 rich edit 控制項。
ms.assetid: 6cdec5b8-4ce7-4fd5-8083-4daa63d17f63
keywords:
- EM_SETZOOM 訊息 Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETZOOM
api_location:
- Richedit.h
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ecf6541bc018df253a3ed45f8bced42e2f19938449d7fc35bf7f309909d53a3c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119437178"
---
# <a name="em_setzoom-message"></a>EM \_ SETZOOM 訊息

設定多行編輯控制項或 rich edit 控制項的縮放比例。 比率必須是介於1/64 到64之間的值。 編輯控制項必須設定 **ES \_ EX \_ 可** 擴充樣式，此訊息才能有效果，請參閱 [編輯控制項延伸樣式](edit-control-window-extended-styles.md)。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

縮放比例的分子。

</dd> <dt>

*lParam* 
</dt> <dd>

縮放比例的分母。 這些參數可以具有下列值。



| 值                                                                                                                                                                                                                                                              | 意義                                                                                                                                         |
|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="Both_0"></span><span id="both_0"></span><span id="BOTH_0"></span><dl> <dt>**兩者都是0**</dt> </dl>                                                                                                   | 使用 **EM \_ SETZOOM** 訊息關閉縮放， (縮放可能仍會使用 [**TxGetExtent**](/windows/desktop/api/Textserv/nf-textserv-itexthost-txgetextent)) 進行。<br/> |
| <span id="1_64____wParam___lParam____64"></span><span id="1_64____wparam___lparam____64"></span><span id="1_64____WPARAM___LPARAM____64"></span><dl> <dt>**1/64 < (wParam/lParam) < 64**</dt> </dl> | 依縮放比例分子/分母縮放顯示比例<br/>                                                                                |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

如果接受新的縮放設定，則傳回值為 **TRUE**。

如果未接受新的縮放設定，則傳回值為 **FALSE**。

## <a name="remarks"></a>備註

**編輯：** 在 Windows 10 1809 和更新版本中支援。 編輯控制項必須設定 **ES \_ EX \_ 可** 擴充樣式，此訊息才能有效果，請參閱 [編輯控制項延伸樣式](edit-control-window-extended-styles.md)。 如需編輯控制項的詳細資訊，請參閱 [編輯控制項](about-edit-controls.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 可轉散發套件<br/>          | Rich Edit 3。0<br/>                                                              |
| 標頭<br/>                   | <dl> <dt>Richedit .h/Commctrl。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**EM \_ GETZOOM**](em-getzoom.md)
</dt> </dl>

 

 





