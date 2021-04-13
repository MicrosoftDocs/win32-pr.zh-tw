---
title: 'HKM_SETRULES 訊息 (Commctrl .h) '
description: 定義快速鍵控制項的無效組合和預設輔助按鍵組合。
ms.assetid: de3dd463-a534-4c7c-ae04-da80a3bff2ab
keywords:
- HKM_SETRULES message Windows 控制項
topic_type:
- apiref
api_name:
- HKM_SETRULES
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c33c0918a7bb44fdac9a1f2c60fdde8e06b5e679
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465693"
---
# <a name="hkm_setrules-message"></a>HKM \_ SETRULES 訊息

定義快速鍵控制項的無效組合和預設輔助按鍵組合。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

旗標的陣列，指定不正確按鍵組合。 這個參數可以是下列值的組合：



| 值                                                                                                                                                   | 意義                    |
|---------------------------------------------------------------------------------------------------------------------------------------------------------|----------------------------|
| <span id="HKCOMB_A"></span><span id="hkcomb_a"></span><dl> <dt>**HKCOMB \_**</dt> </dl>          | ALT<br/>             |
| <span id="HKCOMB_C"></span><span id="hkcomb_c"></span><dl> <dt>**HKCOMB \_ C**</dt> </dl>          | CTRL<br/>            |
| <span id="HKCOMB_CA"></span><span id="hkcomb_ca"></span><dl> <dt>**HKCOMB \_ CA**</dt> </dl>       | CTRL + ALT<br/>        |
| <span id="HKCOMB_NONE"></span><span id="hkcomb_none"></span><dl> <dt>**HKCOMB \_ 無**</dt> </dl> | 未修改的金鑰<br/> |
| <span id="HKCOMB_S"></span><span id="hkcomb_s"></span><dl> <dt>**HKCOMB \_ S**</dt> </dl>          | SHIFT<br/>           |
| <span id="HKCOMB_SA"></span><span id="hkcomb_sa"></span><dl> <dt>**HKCOMB \_ SA**</dt> </dl>       | SHIFT+ALT<br/>       |
| <span id="HKCOMB_SC"></span><span id="hkcomb_sc"></span><dl> <dt>**HKCOMB \_ SC**</dt> </dl>       | SHIFT + CTRL<br/>      |
| <span id="HKCOMB_SCA"></span><span id="hkcomb_sca"></span><dl> <dt>**HKCOMB \_ SCA**</dt> </dl>    | SHIFT + CTRL + ALT<br/>  |



 

</dd> <dt>

*lParam* 
</dt> <dd>

旗標的陣列，指定當使用者輸入不正確組合時，所要使用的按鍵組合。 如需修飾詞旗標值的清單，請參閱 [**HKM \_ GETHOTKEY**](hkm-gethotkey.md) 訊息的說明。

</dd> </dl>

## <a name="return-value"></a>傳回值

沒有傳回值。

## <a name="remarks"></a>備註

當使用者輸入不正確按鍵組合（如 *wParam* 中所指定的旗標所定義）時，系統會使用位 or 運算子，將使用者輸入的索引鍵與 *lParam* 中指定的旗標合併。 產生的按鍵組合會轉換成字串，然後顯示在快速鍵控制項中。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





