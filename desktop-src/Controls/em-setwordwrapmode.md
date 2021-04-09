---
title: 'EM_SETWORDWRAPMODE 訊息 (Richedit .h) '
description: 設定 rich edit 控制項的自動換行和斷字選項。
ms.assetid: 43703ac8-6ae5-470b-9156-e60330ef97c4
keywords:
- EM_SETWORDWRAPMODE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETWORDWRAPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cf1dc6f064f52bf2a5f58c71db099f38b9350e63
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104025209"
---
# <a name="em_setwordwrapmode-message"></a>EM \_ SETWORDWRAPMODE 訊息

設定 rich edit 控制項的自動換行和斷字選項。

> [!Note]  
> 只有 Microsoft Rich Edit 1.0 的亞洲語言版本才支援此訊息。 任何較新版本都不支援此功能。

 

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

指定下列一或多個值。



| 值                                                                                                                                                         | 意義                                                                                                               |
|---------------------------------------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------|
| <span id="WBF_WORDWRAP"></span><span id="wbf_wordwrap"></span><dl> <dt>**WBF \_ WORDWRAP**</dt> </dl>    | 啟用亞洲特定的文字換行作業，例如日文的避避。 <br/>                                 |
| <span id="WBF_WORDBREAK"></span><span id="wbf_wordbreak"></span><dl> <dt>**WBF \_ WORDBREAK**</dt> </dl> | 啟用日文和中文的英文斷字作業。 啟用 Hangeul 斷詞操作。<br/> |
| <span id="WBF_OVERFLOW"></span><span id="wbf_overflow"></span><dl> <dt>**WBF \_ 溢位**</dt> </dl>    | 辨識溢位標點符號。 目前不支援 (。 ) <br/>                                                |
| <span id="WBF_LEVEL1"></span><span id="wbf_level1"></span><dl> <dt>**WBF \_ 級1**</dt> </dl>          | 將 [層級 1] 標點符號資料表設定為預設值。<br/>                                                         |
| <span id="WBF_LEVEL2"></span><span id="wbf_level2"></span><dl> <dt>**WBF 的 \_ 級別2**</dt> </dl>          | 將層級2標點符號資料表設定為預設值。<br/>                                                         |
| <span id="WBF_CUSTOM"></span><span id="wbf_custom"></span><dl> <dt>**WBF \_ 自訂**</dt> </dl>          | 設定應用程式定義的標點符號資料表。<br/>                                                            |



 

</dd> <dt>

*lParam* 
</dt> <dd>

未使用此參數;它必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

這則訊息會傳回目前的自動換行和斷詞選項。

## <a name="remarks"></a>備註

此訊息不得由應用程式定義的斷詞程式傳送。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



 

 





