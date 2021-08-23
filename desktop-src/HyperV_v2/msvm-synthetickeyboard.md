---
description: 代表綜合鍵盤裝置。
ms.assetid: 8fe9bdd5-59e8-421d-812a-08aa3c54c88f
title: Msvm_SyntheticKeyboard 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- Msvm_SyntheticKeyboard
api_type:
- DllExport
api_location:
- vmms.exe
ms.openlocfilehash: 86ee3a7835349ab47082627f98020f84084b4b86e9c6b4ce4a37ba2f455497cb
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119582218"
---
# <a name="msvm_synthetickeyboard-class"></a>Msvm \_ SyntheticKeyboard 類別

代表綜合鍵盤裝置。

下列語法已經過受管理物件格式 (MOF) 程式碼簡化，並包含所有已繼承的屬性。

## <a name="syntax"></a>語法

``` syntax
[Dynamic, Provider("VmmsWmiInstanceAndMethodProvider"), AMENDMENT]
class Msvm_SyntheticKeyboard : CIM_UserDevice
{
};
```

## <a name="members"></a>成員

**Msvm \_ SyntheticKeyboard** 類別具有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**Msvm \_ SyntheticKeyboard** 類別具有這些方法。



| 方法                                                                  | 描述                         |
|:------------------------------------------------------------------------|:------------------------------------|
| [**RequestStateChange**](msvm-synthetickeyboard-requeststatechange.md) | 要求狀態變更。<br/> |
| [**重設**](msvm-synthetickeyboard-reset.md)                           | 重設裝置。<br/>       |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|---------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 10 \[僅限桌面應用程式\]<br/>                                                             |
| 最低支援的伺服器<br/> | Windows Server 2016<br/>                                                                          |
| 命名空間<br/>                | 根 \\ 虛擬化 \\ v2<br/>                                                                     |
| MOF<br/>                      | <dl> <dt>WindowsVirtualization。</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Vmms.exe</dt> </dl>                     |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**CIM \_ UserDevice**](cim-userdevice.md)
</dt> </dl>

 

 




