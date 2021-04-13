---
title: 'EM_GETIMECOMPMODE 訊息 (Richedit .h) '
description: 抓取 rich edit 控制項的目前輸入方法編輯器 (IME) 模式。
ms.assetid: dac96833-4c3d-4da7-9ea4-52204434ec10
keywords:
- EM_GETIMECOMPMODE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_GETIMECOMPMODE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 1feb2f5f31831e0e292bf002f24ca4978f25753a
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466105"
---
# <a name="em_getimecompmode-message"></a>EM \_ GETIMECOMPMODE 訊息

抓取 rich edit 控制項的目前輸入方法編輯器 (IME) 模式。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

未使用;必須為零。

</dd> <dt>

*lParam* 
</dt> <dd>

未使用;必須為零。

</dd> </dl>

## <a name="return-value"></a>傳回值

傳回值是下列其中一個值。



| 傳回碼                                                                                     | Description                  |
|-------------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**ICM \_ NOTOPEN**</dt> </dl>     | 未開啟 IME。<br/>  |
| <dl> <dt>**ICM \_ 級別3**</dt> </dl>      | True 內嵌模式。<br/> |
| <dl> <dt>**ICM \_ 2-2**</dt> </dl>      | 層級2。<br/>          |
| <dl> <dt>**ICM \_ 2- \_ 5**</dt> </dl>   | 層級2。5<br/>         |
| <dl> <dt>**ICM \_ 級別 2 \_ SUI**</dt> </dl> | 特殊的 UI。<br/>       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



 

 





