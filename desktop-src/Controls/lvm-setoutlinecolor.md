---
title: 'LVM_SETOUTLINECOLOR 訊息 (Commctrl .h) '
description: 如果 \_ \_ 已設定 lvs) EX BORDERSELECT 擴充視窗樣式，則設定清單視圖控制項框線的色彩。
ms.assetid: c2b606fa-8d47-4192-94b7-d01c3cfdc514
keywords:
- LVM_SETOUTLINECOLOR message Windows 控制項
topic_type:
- apiref
api_name:
- LVM_SETOUTLINECOLOR
api_location:
- Commctrl.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 776cb13479e4d091d394941844691c117a4ebbef
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103843091"
---
# <a name="lvm_setoutlinecolor-message"></a>LVM \_ SETOUTLINECOLOR 訊息

如果已設定 [**lvs) \_ EX \_ BORDERSELECT**](extended-list-view-styles.md) 擴充視窗樣式，則設定清單視圖控制項框線的色彩。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>必須為零。</dd> <dt>

*lParam* 
</dt> <dd>**COLORREF** 結構，指定要設定框線的色彩。</dd> </dl>

## <a name="return-value"></a>傳回值

傳回包含外框色彩的 **COLORREF** 結構。

## <a name="remarks"></a>備註

> [!Note]  
> 若要使用此訊息，您必須提供指定 Comclt32.dll 6.0 版的資訊清單。 如需資訊清單的詳細資訊，請參閱 [啟用視覺化樣式](cookbook-overview.md)。

 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Commctrl。h</dt> </dl> |



 

 





