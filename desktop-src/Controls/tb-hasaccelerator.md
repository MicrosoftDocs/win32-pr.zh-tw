---
title: 'TB_HASACCELERATOR 訊息 (Commctrl .h) '
description: 抓取具有指定快速鍵的工具列按鈕計數。
ms.assetid: 41167815-fb64-4203-a32c-b2a88ce7bce1
keywords:
- TB_HASACCELERATOR message Windows 控制項
topic_type:
- apiref
api_name:
- TB_HASACCELERATOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2544eae629876e4527ea4e47477b50ea59b796c8
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104465565"
---
# <a name="tb_hasaccelerator-message"></a>TB \_ HASACCELERATOR 訊息

\[適用于內部用途;不建議在應用程式中使用。 未來的 Windows 版本可能不支援此訊息。\]

抓取具有指定快速鍵的工具列按鈕計數。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

**WCHAR** ，表示要測試的輸入快速鍵字元。

</dd> <dt>

*lParam* 
</dt> <dd>

整數的指標，該 **int** 會接收具有快速鍵字元的按鈕數目。

</dd> </dl>

## <a name="return-value"></a>傳回值

未使用傳回值。

## <a name="security-considerations"></a>安全性考量

使用此訊息可能會危害程式的安全性。

## <a name="remarks"></a>備註

首先，系統會查詢所有工具列按鈕，以進行相符的快速鍵。 如果找不到相符專案，系統會將 [TBN \_ MAPACCELERATOR](tbn-mapaccelerator.md) 通知傳送至父視窗，要求具有指定快速鍵的按鈕索引。 如果父系提供索引，則計數會設定為1。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





