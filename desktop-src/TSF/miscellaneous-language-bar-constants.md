---
title: '其他語言橫條常數 (Ctfutb .h) '
description: 其他語言 bar 常數會設定語言列的特定屬性。
ms.assetid: c1740636-7ba3-4748-9005-ee94d04dbb15
topic_type:
- apiref
api_name:
- TF_DTLBI_USEPROFILEICON
- TF_INVALIDMENUITEM
- TF_LBI_BMPF_VERTICAL
- TF_LBI_DESC_MAXLEN
api_location:
- Ctfutb.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 91fd1a371581dea02226ba6539ca25a06ef98e75
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104385110"
---
# <a name="miscellaneous-language-bar-constants"></a>其他語言橫條圖常數

其他語言 bar 常數會設定語言列的特定屬性。



| 常數/值                                                                                                                                                                                                                                               | Description                                                                                                                                                                                                                                                                                                              |
|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="TF_DTLBI_USEPROFILEICON"></span><span id="tf_dtlbi_useprofileicon"></span><dl> <dt>**TF \_DTLBI \_ USEPROFILEICON**</dt> <dt>0x00000001</dt> </dl> | 系統語言列專案應該會顯示為語言設定檔指定的圖示。 用於 [ITfSystemDeviceTypeLangBarItem：： GetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode) 和 [ITfSystemDeviceTypeLangBarItem：： SetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode) 方法。<br/> |
| <span id="TF_INVALIDMENUITEM"></span><span id="tf_invalidmenuitem"></span><dl> <dt>**TF \_INVALIDMENUITEM**</dt> <dt> (UINT)  (-1)</dt> </dl>                 | 未使用。<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_BMPF_VERTICAL"></span><span id="tf_lbi_bmpf_vertical"></span><dl> <dt>**TF \_LBI \_ BMPF \_ 垂直**</dt> <dt>0x00000001</dt> </dl>         | 未使用。<br/>                                                                                                                                                                                                                                                                                                     |
| <span id="TF_LBI_DESC_MAXLEN"></span><span id="tf_lbi_desc_maxlen"></span><dl> <dt>**TF \_LBI \_ DESC \_ MAXLEN**</dt> <dt>32</dt> </dl>                       | 結構成員 [TF \_ LANGBARITEMINFO. szDescription](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)的長度（以 WCHAR 字元為單位）。<br/>                                                                                                                                                                                                 |



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                            |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                  |
| 可轉散發套件<br/>          | Windows 2000 Professional 上的 TSF 1。0<br/>                                       |
| 標頭<br/>                   | <dl> <dt>Ctfutb。h</dt> </dl>   |
| Idl<br/>                      | <dl> <dt>Ctfutb .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[ITfSystemDeviceTypeLangBarItem::GetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-geticonmode)
</dt> <dt>

[ITfSystemDeviceTypeLangBarItem::SetIconMode](/windows/desktop/api/Ctfutb/nf-ctfutb-itfsystemdevicetypelangbaritem-seticonmode)
</dt> <dt>

[TF \_ LANGBARITEMINFO](/windows/desktop/api/Ctfutb/ns-ctfutb-tf_langbariteminfo)
</dt> </dl>

 

 





