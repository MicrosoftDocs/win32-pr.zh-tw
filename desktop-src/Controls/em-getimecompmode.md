---
title: 'EM_GETIMECOMPMODE 訊息 (Richedit .h) '
description: 抓取 rich edit 控制項的目前輸入方法編輯器 (IME) 模式。
ms.assetid: dac96833-4c3d-4da7-9ea4-52204434ec10
keywords:
- EM_GETIMECOMPMODE 訊息 Windows 控制項
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
ms.openlocfilehash: 53b9c0242872446c22034502d92af00ead7289fc68b4d5a66d79c3ef68be5eaa
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119019546"
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



| 傳回碼                                                                                     | 描述                  |
|-------------------------------------------------------------------------------------------------|------------------------------|
| <dl> <dt>**ICM \_NOTOPEN**</dt> </dl>     | 未開啟 IME。<br/>  |
| <dl> <dt>**ICM \_LEVEL3**</dt> </dl>      | True 內嵌模式。<br/> |
| <dl> <dt>**ICM \_級**</dt> </dl>      | 層級2。<br/>          |
| <dl> <dt>**ICM \_\_第2級5**</dt> </dl>   | 層級2。5<br/>         |
| <dl> <dt>**ICM \_級別 2 \_ SUI**</dt> </dl> | 特殊的 UI。<br/>       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



 

 





