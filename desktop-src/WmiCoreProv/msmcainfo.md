---
description: 從中衍生所有機器檢查架構 (MCA) 提供者資料類別（例如 MSMCAInfo RawMCAData）的抽象基類 \_ 。 此類別僅適用于64位的 Windows 系統。
ms.assetid: 22ec8343-fc4f-4b14-9354-26b5d6a6fe09
title: MSMCAInfo 類別
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- MSMCAInfo
api_type:
- DllExport
api_location:
- Wmiprov.dll
ms.openlocfilehash: 31fc35b1d680d900af929ea8a828bcb23d222f66
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104026206"
---
# <a name="msmcainfo-class"></a>MSMCAInfo 類別

**MSMCAInfo** 類別是一個抽象基類，所有機器檢查架構 (MCA) 提供者資料類別（例如 [**MSMCAInfo \_ RawMCAData**](msmcainfo-rawmcadata.md)）都會衍生。 MCA 提供者也有衍生自 [**>register-wmievent**](wmievent.md)的事件類別。 此類別僅適用于64位的 Windows 系統。

下列語法已從受控物件格式的 (MOF) 程式碼簡化，並包含其所有繼承的屬性。 屬性和方法是以字母順序排列，而不是 MOF 順序。

## <a name="syntax"></a>語法

``` syntax
class MSMCAInfo
{
};
```

## <a name="members"></a>成員

**MSMCAInfo** 類別不會定義任何成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows XP<br/>                                                                  |
| 最低支援的伺服器<br/> | Windows Server 2003<br/>                                                         |
| 命名空間<br/>                | 根 \\ wmi<br/>                                                                   |
| MOF<br/>                      | <dl> <dt>Wmicore mof</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Wmiprov.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[MSMCA 類別](msmca-classes.md)
</dt> <dt>

[**MSMCAEvent \_ 標頭**](msmcaevent-header.md)
</dt> <dt>

[**>register-wmievent**](wmievent.md)
</dt> </dl>

 

 




