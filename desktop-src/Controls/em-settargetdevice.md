---
title: 'EM_SETTARGETDEVICE 訊息 (Richedit .h) '
description: 設定用於 \ 0034 的目標裝置和行寬度; 您所看到的內容是您所得到的 \ 0034; (WYSIWYG) 在 rich edit 控制項中格式化。
ms.assetid: dfc829f5-e711-419e-abb5-c1e8df994c4a
keywords:
- EM_SETTARGETDEVICE message Windows 控制項
topic_type:
- apiref
api_name:
- EM_SETTARGETDEVICE
api_location:
- Richedit.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8f82d6ee5df86572564cffcf192395ccee1fbd05
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104104214"
---
# <a name="em_settargetdevice-message"></a>EM \_ SETTARGETDEVICE 訊息

設定在 rich edit 控制項中，用於「您看到的內容」 (WYSIWYG) 格式的目標裝置和線條寬度。

## <a name="parameters"></a>參數

<dl> <dt>

*wParam* 
</dt> <dd>

目標裝置的 HDC。

</dd> <dt>

*lParam* 
</dt> <dd>

用於格式化的線條寬度。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果作業失敗，則傳回值為零，如果成功，則為非零。

## <a name="remarks"></a>備註

預設印表機的 HDC 可以依照下列方式取得。


```
PRINTDLG pd = { sizeof(pd) };
pd.Flags = PD_RETURNDC | PD_RETURNDEFAULT;
if (PrintDlg(&pd))
{
    HDC hdc = pd.hDC;
    ...
}
```



如果 *lParam* 為零，則不會建立任何分行符號。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                  |
| 標頭<br/>                   | <dl> <dt>Richedit。h</dt> </dl> |



 

 





