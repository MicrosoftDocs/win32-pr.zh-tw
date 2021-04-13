---
title: 'VMMouseButton 列舉 (VPCCOMInterfaces) '
description: 指定滑鼠按鍵。
ms.assetid: d09e63cb-9dc5-424f-b130-c0b0dd07fe11
keywords:
- VMMouseButton 列舉虛擬電腦
topic_type:
- apiref
api_name:
- VMMouseButton
api_location:
- VPCCOMInterfaces.h
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 18744af5a4f8068b9bb371cb15e06c365561f2cf
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "104466369"
---
# <a name="vmmousebutton-enumeration"></a>VMMouseButton 列舉

\[Windows 8 不能再使用 Windows Virtual PC。 請改為使用 [HYPER-V WMI 提供者 (V2) ](/windows/desktop/HyperV_v2/windows-virtualization-portal)。\]

指定滑鼠按鍵。

## <a name="syntax"></a>Syntax


```C++
typedef enum  { 
  vmMouseButton_Left    = 1,
  vmMouseButton_Right   = 2,
  vmMouseButton_Center  = 3
} VMMouseButton;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="vmMouseButton_Left"></span><span id="vmmousebutton_left"></span><span id="VMMOUSEBUTTON_LEFT"></span>**\_左 vmMouseButton**
</dt> <dd>

滑鼠左鍵。

</dd> <dt>

<span id="vmMouseButton_Right"></span><span id="vmmousebutton_right"></span><span id="VMMOUSEBUTTON_RIGHT"></span>**vmMouseButton \_ Right**
</dt> <dd>

滑鼠右鍵。

</dd> <dt>

<span id="vmMouseButton_Center"></span><span id="vmmousebutton_center"></span><span id="VMMOUSEBUTTON_CENTER"></span>**vmMouseButton \_ 中心**
</dt> <dd>

中間的滑鼠按鍵。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows 7 桌面應用程式\]<br/>                                                    |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                                     |
| 用戶端支援結束<br/>    | Windows 7<br/>                                                                          |
| 產品<br/>                  | Windows Virtual PC<br/>                                                                 |
| 標頭<br/>                   | <dl> <dt>VPCCOMInterfaces。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IVMMouse**](ivmmouse.md)
</dt> </dl>

 

