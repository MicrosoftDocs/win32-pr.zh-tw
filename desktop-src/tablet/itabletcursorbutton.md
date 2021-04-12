---
description: 表示手寫筆裝置上按鈕的一般資訊。
ms.assetid: 20c9f8bb-8f8d-4469-baff-b9001c8adb3b
title: ITabletCursorButton 介面
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ITabletCursorButton
api_type:
- COM
api_location:
- wisptis.exe
- wisptis.exe.dll
ms.openlocfilehash: c8f13e46699c1bea42bd8f8a7f78313aeba68aaf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104319723"
---
# <a name="itabletcursorbutton-interface"></a>ITabletCursorButton 介面

表示手寫筆裝置上按鈕的一般資訊。

## <a name="members"></a>成員

**ITabletCursorButton** 介面繼承自 [**IUnknown**](/windows/desktop/api/unknwn/nn-unknwn-iunknown)介面。 **ITabletCursorButton** 也有下列類型的成員：

-   [方法](#methods)

### <a name="methods"></a>方法

**ITabletCursorButton** 介面具有這些方法。



| 方法                                         | 描述                                                      |
|:-----------------------------------------------|:-----------------------------------------------------------------|
| [**GetGuid**](itabletcursorbutton-getguid.md) | 抓取手寫筆按鈕的唯一識別碼。<br/> |
| [**GetName**](itabletcursorbutton-getname.md) | 抓取手寫筆按鈕的名稱。<br/>              |



 

## <a name="remarks"></a>備註

開發人員不應使用此介面。

下列程式碼說明如何定義 **ITabletCursorButton** 介面。

``` syntax
[
    object,
    uuid(997A992E-8B6C-4945-BC17-A1EE563B3AB7),
    pointer_default(unique)
]
interface ITabletCursorButton : IUnknown
{
    HRESULT GetName(
        [out] LPWSTR *ppwszName);

    HRESULT GetGuid(
        [out] GUID *pguidBtn);
};
```

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP Tablet PC Edition \[ 桌面應用程式\]<br/>                          |
| 最低支援的伺服器<br/> | 都不支援<br/>                                                              |
| 程式庫<br/>                  | <dl> <dt>Wisptis.exe</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ITabletCursorButton 介面**](itabletcursorbutton.md)
</dt> </dl>

 

