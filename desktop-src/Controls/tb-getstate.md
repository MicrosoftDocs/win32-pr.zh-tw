---
title: 'TB_GETSTATE 訊息 (Commctrl .h) '
description: 抓取工具列中指定之按鈕的狀態相關資訊，例如是否已啟用、已按下或已核取。
ms.assetid: e8a9e1ff-506f-413b-8f8c-986c25bce736
keywords:
- TB_GETSTATE message Windows 控制項
topic_type:
- apiref
api_name:
- TB_GETSTATE
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: b3b5c50978da78218be7f3d47208c0ea430ff36c
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843247"
---
# <a name="tb_getstate-message"></a>TB \_ >getstate 訊息

抓取工具列中指定之按鈕的狀態相關資訊，例如是否已啟用、已按下或已核取。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

要取得其資訊之按鈕的命令識別碼。

</dd> <dt>

*lParam* 
</dt> <dd>必須為零。</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回按鈕狀態資訊，否則傳回-1。 按鈕狀態資訊可以是 [ [**工具列按鈕狀態**](toolbar-button-states.md)] 中所列的值組合。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





